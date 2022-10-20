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
h1 {
    color: red;
}
button {
    background: black;
    color:white;
    border: 0;
    border-radius: 0;
}
</style>
