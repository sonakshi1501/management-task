<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red' : 'green'"/>
  </header>
</template>

<script>
import Button from "../components/Button.vue"
export default {
  name: "Header",
  props: ['title', 'showAddTask'],                         //          1st way
  //    props: {
  //     title: String
  //    }                        2nd way
//   props: {
//     title: {
//       type: String,
//       default: "Hello World",             3rd way
//     },
//   },
    components:{
        Button
    },
    emits: ['toggle-add-task']

};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>