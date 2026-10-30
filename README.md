# Pivara – evidencija bačvi

Web aplikacija za evidenciju punjenja i statusa bačvi.

## Datoteke
- `index.html` – sučelje aplikacije, prijava, pregled bačvi, unos punjenja i QR skener.
- `config.js` – javne postavke povezivanja sa Supabaseom.

## Postavljanje Supabase postavki
Uredi `config.js` i zamijeni:
- `OVDJE_UNESI_SUPABASE_PROJECT_URL` s Project URL vrijednošću iz Supabasea.
- `OVDJE_UNESI_SUPABASE_PUBLISHABLE_ILI_ANON_KEY` s Publishable key (ili legacy anon public key).

U ovu datoteku nikada ne stavljaj `service_role` ili `secret` ključ.

## Objavljivanje preko GitHub Pages
1. Otvori Settings → Pages u repozitoriju.
2. Pod Build and deployment odaberi Deploy from a branch.
3. Odaberi branch `main` i folder `/ (root)), pa Save.
4. Nakon objave aplikacija će biti dostupna na `https://ilicos-del.github.io/pivara-kegovi/`.

QR kamera zahtijeva HTTPS i dopuštenje za kameru u pregledniku.

## Napomena
Prije stvarnog rada s više zaposlenika potrebno je dovršiti i provjeriti RLS pravila i autorizaciju u Supabaseu. Klijentsko sučelje nije sigurnosna granica; ovlasti se moraju provoditi u bazi.
