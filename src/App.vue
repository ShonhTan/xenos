<template>
  <div id="app">

    <router-view/>
    
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
export default {
  components: {
    Header
  }
}
</script>


<style lang="scss">
@import './assets/css/reset.css';
@import './assets/css/jam.min.css';

@font-face {
  font-family: "Barlow-Bold";
  src: url("./assets/fonts/Barlow-Bold.ttf");
}
@font-face {
  font-family: "Barlow-Medium";
  src: url("./assets/fonts/Barlow-Medium.ttf");
}
@font-face {
  font-family: "Barlow-Regular";
  src: url("./assets/fonts/Barlow-Regular.ttf");
}

//VARIABLE
:root {
  --font-regular: "Barlow-Regular";
  --font-medium: "Barlow-Medium";
  --font-bold: "Barlow-Bold";
  --gradient-from: #FF5F6D;
  --gradient-to: #FFC371;
  --main-orange:#FF966F;
  --main-dark: #333333;
  --secondary-dark: #4F4F4F;
  --main-grey: #C8C8C8;
  --main-dark-white: #F8F8F8;
  --main-white: #FFFFFF;
}

body {
  height: 100vh;
  overflow-x: hidden;
  background-color: var(--main-dark);
  --header-color:var(--main-dark);
  --header-item-color: #ffffff;
}
#app {
  @media (min-width: 768px) { 
  }
    //   max-width: 100vw;
    // overflow-x:hidden;
  height: 100%;
}

h1 {
  font-size:36px;
  font-family: var(--font-bold);
}
h2 {
  font-size:32px;
  font-family: var(--font-bold);
}
h3 {
  font-size:28px;
  font-family: var(--font-bold);
}
h4 {
  font-size:24px;
  font-family: var(--font-bold);
}
h5 {
  font-size:18px;
  font-family: var(--font-regular);
}
h6 {
  text-transform: uppercase;
  font-size:12px;
  font-family: var(--font-bold);
}
p {
  font-size:14px;
  line-height: 22px;
  font-family: var(--font-regular);
}

label {
  text-transform: uppercase;
  font-size:12px;
  font-family: var(--font-bold);
}

.gradientText {
  background: linear-gradient(to right,var(--gradient-from), var(--gradient-to));
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.container {
  box-sizing: border-box;
  padding-left:43px;
  padding-right:43px;

  @media(min-width: 768px){
    padding-right: 60px;
    padding-left: 60px;
  }
  @media(min-width: 1440px){
    padding-right: 122px;
    padding-left: 122px;
  }
}


// Button////////////////////////////////

button, .button {
  font-family: var(--font-bold);
  padding: 12px 32px;
  font-size: 14px;
  color: white;
  cursor: pointer;
  text-align:center;
  border: none;
  background-size: 300% 100%;
  background-image: linear-gradient(45deg, #FF5F6D, #FFC371, #FF5F6D, #FFC371 );
  box-shadow: 0px 4px 10px rgba(255, 150, 111, 0.15);
  border-radius: 50px;
  transition: all .4s ease-in-out;
  -o-transition: all .4s ease-in-out;
  -webkit-transition: all .4s ease-in-out;
  transition: all .4s ease-in-out;

  &:hover {
    background-position: 100% 0;
    transition: all .4s ease-in-out;
    -o-transition: all .4s ease-in-out;
    -webkit-transition: all .4s ease-in-out;
    transition: all .4s ease-in-out;
  }
  &:focus {
    outline: none;
  }
  &:disabled {
    color: var(--main-grey);
    background: var(--secondary-dark) !important;
    box-shadow: none;
    cursor: not-allowed;
  }

  &Container {
    width:min-content;
    color: white;
    white-space: nowrap;
    text-decoration: none;
  }
}

#app {
  position: relative;
}



</style>
