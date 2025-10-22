<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                item:"",
            }
            
        },
        methods:{
            
            add(){
                this.items.push(this.item)
            },
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item,index) in items">
            {{item}}
            <button class="btn" @click="items.splice(index,1)">Delete</button>
        </li>
    </ul>
    <input v-model="item"></input>
    <button @click="add()">Add</button>
</template>
