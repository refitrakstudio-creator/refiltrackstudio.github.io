# RefiTrak - Strona WWW

## Hosting na GitHub Pages

### Instrukcja wgrania strony:

#### 1. Utwórz repozytorium GitHub

1. Wejdź na **github.com** i zaloguj się
2. Kliknij **New repository** (zielony przycisk)
3. Nazwa repozytorium: `refiltrackstudio.github.io`
4. Zaznacz **Public**
5. **NIE zaznaczaj** "Add README"
6. Kliknij **Create repository**

#### 2. Wgraj pliki

**Opcja A - Przez interfejs WWW (najprostrze):**

1. W nowym repozytorium kliknij **uploading an existing file**
2. Przeciągnij wszystkie pliki z folderu `website/`:
   - index.html
   - en.html
   - privacy.html
   - privacy-en.html
   - version.json
   - icon.png
   - favicon.png
3. Wpisz commit message: "Initial website upload"
4. Kliknij **Commit changes**

**Opcja B - Przez Git (dla zaawansowanych):**

```bash
cd /home/ubuntu/refitrak/website
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/TWOJA_NAZWA/refiltrackstudio.github.io.git
git push -u origin main
```

#### 3. Włącz GitHub Pages

1. W repozytorium kliknij **Settings**
2. W menu bocznym kliknij **Pages**
3. W sekcji "Source" wybierz:
   - **Branch:** main
   - **Folder:** / (root)
4. Kliknij **Save**

#### 4. Poczekaj na publikację

- GitHub przetworzy strony (1-5 minut)
- Strona będzie dostępna pod: `https://refiltrackstudio.github.io/`
- Status sprawdzisz w zakładce **Actions**

---

## Struktura plików

```
website/
├── index.html           # Strona główna (polski)
├── en.html              # Strona angielska
├── privacy.html         # Polityka prywatności (PL)
├── privacy-en.html      # Privacy policy (EN)
├── version.json         # Plik z wersją dla auto-update
├── icon.png             # Ikona aplikacji
└── favicon.png          # Favicon
```

---

## Po publikacji

1. **Zaktualizuj linki w aplikacji:**
   - Strony już używają refiltrackstudio.github.io ✓
   - Aplikacja sprawdza aktualizacje z version.json ✓

2. **Wstaw link w Google Play:**
   - Strona WWW: `https://refiltrackstudio.github.io/`
   - Polityka prywatności: `https://refiltrackstudio.github.io/privacy.html`

3. **Aktualizacja version.json:**
   - Przy nowej wersji aplikacji zmięń:
     - `version` - numer wersji
     - `releaseDate` - data
     - `changelog` - opis zmian
     - `downloadUrl` - link do Google Play (po publikacji)

---

## Domena własna (opcjonalnie)

Jeśli chcesz własną domenę (np. refitrak.pl):

1. Kup domenę (home.pl, nazwa.pl, itp.)
2. W panelu domeny dodaj rekord CNAME:
   ```
   www -> refiltrackstudio.github.io
   ```
3. W GitHub repozytorium:
   - Settings → Pages → Custom domain
   - Wpisz: `www.refitrak.pl`
   - Zaznacz "Enforce HTTPS"

---

## Wsparcie

Strona stworzona przez DeepAgent (Abacus.AI)
Aplikacja RefiTrak - ewidencja czynników chłodniczych dla techników HVAC
