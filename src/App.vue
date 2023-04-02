<template>
 <div class="app">
 <p>{{ name }}-{{ age }}</p>
  <button @click="changeName('Manzi')">Change name </button>
  <button @click="changeAge('109')">Change age </button>
 </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from 'vue';
export default defineComponent({
  name: 'App',
  components: { },
  // data (){
  //   return {
  //     name: "Link",
  //     age: 30 as number | string
  //   }
  // },

  setup(){ // for composition api we introduce setup and we either use reactive or refs

    // for reactive
  //   const state = reactive({
  //   name : 'LINK',
  //   age: 10 as string | number
  // })
  // return{...toRefs(state)}

  // for reference
const name = ref('LINK')
const age = ref<string | number>(40)
return { name , age}
  
  },
  methods:{
    changeName (name : string){
      this.name = name
      return name
    },
    changeAge(age: number | string){
      this.age = age
      return age
    }
  }
});
</script>

<style>

</style>
