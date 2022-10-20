<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        {{ counter }}
        <button @click="increment">Increment</button>
    </div>
</template>

<script>
import {ref} from "vue";

export default {
    name: 'HelloWorld',
    props: {
        msg: String
    },
    setup() {
        const counter = ref(0);
        const increment = () => counter.value += 1;

        return {
            counter,
            increment
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
    list-style-type: none;
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
