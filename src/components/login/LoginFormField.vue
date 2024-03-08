<!-- gotta make this secure/non-secure -->
<script setup lang="ts">
defineProps<{
    title: string
    text: string
    iconSrc: string
    iconAlt: string
}>()
</script>

<template>
    <div class="field_title">
        <span>{{ title }}</span>
        <div class="field">
            <div class="text">
                <span>{{ text }}</span>
            </div>
            <img :src="iconSrc" :alt="iconAlt" />
        </div>
    </div>
</template>

<style scoped>
.field_title {
    display: flex;
    flex-direction: column;
    width: 100%;
    padding-bottom: 0.5em;
}

.field_title > span {
    /* header of field: Username, Password, Email, ... */
    font-weight: 400;
    color: #fff;
    font-size: 2em;
    letter-spacing: 0.055em;
}

.field {
    display: flex;
    flex-direction: row;
    border-style: solid;
    border-width: 0em 0em 0.05em 0em;
    border-color: #ffffff;
    width: 100%;
}

.text {
    /* field input */
    display: flex;
    width: 100%;
    font-size: 1.2em;
    align-items: center;
    color: rgb(255, 255, 255, 0.6);
}

.field img {
    align-self: flex-end;
    width: 3rem;
    height: 3rem;
}
</style>
