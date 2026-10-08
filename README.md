# TIKEA — pierwsza wersja strony

Statyczna strona internetowa pod hosting OVH 100 MB. Nie wymaga PHP ani bazy danych.

## Publikacja na OVH

Prześlij zawartość folderu `tikea-website` (a nie sam folder) do katalogu docelowego domeny, zazwyczaj `www`, używając FTP/SFTP. Zachowaj strukturę folderów.

## Edycja tymczasowa

Edytuj `content/site.json` w GitHubie lub lokalnie i prześlij zaktualizowany plik przez FTP. Do podglądu lokalnego użyj serwera HTTP (np. `python -m http.server`), ponieważ przeglądarka może blokować `fetch()` przy otwieraniu pliku przez `file://`.

## CMS — ważne

`/admin/` zawiera konfigurację Decap CMS dla GitHub `modlesnica/tikea-website`. **Logowanie na tej wersji nie jest jeszcze gotowe** — wymaga osobnej usługi OAuth (np. zewnętrznego proxy) i konfiguracji `base_url` w `admin/config.yml`. Nie wstawiaj sekretów do repozytorium. Aby publikowanie przez CMS automatycznie trafiało na OVH, potrzebna jest osobna automatyzacja wdrożeń, np. GitHub Actions z sekretami FTP. Nie jest jeszcze skonfigurowana.

## Treść i zdjęcia

Treść jest początkowa i wymaga sprawdzenia przed publikacją. Grafika muzyczna jest elementem CSS, a nie zdjęciem z wydarzenia. Sekcja galerii i możliwość wgrywania zdjęć przez CMS będą kolejnym etapem.
