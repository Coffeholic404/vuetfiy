<template>
    <v-container fluid>
        <v-row justify="center">
            <v-col cols="4">
                <v-card class="mx-auto pa-4">
                    <v-card-title>Login Here</v-card-title>
                    <v-card-item>
                        <v-form @submit.prevent="submit">
                            <v-text-field v-model="form.email" label="email" variant="solo"
                                prepend-inner-icon="mdi-email"></v-text-field>

                            <v-text-field type="password" v-model="form.password" label="password" variant="solo"
                                prepend-inner-icon="mdi-key"></v-text-field>
                            <v-checkbox v-model="form.remeber" color="indigo" label="Remeber Me"
                                hide-details></v-checkbox>
                            <v-btn color="purple-darken-1" class="mt-2" type="submit" block>Submit</v-btn>
                        </v-form>
                        <v-card-action>
                            <v-btn block to="/register" text="Register" color="purple-darken-2" class="my-2">
                            </v-btn>
                        </v-card-action>
                    </v-card-item>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';

function submit() {
    alert(JSON.stringify(form.value))
}

const form = ref({
    email: '',
    password: '',
    remeber: false
})
</script>
