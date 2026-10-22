# MoneyCode Eventówki — Paper 1.21.4 (v1.0.1)

Projekt źródłowy Gradle, **niezweryfikowany kompilacyjnie ani w grze**.

## Wymagania
- Serwer **Paper 1.21.4**, nie 1.21.1 (poprzedni błąd: Unsupported API version 1.21.4).
- Java 21, WorldEdit i WorldGuard zgodne z Paper 1.21.4.
- Kompilacja GitHub Actions: `.github/workflows/build.yml`; po sukcesie pobierz artifact.

## Instalacja
1. Zrób kopię zapasową serwera i świata; zaktualizuj Paper do 1.21.4.
2. Rozpakuj ten ZIP i wrzuć jego **zawartość** do repozytorium GitHub (zachowaj strukturę katalogów).
3. Uruchom Actions > Build MoneyCode Eventowki > Run workflow.
4. Jeżeli build jest zielony, pobierz JAR z Artifacts i wgraj do `plugins/`.
5. Usuń starszy JAR MoneyCodeEventowki z `plugins/` i uruchom serwer ponownie.
6. Zainstaluj paczkę zasobów ZIP w kliencie Minecraft 1.21.4.

## Przedmioty i regiony
`/mceventowki` — GUI tylko OP lub `moneycode.eventowki.admin`.
Topór Gromu (50s), Gruszka (Regeneration V 3s), Wyrzutnia Otchłani (120s, klatka 15s), Klepsydra Czasu (80s), Hak Otchłani (45s).
Wymagany region WorldGuard z `pvp` w nazwie; każdy region z `spawn` blokuje moc.

## Ograniczenia wymagające testów
- Nie potwierdzono działania ani kompilacji kodu.
- Klatka używa tymczasowych bloków `TINTED_GLASS`; istniejące bloki nie są nadpisywane.
- Odporność na wszystkie inne pluginy, komendy administracyjne, restart/crash oraz obchodzenie klatki wymaga dodatkowych zabezpieczeń.
- Przy nagłym wyłączeniu procesu bloki klatki mogą pozostać: testuj tylko na kopii świata.
