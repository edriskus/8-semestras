# Informacines Saugos Pagrindai

## Įvadas – pagrindinės sąvokos ir problematika

- **Informacijos sauga** - mokslas apie informacijos konfidencialumą, vientisumą ir prieinamumą.
- **CIA** Triada (Confidentiality, Integrity, Availability):
  - Konfidencialumas (**Confidentiality**) - informaciją gali gauti tik tas, kam ji yra siunčiama.
  - Vientisumas (**Integrity**) - niekas negali pakeisti dalies arba visos žinutės turinio.
  - Prieinamumas (**Availability**) - visada prieinama tam, kas ją turi gauti
- Autentiškumas (Authentication) - gavėjas turi būti tikras  nuo ko gavo žinutę. Niekas kitas negali apsimesti siuntėju.
- Negalėjimas atsisakyti (Nonrepudiation) - siuntėjas ir gavėjas vėliau negali paneigti kad jie siuntė ir gavo būtent šią žinutę.
- Prieinamumo kontrolė (Access control) - informacijos šaltinis yra pilnai kontroliuojamas kam tai priklauso.

---

- **Vertybė** - tai išteklius, kuris, veikiant priešiškiems išoriniams veiksniams, prarastas.
  - **Informacinis turtas**: duomenų bazės ir duomenų rinkmenos, dokumentai, vadovai, naudojimo ir palaikymo procedūros, planai, archyviniai duomenys.
  - **Popieriniai dokumentai**: sutartys, rekomendacijos, bendrovės dokumentai, kiti dokumentai.
  - **Programinė įranga**: taikomoji programinė įranga, sistemos programinė įranga, plėtros ir paslaugų priemonės.
  - **Fizinė įranga**: kompiuterinė įranga (sisteminiai blokai, monitoriai), ryšių įranga (maršrutizatoriai, komutatoriai, fakso aparatai), duomenų laikmenos (juostos, diskai), kita įranga (maitinimo šaltiniai, oro kondicionieriai), bal-dai, patalpos.
  - **Žmonės**: darbuotojai, klientai, abonentai.
  - **Įvaizdis**.
  - **Paslaugos**: skaičiavimo ir ryšio paslaugos, komunalinės paslaugos.
- **Grėsmė** - tai scenarijus arba **veiksmų seka**, kuri pasinaudoja informacinės sistemos pažeidžiamumu ir gali sukelti žalą vienai ar kelioms sistemos vertybėms.
- **Pažeidžiamumas** - tai vieno ar kelių sistemos elementų **silpnybė**, kuria pasinaudojus gali būti pažeistas normalus sistemos funkcionalumas.
- **Rizika** – tai tam tikra tvarka **apskaičiuota skaitinė vertė**, nusakanti, kokių pasekmių turės grėsmės realizacija.

---

- Informacinės saugos **principai**:
  - **Mažiausių privilegijų** – bet kuris su sistema susijęs objektas (vartotojas, administratorius, programa, sistema) privalo turėti ne platesnes privilegijas nei tos, kurių reikia atlikti visiems objektui priskirtiems uždaviniams. 
  - **„Gilios“ apsaugos** – negalima pasikliauti priklausomybe nuo vienintelio saugumo mechanizmo, kad ir koks nepažeidžiamas jis atrodytų. Būtinas saugumo sistemų dubliavimas. 
  - **Saugumo požiūrių**
    1. Leista tik tai, kas yra oficialiai leista
    2. Leista viskas, kas nėra oficialiai uždrausta)
  - **Paprastumo** – išvengiama konfigūravimo klaidų, rekomendacijų vykdymo vengimo, neaiškumų. 
  - **Saugumo per neaiškumą** – esmė yra neįprasta konfigūracija, arba ta, kurią sunku suprasti. Tai gali būti nestandartinių prieigų parinkimas teikiamiems servisams, netradicinė duomenų ar konfigūracinių failų lokalizacija.

### Atakų prieš informacijos saugą rūšys

![Atakų prieš informacijos saugą rūšys](ataku_rusys.png)

- **Pasyvios** atakos - nekeičia informacijos srauto
  - Informacijos **nutekėjimas**
  - Informacijos **srauto analizė** (traffic analysis)
- **Aktyvios** atakos - keičiama informacija sraute
  - **Apsimetimas** (masquerade)
  - Informacijos **užlaikymas** (replay)
  - Informacijos turinio **pakeitimas** (modification)
  - Paslaugų **blokavimas** (denial of service)

---

