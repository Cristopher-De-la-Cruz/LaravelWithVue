<template>
    <div>
        <h3>{{counter}}</h3>
        <button @click="increment">Increment</button>
        <button @click="decrementarCounter">Decrementar</button>
        <p>{{ msj }}</p>
    </div>
</template>


<script lang="ts">
    import {defineComponent, Ref, ref} from 'vue';
    export default defineComponent({
        name: 'counterComposition',
        setup() {
            let counter:Ref = ref(0);
            let msj:Ref = ref('');
            
            const increment = ():void => {
                counter.value++
                if(counter.value === 10){
                    msj.value = 'Es 10'
                } else{
                    msj.value = ''
                }
            }
            const decrementarCounter = ():void => {
                counter.value--
                if(counter.value === 10){
                    msj.value = 'Es 10'
                } else{
                    msj.value = ''
                }
            }
            return {counter, msj, increment, decrementarCounter};
        }
    })
</script>








