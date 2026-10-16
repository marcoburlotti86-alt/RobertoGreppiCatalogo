# Roberto Greppi Milano — progetto Netlify

## Cosa contiene questa consegna
- Sito responsive con identità visiva bianca/nera, logo originale ricevuto e profondità/ombre 3D.
- Catalogo intenzionalmente vuoto: nessun bijoux, prezzo, stock, cliente o contatto inventato.
- Interfaccia per ricerca e filtri; carrello dimostrativo e riepilogo ordine scaricabile.
- Struttura iniziale per area clienti, flusso B2B e storico ordini.
- `supabase/schema.sql`: schema di partenza per un backend reale con profili, ruoli, articoli, prezzi per cliente e ordini, con Row Level Security.
- `netlify/functions/health.js`: endpoint di controllo deploy.

## Pubblicazione frontend su Netlify
Nel repository GitHub collegato a Netlify, caricare/sostituire **tutti i file e le cartelle** contenuti in questo progetto mantenendo la struttura. Impostazioni build: comando vuoto; directory pubblicazione `.`; directory funzioni `netlify/functions`.

## Importante: cosa non è ancora live
Il sito statico non può garantire autenticazione, prezzi privati o dati condivisi fra dispositivi. Login, amministrazione protetta, database, upload immagini, prezzi personalizzati e ordini con storico richiedono un backend configurato. Il carrello in questa versione è una dimostrazione locale e non invia ordini. Non inserire credenziali reali.

## Backend di produzione
1. Creare un progetto Supabase.
2. Eseguire `supabase/schema.sql` nel SQL Editor e verificare le policy con un tecnico prima di inserire dati reali.
3. Configurare Auth, creare l'utente amministratore e assegnare esplicitamente il ruolo `admin` al relativo profilo.
4. Configurare variabili ambiente lato server su Netlify; mai pubblicare la service-role key nel browser o nel repository.
5. Collegare funzioni server per CRUD prodotti, immagini, prezzi per account, creazione ordine e storico; verificare le policy e il flusso ordine prima di usarlo con clienti.
6. Inserire il numero WhatsApp aziendale verificato solo quando disponibile.

Nessun dato commerciale, numero WhatsApp o account è stato inventato. Il logo è stato copiato in `assets/` dai file forniti dall'utente.
