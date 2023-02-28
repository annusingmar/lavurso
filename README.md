# lavurso — e-kooli veebirakendus ![image](https://user-images.githubusercontent.com/108177565/183647142-cacb64ee-f05a-499c-8033-facf81ee09bd.png)

### Installatsioon

Vajalik tarkvara

- `git`
- `docker`
- `docker-compose-plugin` (osal süsteemidest `docker-compose`)

Jooksuta käsureal

```
git clone --recurse-submodules --remote-submodules git@github.com:annusingmar/lavurso.git
```
<!-- Märge arendajale - ssh asemel võiks kastuada https, kuid https autenteerimine on raskem kui ssh-ga -->

Muuda vastavalt vajadusele faili `docker-compose.yml` (kindlasti `POSTGRES_PASSWORD` ja `DATABASE_PASSWORD`)

Seejärel jooksuta rakendust (osal süsteemidest on `docker compose` asemel `docker-compose`)

```
docker compose up -d
```



### [front-end](https://github.com/annusingmar/lavurso-frontend)

loodud [Vue'](https://vuejs.org/) ja [Quasariga](https://quasar.dev/)

---

### [back-end](https://github.com/annusingmar/lavurso-backend)

loodud [Go'ga](https://github.com/golang/go)

---

### arendamisel kasutatud programme

Git ja Github

[VSCodium](https://github.com/VSCodium/vscodium)

[Beekeeper Studio](https://github.com/beekeeper-studio/beekeeper-studio)

[Docker](https://docs.docker.com/engine/)
