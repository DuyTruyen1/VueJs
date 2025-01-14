<script setup>
import { reactive , ref } from 'vue';
// dùng ref thì phải bắt buộc có value
// dùng reactive thì không  cần phải chấm đến value
 const object = reactive({
  count:2,
  user:{
    age:18
  },
  arr: [1,2,3]
 })

 const change = () => {
  object.value.count++
  object.value.user.age++
  object.value.arr.push(4)
 }
</script>

<template>
  <div> = 
    <p>Count: {{ object.count }}</p>
    <p>Age: {{ object.user.age }}</p>
    <p>Age: {{ object.arr }}</p>
  <button @click="change">Increase</button>
  </div>
</template>
