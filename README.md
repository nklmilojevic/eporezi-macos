# ePorezi

_Prvobitno objavljeno na [mom blogu](https://nikola.milojevic.me/blog/eporezi-macos-mup/)_

Posle puno pitanja i pojedinačnog objašnjavanja na Slacku Digitalne zajednice, rešio sam da napišem kratko uputstvo kako sam namestio da aplikacija ePorezi radi na macOSu sa sertifikatima MUPa.

_Napomena: Sve ovo koristite na sopstvenu odgovornost. Modul je dobijen od PKS CA i nije prepravljan, već je u izvornom obliku u kome sam ga i dobio. Ovo bi sve trebalo da radi i za sertifikate koje je izdala PKS, ali nisam imao mogućnosti da proverim._

Uslovi da bi vam ovo proradilo:

- Lična karta izdata **posle** 18.8.2014. godine
- macOS
- modifikovana ePorezi aplikacija od strane Gorana Rakića koju možete skinuti [ovde](http://goranrakic.com/tmp/ePorezi_1.1_mac.zip).
- Instalirana Java
- Library za middleware koji MUP koristi koji je uploadovan u ovaj repo.

Instalirajte Javu, iskopirajte middleware u `/usr/local/lib` i prebacite modifikovanu verziju ePorezi za macOS u `Applications` folder. Na Catalini je potrebno da držite ctrl i pritisnete desni klik i open prilikom prvog otvaranja aplikacije zbog novih sigurnosnih pravila na ovoj iteraciji OSa.

To bi trebalo da bude to. Ubacite ličnu karticu i zakačite smart card čitač i trebalo bi sve da radi.

Moguće greške i problemi:

- Ako piše da čitač ili lična karta nisu povezani, proverite da li je čitač prepoznat od strane macOSa. Isto tako, proverite kada Vam je izdata lična karta jer datum mora biti posle 18.8.2014.
- Probajte da odete u `/usr/local/lib` i da otvorite `libnstpkcs11.dylib` sa desnim klikom dok držite ctrl i da pritisnite open.

Zahvaljujem Goranu Rakiću na modifikovanoj verziji kao i na instrukcijama koje možete naći na njegovom gistu na [GitHub-u](https://gist.github.com/grakic/9a850411c3b9294ff0c226e4f914be35).
