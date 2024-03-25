<template>
    <div>

    </div>
</template>

<script setup>
import axios from 'axios';
import { useRoute } from 'vue-router';

const route = useRoute();
const getWeatherData = async () => {
    try {
        const weatherData = await axios.get(`https://api.openweathermap.org/data/3.0/onecall?lat=${route.query.lat}&lon=${route.query.lng}&exclude={part}&appid=55eac4c8e1ea5be90ed532e3972ae179&units=imperial
`);
    } catch (error) {
        console.log(error)
    }
};
</script>
