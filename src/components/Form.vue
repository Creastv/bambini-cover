<template>
  <div class="form">
    <header>
      <p>
        <b>{{ inf.title }}</b>
      </p>
      <p>{{ inf.desc }}</p>
      <ul>
        <li v-for="error in errors" :key="error">{{ error }}</li>
      </ul>
    </header>
    <form @submit.prevent="validation" method="post" v-if="!removeForm">
      <div class="form-control">
        <input
          class="email"
          type="text"
          name="email"
          id="email"
          autocomplete="off"
          v-model="personFEmail"
        />
        <input
          class="phone"
          type="text"
          name="phone"
          id="phone"
          autocomplete="off"
          v-model="personFPhone"
        />
        <input
          type="text"
          name="per"
          id="per"
          placeholder="Twój adres mailowy"
          v-model="personEmail"
          autocomplete="off"
        />
        <span class="err"></span>
        <button type="submit">Wyślij</button>
      </div>
      <div class="form-control-checkbox">
        <input type="checkbox" name="zgoda" id="zgoda" v-model="personZgoda" />
        <label :class="{ open: open }" for="checkbox">{{ checkboxInfo }}</label>
        <span @click="extend" v-if="!open">Rozwiń</span>
        <span @click="extend" v-else>Zwiń</span>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inf: {
        title: "Zostaw swojego maila",
        desc: "poinformujemy cię o rozpoczęciu zapisów!"
      },
      errors: [],
      personFEmail: null,
      personFPhone: null,
      personEmail: null,
      personZgoda: false,
      checkboxInfo:
        "Wysyłając formularz wyrażam zgodę na przetwarzanie swoich danych osobowych przez Bambini - Klub Malucha oraz przez podmioty współpracujące na podstawie umów powierzenia, w zakresie niezbędnym do realizacji mojego zapytania. Wyrażam zgodę na otrzymywanie informacji, stanowiącej odpowiedź na niniejsze zapytanie za pomocą środków komunikacji elektronicznej.",
      open: false,
      removeForm: false
    };
  },

  methods: {
    extend() {
      this.open = !this.open;
    },
    validation() {
      this.errors = [];
      var validRegex =
        /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/;

      if (!this.personEmail && !this.personZgoda) {
        this.errors.push("Podaj adres email.");
        this.errors.push("Należy wyrazić zgodę.");
      } else if (!this.personZgoda) {
        this.errors.push("Należy wyrazić zgodę.");
      } else if (!this.personEmail) {
        this.errors.push("Podaj adres email.");
      } else if (!this.personEmail.match(validRegex)) {
        this.errors.push("Nie prawidłowy adres email.");
      } else {
        if (!this.personFEmail && !this.personFPhone) {
          this.send();
          this.removeForm = true;
          this.inf = {
            title: "Dziękujemy za wypełnienie formularza",
            desc: "jak tylko zaczniemy zapisy poinformujemy Ciebie"
          };
        } else {
          alert("error");
        }
      }
    },
    send() {
      fetch(
        "https://zapisy-98caa-default-rtdb.europe-west1.firebasedatabase.app/zapisy.json",
        {
          method: "POST",
          headers: {
            "Content-Type": "application/json"
          },
          body: JSON.stringify({
            email: this.personEmail,
            zgoda: this.personZgoda
          })
        }
      );
    }
  }
};
</script>

<style scoped>
.form {
  padding: 0 15px;
  display: block;
  width: 400px;
  margin: 0 auto;
}
p {
  color: #464646;
  margin: 0;
}
p b {
  font-size: 28px;
  text-transform: uppercase;
}
ul {
  list-style: none;
  padding: 0;
  margin: 10px 0 0;
}
ul li {
  color: red;
  font-size: 12px;
}
form {
  padding: 15px 0;
}

.form-control {
  display: flex;
  justify-content: center;
  margin-bottom: 10px;
}
.email,
.phone {
  display: none !important;
  opacity: 0;
}
.form-control-checkbox {
  text-align: left;
  display: flex;
  align-items: flex-start;
  flex-wrap: wrap;
}
.form-control-checkbox input {
  max-width: 10%;
  min-height: initial;
  box-shadow: none;
}
.form-control-checkbox label {
  position: relative;
  font-size: 12px;
  overflow: hidden;
  height: 30px;
  width: 90%;
  transition: 0.2s all;
}

.form-control-checkbox label.open {
  height: 100%;
}
.form-control-checkbox span {
  cursor: pointer;
  /* display: block; */
  width: 100%;
  padding: 5px;
  text-align: center;
  font-size: 12px;
  color: green;
}

input {
  margin: 5px;
  padding: 10px;
  border: 1px solid rgba(0, 0, 0, 0.3);
  border-radius: 3px;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.3);
  min-height: 30px;
  flex: auto;
}
button {
  margin: 5px;
  padding: 10px 20px;
  background-color: #179ad7;
  border: 0;
  border-radius: 3px;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.3);
  color: #fff;
  text-transform: uppercase;
  font-weight: bold;
  letter-spacing: 1px;
}
</style>
