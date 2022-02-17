<template>
  <div id="app">
      <h1>Cuenta Regresiva</h1>
    
      <p>Ingrese un numero: <input type="text" v-model="timerCount" /></p>


    {{ timerCount }}
  </div>
    
</template>

<script>
    export default {
        data() {
            return {
                timerCount: ""
            }
        },
        watch: {
            timerCount: {
                handler(value) {
                    if (value > 1) {
                        setTimeout(() => {
                            this.timerCount--;
                        }, 1000);
                    }
                },
                immediate: true // This ensures the watcher is triggered upon creation
            }
        }
    }
</script>
