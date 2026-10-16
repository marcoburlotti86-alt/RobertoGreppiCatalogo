# Roberto Greppi — starter Netlify

Include una homepage responsive, un catalogo dimostrativo filtrabile e una modale di accesso solo grafica, oltre a configurazione Netlify e funzione health-check.

**Non è ancora pronto per uso commerciale.** Non contiene autenticazione reale, database persistente, ruoli admin/cliente, prezzi personalizzati, upload foto, pannello amministratore o ordini WhatsApp configurati. Non inserire dati reali in questa versione.

## Pubblicazione
1. Caricare tutti i file nella root del repository GitHub.
2. In Netlify scegliere Add new project → Import an existing project → GitHub.
3. Selezionare il repository; build command vuoto e publish directory `.`.
4. Pubblicare. Test health-check: `/.netlify/functions/health`.

## Da completare prima della produzione
Collegare database e autenticazione server-side; definire ruoli; creare API protette per catalogo, prezzi e ordini; configurare archiviazione foto e numero WhatsApp commerciale. I segreti vanno impostati nelle environment variables Netlify, mai nel codice client.
