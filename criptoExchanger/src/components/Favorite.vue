<template>
    <div>
        <h2>Варианты в избранном</h2>
        <div @click="getFromFavs(index)" className="list-favs" v-for="(el, index) in favs" :key="index">
            <span>{{ el.from }}</span>
            <span>{{ el.to }}</span>
        </div>
    </div>

</template>

<script>
export default{
    props:{
        favs:{
            type: Array,
            required: true
        },
        getFromFavs : {
            type: Function,
            required: true
        }
    }
}
</script>

<style scoped>
h2{
    color: #fff;
}

.list-favs{
    display: flex;
    justify-content: space-around;
    width: 500px;
    margin: 10px auto;
    transition: all 500ms ease;
}

span{
    padding: 10px 15px;
    background: #8c00ff;
    color: #fff;
}

.list-favs:hover{
    opacity: 0.7;
    transform: scale(1.1);
    cursor: pointer;
}

</style>