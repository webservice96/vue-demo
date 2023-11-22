<script setup>
const props = defineProps({
    label: {
        type: String,
        default :"This is a button"
    },
    url:{
        type: String,
        default:"#"
    },
    color:{
        type: String,
        default: "blue"
    }
})

function getColor(){
    return `bg-${props.color}-500 hover:bg-${props.color}-700`
}
</script>
 
<template>
    <a target="_blank" :href="url" :class="getColor()" class=" text-white font-bold py-2 px-4 rounded">
        {{ label }}
    </a>
</template>
 
<style scoped></style>