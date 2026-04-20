# FlashView

**Durch 100.000 Fotos blättern. Schneller als du denken kannst.**

Ein schneller, schlanker Foto-Viewer für Windows — für Fotografen, die riesige Archive durchsehen und sortieren wollen.

> **Webseite & Download → [flashview.net](https://flashview.net)**
>
> Dieses Repo ist ausschließlich der **Issue-Tracker**. Der Quellcode ist (noch) nicht öffentlich.

[English](README.md) · Deutsch

## Was es tut

Einen Ordner mit Tausenden Fotos öffnen. Flüssig durchscrollen. Keeper mit einem Tastendruck bewerten, Ausschuss markieren, auf das Wesentliche herunterfiltern, Bewertungen als Standard-XMP exportieren — direkt lesbar in Lightroom, Bridge, Photo Mechanic oder digiKam.

FlashView ist das schnelle Erstdurchgangs-Tool zwischen Speicherkarte kopieren und Editor öffnen.

## Was es besonders macht

**Gebaut für riesige Ordner.** Virtualisiertes Grid, Streaming-Thumbnails, kein Vor-Indexieren — bleibt auch bei 100.000+ Bildern in einem einzelnen Ordner flüssig.

**Blitzschnell blättern.** Pfeiltasten, Mausrad, Scroll — jede Eingabe zeigt das nächste Bild mit unter 50 ms Latenz, auch bei 45-Megapixel-JPEGs. Das ist das *Flash* im Namen.

**Nativer Windows-Explorer-Workflow.** Rechtsklick auf ein Bild → *Öffnen mit FlashView* → in unter einer Sekunde in der Loupe, mit dem ganzen Ordner bereits geladen. `Strg+C` kopiert das Bild, Pfeiltasten gehen zum nächsten.

## Features

- **XMP-Metadaten, die jedes größere Tool liest.** Sterne, Farbmarken und Pick/Reject-Flags werden als Standard-XMP geschrieben — direkt in die JPEG eingebettet oder als Sidecar neben der RAW. Jedes XMP-fähige Programm liest sie: Lightroom, Bridge, Photo Mechanic, digiKam und alles andere, das XMP spricht.
- **Hunderte auf einmal bewerten.** 200, 1.000 oder mehr Dateien auswählen — `3` drücken, fertig. Sterne, Farbmarken, Pick/Reject — alles mit einem Tastendruck, gleichermaßen für JPEGs und XMP-Sidecars. `Strg+Z` macht den letzten Batch rückgängig.
- **Live filtern.** Nach Sternen (mindestens/genau/höchstens), Farbmarke, Pick, Reject — oder RAW-Dateien ganz ausblenden. Genau auf das herunterfiltern, was gerade beurteilt wird.
- **Sortieren und gruppieren.** Name oder Datum, auf- oder absteigend. Einen Elternordner nach Shoots gruppieren, mit konfigurierbarer Tiefe.
- **Fünf Farbmarken.** Rot (`6`), Gelb (`7`), Grün (`8`), Blau (`9`), Lila (`V`) — als Standard-XMP, lesbar in jeder größeren Software.
- **Keyboard-first.** `←→` navigieren, `0–5` bewerten, `P` Pick, `X` Reject, `U` Flags löschen, `G/L` Grid/Loupe, `F` Vollbild, `I` EXIF, `Entf` Papierkorb, `Strg+Z` rückgängig, `Strg+A` alle auswählen, `Strg+O` Ordner öffnen, `R` rekursiv, `F1` zeigt die vollständige Liste.
- **Hoch und runter durch die Struktur.** Einen Elternordner öffnen und Shoots gruppiert sehen. In einen Unterordner zoomen oder alle rekursiv zusammen durchsehen.
- **Zuletzt geöffnete Ordner.** Schneller Zugriff auf die letzten Roots.
- **Dunkles UI, DE/EN.** Folgt automatisch der Systemsprache.
- **Zoom und Details.** 1:1-Pixelansicht, an Bildschirm anpassen, Pan.
- **EXIF-Panel.** Kamera, Objektiv, Brennweite, Blende, Verschlusszeit, ISO, Datum, Pixelgröße, Fotograf, Copyright — in der Loupe mit `I` einblendbar.

## Unterstützte Formate

- **Bilder:** JPEG (`.jpg`, `.jpeg`, `.jpe`, `.jfif`), PNG
- **RAW** — Best-Effort über eingebettetes Preview-JPEG, keine externe RAW-Engine:
  - Canon CR3, CR2
  - Nikon NEF / NRW
  - Sony ARW / SR2
  - Adobe DNG (Leica M8 fällt auf EXIF zurück)
  - Pentax PEF
  - Olympus ORF (moderne Bodys; alte Kompakte zeigen nur Kamera-Thumbnails)
  - Panasonic RW2

## Was es nicht ist

- Kein Entwicklungstool — keine Belichtung, Beschnitt oder Weißabgleich.
- Noch nicht farb-managed — sRGB wird angenommen.
- Keine Bibliothek und kein Katalog — Ordner sind dein Katalog, kein Import-Schritt.
- Keine Cloud-Synchronisation — rein lokal.

## Wo es einsortiert

Die meisten Foto-Browser versprechen Geschwindigkeit. Die meisten funktionieren bei ein paar hundert Bildern, geraten bei 10.000 ins Hintertreffen und geben bei 100.000 auf. FlashView ist für die zweite Hälfte dieser Kurve gebaut — für die Ordner, die echte Fotografen tatsächlich ansammeln.

Lightroom ist Editor-first; das Bibliotheksmodul ist nicht aufs schnelle Cullen optimiert. Photo Mechanic beherrscht die Größenordnung, liegt aber im Profi-Preissegment. FlashView schließt die Lücke: schnell genug für einen Fünfzigtausend-Bilder-Shoot, schlank genug, um auf jedem deiner Rechner zu laufen.

## Ökosystem

FlashView arbeitet Hand in Hand mit [StarRate](https://github.com/merlin1de/starrate) — einem Nextcloud-Plugin für Gast- und Modellbewertungen. Der Workflow: shooten → FlashView für den eigenen ersten Durchgang → nach Nextcloud hochladen → StarRate sammelt externe Bewertungen → zurück in FlashView siehst du eigene und Gast-Bewertungen konsolidiert, alles in Standard-XMP.

## Feedback

Bug oder Feature-Idee? [Issue öffnen](../../issues/new). Dieses Repo ist nur für Issues — keine Pull Requests, aber Bug Reports, Workflow-Kritik und Screenshots sind sehr willkommen.

## Hintergrund

Entstanden aus dem eigenen Canon-Workflow (20D bis R6 Mk III). Lightroom ist exzellent für die Entwicklung, aber der Schritt *davor* — durch 800 Frames klicken und die Keeper markieren — hat sich immer zäh angefühlt. FlashView macht diesen Schritt schnell.

Wer ähnlich fotografiert, für den ist es vielleicht auch schneller.

---

Dev-Referenz (Build, Env-Vars, Architektur): siehe [`docs/dev-reference.md`](docs/dev-reference.md).

© Mathias Mischler. Beta-Release, „wie besehen", ohne Gewährleistung.
