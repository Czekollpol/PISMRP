# PISM — Generator dokumentów (GitHub Pages)

## Zawartość
- `index.html` — formularz i widok aplikacji.
- `styles.css` — responsywny interfejs oraz podgląd dokumentu.
- `app.js` — walidacja, numeracja, generowanie PDF, podgląd i archiwum.
- `assets/DejaVuSans.ttf` — dołączona lokalna czcionka Unicode (polskie znaki).

## Publikacja na GitHub Pages
1. Utwórz repozytorium na GitHubie.
2. Wgraj wszystkie pliki i katalog `assets` do głównego katalogu repozytorium.
3. Wejdź w Settings → Pages.
4. W sekcji Build and deployment wybierz Deploy from a branch.
5. Wybierz gałąź `main` oraz folder `/ (root)`, następnie Save.
6. Po opublikowaniu otwórz adres GitHub Pages repozytorium.

## Uruchomienie lokalne
Najlepiej uruchomić przez lokalny serwer statyczny, np.:
`python -m http.server 8000`
Następnie otworzyć `http://localhost:8000`.

## Ważne informacje o funkcjach
- PDF jest generowany po stronie przeglądarki przez jsPDF ładowany z CDN. Do pierwszego generowania wymagane jest połączenie z internetem. Font DejaVu Sans jest dołączony lokalnie i osadzany w PDF.
- Numeracja `PISM/001/ROK` jest przechowywana w localStorage przeglądarki. Jest ciągła wyłącznie w obrębie tej przeglądarki/urządzenia; czyszczenie danych witryny lub użycie innego urządzenia może zresetować licznik. Nie jest to centralna numeracja urzędowa.
- Archiwum PDF jest przechowywane w IndexedDB przeglądarki. Nie synchronizuje się między urządzeniami, profilami przeglądarki ani użytkownikami i może zostać usunięte wraz z danymi witryny.
- Nie zapisuj w tej demonstracyjnej aplikacji danych wrażliwych ani danych osobowych, jeśli nie masz odpowiedniej podstawy i zabezpieczeń.
- Nazwa PISM, podstawa prawna i treść zarządzenia to przykładowy wzór dostarczony w rozmowie. Przed rzeczywistym wykorzystaniem trzeba zweryfikować umocowanie instytucji, przepisy i treść dokumentu.
