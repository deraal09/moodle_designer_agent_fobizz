# Moodle Designer Agent (Fobizz)

Systemprompt für einen Fobizz-Agenten, der aus Stichpunkten, Aufgabenstellungen oder vorhandenem HTML fertig formatierte Moodle-Inhalte erstellt.

## Verwendung

1. Öffne den Fobizz-Agenten-Editor (funktioniert mit ChatGPT- und Claude-Modellen, z. B. Claude Sonnet 5).
2. Kopiere den gesamten Inhalt von [`prompts/moodle-agent-systemprompt.md`](prompts/moodle-agent-systemprompt.md) in das Systemprompt-Feld.
3. Fertig – der Agent fragt bei Bedarf nach, ob eine **Textseite**, ein **Lernpfad** oder ein **H5P-Inhalt** erstellt werden soll, und liefert direkt kopierbaren Code für den jeweiligen Moodle-/H5P-Editor.

## Inhalt des Prompts

Der Prompt ist modular aufgebaut:

- **Teil A** – gemeinsame Gestaltungsbasis (Farben, Boxen, Buttons, Tabellen, Hinweise) für alle Formate.
- **Teil B** – Moodle-Textseiten (`mod_page`), der ursprüngliche, bewährte Kern.
- **Teil C** – Lernpfade: entweder eine verlinkte Seitenfolge mit Navigation, oder eine verzweigte Moodle-Lektion (`mod_lesson`).
- **Teil D** – H5P-Inhalte: Text in der jeweiligen H5P-Eingabesyntax (z. B. Lückentext, Drag the Words) oder ein strukturierter Bauplan für Inhaltstypen ohne Texteingabe (Drag & Drop, Interactive Video, Branching Scenario, Course Presentation, Interactive Book, Question Set).
- **Teil E/F** – Sprache/Didaktik (Sie-Form, keine erfundenen Fachinhalte, Rückfragen bei Unklarheit) und das Ausgabeformat.

## Weiterentwicklung

Alle drei Formate teilen sich Farbpalette und Baustein-Stile aus Teil A, damit Textseiten, Lernpfade und H5P-Inhalte optisch zusammenpassen. Weitere Formate oder H5P-Inhaltstypen können als neue Unterabschnitte in Teil C/D ergänzt werden, ohne die gemeinsame Basis zu verändern.
