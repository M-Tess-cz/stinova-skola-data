# Stínová škola – koncept v0.4

Datum debaty: 2026-11-01
Stav: ladění zadání, SKILL.md se zatím nepíše.

## Účel
Organizace domácí výuky: přehled o škole (rozvrh, učivo, úkoly, testy, známky), plánování přípravy a procvičování, hlídání úkolů. Všechny předměty, celý rok, včetně pomůcek a oblečení (TV, dílny, praxe).

## Rozhodnutí
| # | Téma | Rozhodnutí |
|---|------|-----------|
| 1 | Pro koho | Obecně pro kohokoli, libovolná škola včetně ZŠ. Při onboardingu se zeptá, jak žákovi říkat. |
| 2 | Kdo mluví | Žák v roli žáka, rodič v roli rodiče. |
| 3 | Úložiště | Git repo `M-Tess-cz/stinova-skola-data` (soukromé), vše v MD. |
| 4 | Zdroj dat | Zatím ruční zápis + foto. |
| 5 | Přísnost | Přísná. |
| 6 | Aktivita | Jen na vyžádání; z každé session nový MD soubor se zápisem. |
| 7 | Předměty | Všechny. |
| 8 | Spouštění | `/škola` (technicky asi `/skola` – název skillu bez diakritiky, ověřit). |
| A | Úložiště | GitHub (FTP/síťový disk z cloudu nedostupný). |
| B | Učitel | Zůstává samostatný skill; Stínová škola ho jen doporučí. Zobecnění Učitele později. |
| C | Více žáků | Jedno repo, každý žák ve vlastní složce. |
| D | Termín úkolu | Hotovo nejpozději den před termínem do 20:00, jinak eskalace rodiči. |
| E | Ověření role | Zatím prohlášením (bez hesla). |
| – | Uživatelé | Více lidí z různých účtů (GitHub + Claude). |
| – | Fotky | Plné rozlišení. |

## Onboarding žáka
Oslovení, škola, typ školy, obor, ročník, třída; rozvrh (foto/ručně, liché/sudé týdny); předměty (vyučující, učebnice, pomůcky, oblečení); školní rok (prázdniny, pololetí, ředitelská volna).

## Role
- Žák: co mám zítra, co sbalit, zapiš úkol/test, nafocený zápis, procvičování (výklad → Učitel).
- Rodič: přehled, rizika, prošvihnuté úkoly, známky, zadání úkolu, poznámka pro dítě.
- Rodič vidí vše; žák nevidí poznámky rodiče (pravidlo chování, ne zabezpečení).

## Přísnost
- Každá session začíná kontrolou: úkoly po termínu, testy do 3 dnů, nevyřešené z minula.
- Hotovo = doloženo (foto/popis).
- Úkol nehotový den před termínem v 20:00 → `06-pro-rodice.md`; rodič to vidí jako první.
- Kontrola proběhne při nejbližší session (skill je na vyžádání); případné automatické hlášení v 20:00 = budoucí naplánovaná úloha.
- Odbočení od nepříjemného tématu: jedna stručná připomínka, pak dál.

## Úložiště a práce s gitem
Struktura viz README. Pravidla:
- Začátek session: `pull`. Konec: commit + `push`; při konfliktu `pull --rebase` a sloučení.
- Session soubory s unikátním názvem `RRRR-MM-DD_HHMM_<role>_<uzivatel>.md`.
- Sdílené soubory editovat po řádcích, úkoly s ID (U-0001…).
- Autor (role + jméno) v commitu i zápisu.
- Soukromí: všichni collaboratoři vidí všechny žáky; jiná rodina = jiné repo.

## Zápis session
Kdo, kdy, co se řešilo, co se změnilo (úkoly, známky, témata), co zůstalo otevřené, co příště zkontrolovat.

## Otevřené body
- Fotky: Git LFS, nebo roční archivace mimo repo (odhad ~2 GB/žák/rok).
- Název skillu `/skola` vs. `/škola` – ověřit.
- Plánování přípravy na testy (např. 5–3–1 den předem), týdenní přehled pro rodiče, přesný formát zápisu session.

## Zprovoznění přístupu (2026-11-01)
1. GitHub účet `M-Tess-cz`, repo `stinova-skola-data` (Private).
2. Claude → Settings → Connectors → GitHub Integration → Connect. Pozor: připojení se otevírá v prohlížeči, kde musí být na claude.ai přihlášený stejný účet (jinak přesměruje na stránku s plány).
3. Instalace Claude GitHub App s přístupem k repu (github.com/apps/claude/installations/select_target) – bez ní funguje jen čtení, ne push.
4. Další uživatelé: vlastní GitHub účet → collaborator v repu → GitHub v Claude → Claude GitHub App.
