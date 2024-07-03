<template>
  <section class="flexBox">
    <form class="formulario">
      <label for="input1">Color de fondo:</label>
      <input v-model="fondo" type="text" id="input1" name="input1" /><br /><br />

      <label for="input2">color de texto</label>
      <input v-model="color" type="text" id="input2" name="input2" /><br /><br />

      <label>
        Mostrar texto
        <input type="checkbox" id="input3" name="input3" v-model="mostrarTexto" /> </label><br /><br />

      <label for="input4">Borde</label>
      <input type="range" id="input4" name="input4" v-model="borde" min="0" max="200" /><br /><br />

      <label for="input5">Contenido actual</label>
      <input v-model="texto" type="text" id="input5" name="input5"  /><br /><br />

      <label>
        Tipografía:
        <select id="input6" name="input6" v-model="tipoLetra">
          <option v-for="fuente in fuentes" :key="fuente" :value="fuente">
            {{ fuente }}
          </option>
        </select>

        <!-- <select id="input6" name="input6" v-model="tipoLetra">
          <option value="arial">Arial</option>
          <option value="cursiva">Cursiva</option>
          <option value="impact">impact</option>
          <option value="garamond">Garamond</option>
        </select>  </label><br /><br /> --> </label><br /><br />

      <label>
        Opacidad
        <input type="checkbox" id="input7" name="input7" v-model="opacity" /> </label><br /><br />

      <label>
        Tamaño de letra
        <input v-model="tamanoLetra" type="radio" id="pequenio" name="tamano" value="pequenio" />
        <label for="pequenio">Pequeño</label>
        <input v-model="tamanoLetra" type="radio" id="mediano" name="tamano" value="mediano" />
        <label for="mediano">Mediano</label>
        <input v-model="tamanoLetra" type="radio" id="grande" name="tamano" value="grande" />
        <label for="grande">Grande</label> </label><br /><br />
    </form>

    <div :class="{ opacidad: opacity === true }" :style="{
      fontFamily: tipoLetra,
      color: color,
      backgroundColor: fondo,
      borderRadius: borde + 'px',
      fontSize:
        tamanoLetra === 'pequenio'
          ? '12px'
          : tamanoLetra === 'mediano'
            ? '16px'
            : '20px',
    }" class="cuadroDinamico">
      <h1 v-if="mostrarTexto">{{ texto }}</h1>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fondo: "",
      texto: "",
      color: "white",
      mostrarTexto: true,
      tipoLetra: "",
      fuentes: ["Arial", "Cursiva", "Impact", "Garamond"], // Arreglo para el v-for
      borde: 0,
      opacity: "",
      tamanoLetra: "",
    };
  },
};
</script>

<style>
.formulario {
  display: flex;
  flex-direction: column;
  padding: 20px;
  width: 25%;
  background-color: gray;
}

.flexBox {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-top: 100px;
  background-color: black;
}

.cuadroDinamico {
  width: 400px;
  height: 400px;
  border: solid white;
  text-align: center;
  overflow: auto; /* Oculta el contenido desbordado */
  word-wrap: break-word; /* Permite que las palabras largas se rompan */
  white-space: pre-wrap; /* Mantiene los espacios en blanco y hace que el texto se ajuste al cuadro */

}

.fondo {
  background-color: blue;
}

.opacidad {
  opacity: 0.3;
}

body {
  background-color: black;
}
</style>
