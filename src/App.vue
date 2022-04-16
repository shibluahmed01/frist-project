<template>
    <div class="container">
        <button @click="godBoy='compHome'">Home</button>
        <button @click="godBoy='compAbout'">About</button>
        <button @click="godBoy='compContact'">Contact</button>
        

        <keep-alive>
            <component :is="godBoy"></component>
        </keep-alive>
    </div>
</template>

<script>
import compHome from './Components/HomeView.vue'
import compAbout from './Components/AboutView.vue'
import compContact from './Components/ContactView.vue'
export default{
    data(){
        return{
            godBoy: compHome
        }
    },
    components: {
        compHome,
        compAbout,
        compContact
    }
}
</script>