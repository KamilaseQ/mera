# MERA × Politechnika — prezentacja

Statyczny, samowystarczalny landing page (jeden plik `index.html` z wbudowanymi grafikami i stylami — bez zależności, bez build-stepu). Gotowy do wdrożenia na Vercel.

## Wdrożenie na Vercel

Trzy sposoby, dowolny działa:

### A. Przez GitHub (zalecane)
1. Utwórz nowe repo na GitHub i wypchnij ten folder:
   ```bash
   git remote add origin git@github.com:<login>/<repo>.git
   git push -u origin main
   ```
2. Wejdź na [vercel.com/new](https://vercel.com/new), zaimportuj repo.
3. Framework Preset: **Other**. Build Command: puste. Output Directory: puste (albo `.`).
4. Deploy. Strona ląduje pod `https://<projekt>.vercel.app`.

### B. Vercel CLI
```bash
npm i -g vercel
vercel        # podgląd
vercel --prod # produkcja
```

### C. Drag & drop
Przeciągnij ten folder na [vercel.com/new](https://vercel.com/new) (opcja „deploy without Git").

## Własna domena
W panelu Vercel: **Settings → Domains → Add** i wskaż domenę (np. `mera.twojadomena.pl`).

## Aktualizacja treści
Ten `index.html` jest generowany ze źródła w katalogu nadrzędnym (`src-content.html` + `python build.py`). Po każdej zmianie build nadpisuje `mera-landing/index.html` — wystarczy je zacommitować i wypchnąć (albo `vercel --prod`).
