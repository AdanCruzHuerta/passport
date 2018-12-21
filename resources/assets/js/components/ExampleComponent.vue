<!--
Para recibir eventos se debe hacer referencia al nombre del evento en el componente en el que se genero el evento
<child-component @my-event="getMessage"></child-component>
-->
<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card card-default">
                    <div class="card-header">Componente padre</div>
                    <div class="card-body">
                        <label class="text-success text-center" v-show="mostrarMensaje == true">Este es mi mensaje en el componente padre</label>
                        <child-component @my-event="getMessage"></child-component>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        data() {
            return {
                mostrarMensaje: true
            }
        },
        methods: {
            getMessage() {
                this.mostrarMensaje = !this.mostrarMensaje;
            }
        }
    }
</script>

<style scoped>
    .container{
        margin-top: 25px !important;
    }
</style>
