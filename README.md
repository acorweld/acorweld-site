# Strona ACorWeld — wdrożenie na GitHub Pages

## Co jeszcze trzeba uzupełnić przed publikacją
- **Sekcja Rekomendacje** (`index.html`, `id="rekomendacje"`) — 4 cytaty-placeholdery, w dwóch identycznych blokach (drugi to duplikat do pętli animacji). Podmień treść, autora i `src` zdjęcia w obu miejscach.
- **Kontakt** — obecnie `kontakt@acorweld.com` i link LinkedIn z placeholderem `PODMIEN-LINK`. Podmień na prawdziwe dane.
- **CV** — przyciski linkują do `cv-maciej-kochel.pdf`, którego nie ma w tym folderze. Wgraj plik PDF o tej nazwie do repozytorium (obok `index.html`) albo zmień link.
- **Logo/baner** — na razie strona używa samego wordmarku tekstowego "ACORWELD" w nawigacji. Jeśli chcesz wstawić prawdziwe pliki `AcorWeld_logo.png` / baner, dodaj je do repo i podmień `.nav-logo` w `index.html` na `<img>`.

## Wdrożenie na GitHub Pages
1. Załóż nowe repozytorium na GitHub, np. `acorweld-site` (może być prywatne lub publiczne — dla Pages nie ma to znaczenia poza kontem darmowym, gdzie repo musi być publiczne).
2. Wgraj do niego pliki z tego folderu: `index.html`, `style.css`, `script.js`, `CNAME` (oraz CV, gdy będzie gotowe).
3. W repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Po chwili GitHub poda adres typu `https://twoja-nazwa.github.io/acorweld-site` — to Twój tymczasowy adres, zanim zadziała domena.

## Podpięcie domeny acorweld.com (Hostinger)
Plik `CNAME` w repo już zawiera `acorweld.com` — to mówi GitHub Pages, na jaką domenę ma reagować. Zostaje ustawić DNS u Hostingera:

W hPanel Hostingera → Domeny → acorweld.com → DNS / Nameservery, dodaj:
- 4 rekordy **A** dla `@` (czyli acorweld.com) wskazujące na adresy IP GitHub Pages: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- 1 rekord **CNAME** dla `www` wskazujący na `twoja-nazwa.github.io`

Propagacja DNS: zwykle do kilku godzin, czasem do 24h. Po propagacji w Settings → Pages GitHub pokaże domenę jako zweryfikowaną — wtedy warto zaznaczyć tam też "Enforce HTTPS".
