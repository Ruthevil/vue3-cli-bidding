<template>
    <div class="hello">
        <h1 ref="root">{{ msg }}</h1>
        <div>count:{{state.count}}</div>
        <div>double:{{double}}</div>
        <button @click="add">add</button>
    </div>
</template>

<script>
    import {reactive, computed, watch, ref, onMounted} from "vue"

    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        },
        setup() {
            const state = reactive({
                count: 0
            });

            const double = computed(() => state.count * 2);

            // ref 创建响应式数据 基本类型数据装箱响应式
            const root = ref(null);
            onMounted(() => {
                const dom = root.value;
                dom.style.color = "red";
            });

            const add = () => {
                state.count++
            };

            watch(() => state.count, value => console.log(`state changed ${state.count}`));

            return {
                state, double, add, root
            }
        }
    }
</script>

<style scoped>

</style>
