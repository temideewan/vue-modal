<template>
    <div class="backdrop">
        <!-- setting a class depending on whether a condition is true or not -->
        <!-- we use the class binding and the object syntax in that -->
        <div class="modal" :class="{sale: theme === 'sale'}">
            <h1>{{header}}</h1>
            <p class="modal_content">{{text}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props:['header', 'text', 'theme']
}
</script>

<style scoped>
.modal{
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: #fff;
    border-radius: 10px;
}

.backdrop{
    top:0;
    position: fixed;
    background-color: rgba(0,0,0,0.5);
    width:100%;
    height:100%;
}

.modal h1{
    color: green;
    border: none;
    padding: 0;
}

.modal.sale{
    background: crimson;
    color: white;
}

.modal.sale h1{
    color: white;
}


</style>