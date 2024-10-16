
<script setup>
    const props = defineProps({
        state: {
            type: Number, default: 0,
        },
        
    })


</script>


<template>
    <div v-if="props.state <= 2 " >
        <div class="Brique" v-if="props.state == 0" >
             {{ props.place}}
        </div>
        <div class="Triangle" v-else-if="props.state == 1">

        </div>
        <div class="Cercle" v-else-if="props.state == 2">

        </div>
    </div>
    
</template>


<!-- scoped = css que pour ce fichier -->
 <!-- "." pour les class et "#" pour les Id -->
<style lang="scss" scoped>
    .Brique {
        width: 60px ;
        height: 60px;
        background-color: cyan;
    }
    .Triangle{
        width: 0;
        height: 0;
        border-style: solid;
        border-width: 0 30px 60px 30px;
        border-color: transparent transparent green transparent;


    }
    .Cercle {
        width: 60px ;
        height: 60px;
        background-color: magenta;
        border-radius: 50%;
    }

</style>
