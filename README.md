# DanceEmotion — Piattaforma per scuole di ballo e ballerini

## Descrizione

**DanceEmotion** è un'applicazione web progettata per favorire l'incontro tra ballerini e scuole di danza.
Gli utenti possono scoprire corsi, eventi e materiali, prenotare lezioni, lasciare recensioni e ricevere aggiornamenti dalle scuole seguite.

<div align="center">
  <img alt="Piattaforma DanceEmotion" src="public/images/logo-white.png" />
</div>

## Video di presentazione

Nel seguente video di presentazione viene effettuata una breve panoramica del progetto, vengono discusse le **scelte progettuali adottate**: layout, struttura del database, componenti principali, logiche funzionali e scelte implementative.

- [DanceEmotion - Presentazione progetto](https://www.youtube.com/watch?v=Lqv96jZUZwA)

## Demo online

Tramite il seguente link [danceemotion.cristiancrazy.it](http://danceemotion.cristiancrazy.it) è possibile accedere ad una versione dimostrativa della piattaforma (solo versione NON HTTPS).

> **Nota**: l’istanza dimostrativa online è fornita a scopo dimostrativo e potrebbe non essere sempre disponibile. Pertanto, non si garantiscono uptime, continuità del servizio o livelli di disponibilità paragonabili all’ambiente di produzione. 

## Installazione manuale (versione demo)

Per installare la versione dimostrativa dell'applicazione sarà necessario:

0. Accedere alla cartella del progetto

1. Scaricare il framework **Bootstrap 5** e **Bootstrap Icons** e inserirne il contenuto nelle directory `public/bs` e `public/bs-icons`, come indicato nei `README.txt` delle rispettive cartelle.

2. Lanciare il comando `npm install` e attendere l'installazione delle dipendenze.

3. Eseguire il comando `npm start` e attendere l'avvio del server.

> **Nota**: questa è la procedura per l'installazione della versione dimostrativa dell'applicazione (contiene dati di test che consentono di provare l'applicazione web).

### File `.env`

Nella cartella del progetto è presente un file nel quale dovranno essere specificati i seguenti parametri:

| Parametro     | Descrizione                                      |
|---------------|--------------------------------------------------|
| `ADDRESS`     | Indirizzo sul quale il server rimarrà in ascolto |
| `PORT`        | Porta sul quale il server rimarrà in ascolto     |
| `SESSIONSS`    | Il secret per la gestione della sessione         |
| `GOOGLEAPIKEY`| L'API KEY per Distance Matrix API di Google      |

## Credenziali di esempio (versione demo)

| Email                                | Password            | Tipo         |
|--------------------------------------|---------------------|--------------|
| mario.rossi@email.com                | M!Rossi.            | Ballerino    |
| luca.gialli@email.com                | L!Gialli.           | Ballerino    |
| cristian.neri@email.com              | C!Neri.             | Ballerino    |

| Email                                | Password            | Tipo         |
|--------------------------------------|---------------------|--------------|
| latinfusion@email.com                | LF_School           | Scuola       |
| dancegalaxy@email.com                | DG_School           | Scuola       |
| flydance@email.com                   | FD_School           | Scuola       |

## Documentazione aggiuntiva 

È inoltre disponibile ulteriore documentazione tecnica nella cartella `/docs`.

La cartella `docs/` contiene tutti i materiali di supporto al progetto:

| Link                                | File                  | Contenuto                                                                |
|-------------------------------------|-----------------------|--------------------------------------------------------------------------|
| [Leggi](docs/database.pdf)          | `database.pdf`        | Specifiche del database, struttura relazionale e dettagli implementativi |
| [Leggi](docs/diagramma.pdf)         | `diagramma.pdf`       | Diagramma del database, struttura e relazioni                            |

> Nota: nel `database.pdf` non era stato definito l'utilizzo di `Corsi.IDScuola` (chiave esterna che referenzia `Scuola`). 

---

## Versione produzione (Docker)

Per l’ambiente di produzione è disponibile una versione dedicata della piattaforma, distribuita tramite container Docker.

Questa versione include:

- Configurazioni ottimizzate per il deploy reale  

- Database inizializzato **senza dati demo**  

- Script di avvio e gestione dei container

### Installazione (Produzione)

Per installare la versione di produzione:

1. Scaricare il file **`danceemotion-docker.tar.gz`**.

2. Decomprimere l’archivio nella macchina di destinazione.

3. Consultare il documento **`INSTALLAZIONE_README.md`** presente all’interno dell’archivio, che contiene:

   - Le istruzioni per l’installazione dell'immagine Docker

   - Le note sulla configurazione dell’ambiente

> **Nota:** la versione Docker è quella utilizzata per l’ambiente di produzione.  
> È progettata per essere stabile. La disponibilità dipende dall’infrastruttura su cui viene eseguita.

---
