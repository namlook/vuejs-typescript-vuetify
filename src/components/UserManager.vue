
<template>
    <div>
       aaaaa {{message}} aaa
    </div>
</template>



<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'
import { State } from 'vuex-class'

@Component({})
export default class extends Vue {
    @State message
}
</script>