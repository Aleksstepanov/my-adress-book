<template>
  <form class="form" @submit.prevent="registerFormClickHandler()">
    <div class="form__title">
      <div class="fomr_back"></div>
      <div class="form__logo">
        <Logo />
      </div>
      <h1 class="title">Register</h1>
    </div>
    <div class="form__main">
      <div class="form__group">
        <label> User Name </label>
        <input v-model="userName" type="text" class="form-input" />
      </div>
      <div class="form__group">
        <label> Email </label>
        <input v-model="email" type="email" class="form-input" />
      </div>
      <div class="form__group">
        <label> Password </label>
        <input v-model="password" type="password" class="form-input" />
      </div>
      <div class="form__group">
        <label> Confirm Password </label>
        <input type="password]" class="form-input" />
      </div>
      <div class="form__group">
        <button class="form__button">Register</button>
      </div>

      <router-link to="/login" class="form__back"
        >Back to login form</router-link
      >
    </div>
  </form>
</template>

<script>
import Logo from "@/components/Logo.vue";

export default {
  name: "Register",

  data() {
    return {
      userName: "",
      email: "",
      password: "",
    };
  },

  components: {
    Logo,
  },

  methods: {
    registerFormClickHandler() {
      console.log(this.userName, this.email, this.password);
    },
  },
};
</script>

<style lang="scss">
.form {
  position: relative;
  background: #fff;
  width: 380px;
  border-radius: 4px;
  box-shadow: 0 0 30px rgba(black, 0.1);
  box-sizing: border-box;
  overflow: hidden;
}

.title {
  text-align: center;
  font-size: 24px;
}
.form__title {
  display: flex;
  flex-direction: column;
}

.form__logo {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
}

.form__title {
  font-size: 24px;
}

.form__main {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 30px;
}
.form__group {
  display: flex;
  flex-direction: column;
  width: 80%;
  justify-content: center;
  margin-top: 15px;
}
label {
  display: block;
  margin: 0 0 10px;
  color: rgba(black, 0.6);
  font-size: 12px;
  font-weight: 500;
  line-height: 1;
  text-transform: uppercase;
}
.form__button {
  margin-top: 50px;
  margin-bottom: 50px;
  outline: none;
  background: #4285f4;
  width: 100%;
  border: 0;
  border-radius: 4px;
  padding: 12px 20px;
  color: #fff;
  font-family: inherit;
  font-size: inherit;
  font-weight: 500;
  line-height: inherit;
  text-transform: uppercase;
  cursor: pointer;
}
.form-input {
  outline: none;
  display: block;
  background: rgba(black, 0.1);
  width: 100%;
  border: 0;
  border-radius: 4px;
  box-sizing: border-box;
  padding: 12px 20px;
  color: rgba(black, 0.6);
  font-family: inherit;
  font-size: inherit;
  font-weight: 500;
  line-height: inherit;
  transition: 0.3s ease;
}
</style>
