<!--
Para emitir evento es importante definir el nombre del evento en nomenclatura minusculas y separado por guiones
por ejemplo 'my-even'
-->
<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card card-default">
                    <div class="card-header">Componente Hijo</div>
                    <div class="card-body">
                        <button class="btn btn-primary" @click="$emit('my-event')">Ocultar mensaje</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ChildComponent",
        methods: {
            //
        }
    }
</script>

<style scoped>
    .container{
        margin-top: 10px !important;
    }
</style>