<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood which are used for the bootstrap post 
        // 1. Declare props and define the inputs the components would need to render a post 
        props: {
            subject: String,
            entry: String,
            mood: String,
        },
        // 3.this makes the image reactive to mood changes 
        computed: {
            imgLoc(){
                console.log(this.mood)
                return `/assets/${this.mood.toLowerCase()}.png`
            }
        }
    }
</script>


<template>
    <!-- TODO: add your template code here. Use boostrap card -->
    <!-- 2.
    - add the template for bootstrap card to verify the placeholders 
    -->
    <div class="card mb-3" style="width: 18rem;">
    <img :src="imgLoc" class="card-img-top" alt="...">
    <div class="card-body">
        <h5 class="card-title">{{subject}}</h5>
        <p class="card-text">{{entry}}</p>
    </div>
    </div>
</template>

