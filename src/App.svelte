<script>
  import flagImg from './assets/flag-orpheus-top.svg';
  import borderImg from './assets/border.png';
  import titleImg from './assets/title.png';
  import waveImg from './assets/wave.png';
  import doomImg from './assets/doom.png';
  import stickerImg from './assets/sticker.png';
  import houseImg from './assets/house.png';
  import cuttout1 from './assets/cuttout1.png';
  import cuttout2 from './assets/cuttout2.png';
</script>

<div class="page">
  <div class="side-wave left">
    <img src={borderImg} alt="" aria-hidden="true" />
  </div>

  <main>
    <header>
      <img class="hack-icon" src={flagImg} alt="Hack Club" />
      <img class="title-img" src={titleImg} alt="RELOAD" />
      <p class="subtitle">
        CODE XX HOURS ON A RETRO PROJECT, COME SHOW YOUR PROJECT OFF AT A RETRO GAME CONVENTION!
      </p>
    </header>

    <img class="wave-divider" src={waveImg} alt="" aria-hidden="true" />

    <section class="content">
      <div class="row">
        <div class="img-col">
          <img class="pixel" src={doomImg} alt="Doom (1993) screenshot" />
          <span class="caption">doom (1993) by id Software</span>
        </div>
        <div class="text-col">
          <p>MAKE RETRO THEMED PROJECTS IN GODOT(OR OTHER GAME ENGINES/FRAMEWORKS)</p>
        </div>
      </div>

      <div class="row">
        <div class="text-col">
          <p>MAKE YOUR LEVELS IN TRENCHBROOM AND GET A STICKER!!!</p>
        </div>
        <div class="img-col">
          <img src={stickerImg} alt="Dino sticker" />
        </div>
      </div>

      <p class="or">OR...</p>

      <div class="row">
        <div class="text-col">
          <p>MAKE A SOFTWARE RENDERER!!</p>
        </div>
        <div class="img-col">
          <img class="pixel" src={houseImg} alt="3D software renderer output" />
          <span class="caption">3D renderer made by sneb for Sprig by hackl!</span>
        </div>
      </div>
    </section>

    <div class="submit-area">
      <button>submit</button>
    </div>

    <footer>
      <img src={cuttout1} alt="" class="footer-cutout" aria-hidden="true" />
      <div class="footer-text">
        <p>made with &lt;3 by violet</p>
        <p>sticker art by moth</p>
      </div>
      <img src={cuttout2} alt="" class="footer-cutout" aria-hidden="true" />
    </footer>
  </main>

  <div class="side-wave right">
    <img src={borderImg} alt="" aria-hidden="true" />
  </div>
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');

  :global(*, *::before, *::after) {
    box-sizing: border-box;
  }

  :global(body) {
    margin: 0;
    background: #0f0d18;
    font-family: 'Press Start 2P', monospace;
    color: #e8dff5;
  }

  .page {
    display: flex;
    justify-content: center;
    align-items: stretch;
    min-height: 100vh;
  }

  /* --- Side borders --- */
  .side-wave {
    position: fixed;
    top: 0;
    bottom: 0;
    width: 48px;
    overflow: hidden;
    z-index: 10;
  }

  .side-wave.left { left: 0; }
  .side-wave.right { right: 0; }

  .side-wave img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
    display: block;
    image-rendering: pixelated;
  }

  /* --- Main column --- */
  main {
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 0 48px 48px;
    box-sizing: border-box;
  }

  /* --- Header --- */
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 32px 40px 16px;
    position: relative;
    max-width: 900px;
    width: 100%;
    align-self: center;
    box-sizing: border-box;
  }

  .hack-icon {
    position: absolute;
    top: 0;
    left: 24px;
    width: 140px;
  }

  .title-img {
    width: 90%;
    max-width: 620px;
    margin-top: 48px;
    image-rendering: pixelated;
  }

  .subtitle {
    font-size: 10px;
    line-height: 2;
    text-align: center;
    margin: 24px 0 32px;
    color: #c8bfda;
    max-width: 560px;
  }

  /* --- Wave divider --- */
  .wave-divider {
    width: 100%;
    display: block;
    margin: 0;
    image-rendering: pixelated;
  }

  /* --- Content rows --- */
  .content {
    display: flex;
    flex-direction: column;
    gap: 48px;
    padding: 48px 40px;
    max-width: 900px;
    width: 100%;
    align-self: center;
    box-sizing: border-box;
  }

  .row {
    display: flex;
    align-items: center;
    gap: 40px;
  }

  .row.reverse {
    flex-direction: row-reverse;
  }

  .img-col {
    flex: 0 0 45%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }

  .img-col img {
    width: 100%;
    display: block;
  }

  .img-col img.pixel {
    image-rendering: pixelated;
  }

  .caption {
    font-size: 7px;
    color: #8a7fa0;
    text-align: center;
    line-height: 1.8;
  }

  .text-col {
    flex: 1;
  }

  .text-col p {
    font-size: 12px;
    line-height: 2.2;
    text-align: center;
    margin: 0;
    text-transform: uppercase;
    color: #e8dff5;
  }

  .or {
    font-size: 28px;
    text-align: center;
    margin: 0;
    color: #e8dff5;
  }

  /* --- Submit --- */
  .submit-area {
    display: flex;
    justify-content: center;
    padding: 48px 40px 24px;
    max-width: 900px;
    width: 100%;
    align-self: center;
    box-sizing: border-box;
  }

  button {
    font-family: 'Press Start 2P', monospace;
    font-size: 16px;
    color: #e8dff5;
    background: transparent;
    border: 2px solid #e8dff5;
    padding: 18px 72px;
    cursor: pointer;
    letter-spacing: 0.05em;
    transition: background 0.15s, color 0.15s;
  }

  button:hover {
    background: #e8dff5;
    color: #0f0d18;
  }

  /* --- Footer --- */
  footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 24px 40px 0;
    margin-top: auto;
  }

  .footer-cutout {
    width: 100px;
    opacity: 0.85;
  }

  .footer-text {
    font-size: 9px;
    line-height: 2;
    text-align: center;
    color: #8a7fa0;
  }

  .footer-text p {
    margin: 0;
  }
</style>
