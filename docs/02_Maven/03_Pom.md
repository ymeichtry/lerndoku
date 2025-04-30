---
id: 3
title: pom.xml
description: How to pom
---

# pom.xml

## Was ist ein pom?

Die Datei `pom.xml` (Project Object Model) ist das Steuerelement eines Maven Projekts. Es beschreibt das Projekt, seine Abhängigkeiten, Plugins und mehr.

## Grundstruktur vom `pom.xml`

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
         http://maven.apache.org/xsd/maven-4.0.0.xsd">

  <modelVersion>4.0.0</modelVersion>

  <groupId>com.beispiel</groupId>
  <artifactId>meine-app</artifactId>
  <version>1.0.0</version>
  <packaging>jar</packaging>

  <name>Meine App</name>
  <description>Ein Beispielprojekt mit Maven</description>

  <dependencies>
    <!-- hier kämen Abhängigkeiten hin -->
  </dependencies>

  <build>
    <plugins>
      <!-- hier kämen Plugins hin -->
    </plugins>
  </build>

</project>
```
