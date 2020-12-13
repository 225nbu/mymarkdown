<template>
    <div id="home">
        <h1>{{msg}}</h1>
        <button @click="googleLogin">Googleアカウントでログイン</button>
    </div>
</template>
<script>
export default {
    name:"home",
    data(){
        return{
            msg:"Welcome to Markdown"
        };
    },
    methods:{
        googleLogin:function(){
            var provider = new firebase.auth.GoogleAuthProvider();
            firebase.auth().signInWithRedirect(provider);
        }
    }
};
</script>