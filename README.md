# HOW TO

- Copia il file `env.example`, rinomina in `.env` e cambia i valori delle variabili desiderati.
- usa `docker compose up --build --watch` per eseguire il container


# FAQ

Q: Voglio cancellare tutto e ricominciare da capo, come faccio?
A: usa `docker compose down -v --remove-ophans`, poi cancella il file `config/odoo.conf` e la cartella `postgres`.

Q: Devo ricaricare qualcosa quando modifico un file?
A: Se modifichi all'interno della cartella `addons` il sistema ricaricherà Odoo da solo. Altrimenti devi chiudere il container e ricostruirlo.
PS: non usare l'opzione `-v` e `--remove-orphans` se devi solo ricaricare il contenuto del container.