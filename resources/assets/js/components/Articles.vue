<template>
<div class="col-md-6"> 
    <h2>Article 12</h2> 
</div>
 </template>

<script>
export default {
    data() {
        return {
            articles: [],
            article:{
                id:'',
                title: '',
                body:''
            },
            article_id: '',
            pagination:{},
            edit:false
        }
    },
    created(){
        this.fetchArticles();
    },
    methods: {
        fetchArticles() {
            fetch('api/articles')
            .then(res => res.json())
            .then(res => {
                console.log(res.data)
            });
        },
    }
    
}
</script>
