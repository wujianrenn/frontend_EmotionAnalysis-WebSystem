<template>
  <ul class="todo-main">
        <MyItem 
        v-for="todoObj in todos" 
        :key="todoObj.id" 
        :todo="todoObj" 
        :checktodo="checktodo"
        :shanchu="shanchu"
        />      
    </ul>
</template>

<script>
import MyItem from './MyItem.vue';
export default {
name:'MyList',
components: {MyItem},
    
    // data() {
    //     return {
    //         todos:[
    //             {id:'001',title:'吃饭',done:true},
    //             {id:'002',title:'喝酒',done:false},
    //             {id:'003',title:'抽烟',done:true},
    //         ]
    //     }
    // },
    props:['todos','checktodo','shanchu']

}
</script>

<style scoped>
/* main */
.todo-main{
    margin-left: 0px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding: 0px;
}

.todo-empty{
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
}
</style>