- Informacinės saugos problemų sprendimas:
  - **Techniniai** sprendimai
    - Šifravimas
    - Tinklų konfigūracija
    - Antivirusai, IDS
  - **Organizaciniai** sprendimai
    - Saugumo politika
    - Standatai, auditas
  - **Rizikos valdymas**
    - Fizinė apsauga ir personalo kontrolė
    - Spynos, priešgaisrinė signalizacija, video stebėjimas

## Prieigos kontrolė

- **Prieigos kontrolė** – tai politika, programinis arba aparatinis komponentas, naudojamas priėjimo teisei išduoti arba suteikti prie tam tikro ištekliaus.
- Apima procesus AAA:
  - **Authentication** (I&A – Identification and Authentication) - vienareikšmiškai apibrėžti vartotoją ir patikrinti, ar iš tikrųjų žmogus (procesas/įrenginys), norintis identifikuotis sistemoje, yra tas, kuo save vadina. 
    - pagal **informaciją** – autentifikacijai pateikiama informacija, kurią teoriškai žino tik teisėtas vartotojas (pvz., slaptažodis, PIN ir t. t.).
    - pagal **tapatybės kodą** – autentifikacijai pateikiamas tapatybę įrodantis kodas, kuris priklauso tik vartotojui, jis pateikiamas tam tikroje laikmenoje arba formate, kurio neįmanoma arba sunku padirbti (tapatybės kortelė, RFID, sertifikatas ir t. t.).
    - pagal **vartotoją** – autentifikacijai pateikiama vartotojo dalis (pvz., skenuojamas piršto antspaudas, akių rainelė ir t. t.).
    - pagal **vietą** – tikrinama, ar bandoma jungtis iš leistinos vietos (pvz., iš vidinio tinklo).
  - **Authorization** - nustato, kokių teisių turi prie informacinės sistemos prisijungęs vartotojas arba esybė
  - **Audit** - įvykių, klaidų, prisijungimų, objektų naudojimo, autentifikacijos bandymų ir kitos susijusios informacijos stebėjimo bei fiksavimo procesas.
- **Prieigos kontrolės modeliai** aprašo teisių valdymo mechanizmą.
  - MAC (mandatory access control)
    - Prieigos valdymo modelis, nusakomas sistemos, bet ne objekto savininko, t.y. prieigos teisės negali būti pakeistos vartotojo arba savininko.
    - MAC modeliu pagristose sistemose visi objektai ir subjektai turi turėti priskirtas saugumo etiketes (label).
    - Subjektas, turintis tam tikrą pasitikėjimo lygį, gali prieiti prie pagal lygį lygių ar žemesnių saugumo kategorijos objektų.
  - DAC (discretionary access control)
    - tai prieigos valdymo modelis, kuriame prieigos teises apibrėžia objekto savininkas, t. y. nusprendžia, kas ir kokiu lygiu gali prieiti prie objekto.
    - Kiekvienas objektas turi savininką.
    - Pirminis objekto savininkas – objekto kūrėjas.
    - Savininkas gali deleguoti savininko teises kitam subjektui.
    - Prieigos teises prie objekto nusako savininkas.
  - RBAC (role-based access control)
    - nauja alternatyva MAC ir DAC modeliams. Modelis pagrįstas vartotojų vaidmenų sukūrimu, kurie tiesiogiai išreiškia jų pareigas

---

- Technologiniai autentifikacijos sprendimai
  - Vartotojo vardas ir slaptažodis
  - Kerberos - "bilietais" grįstas bendravimos protokolas
  - CHAP (Challenge-Handshake Authentication Protocol)
  - Sertifikatai - electronic document used to prove the ownership of a public key.
  - SmartCard - Smart cards can be used as a security token
  - Biometrinė autentifikacija
  - Kelių faktorių autentifikacija

## Kenksmingas programinis kodas ir apsaugos metodai

- ...

## Įsiskverbimų detektavimo sistemos ir medaus puodynės

- ...

## Atakų prieš informacines sistemas pavyzdžiai

- ...

## Kompiuterinių tinklų sauga

- ...

## Organizacinis saugumas: saugumo politika, rizikos valdymas, standartai, auditas, saugumo komanda, incidentų valdymas

- ...

## Fizinė sauga, atsarginės kopijos, sistemų atstatymas

- ...

## Operacinių sistemų ir dalykinių programų sauga

- ...

## Teisiniai ir etiniai informacijos saugos aspektai

- ...

## Šiuolaikinės technologijos bei susijusios grėsmės

- ...

## Įvadas į kriptografiją

- ...