# 💰 Progetto Risparmio

> App per cercare e confrontare le offerte sui prodotti, vedere come cambiano i prezzi nel tempo e trovare le occasioni più vicine a te.

## 📖 Descrizione

**Progetto Risparmio** è un'applicazione che aiuta gli utenti a risparmiare mostrando le offerte disponibili sui prodotti. Ogni offerta è legata a un prodotto, a una categoria e a una posizione geografica; di ogni offerta viene conservato lo storico dei prezzi, così l'utente può capire se un prezzo è davvero conveniente.

Il progetto è attualmente nella fase di **analisi e progettazione**: sono stati realizzati il diagramma dei casi d'uso e il diagramma delle classi.

## ✨ Funzionalità

- **Registrazione e login** dell'utente
- **Visualizzazione delle offerte** disponibili
- **Ricerca dinamica**: filtra le offerte per trovare solo ciò che interessa
- **Ordinamento per prezzo**
- **Visualizzazione dei prezzi nel tempo** (storico dei prezzi di ogni offerta)
- **Visualizzazione della posizione** dell'utente e delle offerte tramite GPS

> Alcune funzioni sono riservate agli utenti registrati (ricerca, ordinamento, visualizzazione delle offerte); l'utente non registrato può registrarsi, accedere e consultare lo storico dei prezzi.

## 👥 Attori del sistema

| Attore | Ruolo |
|--------|-------|
| **Cliente non registrato** | Può registrarsi/effettuare il login e vedere i prezzi nel tempo |
| **Cliente registrato** | Eredita le funzioni del cliente non registrato; può visualizzare e cercare le offerte e ordinarle per prezzo |
| **GPS** | Sistema esterno che fornisce la posizione dell'utente e quella delle offerte |

## 🧩 Modello dei dati

Classi principali individuate nella fase di progettazione:

| Classe | Attributi | Metodi |
|--------|-----------|--------|
| **Cliente** | nome, cognome, email | `registrazione()`, `login()` |
| **ClienteRegistrato** (estende Cliente) | password | `visualizzaOfferte()`, `cercaOfferte(testo)`, `ordinaPerPrezzo()` |
| **Offerta** | descrizione, prezzo | – |
| **StoricoPrezzo** | data, prezzo | – |
| **Prodotto** | nome, descrizione | – |
| **Categoria** | nome | – |
| **Posizione** | latitudine, longitudine | – |
| **GPS** | – | `getPosizione()` |

Relazioni principali:

- Un'**Offerta** ha uno **StoricoPrezzo** (composizione 1 → *)
- Un'**Offerta** riguarda un **Prodotto**, che appartiene a una **Categoria**
- Un'**Offerta** è associata a una **Posizione**; il **GPS** fornisce la **Posizione**
- Un **ClienteRegistrato** è associato a più **Offerte**

## 📋 Requisiti

- Git
- Distribuzione LaTeX (solo per compilare la documentazione)
- _Requisiti dell'app (linguaggio, framework, database): da definire quando inizia l'implementazione_


