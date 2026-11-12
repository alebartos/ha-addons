# Authelia

Avvia l'immagine ufficiale `authelia/authelia` senza modifiche.

La configurazione sta nella cartella `addon_configs` dell'add-on
(`/config` dentro il container):

- `configuration.yml`: configurazione di Authelia (filtro `template` attivo)
- `users.yml`: utenti
- `secrets/`: segreti letti con `{{ secret "/config/secrets/..." }}`

Nessuna porta esposta: il reverse proxy raggiunge l'add-on sulla rete
`hassio`, porta 9091.

La versione segue le release di Authelia tramite una GitHub Action giornaliera.
Prima di aggiornare leggi le note di rilascio nel changelog.
