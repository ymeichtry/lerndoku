---
id: 1
title: Mobile App mit Flutter
description: Wie erstelle ich eine Mobile App mit Flutter
---

import Image from '@theme/IdealImage';

<Image
img={require('@site/static/img/Flutter_Logo.png')}
alt="Apache Maven Logo"
style={{ width: "100%", borderRadius: "12px" }}
/>

# Mobile App mit Flutter

## Einleitung

### Warum Flutter?

Flutter ist ein Open-Source-Toolkit von Google, mit dem man Apps für **Android**, **iOS**, **Web** und **Desktop** mit nur einer Codebasis schreiben kann. Die Programmiersprache dahinter heisst **Dart**. Flutter bringt eine eigene Rendering-Engine mit, wodurch es nicht auf die nativen UI-Elemente der Plattformen angewiesen ist.

Mit Flutter kann man moderne und gut aussehende Benutzeroberflächen schnell und einfach bauen – egal ob für kleinere Apps oder grössere Projekte.

### Was kann ich mit Flutter machen?

mit Flutter kann man Apps entwickeln für:

- Android
- iOS
- Windows
- macOS
- Linux
- Webbrowser

## Flutter Aufsetzen

In dieser Anleitung zeigen wir dir, wie du dein erstes Flutter-Projekt aufsetzt.

### 1. Flutter und Dart installieren

Zuerst musst du Flutter und Dart auf deinem Computer installieren.

#### Flutter installieren

1. Lade das Flutter SDK von der offiziellen Webseite herunter:

   - [Flutter SDK herunterladen](https://flutter.dev/docs/get-started/install)

2. Entpacke das heruntergeladene ZIP-Archiv an einen Ort deiner Wahl (z. B. `C:\src\flutter` auf Windows oder `/home/username/flutter` auf Linux/Mac).

3. Füge den Flutter-Befehl zu deinem System-Pfad hinzu:
   - **Windows**: Öffne die Umgebungsvariablen und füge den `flutter/bin`-Ordner zum PATH hinzu.
   - **macOS/Linux**: Füge folgende Zeile in deine `.bashrc` oder `.zshrc` ein:
     ```bash
     export PATH="$PATH:`<path-to-flutter-directory>/flutter/bin"
     ```

#### Dart installieren

Dart ist bereits im Flutter SDK enthalten, daher musst du Dart nicht separat installieren.

### 2. Überprüfen der Installation

Öffne ein Terminal (oder die Eingabeaufforderung) und gebe folgenden Befehl ein:

```bash
flutter doctor
```

Dieser Befehl prüft, ob alle Tools und Abhängigkeiten die Flutter benötigt installiert sind. Falls etwas fehlt wird es dir direkt in der Konsole angezeigt.

### 3. Entwicklerumgebung einrichten

Um eine Mobile App mit Flutter zu entwickeln empfehlen sich folgende Entwicklerumgebungen (IDE's):

#### Visual Studio Code (VS Code) installieren

1. Lade VS Code von der offiziellen Webseite herunter: (https://code.visualstudio.com/)
2. Installiere das Flutter-Plugin
   - Öffne VS Code un gehe zu `Erweiterungen`/`Extensions'`.
   - Suche nach "Flutter" und installiere das Plugin.
   - Das Dart-Plugin wird automatisch mitinstalliert.

#### Android Studio (optional)

Falls man auch Android-Emlulatoren (Smartphones zum Testen auf dem Desktop) nutzen möchte, kann man Android Studio installieren:

1. Lade Android Studio von der offiziellen Webseite herunter: (https://developer.android.com/studio)
2. Folge den Anweisunge, um die Android SDK und Emulatoren zu installieren.

### 4. Ein neues Flutter-Project erstellen

1. Öffne dein Terminal oder VS Code
2. gehe zu dem Verzeichnis, in dem du dein Flutter Projekt erstellen und speichern möchtest.
3. Erstelle ein neues Flutter-Projekt mit dem folgendem Befehl:

```bash
flutter create mein_erstes_projekt
```

4. Gehe in das Verzeichnis des Projektes:

```bash
cd mein_erstes_projekt
```

5. Starte die App auf einem Emulator oder Gerät:

```bash
flutter run
```

### 5. Erste Changes machen

1. Öffne die `lib/main.dart` -Datei in deinem Projekt.
2. Ändere den Code, um deine ersten Flutter Funktionen zu erstellen
   - Zum Beispiel:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Mein erstes Flutter-Projekt'),
        ),
        body: Center(
          child: Text('Hallo Welt!'),
        ),
      ),
    );
  }
}
```

3. Speichere die Datei und sieh dir deine Änderungen im Emulator oder eine physischen Gerät an.
   Um einen Hotreaload vom Flutter-Projekt durchzuführen tippe ein `r` in die Konsole

## Projektstruktur verstehen

### Wichtige Verzeichnisse

- **`lib/`**  
  → Hauptverzeichnis für deinen Dart-Code. Hier liegt die `main.dart`, der Einstiegspunkt deiner App.  
  Du wirst später eigene Dateien und Ordner hinzufügen wie `screens/`, `widgets/`, `models/` etc.

- **`android/`**  
  → Native Android-spezifische Konfiguration. Nur nötig, wenn du z. B. Android-spezifische Berechtigungen, Icons oder Build-Settings anpassen willst.

- **`ios/`**  
  → Native iOS-spezifische Konfiguration. Analog zu `android/` – wichtig für Xcode-Projekteinstellungen, App Icons oder Signaturen.

- **`test/`**  
  → Für Unit-, Widget- und Integrationstests. Hier kannst du automatisierte Tests schreiben.

- **`build/`**  
  → Automatisch generierter Ordner beim Kompilieren. Enthält Build-Artefakte – **nicht bearbeiten**.

- **`web/`** _(optional)_  
  → Nur wenn du Web-Support aktiviert hast. Enthält HTML/CSS-Dateien und Web-spezifische Konfiguration.

### Wichtige Dateien

- **`main.dart`**  
  → Einstiegspunkt der App. `void main() { runApp(MyApp()); }` startet die App.

- **`pubspec.yaml`**  
  → Zentrale Datei für Abhängigkeiten, Assets (Bilder, Fonts), Versionsnummer etc.  
  Beispiel:
  ```yaml
  dependencies:
    flutter:
      sdk: flutter
    http: ^0.14.0
  ```
- **`pubspec.lock`**
  → Wird automatisch erstellt, speichert genaue Versionen der Abhängigkeiten. Nicht manuell bearbeiten.

- **`.gitignore`**
  → Definiert, welche Dateien bei der Verwendung von Git ignoriert werden (z. B. build/, .dart_tool/).

- **`README.md`**
  → Dokumentation für dein Projekt. Hier kannst du eine Beschreibung, Screenshots, Installationsanleitung usw. einfügen.

## Mehr Informationen

- [Flutter Docs](https://docs.flutter.dev/)
- [Flutter YouTube Channel](https://www.youtube.com/@flutterdev)
