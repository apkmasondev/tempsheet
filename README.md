# TempSheet

Lekki arkusz do szybkich obliczeń w przeglądarce. Obsługuje formuły, formatowanie, sortowanie, wyszukiwanie oraz eksport CSV i XLSX.

**Uruchom aplikację: https://apkmasondev.github.io/tempsheet/**

Dane arkusza pozostają w pamięci karty przeglądarki. Aplikacja nie wysyła ich na serwer i nie zapisuje automatycznie. Aby zachować pracę, pobierz edytowalny plik TempSheet przez menu Export lub skrótem Ctrl/⌘ + S. Lokalnie zapamiętywany jest wyłącznie wybór motywu.

Menu Export oferuje dwa warianty XLSX: „Download XLSX” zapisuje wyniki, a „Download XLSX with formulas” zachowuje formuły do dalszej pracy w Excelu. Oba warianty zachowują formatowanie i szerokości kolumn. Plik z formułami zawiera aktualne wyniki oraz włączone przeliczanie przy otwarciu; nieobsługiwana formuła jest zgłaszana z adresem komórki. TempSheet nie importuje jeszcze XLSX — do ponownego otwarcia arkusza tutaj służy plik `.tempsheet.json`.

## Zawartość repozytorium

- `dist/` — gotowe pliki produkcyjne aplikacji, w tym biblioteka eksportu XLSX ładowana na żądanie.
- `.github/workflows/deploy.yml` — publikacja katalogu `dist/` przez GitHub Pages.
- `README.md` — opis aplikacji i sposobu publikacji.

## Publikacja

GitHub Pages korzysta z GitHub Actions. Zmiany na gałęzi `main` automatycznie publikują zawartość `dist/`. Wdrożenie można również uruchomić ręcznie w zakładce Actions, wybierając „Deploy production to GitHub Pages”.

Jest to repozytorium dystrybucyjne. Nie zawiera źródeł projektu ani narzędzi budowania; do uruchomienia aplikacji wystarcza statyczny hosting plików z `dist/`.
