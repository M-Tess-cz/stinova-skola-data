# Stínová škola – data

Datové úložiště skillu **Stínová škola** (organizace domácí výuky, úkolů, přípravy a rozvrhu).
Spouštění skillu: `/skola`. Formát všech záznamů: Markdown.

## Struktura

```
zaci/<zak>/
  00-profil.md        oslovení, škola, typ školy, ročník, třída
  01-rozvrh.md        týdenní rozvrh, liché/sudé týdny
  02-predmety/        <predmet>.md – vyučující, učebnice, pomůcky, oblečení, aktuální téma, slabá místa
  03-ukoly.md         úkoly a testy s ID (U-0001…), termín, stav, doklad
  04-znamky.md
  05-kalendar.md      prázdniny, pololetí, akce
  06-pro-rodice.md    eskalace a poznámky pro rodiče
  sessions/           RRRR-MM-DD_HHMM_<role>_<uzivatel>.md – zápis každé session
  foto/               nafocené zápisy (datum_predmet), plné rozlišení
spolecne/             sdílené věci (rodinný kalendář apod.)
```

## Pravidla práce s repem

- Na začátku session vždy `pull`, na konci commit + `push`.
- V commitu i v zápisu session je uvedeno, kdo psal (role + jméno).
- Termín úkolu: hotovo nejpozději den před termínem do 20:00, jinak eskalace do `06-pro-rodice.md`.
