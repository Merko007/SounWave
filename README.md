<!DOCTYPE html>
<html lang="sk">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SoundWave</title>
  <link rel="icon" href="https://www.citypng.com/public/uploads/preview/asus-black-logo-free-png-7017516947736750j9ndls8lj.png" type="image/x-icon">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: 'Helvetica Neue', Arial, sans-serif;
      background-color: #f5f7fb;
      color: #333;
      line-height: 1.6;
      padding: 0 20px;
    }
    .header {
      background: linear-gradient(to right,  #efc100, #000000);
      color: white;
      padding: 20px 0;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      border-radius: 0 0 20px 20px;
    }
    .header h1 {
      font-size: 48px;
      letter-spacing: 1px;
      margin-bottom: 15px;
      font-weight: bold;
      animation: fadeIn 2s;
    }
    .header p {
      font-size: 18px;
      font-weight: 300;
      color: #f4f4f4;
    }
    .menu-bar {
      background: #856b00;
      padding: 5px 0;
      display: flex;
      justify-content: center;
      position: sticky;
      top: 0;
      width: 40%;
      z-index: 1000;
      border-radius: 40px;
      margin: 0% auto;
      margin-top:20px;
    }
    .menu-bar a {
      color: white;
      font-size: 20px;
      font-weight: bold;
      text-decoration: none;
      padding: 10px 20px;
      margin: 0 15px;
      transition: background-color 0.3s ease;
    }
    .menu-bar a:hover {
      background-color: #ff6600;
      border-radius: 10px;
      transform: scale(1.1);
    }
    .product-container {
      background-color: white;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
      margin-top: 20px;
    }
    .price-box {
      background-color: #000000;
      width: 30%;
      padding: 15px;
      border-radius: 25px;
      text-align: center;
      margin-bottom: 30px;
      box-shadow: 0 7px 15px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }
    .price-box h2 {
      font-size: 36px;
      font-weight: bold;
      color: #ffbc62;
    }
    .price-box .price {
      font-size: 42px;
      color: #ffffff;
      font-weight: bold;
    }
     .strikethrough {
         text-decoration: line-through;
         color:white;
    }
    .buy-button {
      background-color: #ff0000;
      color: white;
      padding: 18px 40px;
      font-size: 20px;
      border-radius: 100px;
      text-decoration: none;
      transition: background-color 0.3s ease, transform 0.3s ease;
      cursor: pointer;
      display: inline-block;
      margin-top: 15px;
    }
    .buy-button:hover {
      background-color: #cc5200;
      transform: scale(1.1);
    }
    .specs {
      margin-top: 60px;
    }
    .specs h2 {
      text-align: center;
      font-size: 32px;
      margin-bottom: 40px;
      font-weight: 500;
    }
    .spec-boxes {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 40px;
      animation: fadeIn 1s ease-out;
    }
    .spec-box {
      background-color: #f0f0f0;
      border-radius: 8%;
      padding: 30px;
      width: 48%;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }
    .spec-box2 {
      background-color: #f0f0f0;
      border-radius: 12px;
      padding: 30px;
      width: 70%;
      margin: 0% auto;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }
    .left {
     text-align: left;
    }
    .spec-box img {
      width: 100%;
      border-radius: 12px;
      margin-bottom: 20px;
      transition: transform 0.3s ease;
    }
    .spec-box:hover {
      transform: translateY(-10px);
    }
    .spec-box img:hover {
      transform: scale(1.05);
    }
    .custom-img {
      width: 300px;
      height: auto;
      display: block;
      margin: 0 auto 20px auto;
      border-radius: 12px;
    }
    .spec-box ul {
      list-style: none;
      padding: 0;
    }
    .spec-box ul li {
      font-size: 16px;
      margin: 10px 0;
      color: #555;
      text-align: center;
    }
    footer {
      background: #222;
      color: white;
      text-align: center;
      padding: 40px 20px;
      margin-top: 80px;
      border-radius: 12px;
    }
    footer h3 {
      font-size: 28px;
      margin-bottom: 15px;
    }
    footer p {
      font-size: 14px;
      color: #aaa;
    }
    .contact-info {
      margin-top: 30px;
    }
    .contact-info a {
      color: #00aaff;
      text-decoration: none;
      font-weight: bold;
    }
    .service-table-full {
  width: 100%;
  border-collapse: collapse;
  font-family: sans-serif;
  background-color: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.service-table-full th, .service-table-full td {
  border: 1px solid #ddd;
  padding: 12px;
  text-align: left;
}

.service-table-full thead {
  background-color: #111;
  color: white;
}

.service-table-full tbody tr:nth-child(even) {
  background-color: #f2f2f2; /* sivý pás */
}

.service-table-full tbody tr:hover {
  background-color: #d6e4f0; /* jemne modrastý podklad pri prechode kurzorom */
  transition: background-color 0.3s ease;
  cursor: pointer;
}
    /* Responzívne dizajnové zmeny */
    @media (max-width: 768px) {
      .menu-bar {
        width: 100%;
        margin-top: 0;
      }
      .price-box {
        width: 80%;
      }
      .spec-boxes {
        flex-direction: column;
        align-items: center;
      }
      .spec-box {
        width: 80%;
        margin-bottom: 20px;
      }
      .buy-button {
        width: 100%;
      }
      footer {
        padding: 20px;
      }
    }
    @keyframes fadeIn {
      0% {
        opacity: 0;
        transform: translateY(50px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

  </style>
</head>
<body>
    <div class="header" id="info">
      <h1>SoundWave</h1>
      <p>Ozvučenie, ktoré cítiš</p>
    </div>
    <nav class="menu-bar">
      <a href="#info">Domov</a>
      <a href="#features">Naše služby</a>
      <a href="#specs">O nás</a>
      <a href="#gallery">Galéria</a>
      <a href="#buy">Kontaktuj nás</a>
    </nav>
    <div class="specs" id="features">
      <h2>Naše služby</h2>
      <div class="spec-boxes">
        <div class="spec-box">
          <img src="https://www.azcd.cz/data/storage/thumbs/1000x1000-scale/images/blog/jsou-streamovane-koncerty-budoucnosti-zive-hudby.jpg" alt="Ozvučenie podujatí">
          <ul>
            <li>Ozvučenie koncertov a kultúrnych podujatí</li>
            <li>Technická podpora počas celého eventu</li>
            <li>Rýchla montáž a demontáž</li>
            <li>Prispôsobenie techniky podľa priestoru</li>
            <li>Poradenstvo a profesionálny prístup</li>
          </ul>
        </div>
        <div class="spec-box">
          <img src="https://dlcdnwebimgs.asus.com/files/media/173445c8-2fb7-4d7e-a00d-c0d197a11326/v1/assets/image/proart/article_cover.jpg" alt="Technické vybavenie">
          <ul>
            <li>Kvalitné bezdrôtové a dynamické mikrofóny</li>
            <li>Mixážne pulty Soundcraft Ui16, Notepad 124FX</li>
            <li>Reproduktory Monkey Trash 215</li>
            <li>Profesionálne stojany a káble</li>
            <li>Pripravujeme: osvetlenie a videozáznam</li>
          </ul>
        </div>
        <div class="spec-box">
          <img src="https://img.ephoto.sk/images/content/articles/e1673e478b523b1a7b97a4e9d13eacaac7f8395f.jpg" alt="Kompletné služby">
          <ul>
            <li>Fotodokumentácia koncertov a akcií</li>
            <li>Kompletné ozvučenie folklórnych vystúpení</li>
            <li>Možnosť prenájmu techniky</li>
            <li>Individuálne cenové ponuky</li>
            <li>Diskrétna spolupráca s ochrankou Ghost Legion</li>
          </ul>
        </div>
        <div class="spec-box">
          <img src="https://www.investicievovrecku.sk/wp-content/uploads/2024/12/umela-inteligencia-je-buducnost.png" alt="Budúcnosť SoundWave">
          <ul>
            <li>Rozšírenie o bezpečnostnú službu</li>
            <li>Rozvoj firemného webu a rezervačného systému</li>
            <li>Zvýšenie počtu zariadení</li>
            <li>Zavedenie výhodných balíčkov pre školy a organizácie</li>
            <li>Rast s dôrazom na kvalitu a spokojnosť klienta</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="specs"; id="specs">
      <h2>O našej firme</h2>
      <div class="spec-boxes">
        <div class="spec-box2 left">
          <h2>Začiatky </h2>
          <ul>
            <li>Firma SoundWave vznikla s cieľom poskytovať kvalitné a profesionálne ozvučovacie služby na koncertoch, festivaloch a rôznych kultúrnych podujatiach.
               Jej zakladateľ, Miroslav Dimoš, sa už od detstva venoval hudbe a tancu, pričom jeho vášeň pre techniku a zvukovú techniku ho priviedla k tomu, aby vytvoril firmu, ktorá by ponúkala služby na najvyššej úrovni.</li>
                 <li>Po rokoch skúseností s ozvučovaním a prácou v oblasti techniky sa rozhodol Miroslav rozšíriť svoje aktivity a založiť SoundWave, aby poskytoval komplexné služby v oblasti zvukovej techniky a ozvučenia pre rôzne eventy. Firma sa rýchlo etablovala ako spoľahlivý partner pre organizátorov koncertov a podujatí, pričom sa vyznačuje profesionalitou, flexibilitou a kvalitným prístupom k zákazníkom.</li>
          </ul>
        </div>
        <div class="spec-box2 right">
          <h2>Cieľ a vízia</h2>
          <ul>
            <li>Našim cieľom je poskytovať najvyššiu kvalitu zvuku na koncertoch a podujatiach, s dôrazom na inovácie, moderné technológie a flexibilitu, aby sme sa prispôsobili potrebám klientov. Rýchlo reagujeme na požiadavky a prispôsobujeme techniku podľa veľkosti a typu akcie, čím pokrývame aj náročné podujatia s profesionálnou technickou podporou. Neustále sa zlepšujeme implementovaním nových technológií, pričom našou víziou je ponúknuť komplexné audiovizuálne riešenia, vrátane osvetlenia, videozáznamov a streamingu. Podporujeme miestne a kultúrne podujatia v Banskej Bystrici, čím prispievame k oživovaniu regionálnej kultúry a tradícií. Naším cieľom je zaručiť spokojnosť klientov, vytvárať dlhodobé vzťahy a poskytovať kvalitné služby, ktoré prispievajú k ich úspechu.</li>
          </ul>
        </div>
        <div class="spec-box2 left">
          <h2>Naše doterajšie úspechy</h2>
          <ul>
            <li>Od nášho vzniku sme sa podieľali na ozvučení desiatok významných podujatí po celom Slovensku, vrátane mestských festivalov a folklórnych vystúpení. Rozšírili sme naše služby o fotodokumentáciu, živé streamovanie a osvetlenie podujatí, čím sme poskytli komplexné riešenia našim klientom. Naša flexibilita a kvalitné služby nám priniesli dôveru renomovaných klientov, s ktorými sme si vytvorili dlhodobé partnerstvá. Expanziou na trhy v Českej republike sme si upevnili pozíciu v strednej Európe. Investície do najmodernejších technológií nám umožnili ponúknuť profesionálne ozvučenie s najnovšími mixážnymi pultmi a bezdrôtovými mikrofónmi.</li>
          </ul>
        </div>
        <div class="spec-box2 right">
          <h2>Budúcnosť a rast</h2>
          <ul>
            <li>Naša firma SoundWave sa neustále vyvíja a smeruje k zlepšovaniu kvality poskytovaných služieb. V budúcnosti plánujeme expandovať do širších trhov a posilniť našu pozíciu lídra v oblasti ozvučovania a audiovizuálnych riešení. Naša vízia zahŕňa zavedenie nových technológií, ako sú osvetlenie, videozáznamy a live streaming, čím chceme klientom ponúknuť komplexné a špičkové riešenia na mieru. Okrem toho plánujeme rozšíriť našu ponuku prenájmu techniky a začať poskytovať špeciálne balíčky pre organizácie, školy a väčšie podujatia. Naším cieľom je neustále zlepšovať našu službu, zvyšovať spokojnosť zákazníkov a neustále rásť s dôrazom na kvalitu a inovácie.</li>
          </ul>
        </div>
      </div>
    </div>
    <div style="margin-top:50px; display: flex; justify-content: space-between; flex-wrap: wrap; gap: 40px; align-items: flex-start;">
  
    <!-- Kupón -->
  <div class="price-box" style="flex: 1 1 300px; max-width: 400px;">
    <h2>Predbežná rezervácia -5 % zľava</h2>
    <p class="price">od 150 €</p>
    <p class="strikethrough">od 158 €</p>
    <p>Cena závisí od rozsahu podujatia</p>
    <a href="mailto:info.soundwave.sk@gmail.com" class="buy-button">Zarezervuj teraz</a>
  </div>

  <!-- Tabuľka -->
  <div style="flex: 2 1 500px; overflow-x: auto;">
    <table class="service-table-full">
      <thead>
        <tr>
          <th>Názov služby</th>
          <th>Popis</th>
          <th>Cena</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Ozvučenie koncertu</td>
          <td>Profesionálny zvukový systém</td>
          <td>od 150 €</td>
        </tr>
        <tr>
          <td>Technická podpora</td>
          <td>Prítomnosť technika na akcii</td>
          <td>od 50 €</td>
        </tr>
        <tr>
          <td>Videostream</td>
          <td>Živé vysielanie z podujatia</td>
          <td>dohodou</td>
        </tr>
        <tr>
          <td>Osvetlenie pódia</td>
          <td>Farebné LED osvetlenie</td>
          <td>od 80 €</td>
        </tr>
        <tr>
          <td>DJ set + technika</td>
          <td>DJ + kompletná technika</td>
          <td>od 120 €</td>
        </tr>
        <tr>
          <td>Kompletný balík</td>
          <td>Všetky služby naraz</td>
          <td>dohodou</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
    <footer>
      <h3>Kontaktuj SoundWave</h3>
      <div class="contact-info"; id="buy">
        <p>Email: <a href="mailto:info.soundwave.sk@gmail.com">info.soundwave.sk@gmail.com</a></p>
        <p>Telefón: +421 915 528 707</p>
        <p>Adresa: Tulská 53, Banská Bystrica 974 04</p>
      </div>
      <p>© 2025 SoundWave. Všetky práva vyhradené.</p>
    </footer>
  
</body>
</html>
