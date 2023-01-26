<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)

let testarray = [[0,1,2],[3,4,5],[6,7,8]]
</script>

<template>
    <h1>{{ msg }}</h1>
    <div class="card">
        <button type="button" @click="count++">count is {{ count }}</button>
        <p>
        Edit
        <code>components/HelloWorld.vue</code> to test HMR
        </p>
    </div>

    <div>
        <table border="1">
            <tbody>
                <tr v-for="value_array in testarray">
                        <td v-for="value in value_array">
                            <div>{{value}}</div>
                        </td>
                </tr>
            </tbody>
        </table>
    </div>
    <!-- <div v-for="value_array in testarray">
        <div v-for="value in value_array">
                    {{value}}
        </div>

    </div> -->

</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
