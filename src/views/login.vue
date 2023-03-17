<template>
    <div class="center">
        <v-row>
            <v-col cols="2" offset="5" md="4" offset-md="4" :style="`background-color:${randomColor()}`" style="padding: 2%; border-radius: 5%;">
                <v-avatar size="120">
                    <v-img src="@/assets/logo.png"></v-img>
                </v-avatar><br>
                <v-text-field label="Username" v-model="username"></v-text-field>
                <v-text-field label="Password" v-model="password" type="password"></v-text-field><br>
                <v-btn small elevation="5" rounded @click="authenticate()">Spank me</v-btn>
            </v-col>

        </v-row>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                username: "",
                password: ""
            }
        },
        methods: {
            authenticate() {
                alert("Ohhhh yeahhhhhhhhhhhhhh💦💦🍑🍑🍑")
            }
        },
        
    }
</script>

<style lang="scss" scoped>

</style>