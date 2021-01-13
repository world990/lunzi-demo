<template>
 
  <Button @click="open">12332</Button>
  <hr/>
  <Switch v-model:value='bool'/>
  <hr/>
  <Tabs v-model:selected='tabSelected'>
    <Tab title="tab1"></Tab>
    <Tab title="tab2"></Tab>
  </Tabs>
</template>

<script>

import {Button,Switch,Dialog,openDialog,Tabs,Tab } from 'lunzi-ui-1'
import 'lunzi-ui-1/dist/lib/lunzi.css'
import { ref } from 'vue'
export default {
  name: 'App',
  components: {
    Button,Switch,Dialog,Tabs,Tab
  },
 data(){
   return {
     bool:false,
tabSelected:'tab1'
   }
 },
 methods:{
   open(){
     openDialog({title:'标题',content:'内容'})
   }
 }
}
</script>

