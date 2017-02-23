[[TOC]]

# Usecase model

1. Kasutusjuhtude kirjeldus:

    1. User_registration

1. Kasutajad-huvid: Kõik kasutajad. Tahavad ennast süsteemis registreerida. 

2. Primaarne kasutaja (kui on):

3. Üleüldine kirjeldus: Läbi facebooki, google’i, linkedin API’i VÕI registeerib manuaalselt. Selleks on alustuseks vaja emaili. Sisestatakse landing page’l.

4. Infovaade (kus toimub protsess): 

    1. sign up view (punkt 13.2) 

    2. sealt edasi spetsiaalsed vaated täiendava info küsimiseks.

5. Käivitav sündmus: subjekt soovib registreerida

6. Eeltingimused: kasutajal on olemas isiklik email VÕI sotsiaalmeedia konto

7. Järeltingimused: kasutaja on registeeritud, avatakse library vaade.

8. Erinõudmised: 

9. UX-UI tips:

10. UML,mockupid

11. Näited: 

    3. slack.com

    4. [https://blog.hubspot.com/marketing/landing-page-examples-list#sm.00018tqvatadsfkeynp27kz3a2wol](https://blog.hubspot.com/marketing/landing-page-examples-list#sm.00018tqvatadsfkeynp27kz3a2wol)

12. Kasutusjuhu esinemissagedus*:* igapäevaselt

13. Stsenaarium:

    5. Subjekt soovib ennast registeerida landing page’il, vajutades "sign up" nupule.

    6. Süsteem pakub valikut, kas registeerida API’de kaudu või emaili kaudu. (sign up view)

    7. Kasutaja valib emaili teel regamise, sisestades emaili.

    8. Systeem kontrollib, et email poleks eelnevalt võetud. (võimalik, et vaja lisada funktsioon, mis kontrollib, et kasutaja poleks robot).

        1. Kui email on olemas, siis systeem annab teate, et kasutaja on antud emailiga on juba olemas.

    9. Kasutajale saadetakse süsteemi poolt geneeritud 6-kohaline kood emailile.

    10. Süsteem palub sisestada kasutajale saadetud 6-kohaline kood.

    11. Süsteem kontrollib koodi korrektsust.

        2. Kui sisestatud kood on vale, kuvatakse süsteemi poolt teade, et sisestatud kood on vale ja kasutajat ei registeerita.

    12. Järgmisel vormil palutakse sisestada eesnimi, perekonnanimi ja password. Check box võiks olla selleks (by default täidetud), et kasutaja soovib saada infot ridline’i tegemiste kohta.

        3. Password peab olema min 6 kohaline.

        4. Passwordi keerukust kontrollitakse. Selleks annab süsteem tagasisidet 4-kohalisel skaalal.

![image alt text](image_0.png)

    13. Järgmisel vormil süsteem küsib kasutajalt tema peamise rolli kohta (Main role (sound engineer, organizer, artist, venue owner, other). Kasutaja saab antud skippida vajadusel.

    14. Järgmisel formil küsitakse kasutaja eesnime ja perenime (vaja, et kasutajat teistele kasutajatele arusaadavalt display’ida).  Kasutaja saab antud skippida vajadusel.

    15. Süsteem registeerib kasutaja. Süsteem logib kasutaja sisse library vaatesse. Süsteem kuvab teate edukast registreerimisest (modal). 

14. Laiendused (API kaudu registeerimine):

    16. Kasutaja valib API kaudu registeerimise.

    17. Süsteem liidestab kasutaja valitud API’ga (OP.1.4)

    18. Kasutaja sisestab API’le oma kasutajanime, parooli

    19. Süsteem ootab positiivset vastet API kaudu regisreerimisel.

        5. Kui volitus on positiivne JA antud kasutaja pole eelnevalt kasutanud registeerimisel teist API’t, siis jätkatakse punktis 13.9.

        6. Kui volitus on negatiivne, kuvatakse teade, et ei suudetud kasutajat tuvastada ja registeerimine ebaõnnestus.

        7. Kui antud kasutaja on registeeritud teise kasutaja API’ga, siis kuvatakse teade, et kasutaja on juba registeeritud. 

            1. Kasutaja logitakse tema olemasolevasse kontosse library vaatesse.

15. Märkused:

    20.  kastutaja saab alati protsessi pooleli jätta. Selleks igas vaates cancel võimalus.

    21. Kasutaja jääb sisse logituks pärast rakendust väljumist (nt. brauseri akna sulgemisel). Teatud aja pärast rakendatakse automaatne väljalogimine (kasutusjuht "automatic logout")

16. Lahtised probleemid/testimiskohad:

    22. Kuidas kõige vähem kasutajat sisestusandmetega koormata?

    23. Kuidas teha registreerimisprotsessi kiiremaks?

    24. Kas on olemas vigade haldus (nt timeout API’dest jne)?

    25. Passwordi keerukuse kontroll

    26. Kuidas küsida kasutajalt tema peamise rolli kohta?

    27. Kuidas vältida topeltkontosid, kui kasutaja registeerib mitmekordselt erinevate apidega (millele lisaks võib tal olla email:pass meetod)?

    28. Kas captcha lisamine oleks vajalik?

    29. Kuidas vältida, et inimene registeerib erinevate apidega mitu korda?

### User_login

1. Kasutajad, huvid: Kõik kasutajad. Tahavad ennast süsteemis tuvastada.

2. Primaarne kasutaja (kui on): 

3. Üleüldine kirjeldus: Subjekt identifitseerib ennast. Selleks sisestab ta emaili, parooli VÕI kasutades väliseid apisid - fb, google, linkedin. Süsteem autendib subjekti, st. kontrollib subjekti väidetavat identiteeti. Kui subjekt on identifitseeritud, siis lubatakse subjekt süsteemi siseneda, vastasel juhul mitte.

4. Infovaade (kus toimub protsess): login page (punkt 12.2)

5. Käivitav sündmus: 

6. Eeltingimus: Kasutaja on registeeritud.

7. Järeltingimused: Kasutaja on ennast süsteemile tuvastanud ja sisselogitud.

8. Erinõudmised:

9. UX-UI tips:

    1. http://www.uxforthemasses.com/login-page/

10. UML,mockupid:

    2. Põhimõtteline pilt "logimisaknast".

    3. ![image alt text](image_1.png)

11. Näited: 

    4. [https://designmodo.com/login-form-examples/](https://designmodo.com/login-form-examples/)

12. Stsenaarium:

    5. Kasutaja soovib landing page’l süsteemi siseneda, sisestades emaili ja salasõna VÕI kasutades väliseid API’sid (eraldi nupud sellejaoks landing page’l).

    6. Kasutaja sisestab emaili ja salasõna.

    7. Süsteem kontrollib, kas parool/emaili kombinatsioon süsteemis eksisteerib.

    8. Kui eksisteerib, logitakse kasutaja sisse. Süsteemi viib kasutaja library vaatesse.

        1. Kui kasutajanime/parooli kombinatsiooni ei eksisteeri, saab kasutaja korrata.

13. Laiendused (logimine API kaudu):

    9. Kasutaja valib logimiseks API mooduse (valides ühe sotsiaalmeedia kanalitest)

    10. Süsteem liidestab kasutaja valitud API liidesega

    11. Kasutaja sisestab emaili ja salasõna API liidesesse.

    12. Süsteem kontrollib API’lt tulevat vastust.

        2. Kui vastus on positiivne JA eelnevalt on kasutajal konto juba olemas, annab süsteem volituse siseneda, kasutaja on sisse logitud. Süsteem viib kasutaja library vaatesse.

        3. Kui vastus on positiivne JA eelnevalt kontot pole, jätkab süsteem kasutusjuhus "konto registeerimine" punktis 13.9

14. Märkused:

    13. Logimise vaatel on võimalus pöörduda kasutusloole "Salasõna unustatud", “Email unustatud”.

    14. Salasõna on varjatud kujul. Kui kasutaja soovib, siis süsteem näitab sisestamisel salasõna (checkbox "Show password")

    15. Salasõna sisestamisel hoitatakse kasutajat, kui tal on caps lock peal (Warning "Caps lock is on")

    16. Kui salasõna:email kombinatsiooni sisestatakse punktis 12.3 mitu korda valesti, siis kasutajat hoiatakse mitu korda ta saab veel sisestada ennem, kui süsteem lukustatakse 10 minutiks. Nt. "You will be locked for 10 mins after 2 more unsuccessful login attempts".

    17. Email:password väljad on sellised, mida brauserid on võimelised meelde jätma. 

15. Lahtised probleemid/testimiskohad:

    18. Kas kasutaja saab hetkel olla logitud sisse mitmest kohast? Mis siis juhtub?

16. Kasutusjuhu esinemissagedus: igapäevaselt

### Passwordi meeldetuletus

1. *Kasutajad-huvid:* Kõik kasutajad

2. *Primaarne kasutaja (kui on): *

3. *Üleüldine kirjeldus: *Passwordi meeldetuletus juhul kui on ununenud

4. *Infovaade (kus toimub protsess): *"login" vaates on link “Forget password?”**![image alt text](image_2.png)

5. *Käivitav sündmus: *Kasutaja on unustanud parooli. Soovib seda meelde tuletada "login" aknas.

6. *Eeltingimused: *Kasutajal on konto olemas üleüldse

7. *Järeltingimused: *Kasutaja on vahetanud ära salasõna uue vastu

8. *Erinõudmised:*

9. *UX-UI tips:*

10. *UML, mockup’id: *

    1. ![image alt text](image_3.png)

    2. ![image alt text](image_4.png)

    3. ![image alt text](image_5.png)

    4. ![image alt text](image_6.png)

11. *Näited:*

    5. Slack.com

12. *Stsenaarium:*

    6. Kasutaja soovib sisse logida.

    7. Kasutaja on "login" vaates. Selles vaates on tal vaja sisestada email, salasõna. Lisaks sellele on link “Forget password?”

    8. Avades vaate "Forget passwordi" alt, peab kasutaja sisestama oma emaili

    9. Sisestades oma emaili, saadab süsteem talle kinnituskirja koos lingiga

    10. Avades emailis oleva lingi, suunatakse kasutaja vaatesse, kus tal tuleb sisetada uus salasõna

    11. Salasõna sisestamisel näidatakse salasõna tugevust (vt. joonis üleval)

    12. Salasõna kinnitamisel logitakse kasutaja automaatselt süsteemi sisse "library" vaatesse.

13. *Laiendused:*

14. *Märkused: *

    13. Emailis olev link on kehtiv kuni 24h.

    14. Uus sisestatav salasõna ei tohi olla algne salasõna

15. *Lahtised probleemid:*

16. *Kasutusjuhu esinemissagedus: *igapäevaselt

### Emaili meeldetuletus

1. *Kasutajad-huvid:* Kõik kasutajad. Emaili meeldetuletus, mida kasutati registreerimisel

2. *Primaarne kasutaja (kui on): *

3. *Üleüldine kirjeldus: *Kasutajal on ununenud email. Soovitakse seda meeldetuletada.

4. *Infovaade (kus toimub protsess):* protsessi saab käivitada "login" vaates. Selleks on vastav link “Forget your email address?”![image alt text](image_7.png)

5. *Käivitav sündmus: *"Forget your email address" lingi avamine “login” vaates

6. *Eeltingimused: *Kasutajal on eeldatavalt olemas registeeritud konto ja tal on olemas emaili variandid, mida ta kasutas. Vastaselt juhul peab ta pöörduda ridline.com supporti poole.

7. *Järeltingimused: *Kasutajale saadetakse ühele sisestatud emailidest (mida kasutaja arvas, et registeerimisel sisestas) kiri sisuga, kas antud emaili on kasutatud registeerimisel.

8. *Erinõudmised:*

9. *UX-UI tips:*

10. *UML, mockup’id:* 

    1. ![image alt text](image_8.png)

    2. ![image alt text](image_9.png)

    3. Email:![image alt text](image_10.png)

11. *Näited:*

    4. Slack.com

12. *Stsenaarium:*

    5. Kasutaja soovib sisse logida "login" vaates, küll aga email on ununenud

    6. Kasutaja avab lingi "Forget your email address?"

    7. Süsteem kuvab vaate, kus kasutaja saab sisestada kuni 10 emaili (komadega eraldatud)

    8. Süsteem tuvastab emaili/emailid, mis on süsteemis olemas.

    9. Süsteem saadab nendele emailidele kirja sisuga, millal kasutati antud emaili registreerimisel ja kasutaja andmed (eesnimi, perenimi). Juhul, kui emaili ei tuvastata, siis kirja ei saadeta antud aadressile.

13. *Laiendused:*

14. *Märkused*

15. *Lahtised probleemid:*

    10. Tulevikus individuaalne kasutajate nõustamine, kellel tõesti ei ole email meeles. Selleks support kanali avamine - [feedback@ridline.com](mailto:feedback@ridline.com)  vms

16. *Kasutusjuhu esinemissagedus:* Igapäevaselt

### Automatic logout

1. *Kasutajad-huvid:* Turvalisuse mõttes, kui pole teatud aja jooksul kasutaja tegevust toimunud süsteemis (nt. juhul, kui kasutaja on unustanud ennast välja logida vms), siis teatud aja jooksul logitakse kasutaja välja, et vältida süsteemi väärkasutust teiste poolt.

2. *Primaarne kasutaja (kui on): *

3. *Üleüldine kirjeldus: *Kasutaja logitakse süsteemist automaatselt välja, kui tegevust pole toimunud mingi aja vältel.

4. *Infovaade (kus toimub protsess): *Protsess on sõltumatu lahtiolevast vaatest.

5. *Käivitav sündmus: *kasutaja ei ole teostanud tegevusi n ajaintervalli jooksul.

6. *Eeltingimused:  *Kasutaja on eelnevalt ennast sisse loginud

7. *Järeltingimused: *Kasutaja logitakse süsteemist välja. Pooleliolevad andmed salvestatakse.

8. *Erinõudmised:*

9. *UX-UI tips:*

10. *UML, mockup’id:*

11. *Näited:*

12. *Stsenaarium:*

    1. Kasutaja ei ilma tegevust perioodi x jooksul.

    2. Süsteem logib kasutaja välja

    3. Süsteem kuvab kasutajale "login" vaate ja modal kirja “You have been automatically logged out because of inactivity”.

13. *Laiendused:*

14. *Märkused:*

15. *Lahtised probleemid:*

    4. Kas kasutaja peaks saama muuta "advanced settingutes" ajaintervalli või üldse võimalust automaatne väljalogimine tühistada?

16. *Kasutusjuhu esinemissagedus: *igapäevaselt

### Logout

1. *Kasutajad-huvid:* Kõik. Kasutaja tahab turvaliselt süsteemist väljuda. Võimalus salvestada pooleliolevaid andmeid.

2. *Primaarne kasutaja (kui on): *

3. *Üleüldine kirjeldus: *Kasutaja soovib süsteemist väljuda. Süsteem küsib, kas tehtud muudatused salvestada, kui miski on pooleli.

4. *Infovaade (kus toimub protsess): *Igas vaates on võimalik ennast välja logida.

5. *Käivitav sündmus: *Kasutaja soovib süsteemist lahkuda.

6. *Eeltingimused: *Kasutaja on eelnevalt ennast sisse loginud.

7. *Järeltingimused: *Kasutaja on süsteemist välja loginud. Tema kohta käivad muudatused salvestatud.

8. *Erinõudmised:*

9. *UX-UI tips:*

10. *UML, mockup’id: *

    1. ![image alt text](image_11.png)

11. *Näited:*

12. *Stsenaarium:*

    2. Kasutaja esitab süsteemile palve välja logimiseks

    3. Süsteem vaatab, kas kasutajal on avatud tegevusi-protsesse

    4. Süsteem logib kasutaja süsteemist välja

13. *Laiendused:*

    5. Kui kasutajal süsteemis avatud tegevusi, siis süsteem kuvab teate, milles küsitakse, kas olemasolevad muudatused salvestada

    6. Kasutaja kinnitab või mittekinnitab olemasolevate muudatuste salvestamise

    7. Süsteem salvestab/ei salvesta olemasolevad muudatused.

    8. Süsteem logib kasutaja süsteemist välja

    9. Kasutajale kuvatakse landing page ridline.com

14. *Märkused:*

15. *Lahtised probleemid:*

16. *Kasutusjuhu esinemissagedus: *Koguaeg

### Deactivate account

1. *Kasutajad-huvid:* Kõik kasutajad. Kasutaja soovib ennast süsteemist jäädavalt kustutada. Selleks peab eelnevalt konto deaktiveerima

2. *Primaarne kasutaja (kui on): *

3. *Üleüldine kirjeldus: *Pärast konto aktiveerimist kustutatakse konto jäädavalt pärast 30 päeva mitte kasutamist. Kui kasutaja peaks sisse logima uuesti, siis konto aktiveeritakse.

4. *Infovaade (kus toimub protsess): "Profiili halduse" vaade. (vt. allpoolt “profiili andmete haldus”*

5. *Käivitav sündmus: *Kasutaja avaldab soovi konto deakiveerida

6. *Eeltingimused: *Kasutaja on eelnevalt ennast sisse loginud.

7. *Järeltingimused: *Kasutaja konto on deaktiveeritud staatuses. Pärast 30 päeva mittekasutamist pärast aktiveerimist kustutatakse konto jäädavalt.

8. *Erinõudmised:*

9. *UX-UI tips: *Kuna ei ole esmajärgulise tähtsusega funktsionaalsus, siis oluline on, et oleks veidi peidetud kujul (profiili halduse andmete all).

10. *UML, mockup’id:*

    1. ![image alt text](image_12.png)

    2. ![image alt text](image_13.png)

11. *Näited:*

12. *Stsenaarium:*

    3. Kasutaja soovib kontot deaktiveerida. Selleks läheb ta "profiili halduse" vaatesse (joonised üleval)

    4. Süsteem kuvab teate, kas kasutaja tõesti soovib kontot deaktiveerida?

    5. Kasutaja kinnitab. 

    6. Kasutaja peab sisestama oma salasõna.

    7. Süsteem kontrollib salasõna korrektsust

        1. Kui salasõna on korrektne, siis süsteem deaktiveerib süsteemis antud konto.

        2. Kui salasõna on vale, siis süsteem teavitab, et salasõna on vale ja kontot ei deaktiveerita..

    8. Kasutaja viiakse landing page’ile pärast edukat kustutamist. Lisaks modal "You have successfully deactivated your account"

13. *Laiendused:*

    9. Kasutaja ei kinnita

    10. Süsteem ei kustuta kasutaja seotud andmeid

14. *Märkused:*

15. *Lahtised probleemid:*

    11. Võiks olla võimalus, et süsteem küsib, kas soovitakse olemasolevaid andmeid eksportida.

16. *Kasutusjuhu esinemissagedus: *Mitte igapäevane tegevus, siiski tuleb ette.

### Profiili andmete haldus / profile data

1. *Kasutajad-huvid:* Kõik kasutajad. 

    1. Soovitakse, et nende kohta käivad andmed süsteemis oleks kõige aktuaalsemad 

    2. Soovitakse andmeid avalikustada/peita vastavalt soovile.

2. *Primaarne kasutaja (kui on): *

3. *Üleüldine kirjeldus: *Kasutaja saab määrata ja muuta enda kohta käivaid andmeid (profile data) ja mis nendest on avalikud: 

    3. first name

    4. last name

    5. phone

    6. website

    7. skype

    8. Your main role (sound engineer, organizer, artist, venue owner, other). (dropdown). Kui other, siis saab lisaväljal täpsustada.

    9. profile foto (Võimalus võtta FB’st, arvutist pilti)

4. *Infovaade (kus toimub protsess): *"your profile" vaates

5. *Käivitav sündmus: *Kasutaja avab "your profile" vaate

6. *Eeltingimused: *Kasutaja on sisse logitud staatuses.

7. *Järeltingimused: *Kasutaja profiili andmed on muudetud ja salvestatud.

8. *Erinõudmised:*

9. *UX-UI tips: *

10. *UML, mockup’id: *![image alt text](image_14.png)

11. *Näited: *

    10. *tegin Slack’i põhjal*

12. *Stsenaarium:*

    11. Kasutaja valib profiili halduse ülevalt paremalt. "Your profile"

    12. Avanenud vaates ("your profile") on vasakul pool menüü (profile, account, invite). Paremal on vastavate menüü elementide sisu. (profile data, account data, invite)

    13. Kasutaja saab muuta järgmisi andmeid nagu:

        1. eesnimi (osa süsteemi poolt kuvatavast nimest. Nt. "Jonas" juhul kui perenimi pole määratud või “Jonas Jilling” kui mõlemad on määratud.)

        2. perenimi (osa süsteemi poolt kuvatavast nimest. "Jilling" juhul kui eesnimi pole määratud või “Jonas Jilling” kui mõlemad on määratud.)![image alt text](image_15.png)Kui ei ole kumbki määratud, kuvatakse “Jonas Jilling” asemel

        3. Telefoninumbrit (vabas vormis)

        4. Veebilehe aadressi

        5. Skype aadress

        6. Your main role (sound engineer, organizer, artist, venue owner, other). Kui other, siis võimalik täita ära lisaväli. Nt "I am producer"

        7. Profile photo - klikkides pildil, on võimalik kas 

            1. uploadida pilti

            2. võtta FB’st juhul, kui konto ühendatud FB API’ga läbi registreerimise

            3. Võimalik pilti redigeerida (zoom, ääred).

        8. Kasutaja saab määrata, kas tema profiili andmed on projekti kasutajatele nähtavad. 

        9. Pärast muudatuste tegemist saab muudatused ära salvestada vormi all oleval nupuga "Update".

        10. Süsteem kontrollib sisestatud andmete korrektsust.

            4. Juhul, kui andmed on pole vigased, siis uued atribuudite väärtused salvestatakse. Kuvatakse teade edukast muutmisest. "Profile data" vaade suletakse.

            5. Juhul, kui süsteem tuvastab sisestatud andmetes vea (nt. tüübiviga), kuvatakse teade mitteedukast andmete muutmisest.  "Profile data" vaade jääb lahti.

13. *Laiendused:*

14. *Märkused:*

    14. Andmeväljade pikkused? Mis oleksid optimaalsed?

    15. Igale väljale juurde tooltip või miski selgitus.

15. *Lahtised probleemid:*

    16. Kas valitud väljad on õiged? Vajalikud?

    17. Kas kasutaja peaks saama määrata iga välja nähtavust (avalik, privaatne) eraldi?

    18. Mis on väljade puhul olevad constraint’id?

    19. *Kasutusjuhu esinemissagedus: *Igapäevaselt

### **Profiili andmete haldus / account data

1. *Kasutajad-huvid:* Kõik kasutajad. 

    1. Soovitakse, et nende kohta käivad konto (account)  andmed süsteemis oleks kõige aktuaalsemad/sobivamad. 

    2. Soovitakse teostada kontoga (account) seotud administratiivseid toiminguid. 

        1. Näiteks aktiivsetest sessioonidest välja loginud. Võib olla vajalik, kui kasutajal on mitu sessiooni lahti ja soovib turvalisuse kaalutlustel kõik peale käesoleva sessiooni sulgeda.

        2. Näiteks konto deaktiveerimine (vt. kasutusjuht "Konto deaktiveerimine" üleval)

2. *Primaarne kasutaja (kui on): *

3. *Üleüldine kirjeldus: *

    3. Konto andmete haldus. Näiteks emaili, passwordi muutmine. 

    4. Konto deaktiveerimine (vt. kasutusjuht "Konto deaktiveerimine" üleval)

    5. Muudest aktiivsetest sessioonidest välja logimine

4. *Infovaade (kus toimub protsess): *"your profile" vaates.

5. *Käivitav sündmus: *Kasutaja avab "your profile" vaate

6. *Eeltingimused: *Kasutaja on sisse logitud staatuses.

7. *Järeltingimused: *Kasutaja on muutunud emaili/salasõna/deaktiveerinud konto/aktiivsetest sessioonidest välja loginud.

8. *Erinõudmised:*

9. *UX-UI tips:*

10. *UML, mockup’id:*

    6. ![image alt text](image_16.png)

    7. ![image alt text](image_17.png)

    8. ![image alt text](image_18.png)

    9. ![image alt text](image_19.png)

11. *Näited: *

    10. Slack.com

12. *Stsenaarium:*

    11. Kasutaja valib profiili halduse ülevalt paremalt. "Your profile"

    12. Avanenud vaates ("your profile") on vasakul pool menüü (profile, account, invite). Paremal on vastavate menüü elementide sisu. (profile data, account data, invite)

    13. Kasutaja saab muuta järgmisi andmeid nagu:

        3. email

        4. password

            1. Vajutades vastavate väljade kõrvadel olevatel nuppudel "change", avanevad dialoogiaknad

            2. Avanenud dialoogiaknates tuleb sisestada vastavad väärtused, et emaili/passwordi muuta.

                1. Juhul, kui andmed on pole vigased, siis uued atribuudite väärtused salvestatakse. Kuvatakse teade edukast muutmisest. Dialoogiaken suletakse

                2. Juhul, kui süsteem tuvastab sisestatud andmetes vea (nt. tüübiviga), kuvatakse teade mitteedukast andmete muutmisest. Dialoogiaken jääb lahti.

    14. Kasutaja saab logida ennast kõikist aktiivsetest sessioonidest välja

        5. Selleks avaneb dialoogiaken, kuhu kasutaja sisestab oma parooli

            3. Kui parool on korrektne, kuvatakse teade, et kõigist aktiivsetest sessioonidest on välja logitud. Dialoogiaken suletakse.

            4. Kui parool on vale, siis kuvatakse teade, et parool on vale ja aktiivsetest sessioonidest välja ei logitud. Dialoogiaken jääb lahti.

13. *Laiendused:*

14. *Märkused:*

15. *Lahtised probleemid:*

    15. Mis on väljade puhul olevad constraint’id? Ala @ märk emaili puhul ntx.

16. *Kasutusjuhu esinemissagedus: *igapäevaselt

## Mooduli eesmärk/mõte:

## Lausendid

## Ärireeglid

## Ärisündmused

## Mooduli poolt toetatava äriteenuse kirjeldus-eesmärgid:

## Alammoodulid/funktsionaalsed allsüsteemid:

## Kasutajate pädevusalad-rollide kirjeldused:

## Põhiprotsess tekstilisel kujul:

## Põhiprotsessi tegevusdiagramm:

## Nõuete analüüs

### Funktsionaalsed nõudmised:

### Mittefunktsionaalsed nõudmised:

#### Sõltuvus teistest süsteemidest

#### Usaldusväärsus

#### Kättesaadavus

#### Stabiilsus

#### Laiendatavus

#### Hooldatavus

#### Hallatavus

#### Turvalisus

#### Paindlikkus

#### Skaleeritavus

#### Juurepääsetavus

#### Kasutatavus

#### Dokumenteeritus

#### Vastavus standarditele

## Kasutusjuhtud-alamkasutusjuhud struktuur:

![image alt text](image_20.png)

## Infovoogude diagrammid:

## Kasutusjuhtude jadadiagrammid:

## Kasutajate infovajadused (aruanded)

# ANDMEMUDEL

## Registri eesmärk:

## Mooduli registrid:

### Moodul teenindab:

### Moodul kasutab (sh. administratiivsed registrid). Selgitus:

## Olem-suhte diagramm (klassidiagramm, sh primaarne võti, alternatiivne võti, välisvõti)

## Tabel (kuuluvus registrisse, definitsioon, indeksid, piirangud, primaarne võti, alternatiivne võti, välisvõti)

## Kasutajate infovaated

![image alt text](image_21.png)

## Põhiobjekti/põhiobjektide olekudiagrammid

## Tabeli veerud (nende def, tüüp/domeen, tüübi/domeeni nimi, võimalikud väärtused, vaikeväärtus, kohustuslikkus)

## Domeen (nimi, baasandmetüüp, pikkus, võimalikud väärtused, vaikeväärtus, kohustuslikkus)

## Klassifikaatorid (tabeli nimi, koodide omadused, koodid, nimed)

