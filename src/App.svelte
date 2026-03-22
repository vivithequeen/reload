<script>
  import flagImg from './assets/flag-orpheus-top.svg';
  import titleImg from './assets/title.png';
  import waveImg from './assets/wave.png';
  import doomImg from './assets/doom.gif';
  import stickerImg from './assets/sticker.png';
  import houseImg from './assets/house.png';
  import cuttout1 from './assets/cuttout1.png';
  import cuttout2 from './assets/cuttout2.png';
  import crtImg from './assets/crt.jpg';
  import doom2Img from './assets/doom2butnot2.png';
  import sticker2Img from './assets/sticker2.png';
</script>

<div class="page">
  <div class="border-strip left"></div>
  <div class="border-strip right"></div>
  <a href = "https://hackclub.com"><img class="hack-icon" src={flagImg} alt="Hack Club" /></a>
  <header>
    
    <img class="title-img" src={titleImg} alt="RELOAD" />
    <p class="subtitle">
      CODE XX HOURS ON A RETRO PROJECT, COME SHOW YOUR PROJECT OFF AT A RETRO GAME CONVENTION!
    </p>
  </header>

  <img class="wave-divider" src={waveImg} alt="" aria-hidden="true" />

  <main>
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
          <img src={stickerImg} alt="orpheous" />
        </div>
      </div>

      <p class="or">OR...</p>

      <div class="row">
        <div class="img-col">
          <img class="pixel" src={houseImg} alt="3D software renderer output" />
          <span class="caption">3D renderer made by noob for Sprig!</span>
        </div>
        <div class="text-col">
          <p>MAKE A SOFTWARE RENDERER!!</p>
        </div>

      </div>

      <p class="or">AND...</p>

      <div class="row">
        <div class="text-col">
          <p class="big">FLY OUT TO XXX AND SHOW OFF YOUR GAME AT A RETRO GAMING CONVENTION!</p>
        </div>
      </div>
    </section>

    <section class="content">
      <p class="or">PRIZES</p>
      <div class="row">
        <div class="text-col">
          <p>CAN'T MAKE IT? GRAB SOMETHING FROM THE SHOP!!!</p>
        </div>
      </div>
    </section>

    <section class="gallery">
      <div class="gallery-row">
        <div class="gallery-card prize-card">
          <div class="prize-img-wrap">
            <img src={doom2Img} alt="Doom 2 but not Doom 2" class="prize-img" />
          </div>
          <div class="prize-text">
            <p class="prize-title">DOOM 1993</p>
            <p class="prize-desc">Steam key (or if you can find a physical copy thats sick)</p>
          </div>
        </div>
        <div class="gallery-card prize-card">
          <div class="prize-img-wrap">
            <img src={crtImg} alt="CRT TV" class="prize-img" />
          </div>
          <div class="prize-text">
            <p class="prize-title">YOUR OWN CRT</p>
            <p class="prize-desc">get your own cathode ray tube monitor!!</p>
          </div>
        </div>
        <div class="gallery-card prize-card">
          <div class="prize-img-wrap">
            <img src={sticker2Img} alt="Sticker" class="prize-img contain" />
          </div>
          <div class="prize-text">
            <p class="prize-title">STICKERS!!</p>
            <p class="prize-desc">get some stickers!!</p>
          </div>
        </div>
      </div>
    </section>

    <section class="content">
      <p class="or">FAQ</p>
    </section>

    <section class="gallery">
      <div class="gallery-row">
        <div class="gallery-card faq-card">
          <p class="faq-q">What the freak is trenchbroom?</p>
          <p class="faq-a"><a href="https://trenchbroom.github.io/">Trenchbroom</a> is a opensorce level editing software made for quake and has support for many games and game engines, such as <a href="https://github.com/func-godot">godot</a>(:D).</p>
        </div>
        <div class="gallery-card faq-card">
          <p class="faq-q">WHERE IS IT GOING TO BE?</p>
          <p class="faq-a">Undecided atm, will be contacting conventions taking place over september and october :).</p>
        </div>
        <div class="gallery-card faq-card">
          <p class="faq-q">WHAT CAN I MAKE PROJECTS IN?</p>
          <p class="faq-a">- any game engine.</p>
          <p class="faq-a"> -any langauge with graphics api bindings</p>
        </div>
      </div>
    </section>

    <div class="submit-area">
      <button>submit</button>
    </div>
  </main>

  <footer>
    <img src={cuttout1} alt="" class="footer-cutout" aria-hidden="true" />
    <div class="footer-text">
      <p>made with &lt;3 by violet and moth</p>
    </div>
    <img src={cuttout2} alt="" class="footer-cutout" aria-hidden="true" />
  </footer>
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Micro+5&display=swap');

  :global(*, *::before, *::after) {
    box-sizing: border-box;
  }

  :global(body) {
    margin: 0;
    background: #1a1e32;
    font-family: 'Micro 5', monospace;
    color: #e8dff5;
  }

  /* --- Page grid ---
     Columns: left-border | content | right-border
     Rows:    header | wave | main-content | footer
  */
  .page {
    display: grid;
    grid-template-columns: 48px 1fr 48px;
    grid-template-rows: auto auto 1fr auto;
    min-height: 100vh;
  }

  /* --- Borders: span all 4 rows --- */
  .border-strip {
    grid-row: 1 / 5;
    background-image: url('./assets/border.png');
    background-repeat: repeat-y;
    background-size: 48px auto;
    image-rendering: pixelated;
    position: relative;
    z-index: 2;
  }

  .border-strip.left  { grid-column: 1; }
  .border-strip.right { grid-column: 3; transform: scaleX(-1); }

  /* --- Header: row 1, center column --- */
  header {
    grid-column: 2;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 32px 40px 16px;
    position: relative;
    max-width: 900px;
    width: 100%;
    justify-self: center;
  }

  .hack-icon {
    position: absolute;
    top: 0;
    left: 50px;
    width: 180px;
  }

  .title-img {
    width: 90%;
    max-width: 620px;
    margin-top: 48px;
    image-rendering: pixelated;
  }

  .subtitle {
    font-size: 30px;
    line-height: 2;
    text-align: center;
    margin: 24px 0 32px;
    color: #c8bfda;
    max-width: 560px;
  }

  /* --- Wave: row 2, all columns --- */
  .wave-divider {
    grid-column: 1 / 4;
    grid-row: 2;
    width: 100%;
    display: block;
    image-rendering: pixelated;
    position: relative;
    z-index: 1;
  }

  /* --- Main content: row 3, center column --- */
  main {
    grid-column: 2;
    grid-row: 3;
    display: flex;
    flex-direction: column;
    padding: 0 48px 48px;
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
  }

  .row {
    display: flex;
    align-items: center;
    gap: 40px;
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

  .img-col img.pixel { image-rendering: pixelated; }

  .caption {
    font-size: 30px;
    color: #8a7fa0;
    text-align: center;
    line-height: 1.8;
  }

  .text-col { flex: 1; }

  .text-col p.big {
    font-size: 60px;
  }

  .text-col p {
    font-size: 30px;
    line-height: 2.2;
    text-align: center;
    margin: 0;
    text-transform: uppercase;
    color: #e8dff5;
  }

  .or {
    font-size: 55px;
    text-align: center;
    margin: 0;
    color: #e8dff5;
  }

  /* --- Gallery --- */
  .gallery {
    display: flex;
    flex-direction: column;
    gap: 24px;
    padding: 0 0 48px;
    width: 100%;
  }

  .gallery-row {
    display: flex;
    gap: 24px;
    padding: 0 24px;
  }

  .gallery-card {
    flex: 1;
    background: #12162a;
    border: 2px solid #1e2340;
    display: flex;
    flex-direction: column;
  }

  .prize-img-wrap {
    width: 100%;
    aspect-ratio: 4 / 3;
    background: #0d1020;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .prize-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  .prize-img.contain {
    object-fit: contain;
    padding: 16px;
  }

  .prize-card {
    display: flex;
    flex-direction: column;
  }

  .prize-text {
    padding: 16px;
    border-top: 2px solid #1e2340;
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 6px;
  }

  .prize-title {
    font-size: 28px;
    margin: 0;
    color: #e8dff5;
    text-transform: uppercase;
  }

  .prize-desc {
    font-size: 20px;
    margin: 0;
    color: #8a7fa0;
    line-height: 1.6;
  }

  .faq-card {
    display: flex;
    flex-direction: column;
    gap: 8px;
    padding: 20px;
  }

  .faq-q {
    font-size: 26px;
    margin: 0;
    color: #e8dff5;
    text-transform: uppercase;
  }

  .faq-a {
    font-size: 20px;
    margin: 0;
    color: #8a7fa0;
    line-height: 1.8;
  }

  /* --- Submit --- */
  .submit-area {
    display: flex;
    justify-content: center;
    padding: 48px 40px;
    max-width: 900px;
    width: 100%;
    align-self: center;
  }

  button {
    font-family: 'Micro 5', monospace;
    font-size: 48px;
    color: #e8dff5;
    background: transparent;
    border: 3px solid #c44444;
    padding: 18px 96px;
    cursor: pointer;
    letter-spacing: 0.05em;
    transition: background 0.15s, color 0.15s;
  }

  button:hover {
    background: #c44444;
    color: #e8dff5;
  }

  /* --- Footer: row 4, all columns --- */
  footer {
    grid-column: 1 / 4;
    grid-row: 4;
    background: #0d1020;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 32px 40px;
    position: relative;
    z-index: 1;
  }

  .footer-cutout { width: 160px; }

  .footer-text {
    font-size: 30px;
    line-height: 2.2;
    text-align: center;
    color: #e8dff5;
  }

  .footer-text p { margin: 0; }
</style>
