<template>
    <div class="container">
<!--        <div class="col-4 offset-4 mt-5">-->
<!--&lt;!&ndash;            <div class="card">&ndash;&gt;-->
<!--&lt;!&ndash;                <div class="card-header text-center">&ndash;&gt;-->
<!--&lt;!&ndash;                    <h2><strong>{{count}}</strong></h2>&ndash;&gt;-->
<!--&lt;!&ndash;                </div>&ndash;&gt;-->
<!--&lt;!&ndash;                <div class="card-body text-center d-flex justify-content-between p-5">&ndash;&gt;-->
<!--&lt;!&ndash;                    <button type="button" class="btn btn-success" @click="decrement">-</button>&ndash;&gt;-->
<!--&lt;!&ndash;                    <button type="button" class="btn btn-primary" @click=" increment">+</button>&ndash;&gt;-->
<!--&lt;!&ndash;                </div>&ndash;&gt;-->
<!--&lt;!&ndash;            </div>&ndash;&gt;-->
<!--        </div>-->


        <div class="comment col-8 offset-2" v-for:="comment in comments" v-bind:key="comments.id">
            <form>
                <input class="form-control form-control-lg" name="id" type="text">
                <input class="form-control" name="name" type="text">
                <input class="form-control form-control-sm" name="email" type="text">
            </form>

            <div><b>ID: </b>{{comment.id}}</div>
            <div><b>Name: </b>{{comment.name}}</div>
            <div><b>Email: </b>{{comment.email}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return{
                comments:[
                    {
                        id: 1,
                        name: "ali",
                        email: "ali@gmail.com"
                    },
                    {
                        id: 2,
                        name: "yunus",
                        email: "yunus@gmail.com"
                    },
                    {
                        id: 3,
                        name: "yusuf",
                        email: "yusuf@gmail.com"
                    }
                ]
            }
        },
        // methods:{
        //     increment(){
        //         this.count+=1
        //     },
        //     decrement(){
        //         this.count-=1
        //     }
        // },
    }
</script>

<style scoped>
    .container{
        padding: 30px;

    }
    .comment{
      width: 70%;
        border: 5px solid #f1f1f1;
        padding: 5px;

    }
    div{
        margin-bottom: 10px;
    }
</style>