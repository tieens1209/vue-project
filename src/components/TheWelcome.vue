<script setup>
import { reactive, ref } from "vue";
// const hello = 'Hoc VueJS';
// console.log(hello);
// const array = [1, 2, 3, 4, 5];
// let a = 5;
// let b = 10;
// let c = a + b;
// const objectHello = {
//   name: 'tien',
//   title: 'VueJS'
// };

// ref sử dụng 1 đối tượng và thuộc tính
// truy cập thuộc tính ref bằng cách .value
// const count = ref(0);
// count.value = count.value + 1;
// count.value = count.value + 2;
// count.value = count.value + 3;

// reactive cho phép mình sử dụng 1 object trong đó có nhiều đối tượng
// truy cập thuộc tính reactive ko cần .value, chúng ta có thể sd trực tiếp thuộc tính có sẵn
// const count = reactive({
//   title: 'VueJS',
//   author: 'Tien',
//   age: 25,
// });
// count.age = count.age + 1;
// console.log('count', count.title, count.author, count.age);

// const count = ref(1);

// const increase = () => {
//   count.value++;
// }


// const submitForm = () => {
//   count.value++;
// };

// const textInput = ref('');

const props = defineProps(['count']);
const emit = defineEmits(['handle-increase']);
const onIncrease = () => {
  emit('handle-increase', 10)
}; 
</script>

<template>
  <!-- <div class="red">This is {{ count }}</div>
  {{ objectHello.name }}
  <h3>{{ hello }}</h3>
  <h4>{{ array }}</h4>
  {{ c }} -->

  <!-- <form @submit.prevent="submitForm">
    <div>Count: {{ count }}</div>
    <input type="text" v-model="count">
    <button type="submit">Increase</button>
  </form> -->

  <!-- <div>Text: {{ textInput }}</div>
  <input type="text" v-model="textInput"> -->


  <div>Count: {{ props.count }}</div>
  <button @click="onIncrease">Increase</button>

</template>

<style>
/* .red {
  color: red;
} */
</style>
