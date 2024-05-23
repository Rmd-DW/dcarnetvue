<template>
  <div class="carnet">
    <header>
      <p class="p_title">REPÚBLICA DE CHILE</p>
      <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
    </header>

    <div class="carnet_grid">
      <aside>
        <div class="identification">
          <span>CÉDULA DE IDENTIDAD</span>
          <img class="img-band" src="https://banderas.top/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2020/07/Bandera-de-Chile-min.png.webp" alt="Bandera de Chile">
        </div>
        <img class="photo" src="https://www.nmspacemuseum.org/wp-content/uploads/2019/03/Elon_Musk.jpg" alt="Foto de Elon" />
        <p>RUN {{ run }}</p>
      </aside>

      <main>
        <section>
          <div class="grid-2-columns">
            <article>
              <header>APELLIDOS</header>
              <span>{{ apellidos }}</span>
            </article>
            <article>
              <header>NOMBRES</header>
              <span>{{ nombres }}</span>
            </article>
            <article>
              <header>NACIONALIDAD</header>
              <span>{{ nacionalidad }}</span>
            </article>
            <article>
              <header>SEXO</header>
              <span>{{ sexo }}</span>
            </article>
          </div>
          <div class="grid-2-columns">
            <article>
              <header>FECHA DE NACIMIENTO</header>
              <span>{{ fecha_nacimiento }}</span>
            </article>
            <article>
              <header>NÚMERO DOCUMENTO</header>
              <span>{{ numero_documento }}</span>
            </article>
            <article>
              <header>FECHA DE EMISIÓN</header>
              <span>{{ fecha_emisión }}</span>
            </article>
            <article>
              <header>FECHA DE VENCIMIENTO</header>
              <span>{{ fecha_vencimiento }}</span>
            </article>
          </div>
          <article class="firma">
            <header>FIRMA DEL TITULAR</header>
            <span>X Æ A-12</span>
          </article>
        </section>
      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      run: "22.222.222-2",
      apellidos: "Musk",
      nombres: "Elon Reeve",
      nacionalidad: "Sudafricano",
      sexo: "Masculino",
      fecha_nacimiento: "28 JUN 1971",
      numero_documento: "222.222.222",
      fecha_emisión: "01 ENE 2025",
      fecha_vencimiento: "01 ENE 2030",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 60px;
}

header {
  margin: 0.5rem;
  padding: 0.5rem;
  font-weight: 400;
  font-size: 1rem;
  color: rgb(21, 21, 121);
}

span {
  margin: 0.5rem;
  padding: 0.5rem;
  font-weight: bold;
  font-size: 1rem;
  color: rgb(28, 27, 29);
}

.p_title {
  font-size: 1.5rem;
  font-weight: bolder;
}

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: left;
}

section {
  width: 100%;
}

.carnet {
  align-items: center;
  background-color: rgb(150, 199, 245);
  color: rgb(8, 8, 119);
  margin: 12rem;
  padding: 2rem;
  border: 0.1rem solid black;
  border-radius: 2rem;
  text-align: center;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5); /* Agrega una sombra */
}

.carnet_grid {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 5rem;
}

.identification {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.img-band {
  width: 3rem;
}

.photo {
  width: 15rem;
  margin-top: 0.5rem;
}

.grid-2-columns {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
}

article header {
  font-weight: bold;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}
</style>
