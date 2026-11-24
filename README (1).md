# J.A.R.V.I.S. – Web-Assistent

Sprachassistent im Browser mit Hacker-Design. Er hört dauerhaft auf „Hey Jarvis“, öffnet Websites, sucht bei Google/YouTube und antwortet über Claude.

## Auf GitHub Pages veröffentlichen

1. Auf github.com ein neues Repository anlegen, zum Beispiel `jarvis`, Sichtbarkeit Public.
2. `index.html` und diese `README.md` hochladen („Add file → Upload files“) und committen.
3. Im Repository: **Settings → Pages**. Bei „Branch“ `main` und `/ (root)` wählen, speichern.
4. Nach ein bis zwei Minuten läuft die Seite unter `https://DEIN-NAME.github.io/jarvis/`.

GitHub Pages nutzt https. Das ist Voraussetzung für das Mikrofon.

## Erste Schritte

1. Seite öffnen, **EINSTELLUNGEN** klicken, den Anthropic-API-Key eintragen und speichern.
2. **SYSTEM STARTEN** klicken und das Mikrofon einmal erlauben. Chrome und Edge merken sich die Erlaubnis für diese Seite.
3. „Hey Jarvis, what time is it?“ oder „Hey Jarvis, open youtube“ sagen.

Beim ersten Öffnen einer Website blockiert der Browser eventuell das Pop-up. Erlaube Pop-ups für die Seite, dann klappt es künftig ohne Klick. Bis dahin erscheint der Link im Terminal.

## Befehle

- `open <seite>` / `öffne <seite>`: Website öffnen (youtube, github, spotify, beliebige-domain.de …)
- `search <begriff>` / `suche <begriff>`: Google-Suche
- `youtube <begriff>`: YouTube-Suche
- Uhrzeit, Datum, Status
- alles andere: Gespräch mit Claude (braucht den API-Key)

## Datenschutz und Kosten

- Der API-Key wird nur im `localStorage` deines Browsers gespeichert und direkt an Anthropic gesendet. Er steht nicht im Code und nicht auf GitHub.
- Benutze die Seite nicht auf fremden oder geteilten Computern.
- Setze im Anthropic-Konto ein Ausgabenlimit. Jede Antwort kostet nur Bruchteile eines Cents.

## Stimme

Die Stimme kommt aus den Stimmen deines Browsers beziehungsweise Betriebssystems. Für den britischen Butler-Klang in den Einstellungen „Englisch“ wählen und eine britische Männerstimme aussuchen:

- Edge/Windows: „Microsoft Ryan“ oder „Microsoft George“
- Chrome: „Google UK English Male“
- Safari/macOS: „Daniel“

Mit Tonhöhe (etwa 0,8) und Tempo lässt sich der Klang feinjustieren.

## Realistischere Stimmen (optional)

Unter **EINSTELLUNGEN → Sprach-Engine** gibt es neben den Browser-Stimmen zwei Cloud-Dienste mit deutlich natürlicherem Klang:

- **ElevenLabs:** API-Key eintragen, „Meine Stimmen laden“ klicken und eine Stimme wählen, am besten eine britische Männerstimme aus der Standard-Bibliothek.
- **OpenAI:** API-Key eintragen und eine Stimme wählen, zum Beispiel `onyx` oder `echo`.

Beide Dienste sind kostenpflichtig oder haben ein begrenztes Gratis-Kontingent. Klappt die Cloud-Stimme nicht, nimmt Jarvis automatisch die Browser-Stimme.

## Mikrofon

Beim Start fragt die Seite einmal nach dem Mikrofon. Der Pegel links zeigt live, dass es ankommt, und der Kern reagiert auf deine Stimme. Bei „gesperrt“ klickst du in der Adressleiste auf das Schloss-Symbol und erlaubst das Mikrofon.
