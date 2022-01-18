<template>
  <div class="contaner">
    <div class="wraper">
      <img class="logo" :alt="desc" src="./assets/logo.png" />
      <p class="title">{{ title }}</p>
      <h1 class="desc">{{ desc }}</h1>
      <Form />
      <div class="facebook-info">
        <p>
          <b>{{ facebook.descFacebook }}</b>
        </p>
        <a :href="facebook.linkFacebook" target="_blank">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24.875"
            height="24.664"
            viewBox="0 0 34.875 34.664"
          >
            <path
              id="Icon_awesome-facebook"
              data-name="Icon awesome-facebook"
              d="M35.438,18A17.438,17.438,0,1,0,15.275,35.227V23.041h-4.43V18h4.43V14.158c0-4.37,2.6-6.784,6.586-6.784a26.836,26.836,0,0,1,3.9.34V12h-2.2a2.52,2.52,0,0,0-2.841,2.723V18h4.836l-.773,5.041H20.725V35.227A17.444,17.444,0,0,0,35.438,18Z"
              transform="translate(-0.563 -0.563)"
              fill="#76c16b"
            />
          </svg>
          <span> {{ facebook.shortLink }}</span>
        </a>
      </div>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        x="0px"
        y="0px"
        viewBox="0 0 288 288"
        id="bg-animate"
      >
        <linearGradient id="PSgrad_0" x1="70.711%" x2="0%" y1="70.711%" y2="0%">
          <stop offset="0%" stop-color="rgb(240,240,240)" stop-opacity="1" />
          <stop offset="100%" stop-color="rgb(234,234,234)" stop-opacity="1" />
        </linearGradient>
        <path fill="url(#PSgrad_0)">
          <animate
            repeatCount="indefinite"
            attributeName="d"
            dur="10s"
            values="M37.5,186c-12.1-10.5-11.8-32.3-7.2-46.7c4.8-15,13.1-17.8,30.1-36.7C91,68.8,83.5,56.7,103.4,45 c22.2-13.1,51.1-9.5,69.6-1.6c18.1,7.8,15.7,15.3,43.3,33.2c28.8,18.8,37.2,14.3,46.7,27.9c15.6,22.3,6.4,53.3,4.4,60.2 c-3.3,11.2-7.1,23.9-18.5,32c-16.3,11.5-29.5,0.7-48.6,11c-16.2,8.7-12.6,19.7-28.2,33.2c-22.7,19.7-63.8,25.7-79.9,9.7 c-15.2-15.1,0.3-41.7-16.6-54.9C63,186,49.7,196.7,37.5,186z; M51,171.3c-6.1-17.7-15.3-17.2-20.7-32c-8-21.9,0.7-54.6,20.7-67.1c19.5-12.3,32.8,5.5,67.7-3.4C145.2,62,145,49.9,173,43.4 c12-2.8,41.4-9.6,60.2,6.6c19,16.4,16.7,47.5,16,57.7c-1.7,22.8-10.3,25.5-9.4,46.4c1,22.5,11.2,25.8,9.1,42.6 c-2.2,17.6-16.3,37.5-33.5,40.8c-22,4.1-29.4-22.4-54.9-22.6c-31-0.2-40.8,39-68.3,35.7c-17.3-2-32.2-19.8-37.3-34.8 C48.9,198.6,57.8,191,51,171.3z; M37.5,186c-12.1-10.5-11.8-32.3-7.2-46.7c4.8-15,13.1-17.8,30.1-36.7C91,68.8,83.5,56.7,103.4,45 c22.2-13.1,51.1-9.5,69.6-1.6c18.1,7.8,15.7,15.3,43.3,33.2c28.8,18.8,37.2,14.3,46.7,27.9c15.6,22.3,6.4,53.3,4.4,60.2 c-3.3,11.2-7.1,23.9-18.5,32c-16.3,11.5-29.5,0.7-48.6,11c-16.2,8.7-12.6,19.7-28.2,33.2c-22.7,19.7-63.8,25.7-79.9,9.7 c-15.2-15.1,0.3-41.7-16.6-54.9C63,186,49.7,196.7,37.5,186z	"
          />
        </path>
      </svg>
    </div>
    <div class="shapes">
      <svg class="star" xml:space="preserve" viewBox="0 0 16.8 16">
        <path
          d="M.4 6c.3-.4.4-.5.9-.3.1 0 .1 0 .2.1.1 0 .4.1.6.2.3.1.5.4.4.7-.1.2-.4.4-.7.3-.3-.1-.7-.2-1-.3-.3-.1-.4-.2-.4-.4V6zm2 4.1c0-.4.2-.7.4-.9l1.8-1.8c.1-.1.1-.2.1-.3-.2-.7-.3-1.6-.5-2.4-.1-.5.1-.9.5-1.2.4-.3.9-.3 1.4-.1.7.4 1.5.8 2.2 1.2.1.1.2.1.4 0 .7-.4 1.4-.7 2.1-1.1.8-.4 1.7 0 1.9.7.1.3 0 .6 0 .9-.1.7-.2 1.5-.4 2.2 0 .1 0 .2.1.2l1.8 1.8c.4.3.5.8.3 1.2-.1.5-.4.8-.9.9-.3.1-.6.1-.9.1l-1.8.3c-.1 0-.1.1-.2.1-.4.8-.8 1.5-1.1 2.3-.4.8-1.3 1-2 .4-.1-.1-.3-.3-.3-.5-.4-.7-.7-1.5-1.1-2.2-.1-.1-.1-.2-.2-.2-.8-.1-1.7-.2-2.5-.4-.7 0-1.1-.6-1.1-1.2zm6-4.3c-.1-.1-.2-.1-.3-.2-.9-.4-1.7-.8-2.5-1.3-.1 0-.2-.1-.3 0l-.1.2c.1.9.3 1.8.5 2.7.1.3 0 .5-.2.7-.6.7-1.2 1.4-1.9 2l-.1.1c-.1.1 0 .2.1.3h.2c.9.1 1.8.3 2.8.4.3 0 .4.2.5.4.4.8.8 1.7 1.2 2.5 0 0 0 .1.1.1.1.1.2.1.3 0l.1-.1c.4-.8.8-1.7 1.2-2.5.1-.2.2-.3.4-.3.7-.1 1.3-.2 2-.3.3 0 .6-.1.9-.1.1 0 .2-.1.2-.1 0-.1 0-.1-.1-.2l-.1-.1c-.7-.7-1.3-1.4-1.9-2-.2-.2-.3-.5-.2-.8.2-.9.3-1.8.5-2.7 0-.1 0-.2-.1-.2h-.3c-.8.4-1.6.9-2.4 1.3-.2.1-.3.1-.5.2zm7.6-.2c.3 0 .5.2.5.4.1.2-.1.5-.3.6-.4.2-.8.3-1.2.4-.2.1-.5-.1-.6-.3-.1-.2 0-.6.2-.7.5-.1.9-.3 1.4-.4zm-3.2 8.2c.1 0 .3.1.4.2l.6.9c.2.3.1.6-.1.8-.2.2-.6.1-.8-.1-.2-.3-.4-.6-.7-.9-.1-.2-.1-.4 0-.6.1-.3.3-.3.6-.3zm-8.7 0c.4 0 .7.5.5.8-.2.3-.5.7-.7 1-.2.2-.5.2-.7.1-.2-.2-.3-.5-.1-.7.2-.3.5-.6.7-1 .1-.2.2-.3.3-.2zM9 1.4V2c0 .3-.2.5-.5.5S8 2.3 8 2V.9c0-.3.2-.5.5-.5.2-.1.5.1.5.4v.6z"
          class="st1"
          opacity=".2"
        />
      </svg>
      <svg class="heart" xml:space="preserve" viewBox="0 0 16.8 16">
        <path
          fill="#f38bb3"
          d="M10.4 5.6h1.3c1.1 0 2.1.3 2.9 1 1.6 1.3 2 3.6 1 5.4-.6 1.2-1.6 2-2.9 2.4-1.3.5-2.7.7-4.1.7-1.5.1-3.1 0-4.6-.3-.9-.1-1.4-.6-1.7-1.4-.6-1.9-1-3.7-1.1-5.7-.1-1.1-.1-2.3.3-3.5.6-1.9 1.8-3.1 3.8-3.4 2.3-.4 4.4 1.1 4.9 3.3.1.5.1 1 .2 1.5v.1-.1z"
          opacity=".2"
        />
      </svg>
      <svg class="plus" xml:space="preserve" viewBox="0 0 8.9 8.6">
        <g class="st0">
          <path
            fill="#fdbd5c"
            d="M7.8 5.2h-7c-.4 0-.8-.4-.8-.9s.4-.8.8-.8h7c.5 0 .8.4.8.8 0 .5-.3.9-.8.9z"
            class="st1"
          />
        </g>
        <g class="st0">
          <path
            fill="#fdbd5c"
            d="M4.3 8.6c-.5 0-.8-.4-.8-.8v-7c0-.4.4-.8.8-.8.5 0 .8.4.8.8v7c.1.5-.3.8-.8.8z"
            class="st1"
          />
        </g>
      </svg>

      <svg class="heart-2" xml:space="preserve" viewBox="0 0 27.3 23.9">
        <path
          fill="none"
          stroke="#fcdede"
          stroke-miterlimit="10"
          stroke-width="2"
          d="M12.7 5.4c.4-.5.8-1 1.2-1.6 1-1.3 2.3-2.2 4-2.6 3.1-.7 6.3.9 7.6 3.8.9 1.9.9 3.9.3 5.8-.6 2.1-1.7 3.9-3 5.7-1.4 1.9-2.9 3.7-4.6 5.4-.9.9-2.1 1.2-3.3.7-2.8-1-5.5-2.3-8-4-1.6-1.1-3.1-2.3-4.2-3.8C1 12.3.7 9.7 2.1 7c1.5-3 5.3-4.3 8.6-2.8.7.3 1.3.8 1.9 1.2.1 0 .2.1.2.2 0-.1 0-.1-.1-.2z"
          opacity=".46"
        />
      </svg>
    </div>
  </div>
