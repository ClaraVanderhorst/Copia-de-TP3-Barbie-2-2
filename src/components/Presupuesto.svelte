<script>
  // Función para inicializar el componente de Flourish y tomar el script que nos permite hacer el scrolly gratis!
  import { onMount } from 'svelte';

  

  // Array para guardar la data de cada slide. Cambiar cada uno con el epígrafe específico para cada slide.
  const slides = [
    "Texto slide 1. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 2. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 3. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 4. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 5. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 6. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 7. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 8. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 9. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 10. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 11. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 12. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 13. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 14. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 15. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 16. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 17. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 18. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 19. Fusce quis augue et tortor interdum bibendum. Nam dolor elit"
  ]

  function loadFlourishScrolly() {
    const script = document.createElement('script')
    script.src = "https://cdn.flourish.rocks/flourish-scrolly-v3.1.0.min.js"
    script.type = "text/javascript"
    script.onload = () => initFlourishScrolly()
    document.body.appendChild(script)
  }


  onMount(() => {
    loadFlourishScrolly()
  });
  export let goHome;
</script>

<main>

  <div class="text-container">
    <h1>Marcas</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam officia itaque doloribus quae quis dolorem impedit, voluptates nostrum. Repudiandae adipisci magni ipsam quisquam explicabo excepturi quia voluptas, natus magnam vel.</p>
  </div>

<div class="button-container">
  <button on:click={() => goHome("home")}>
    <img src="/images/casacuartos/casamattel.png" alt="Casa" class="casa-image">
</button>
</div>

<section id="header">
  <h1 id="main_title">
    Uno por uno, quiénes son los jugadores con más chances de jugar en el Mundial
  </h1>
</section>

<div class="texto_container">
  <p class="texto_parrafo">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eget mi eu nulla porta fringilla. Curabitur quis tincidunt purus. Duis nec neque et augue dictum blandit a eget neque. Phasellus tempor, metus et finibus pretium, eros est sagittis orci, vitae pellentesque nisl lectus et velit. Praesent fringilla mauris vitae magna sollicitudin, sit amet tincidunt dolor facilisis. Fusce quis augue et tortor interdum bibendum. Nam dolor elit, posuere nec tortor non, molestie congue justo. Praesent nisl arcu, consectetur sed hendrerit eget, interdum ac nisi. Vestibulum tempor mattis purus. Aliquam tempus neque sed velit convallis tempor. Cras sodales nunc lorem. Nulla pharetra malesuada consequat. Nulla elementum odio non mauris mollis suscipit. Praesent consectetur nunc eget ex varius blandit. Sed id facilisis tellus.
  </p>
</div>

<div class="texto_container">
  <h2 class="subtitulo">Los posibles elegidos de Scaloni</h2>
</div>

<!-- Contenedor de la story de flourish (scrolly)-->
<div id="my-wrapper">
  <!-- Reemplazar el ID de jeemplo por el de la story propia -->
  <div class="flourish-embed" data-src="story/2041907" data-url="https://flo.uri.sh/story/2041907/embed" data-height="100vh">
    
    <!-- <script src="https://public.flourish.studio/resources/embed.js"></script> -->
  </div>

  <!-- Iteramos sobre las distintas slides del componente de Flourish -->
  {#each slides as slide, index}
    <p>
      {@html slide}
      <!-- svelte-ignore a11y-missing-content -->
      <a href={"#story/2041907/slide-" + (index + 1)}></a>
    </p>
  {/each}
</div>

<div class="texto_container">
  <p class="texto_parrafo">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eget mi eu nulla porta fringilla. Curabitur quis tincidunt purus. Duis nec neque et augue dictum blandit a eget neque. Phasellus tempor, metus et finibus pretium, eros est sagittis orci, vitae pellentesque nisl lectus et velit. Praesent fringilla mauris vitae magna sollicitudin, sit amet tincidunt dolor facilisis. Fusce quis augue et tortor interdum bibendum. Nam dolor elit, posuere nec tortor non, molestie congue justo. Praesent nisl arcu, consectetur sed hendrerit eget, interdum ac nisi. Vestibulum tempor mattis purus. Aliquam tempus neque sed velit convallis tempor. Cras sodales nunc lorem. Nulla pharetra malesuada consequat. Nulla elementum odio non mauris mollis suscipit. Praesent consectetur nunc eget ex varius blandit. Sed id facilisis tellus.
  </p>
</div>

</main>



<style>

main{background-color: #ffffff;}

.text-container {
    width: 100%;
    text-align: center;
    padding: 20px 0;
   
}
  
.text-container h1 {
    font-family: "Bartex";
    font-size: 7em;
    margin: 0;
    color: #ffffff;
    font-weight: 600;
    text-shadow: 3px 5px 0px #E81D8D;
}
  
.text-container p {
    font-family: "Helvetica";
    font-size: 1em;
    margin: 20px 200px;
    color: #710A43;
}

.button-container {
  background-color: #ffffff;
  width: 100%;
  position: sticky;
  top: 0;
  z-index: 10;
  display: flex; /* Flexbox para centrar contenido */
  justify-content: center; /* Centra horizontalmente */
  align-items: center; /* Centra verticalmente */
  height: 200px; /* Ajusta la altura del contenedor */
}

/* Botón */
button {
  cursor: pointer;
  background-color: transparent; /* Fondo transparente */
  border: none; /* Sin bordes */
  padding: 0; /* Sin padding para ajustar al tamaño de la imagen */
  display: flex; /* Flexbox para centrar la imagen dentro del botón */
  justify-content: center;
  align-items: center;
  width: 100px; /* Ancho del botón */
  height: 100px; /* Alto del botón */
}

/* Imagen de la casa */
.casa-image {
  max-width: 100%;
  max-height: 100%;
  width: auto; /* Mantiene proporciones */
  height: auto; /* Mantiene proporciones */
}

a {
  font-weight: 500;
  color: #646cff;
  text-decoration: inherit;
}
a:hover {
  color: #535bf2;
}


#my-wrapper {
  margin: auto;
  max-width: 1280px;
}

#header {
  max-width: 800px;
  text-align: center;
  margin: 50px auto;
}
#main_title {
  font-size: 3em;
  line-height: 1.1;
}

.subtitulo {
  font-size: 1.5em;
  text-align: center;
}
.texto_container {
  max-width: 700px;
  padding: 0 20px;
  margin: auto;
  margin-bottom: 100px;
  text-align: left;
}
.texto_parrafo {
  margin: 50px auto;
}

</style>