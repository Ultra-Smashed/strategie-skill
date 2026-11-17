# Strategie-Skill

Ein Skill für Claude. Der Strategie-Skill schärft deine Positionierung, bis sie in einen Satz passt, baut aus deinen Leistungen eine Angebotstreppe mit Preisen, spielt große Entscheidungen vorher durch und bricht dein Jahresziel auf jede Woche herunter. Der Konkurrenz-Check analysiert deine fünf größten Mitbewerber und zeigt dir die Lücke, die noch keiner besetzt hat. Kostenlos, MIT-Lizenz.

| Modul | Was es macht |
| --- | --- |
| **Positionierung** | Aus deinen Lieblingskunden und Stärken entstehen drei Optionen, du wählst eine. Dazu Elevator Pitch, Website-Hero und Bio. |
| **Angebotstreppe** | Kostenlos, Einstieg, Kern, Premium, wiederkehrend. Mit Rechnung, ob das zu deiner Zeit passt, und dem Mut zum Weglassen. |
| **Entscheidungs-Check** | Gewichtete Kriterien, Szenarien in Zahlen und ein Pre-Mortem: Es ist ein Jahr später und es ist schiefgegangen. Warum? |
| **Jahresplan** | Vom Jahresziel rückwärts gerechnet auf Quartale, Monate und einen Wochenrhythmus, dazu eine Tabelle mit 52 Wochen. |
| **Konkurrenz-Check** | Fünf Mitbewerber mit Angebot, Preisen und Bewertungen, die häufigsten Beschwerden ihrer Kunden und eine Matrix mit der freien Lücke. |

## Installation

### Claude-App (Web, Desktop)

Am schnellsten: den Link in einen neuen Chat einfügen und Claude bitten, den Skill zu installieren:

```
https://github.com/Ultra-Smashed/strategie-skill

Installier diesen Skill für mich.
```

Oder von Hand:

1. [`strategie.zip`](https://github.com/Ultra-Smashed/strategie-skill/raw/main/strategie.zip) herunterladen (nicht entpacken).
2. In Claude unter **Settings → Capabilities** den Schalter **Code execution and file creation** einschalten. In der neueren Ansicht heißt er **Create and edit files**.
3. **Customize → Skills** öffnen, auf **+** klicken, dann **Create skill → Upload a skill** und die ZIP-Datei wählen.

Als Plugin: **Customize → Plugins**, bei den persönlichen Plugins auf **+**, dann **Add from a repository** und `Ultra-Smashed/strategie-skill` eintragen.

Die Menünamen stehen hier so, wie Anthropic sie in der Hilfe nennt. In der deutschen Oberfläche können sie übersetzt sein.

### Claude Code

Als Plugin:

```
/plugin marketplace add Ultra-Smashed/strategie-skill
/plugin install strategie@strategie
```

Oder den Ordner kopieren:

```bash
git clone https://github.com/Ultra-Smashed/strategie-skill.git
cp -r strategie-skill/skills/strategie ~/.claude/skills/
```

## Benutzen

Einfach schreiben, was du brauchst, zum Beispiel:

> Analysier meine fünf größten Mitbewerber. Ich bin Fotografin für Hochzeiten in Leipzig.

> Ich überlege, meine erste Mitarbeiterin einzustellen. Spiel das mit mir durch.

> Mein Ziel für nächstes Jahr sind 120.000 Euro Umsatz. Brich das auf Wochen herunter.

Der Skill schmeichelt nicht. Hat dein Plan eine Schwäche, sagt er es und begründet es. Danach kommt immer ein Weg nach vorn.

## Dateien

```
skills/strategie/SKILL.md            Ablauf, Module, Regeln
skills/strategie/modes/               eine Anleitung pro Modul
strategie.zip                       derselbe Skill-Ordner als ZIP für die Claude-App
.claude-plugin/                     plugin.json, marketplace.json
```

Nach einer Änderung im Skill-Ordner die ZIP neu bauen: `cd skills && zip -r ../strategie.zip strategie`.

Anleitung: [thanisch.co/wissen/guides/strategie-skill-claude](https://thanisch.co/wissen/guides/strategie-skill-claude)

MIT-Lizenz, siehe [LICENSE](LICENSE). Von [Christopher Thanisch](https://thanisch.co).