</template>

<script>
import Form from "./components/Form.vue";
export default {
  components: {
    Form
  },
  data() {
    return {
      title: "Już wkrótce otwarcie!",
      desc: "Bambini - Klub Malucha",
      facebook: {
        descFacebook: "Śledź nas na Facebooku i bądź na bierząco",
        linkFacebook: "https://www.facebook.com/bambini.klub.malucha/",
        shortLink: "/bambini.klub.malucha"
      }
    };
  }
};
</script>

<style>
body {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  margin: 0;
  padding: 0;
}
#app {
  font-family: "Cabin", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow: hidden;
}
.contaner {
  padding: 0 20px;
  width: 100%;
  height: 100vh;
}
.wraper {
  position: absolute;
  width: 100%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.logo {
  margin-bottom: 20px;
}
.title {
  font-family: "Paytone One", sans-serif;
  font-size: 71px;
  margin: 0;
  padding: 0;
  color: #464646;
  line-height: 1;
  margin-bottom: 15px;
}
.desc {
  font-size: 21px;
  margin: 0;
  padding: 0;
  color: #179ad7;
  margin-bottom: 0px;
}
@media only screen and (max-width: 768px) {
  .title {
    font-size: 41px;
  }
}
.facebook-info a {
  color: #76c16b;
  display: flex;
  align-items: center;
  justify-content: center;
}
.facebook-info a svg {
  /* width: 22px; */
  margin-right: 15px;
}
#bg-animate {
  position: absolute;
  max-width: 600px;
  width: 100%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: -1;
}
.star {
  position: absolute;
  top: 40%;
  left: 25%;
  width: 22px;
  height: 22px;
  animation-name: float;
  animation-duration: 15s;
  animation-iteration-count: infinite;
}
.heart {
  position: absolute;
  top: 15%;
  left: 40%;
  width: 22px;
  height: 22px;
  animation-name: float2;
  animation-duration: 5s;
  animation-iteration-count: infinite;
}
.plus {
  position: absolute;
  top: 25%;
  right: 30%;
  width: 22px;
  height: 22px;
  opacity: 0.3;
  animation-name: float2;
  animation-duration: 10s;
  animation-iteration-count: infinite;
}
.heart-2 {
  position: absolute;
  bottom: 15%;
  right: 40%;
  width: 22px;
  height: 22px;
  animation-name: float;
  animation-duration: 5s;
  animation-iteration-count: infinite;
}

@keyframes float {
  0% {
    transform: translatey(0px);
  }
  50% {
    transform: translate(-20px, -30px);
  }
  100% {
    transform: translatey(0px);
  }
}
@keyframes float2 {
  0% {
    transform: translatey(0px);
  }
  50% {
    transform: translate(0px, -20px);
  }
  100% {
    transform: translatey(0px);
  }
}

@media only screen and (max-width: 768px) {
  .title {
    font-size: 41px;
  }
  .star {
    top: 72%;
    left: 15%;
  }
  .plus {
    position: absolute;
    top: 15%;
    right: 20%;
  }
}
</style>
