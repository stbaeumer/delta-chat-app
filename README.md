# delta-chat-app

## Automatisches Release

Beim Push auf den Branch `main` erstellt GitHub Actions automatisch ein Release:

- Der Ordner `delta-chat-app` wird als `.xdc` gepackt.
- Das Paket wird mit folgendem Befehl erzeugt:

	`(cd delta-chat-app && zip -9 --recurse-paths - *) > delta-chat-app-<version>.xdc`

- Die Version wird automatisch hochgezählt (Minor), beginnend bei `1.0.0`.

Die Workflow-Datei liegt unter `.github/workflows/release.yml`.