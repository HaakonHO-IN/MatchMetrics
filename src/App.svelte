<script>
  import sommer from "./assets/ferie1.jpg";
  import vinter from "./assets/ferie2.jpg";
  import skog from "./assets/ferie3.jpg";
  import langtHår from "./assets/langt.jpg";
  import curlyHår from "./assets/curly.jpg";
  import middelHår from "./assets/middel.jpg";
  let age = 18;
  let height = 205;
  let totalScore = 0;
  let showScore = false;


  function handleViewToggle() {
    showScore = true;
  }


</script>

<main>
  <button class="omOss">Om oss</button>


  <h1 class="overskrift">Matcher du med Håkon?</h1>
  
  {#if showScore}
    <h3>Her er resultatet ditt:</h3>
    <p>{totalScore}</p>
  {:else}
    <p></p>

    <h2>
      Velkommen, her skal du få vite om du er en match med Håkon. Svar på
      spørsmålenen under og få ditt resultat
    </h2>
    <div class="forNavn">
      <span>Fornavn:</span>
      <input type="text" />
    </div>
    <div class="etterNavn">
      <span>Etternavn:</span>
      <input type="text" />
    </div>
    <div class="alder">
      <span>Alder:{age} </span>
      <input type="range" id="ageSlider" min="0" Max="100" bind:value={age} />
    </div>
    <div class="høyde">
      <span>Høyde:</span>
      <input
        type="range"
        id="ageSlider"
        min="100"
        Max="205"
        bind:value={height}
      />
      <span>{height}cm</span>
    </div>
    <div>
      <div>
        <label for="måned">Hvilket kjønn er du?</label>
        <select name="Kjønn">
          <option value="Mann">Mann</option>
          <option value="Dame">Dame</option>
          <option value="Annet">Annet</option>
        </select>
      </div>

      <h3>Nå kommer litt mer generelle spørsmål om deg selv</h3>

      <div>
        <legend><h4>Hva gjør du på fritiden?</h4></legend>
        <input type="checkbox" id="hobby" value="styrke" name="styrke" />
        <label for="styrke">Styrke</label>
      </div>
      <div>
        <input type="checkbox" id="hobby" value="fotball" name="fotball" />
        <label for="fotball">Fotball</label>
      </div>
      <div>
        <input type="checkbox" id="hobby" value="tennis" name="tennis" />
        <label for="tennis">Tennis</label>
      </div>
      <div>
        <input type="checkbox" id="hobby" value="gaming" name="gaming" />
        <label for="gaming">Gaming</label>
      </div>
    </div>

    <div>
      <h4>Hvis noen skulle ha beskrevet deg med et ord, hva hadde det vært?</h4>
      <span>En venn ville ha beskrevet meg som </span>
      <select name="beskrivelse">
        <option value="Morsom">Morsom</option>
        <option value="Hyggelig">Hyggelig</option>
        <option value="Hjelpsom">Hjelpsom</option>
        <option value="inkluderende">inkluderende</option>
      </select>
    </div>
    <div class="ferie">
      <h4>Hvor vil du reise på ferie?</h4>
      <input type="radio" name="ferie" id="ferie1" value="destination" />
      <label for="ferie1">
        <img src={sommer} />
      </label>
      <input type="radio" name="ferie" value="ferie2" id="destination" />
      <label for="ferie2">
        <img src={vinter} />
      </label>
      <input type="radio" name="ferie" value="ferie3" id="destination" />
      <label for="ferie3">
        <img src={skog} />
      </label>
    </div>

    <div>
      <h4>Hårlengde</h4>
      <input type="radio" name="hårlengde" value="d" id="langt" />
      <label for="langt">
        <img src={langtHår} />
      </label>
      <input type="radio" name="hårlengde" value="s" id="curly" />
      <label for="curly">
        <img src={curlyHår} />
      </label>
      <input type="radio" name="hårlengde" value="a" id="middel" />
      <label for="middel">
        <img src={middelHår} />
      </label>
    </div>

    <div>
      <span><h4>Hårfarge</h4></span>
      <nav class="segmented">
        <input type="radio" name="color" value="brunt" id="1" />
        <label for="1">brunt</label>
        <input type="radio" name="color" value="blondt" id="b" />
        <label for="b">blondt</label>
        <input type="radio" name="color" value="svart" id="sv" />
        <label for="sv">svart</label>
        <input type="radio" name="color" value="grått" id="g" />
        <label for="g">grått</label>
        <input type="radio" name="color" value="ginger" id="gi" />
        <label for="gi">ginger</label>
      </nav>
    </div>
  {/if}

  <button on:click={handleViewToggle}><h2>Resultat</h2></button>
</main>

<style>
  main{
    background-color: beige;
  } 
.overskrift{
  background-color:whitesmoke;
}
.forNavn{
  margin-bottom: 10px;
}
.etterNavn{
  margin-top:10px;
  margin-bottom: 10px ;
}
.alder{
  margin-top: 10px;
  margin-bottom: 10px;
}
.høyde{
  margin-top: 10px;
  margin-bottom: 10px;
}

</style>
