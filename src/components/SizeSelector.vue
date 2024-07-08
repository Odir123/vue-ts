<script setup lang="ts">

const possibleSizes = ['XS', 'S', 'M', 'L', 'XL', 'XXL'];

// JavaScript
//const props = defineProps({
//  selectedSize: { type: String, requerid: true}
//});

//const emits = defineEmits({
   // onChangeSize: String
//});

//TyoeScript
const props = defineProps<{
    selectedSize: string
}>();


const emits = defineEmits<{
    ( event: 'onChangeSize', value: string): void,
}>();

</script>



<template>
  <button
    v-for="size in possibleSizes"
    :class="{ 'active': props.selectedSize == size }" 
    @click="emits('onChangeSize', size)"
  >
   
    {{ size }}
  </button>

</template>
