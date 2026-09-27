# Eine Shell, die man wegwerfen kann

Ein Erfahrungsbericht: wie man einem Assistenten Systemzugriff auf Windows gibt,
ohne ihn auf den Rechner zu lassen, auf dem die Arbeit liegt.

Zwei Bauarten, beide gemessen und beide mit den Fehlversuchen dokumentiert, die
dazwischen lagen:

1. **Windows Sandbox auf dem Arbeitsrechner** (14./15.09.2026). Wegwerfbar, ohne
   echten Bildschirm, mit einer Portbrücke, weil die Adresse bei jedem Start
   wechselt. Elf Fehlversuche.
2. **Ein eigenes Gerät im LAN** (17. und 27.09.2026). Feste Adresse, keine
   Brücke, echter Bildschirm, und es meldet sich nach einem Neustart selbst
   wieder an. Sieben weitere Fehlversuche.

Der Text ist als einzelne, in sich geschlossene HTML-Seite geschrieben. Kein
Build, kein Framework, keine Abhängigkeiten. Eine Datei, ein Doppelklick.

## Inhalt

    index.html    die ganze Seite, mit Stilen und Inhalt in einer Datei
    README.md     diese Datei

Eingebunden wird von außen nur eine Schriftart von Google Fonts. Wer auch das
nicht will, entfernt die beiden `<link rel="preconnect">` und das Stylesheet im
Kopf; die Seite fällt dann auf Systemschriften zurück und bleibt lesbar.

## Was drinsteht und was nicht

**Drin:** die tatsächlichen Fehlermeldungen, Rückgabewerte und Messwerte aus dem
Verlauf. Die Rückgabewerte sind der eigentliche Ertrag, weil mehrere davon wie
ein Absturz aussehen und keiner sind.

**Nicht drin, und das ist geprüft:** keine Schlüssel, keine Zugangsdaten, keine
Rechnernamen, keine echten LAN-Adressen, keine Pfade aus dem Arbeitssystem. Die
Adressen im Text sind entweder maskiert (`192.168.x.y`) oder die
NAT-Adressen der Windows Sandbox, die bei jedem Start ohnehin andere sind.

Wer den Text ändert, prüft das vor dem nächsten Hochladen erneut. Ein
Erfahrungsbericht wird nur dadurch nützlich, dass er echte Werte nennt, und
genau deshalb muss jemand hinsehen, welche echten Werte das sind.

## Stand und Pflege

Die Seite ist ein lebendes Dokument. Dazukommen soll, was gemessen wurde, nicht
was plausibel klingt. Zwei Regeln, nach denen sie bisher gewachsen ist:

- **Berichtigungen bleiben sichtbar.** An zwei Stellen steht im Text, dass eine
  frühere Aussage falsch war, samt Grund. Das ist kein Schönheitsfehler, das ist
  der Teil, der etwas wert ist.
- **Was zweimal funktioniert hat, ist ein Verfahren. Was einmal funktioniert
  hat, war ein Abend.** Der zweite Teil entstand, weil der erste ein zweites Mal
  angewendet wurde.

## Verwendete Bausteine

- [`windows-mcp`](https://github.com/CursorTouch/Windows-MCP) (MIT)
- `mcp-remote`
- [`uv`](https://github.com/astral-sh/uv) (Astral)
- Windows Sandbox, Teil von Windows 11 Pro

Diese Seite beschreibt deren Einsatz, sie enthält keinen Code daraus.

## Lizenz

Noch nicht festgelegt. Vor dem Veröffentlichen entscheiden: ohne Lizenzangabe
gilt volles Urheberrecht, also darf niemand den Text weiterverwenden. Für einen
Erfahrungsbericht ist CC BY 4.0 die naheliegende Wahl, aber das ist eine
Entscheidung und keine Formalie.
