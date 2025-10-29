<script>
    //import component
    import SoundIcon from './subcomponents/SoundIcon.vue';

    export default { 
        data() {
            return {
                soundLevel: 0
            }
        },
        components: { SoundIcon },                            // <- register here
    }
</script>

<template>

   Sound level
    <input type="number" min="0" max="3" v-model="soundLevel"> 
    <!-- TODO: Add Code Here to make use of the component -->
    <!-- Pass soundLevel to the child as a prop -->
    <sound-icon :level="soundLevel" ></sound-icon>

</template>

