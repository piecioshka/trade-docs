# Współtworzenie

Jak zorganizowane są notatki i jak je rozwijać. Sama treść jest w [README](README.md).

## Organizacja repozytorium

| Ścieżka      | Co zawiera                                                        |
| ------------ | ----------------------------------------------------------------- |
| `README.md`  | całe kompendium: spis treści, część I (podstawy), część II (CFD)  |
| `README.pdf` | wersja PDF wygenerowana z `README.md`                             |
| `assets/`    | diagramy SVG wstawiane do README (świeca, spread, rolowanie itd.) |

Strona GitHub Pages jest serwowana z gałęzi `main` (katalog główny), dlatego PDF jest dostępny pod adresem podanym w README.

## Jak dodać sekcję

1. Dopisz sekcję `## ...` w odpowiedniej części `README.md`.
2. Dodaj ją do spisu treści na górze pliku (link do kotwicy nagłówka).
3. Diagram zapisz jako SVG w `assets/` i wstaw ścieżką względną, np. `![Opis](assets/spread.svg)`.
4. Nazwy brokerów, regulatorów, giełd i źródeł danych linkuj do ich stron, a źródła dopisz do sekcji "Źródła i przydatne linki".
5. Liczby zależne od oferty brokera opatrz datą weryfikacji (patrz notka "Aktualność danych" na górze README).

## Generowanie PDF

```bash
npx md-to-pdf README.md
```

Komenda nadpisuje `README.pdf`. Regenerację PDF commituj osobno.

## Konwencje

- Commity w stylu Conventional Commits po angielsku: `docs:` dla treści, `chore: regenerate PDF` dla nowego PDF.
- Przykłady liczbowe dla surowców liczone na Brent (OIL).
- Pliki tymczasowe w `tmp/` (ignorowany przez git).
