<template>
    <div class="main">
        <form>
            <h4>Создание поста</h4>
            <input class="" type="text" placeholder="Название поста">
            <input type="text" placeholder="Название описания">
            <button>Создаnm</button>
        </form>
        <div class="post" v-for="post in posts" :key="post.posts">
            <div> <strong> Название:</strong> {{post.title}} </div>
            <div> <strong> Описание:</strong> {{post.body}} </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            posts:[
                {id:1, title: 'Javascript', body: 'Описание поста'},
                {id:2, title: 'Javascript 2', body: 'Описание поста 2'},
                {id:3, title: 'Javascript 3', body: 'Описание поста 3'},
            ]
        }
    },
    methods: {
        addLike(){
            this.likes += 1;
        },
        disLike(){
            this.dislikes += 1;
        }
    }
}
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.post{
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;
}
</style>