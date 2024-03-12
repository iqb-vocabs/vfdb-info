[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

Dieses Repo enthält alle Dateien für den Inhalt und die Steuerung der Erzeugung einer statischen Website des [IQB](https://www.iqb.hu-berlin.de):

[VerbundFDB-info](https://iqb-vocabs.github.io/vfdb-info)

# Technische Umsetzung

Es handelt sich hier um statische Webseiten. Die Inhalte (Texte, Bilder usw.) müssen zuerst als Dateien gespeichert werden. Danach wird das Programm [Quarto](https://quarto.org) aufgerufen, das daraus komplexe Html-Dateien erzeugt und auch die Gestaltung über CSS definiert. Nach jeder Änderung am Inhalt ist also ein solcher Übersetzungsprozess anzustoßen.

Die Texte sind in einer einfachen Auszeichnungssprache geschrieben: [Markdown](https://markdown.de/). Nach kurzer Einarbeitung weiß man, wie man z. B. Überschriften, Einrückungen oder Links schreibt.

```md
# Das ist eine Überschrift

Das ist normaler Text der **hier fettgedruckt** ist und einen [Link](https://www.iqb.hu-berlin.de) enthält.
```

Durch Verwendung der Auszeichnungssprache kann man gewährleisten, dass alle Seiten gleich aussehen.

Dieses GitHub-Repository erfüllt folgende Funktionen:

* Speicherung der Texte und Bilder
* Definition der Seitenstruktur in Quarto-Syntax
* Versionierung, so dass vorherige Textversionen nicht verloren gehen
* automatische Erzeugung der statischen Html-Seiten nach Änderungen
* Anzeige der statischen Html-Seiten (Funktion "Pages" von GitHub)
* Entgegennahme von Meldungen durch Nutzer\*innen; hier werden sog. Tickets erzeugt, die den Autor\*innen helfen, Probleme zu vermeiden bzw. zu beheben

# Änderungen vornehmen

## Direkt in GitHub

Kleinere Änderungen kann man nach der Anmeldung direkt in GitHub vornehmen. Dazu klickt man auf den Edit-Schalter einer Textseite und bestätigt die Änderung (sog. Commit). Danach wird automatisch die Erzeugung der Html-Seiten angestoßen und die Änderungen sind nach wenigen Minuten online.

## Extern auf dem eigenen Computer

Bei größeren Änderungen empfiehlt es sich, auf dem eigenen Computer die Texte und Seitenstruktur zu bearbeiten. Dazu ist jeweils folgender Arbeitsablauf erforderlich:

1) Kopieren des gesamten Inhaltes auf den lokalen Computer. Diesen Schritt nennt man "Auschecken des Repos". Es wird das Git-Kommando `pull` verwendet. Auch wenn man bereits eine Kopie des Inhaltes auf dem eigenen Computer hat, ist zu Beginn ein `pull` zu empfehlen, damit die lokalen Dateien auf jeden Fall aktuell sind.
2) Änderungen über einen Texteditor, z. B. Visual Studio Code.
3) Prüfen der Änderungen über die Funktion "Preview".
4) Bestätigen der lokalen Änderungen: Git-Kommando `commit`.
5) Hochladen der Änderungen in das GitHub-Repository: Git-Kommando `push`.

Durch das Hochladen wird automatisch die Erzeugung der Html-Seiten angestoßen und die Änderungen sind nach wenigen Minuten online.

### Quarto installieren

Quarto ist nur für die Funktion "Preview" notwendig, also für das Prüfen der Änderungen. Für Windows kann man sich von der [Quarto-Seite](https://quarto.org/docs/get-started/) ein Installationspaket herunterladen und ausführen. Es sind keine Administrationsrechte auf dem Windows-Computer erforderlich. Nach der Installation muss man keinerlei Konfiguration vornehmen.

### Visual Studio Code installieren

Visual Studio Code ist eine leistungsfähige universelle Software für das Programmieren. Sie ist recht schlank und eignet sich auch sehr gut für das Editieren einfacher Texte. Die Verbindung mit dem Repository bei GitHub ist integriert, es stehen also Menüpunkte für das Auschecken und Hochladen usw. zur Verfügung.

Die Installation erfolgt nach dem [Herunterladen](https://code.visualstudio.com/download).

Nach Bedarf sollte man zunächst die deutsche Sprachvariante aktivieren. Außerdem ist zu empfehlen, die Erweiterung "Quarto" zu installieren. Dann steht bei Änderungen eine Syntaxprüfung zur Verfügung und die Funktion "Preview" ist über einen Schalter erreichbar und muss nicht über ein Kommando aufgerufen werden.

## Zusammenarbeit mehrerer Auto\*innen

Git ist eine leistungsfähige Codeverwaltung. Dazu gehört, dass man Änderungen parallel in einem Versionszweig (sog. "Branch") vornehmen kann und erst später in den Hauptzweig "main" übernimmt (sog. "Merge"). So ist eine Arbeitsweise "vorläufige Änderungen" möglich und man kann vor der Freigabe andere Personen mit einer abschließenden Redaktion beauftragen.

Außerdem wäre es möglich, Textbeiträge von unbekannter Quelle zu erlauben. Eine in GitHub registrierte Person nimmt Änderungen vor und speichert diese als neuen Zweig in das Code-Repo. Dann beantragt diese Person eine Übernahme in den Hauptzweig. Diesen Antrag nennt man bei GitHub "Pull-Request".

# Unterstützung durch IT-Fachkräfte

Die Einrichtung einer Webseite, die auf Quarto basiert, ist nicht trivial. Bevor Autor\*innen arbeitsfähig sind, sollten IT-Spezialist*innen das Repository einrichten und die entsprechenden Automatismen konfigurieren. Eine Einweisung auch in die Markdown-Syntax ist wichtig.

Wenn mehrere Personen über mehrere Versionszweige arbeiten sollen, ist zusätzlich die ständige Verfügbarkeit von erfahrenen IT-Fachkräften erforderlich. Sollten z. B. zwei Personen gleichzeitig lokal an den Inhalten arbeiten, ist vor dem Hochladen manuell ein Abgleich (sog. "Merge") nötig. Diese Funktionen von Git zu verstehen und ausführen zu können, erfordert technische Erfahrung.