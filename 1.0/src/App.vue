
<template>
  <div class="padre">
    <div class="header">
      <h1>TALONARIO</h1>
    </div>
    <div class="info">
      <div class="info1">
        <h2>Informacion</h2>
        <div>
          <p>🎁:{{ premio }}</p>
          <p>💰:{{ valor }}</p>
          <p>🏰:{{ loteria }}</p>
          <p>📅:{{ fecha }}</p>
        </div>
      </div>
      <div class="agendar">




        <!-- Button trigger modal -->
        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
          Crea tu Talonario
        </button>

        <!-- Modal -->
        <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
          <div class="modal-dialog">
            <div class="modal-content">
              <div class="modal-header">
                <h1 class="modal-title fs-5" id="exampleModalLabel">Crea tu Talonario</h1>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
              </div>
              <div class="modal-body">
                <input type="text" placeholder="premio" v-model="premio">
                <input type="text" placeholder="valor boleta" v-model="valor">
                <select name="" id="" v-model="loteria">
                  <option value="La culona">La culona</option>
                  <option value="La santander">La santander</option>
                  <option value="La pulga">La pulga</option>
                </select>
                <select name="" id="" v-model="cantidad">
                  <option value="50">50</option>
                  <option value="75">75</option>
                  <option value="100">100</option>
                </select>
                <input type="date" placeholder="loteria" v-model="fecha">
              </div>
              <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">cerrar</button>
                <button type="button" class="btn btn-primary" @click="guardar()">guardar</button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="chucho">
        <h2>Acciones</h2>
        <button>Estado</button>
        <button>📝Listar tus boletas</button>
        <button>
          <p>📑Personalizar </p>
        </button>
        <button>
          <P> 📩Generar pdf</P>
        </button>
      </div>

    </div>
    <div class="footer">
      <h3>copyraingt 2023-Todos los derechos reservados</h3>
    </div>

  </div>
</template>

<script setup>
import { ref } from 'vue'

const premio = ref('')
const valor = ref('')
const loteria = ref('')
const cantidad = ref('')
const fecha = ref('')



const guardar=()=>{
  

  
  const datos=ref({
  premio:premio.value,
  valor:valor.value,
  loteria:loteria.value,
  cantidad:cantidad.value,
  fecha:fecha.value
}) 
for (let index = 0; index < cantidad; index++) {

  
}
console.log(datos.value)


}


</script>

<style scoped>
.padre {
  display: grid;
  grid-template-rows: 10vh 80vh 10vh;

}

.header {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #ffc018;
  color: white;
}

.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #ffc018;
  color: white;
  padding: 10px;
}

.info {
  display: grid;
  grid-template-columns: 20% 60% 20%;
  gap: 10px;
  padding: 30px;

}

.info1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 10px;
  padding: 5px;
  border: 1px solid black;
  width: 80%;
  height: 80%;
  margin-top: 25%;
  border-radius: 10px;
  background-color: #f8f69f;

}

.chucho {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 10px;
  padding: 5px;
  border: 1px solid black;
  width: 80%;
  height: 80%;
  margin-top: 25%;
  border-radius: 10px;
  padding: 10px;
  background-color: #f8f69f;
}

.chucho button {
  width: 100%;
  height: 10%;

  background-color: #ff9934;

  border-radius: 5px;

}

.agendar {
  display: flex;
  justify-content: center;
  align-items: center;
  
}
.agendar button{
  width: 20%;

  background-color: #ff9934;
  border-radius: 5px;
  color: black;
}
.modal-body{
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 10px;
}</style>
