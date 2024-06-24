<template>
    <div class="first-app">
        {{ msg }}
        <p><router-link to="/second">去第二个页面</router-link></p>
        <Confirm text="注册" @message="getMessage"></Confirm>
    </div>
</template>

<script>
import Confirm from '../sub/Confirm'
export default {
    name : "First",
    components : {
        Confirm
    },
    data() {
        return {
            msg : "Welcome to First App"
        };
    },
    methods: {
        getMessage(val) {
            alert(val);
        }
    }
};
</script>


<style lang="less" scoped>
.first-app {
    font-size: 30px;
    .link {
        a {
            color: red;
        }
    }
}
</style> 

<!-- http://localhost:8080/#/first -->
