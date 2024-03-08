<script setup lang="ts">
import LoginFormField from '@/components/login/LoginFormField.vue'
</script>

<template>
    <div class="form">
        <div class="logo">
            <img src="../../public/MealBuddy.png" alt="MealBuddy" />
        </div>
        <div class="login">
            <div class="fields">
                <LoginFormField
                    title="Username"
                    text="john123"
                    iconSrc="/user.svg"
                    iconAlt="username"
                />
                <LoginFormField
                    title="Password"
                    text="..."
                    iconSrc="invisible.svg"
                    iconAlt="password"
                />
            </div>
            <div class="submit">
                <div>
                    <span onclick="submitForm">Log In</span>
                </div>
                <div>
                    <span onclick="forgotPassword">Forgot password</span>
                </div>
            </div>
        </div>
        <div class="signUp">
            <span
                >If you don't have an account,
                <span class="blueClick" onclick="signUp">sign up</span></span
            >
        </div>
    </div>
</template>

<style scoped>
.form {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 28rem;
    background-color: rgb(0, 0, 0, 0.8);
    font-family: 'Josefin Slab';
    font-weight: 400;
    color: #fff;

    padding-left: 2.5rem;
    padding-right: 2.5rem;
}

.form > div {
    padding-bottom: 3em;
    width: 100%;
}

.login {
    margin-bottom: 2em;
}

.fields {
    width: 100%;
    padding-bottom: 1em;
}

.logo {
    display: flex;
    justify-content: center;
}

.logo > img {
    width: 10rem;
    height: 10rem;
}

.submit {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;
}

.submit > div {
    /* underlining */
    border-style: solid;
    border-width: 0em 0em 0.05em 0em;
}

.submit > div > span {
    letter-spacing: 0.04em;
    font-weight: 300;
    font-size: 1.3em;
}

.signUp {
    width: 100%;
    font-weight: 300;
    font-size: 1.2em;
}

.blueClick {
    /* click to sign up */
    color: rgb(0, 0, 200);
    text-decoration: underline;
    font-weight: 800;
}
</style>
