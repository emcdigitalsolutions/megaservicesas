# MegaService SAS — Sito vetrina

Sito vetrina ufficiale di **MegaService SAS** — stazione di servizio Q8, AdBlue certificato, CarWash, olio, batterie e accessori auto e camion. Punti vendita a **Campobello di Licata (AG)** ed **Enna**.

Single-page in HTML/CSS/JS puro (nessun build), mobile-first, multi-sezione:
Home · Storia · Prodotti & Servizi · AdBlue · Rete & Extrarete · Galleria · Eventi & News · Recensioni · Contatti.

## Sviluppo
Il sito è interamente in `index.html`. Per l'anteprima basta aprirlo in un browser.

## Hosting
Pubblicato tramite **GitHub Pages**. Anteprima: https://emcdigitalsolutions.github.io/megaservicesas/

## Privacy / Cookie / SEO
- `privacy.html` — Privacy & Cookie Policy (GDPR). Linkata dal footer e dal form.
- Banner cookie + **Google Maps caricato solo previo consenso** (gating via `data-src`, scelta salvata in `localStorage` chiave `mgs-cookie-consent`).
- `robots.txt`, `sitemap.xml`, tag `canonical` + Open Graph/Twitter già presenti.

## Go-live dominio (megaservicesas.it)
Quando il dominio è registrato (Aruba):
1. **DNS su Aruba** — per dominio apex `megaservicesas.it` puntare ai 4 IP di GitHub Pages con record **A**:
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
   (Opzionale `www` → record **CNAME** verso `emcdigitalsolutions.github.io`.)
2. **Attivare il file `CNAME`** (già pronto in repo, contiene `megaservicesas.it`): rimuovere la riga `CNAME` dal `.gitignore` e fare commit del file.
3. In GitHub → Settings → Pages: impostare il custom domain e attivare **Enforce HTTPS**.
4. **Aggiornare gli URL assoluti** da `https://emcdigitalsolutions.github.io/megaservicesas/` a `https://megaservicesas.it/` in: `index.html` (canonical, og:url, og:image, twitter:image), `privacy.html` (canonical), `sitemap.xml`, `robots.txt`.

---

Progettato e sviluppato da [EMC Digital Solutions](https://www.emcdigitalsolutions.it).
