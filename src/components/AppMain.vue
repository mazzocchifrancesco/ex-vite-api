<script>
import AppCard from './AppCard.vue'
import { database } from "./database.js" //state management
import axios from 'axios'; //importo Axios




export default {
    name: "AppMain",
    components: {
        AppCard,
    },
    data() {
        return {
            database
        }
    },
    mounted() {
        this.getBeer()
    },
    methods: {

        getBeer() {
            axios.get(this.database.apiUrl).then(risultato => {
                console.log(risultato);
            });
        }
    }
}
</script>
<template>
    <AppCard />
</template>
<style scoped></style>