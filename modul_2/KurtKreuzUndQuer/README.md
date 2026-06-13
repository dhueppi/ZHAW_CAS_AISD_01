# LaTeX-Projekt

Dieses Verzeichnis enth\"alt ein minimales LaTeX-Grundger\"ust.

## Struktur

- `main.tex`: Einstiegspunkt des Dokuments
- `sections/`: Inhalt in getrennten Dateien
- `latexmkrc`: Standardkonfiguration f\"ur lokale Builds
- `.vscode/`: VS-Code-Einstellungen und Tasks

## Build

Mit installiertem `latexmk`:

```sh
latexmk -pdf main.tex
```

Mit `pdflatex` als einfachem Fallback:

```sh
pdflatex -interaction=nonstopmode main.tex
```

In VS Code kannst du den Task `Build LaTeX` ausf\"uhren.

## macOS TeX-Installation

Aktuell ist lokal kein TeX-Compiler vorhanden. Auf macOS ist ein schlanker Start mit Homebrew und BasicTeX meist ausreichend:

```sh
brew install --cask basictex
sudo tlmgr update --self
sudo tlmgr install latexmk collection-latexrecommended collection-fontsrecommended
```

Danach sollte der VS-Code-Task `Build LaTeX` ohne weitere Anpassungen funktionieren.