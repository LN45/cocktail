<template>
  <div>
    <h1>Connexion</h1>

    <form @submit.prevent='login'>
        <div class="formgroup">
            <label for="userr-login">Login</label>
            <input type="text" id="user-login" v-model="user.login">
        </div>
        <div class="formgroup">
            <label for="user-password">Password</label>
            <input type="text" id="user-password" v-model="user.password">
        </div>
        <div class="formgroup">
            <button type="submit" class="button">Connexion</button>
        </div>
    </form>
  </div>
</template>

<script>
export default {
    name: 'Login',
    data() {
        return {
            user: {
                login: '',
                password: ''
            }
        }
    },
    methods: {
        login() {
            console.log('stop form');
            console.log(this.user);
            localStorage.setItem('token', this.user.login);
            this.$router.push('/admin');
        }
    }
}
</script>

<style>

</style>