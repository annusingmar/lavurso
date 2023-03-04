# lavurso — e-kooli veebirakendus ![image](https://user-images.githubusercontent.com/108177565/183647142-cacb64ee-f05a-499c-8033-facf81ee09bd.png)

### Installatsioon

Vajalik tarkvara

- `git`
- `docker`
- `docker-compose-plugin` (osal süsteemidest `docker-compose`)

Jooksuta käsureal

```
git clone --recurse-submodules --remote-submodules https://github.com/annusingmar/lavurso.git
```

Muuda vastavalt vajadusele faili `docker-compose.yml` (kindlasti `POSTGRES_PASSWORD` ja `DATABASE_PASSWORD`)

Seejärel jooksuta rakendust (osal süsteemidest on `docker compose` asemel `docker-compose`)

```
docker compose up -d
```
---
Peale esmast käivitamist saab sisse logida e-postiga `admin@example.com` ja parooliga `adminPassword` ning seejärel tuleb muuta parool, mida saab teha kas külgribalt "Profiil" alt või administraatori kasutajate haldamise lehelt, külgribal "Kasutajad".

Kasutajad on eraldatud rollidega:
* administraator - kasutaja saab luua/muuta kasutajaid, gruppe, klasse, hindeväärtusi, õppeaineid ja -aastaid; ligipääs kõigile päevikutele ja õpilaste andmetele;
* õpetaja - kasutaja saab luua päevikuid ning teda saab määrata klassijuhatajaks, st saab ligipääsu klassi õpilaste andmetele;
* õpilane - õpetaja saab lisada kasutajat päevikusse õpilaseks, kasutajal endal on vaade oma toimunud tundidest, hinnetest, ülesannetst; loomisel on kohustuslik määrata klass;
* lapsevanem - kasutajat saab lisada õpilase lapsevanemaks, saab ligipääsu õpilase andmete ja vaatele.

Grupid on sõnumisüsteemi jaoks ning koosnevad kasutajatest, gruppe saab luua/muuta ainult administraator. Sõnumisüsteemis on võimalik saata sõnumeid kasutajate või gruppide kaupa.

Õppeaineid lisab administraator ning neid saab valida päeviku loomisel. Hindeväärtuste lehel määrab administraator lubatud hinded, nt "5", "F" jne.

Klassid ja õppeaastad on seotud, kui klassil on määratud õppeaasta jaoks kuvatav nimi. Seost saab administraator muuta/luua käsitsi klasside lehel ning ka uut õppeaastat alustades õppeaastate lehel. Uue õppeaasta alustamise viisardis loob administraator uue õppeaasta, uued klassid ning kannab üle valitud klassid uude õppeaastasse neile kuvatava nime andmisega.

Päeviku loomisel tuleb anda päevikule nimi ja õppeaine. Hiljem saab muuta päeviku nime ja päevikule ligi pääsevaid õpetajaid, kuid mitte selle nime. Päevikusse saab lisada õpilasi klasside kaupa või ükshaaval. Päevik jaguneb kursusteks, mille arv ei ole piiratud. Kursusele saab lisada tunde toimumiskuupäevaga. Tunnis on võimalik panna õpilastele märkeid: puudumine, hilinemine, tegemata töö, kiitus, teade, märkus ja hinne. Kursusele saab panna kursusehindeid ning päevikus saab lisada ainehindeid. Päevikus saab õpilastele lisada ka tähtajaga ülesandeid, st kodutöö või kontrolltöö.

Õpilane näeb temale määratud ülesandeid ning n-ö ajajoonel ka lisatud märkeid ja toimunud tunde. Ta saab vaadata õppeaasta lõikes päevikute kaupa märkeid ja toimunud tunde ning tabelina kokkuvõtvaid kursuse- ja ainehindeid õppeainete kaupa.

---
### [front-end](https://github.com/annusingmar/lavurso-frontend)

loodud [Vue](https://vuejs.org/) ja [Quasariga](https://quasar.dev/)

---

### [back-end](https://github.com/annusingmar/lavurso-backend)

loodud [Go'ga](https://github.com/golang/go)

---

### arendamisel kasutatud programme

Git ja GitHub

[VSCodium](https://github.com/VSCodium/vscodium)

[Beekeeper Studio](https://github.com/beekeeper-studio/beekeeper-studio)

[Docker](https://docs.docker.com/engine/)
