<template>
<div id="DinoCard">
<header>{{title}}</header>
<div>
<input id="itemForm" v-on:keypress.enter="addItem"/>
<button v-on:click="addItem">Add Dinosaur</button>
</div>
<ul>
<li v-for="(item, index) in items">
<button v-on:click="deleteItem(index)">X</button>
{{item.text}}
</li>
</ul>
</div>
</template>

<script>
export default {
  name: 'DinoCard',
  data () {
    return {
    title: "Dinosaurs",
    items: [
      {text: "stegasaurus", update: false},
      {text: "velociraptor", update: false},
      {text: "T Rex", update: false}
    ]
    }
  },
  methods: {
    addItem: function(){
      let input = document.getElementById('itemForm');

      if(input.value !== ''){
        this.items.push({
          text: input.value
        })
      }
      input.value = "";
    },
    deleteItem: function(index){
      
      this.items.splice(index,1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  display: flex;
  flex-direction: column;
  justify-content: flex;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
