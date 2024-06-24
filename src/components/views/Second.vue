<template>
    <div class="second-app">
        {{ msg }}
        <p><router-link to="/first">去第一个页面</router-link></p>
        <Confirm text="注册" @message="getMessage"></Confirm>
    </div>
</template>

<script>
import Confirm from '../sub/Confirm'
export default {
    name : "Second",
    components : {
        Confirm
    },
    data() {
        return {
            msg : "Welcome to Second App"
        };
    },
    methods: {
        getMessage(val) {
            alert(val);
        }
    }
};
</script>

<style>

</style>