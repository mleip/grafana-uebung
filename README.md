# Prometheus & Grafana Übung

(basierend auf [shelleg/prom_exercise_01](https://github.com/shelleg/prom_exercise_01))

## Setup

* Bitte Sicherstellen, dass folgende Komponenten auf dem System verfügbar sind:
  *  docker
  *  docker-compose
* Sollte auf dem eigenen System Fehler auftreten, kann auch auf eine Virtuelle Maschine in der Cloud zurück gegeriffen werden
* diese Repository clonen und in das entsprechende Verzeichnis wechseln

## Ausgangssituation

* Mit Hilfe von Docker soll das Grundgerüst gestartet werden:
  ```
  docker-compose up
  ```
* Nach dem Start sind folgende Dienste Erreichbar:
  * Prometheus: http://localhost:9090/
  * Grafana: http://localhost:3000/
    * Login-Benutzer: `admin`
    * Passwort ist der `docker-compose.yml` Datei zu entnehmen
* Im Prometheus sind 4 targets bereits eingerichtet
  * `node` und `prometheus` sind erreichbar und sammeln bereits Daten
  * `containers` und `datasources` sind noch nicht erreichar


## Aufgabenstellung

* Es soll folgender cAdvisor-Exporter from https://github.com/google/cadvisor hinzugefügt werden
* Es soll ein mysql-Container in die `docker-compose.yml` hinzugefügt werden
* Es soll ein MySQL-Exporter für Prometheus hinzugefügt werden
* Alle Targets sind in Prometheus erreichbar (grün) und sammeln Daten
* In Grafana soll Prometheus als Datenquelle hinzugefügt werden
* Es soll ein eigenes Grafana-Dashboard basierend auf Prometheus erstellt werden

## Abgabe

* Ein Fork dieses Repository in den eigenen Account
* Angepasste  `docker-compose.yml` im eigenen Repository committen
* Screenshots ebenfalls im Repository committen, ggf. mit einer eigenen Dokumentation im Markdown-Format ergänzen
* Es soll ein Pull-Request von dem eigenen Fork zu dem Ursprünglichen Repository erstellt werden![d857482c-70ae-465e-a7d5-e4b0027985c1](https://user-images.githubusercontent.com/102225659/208913529-c06baca9-47d9-4d2a-b47d-99df4ea0a089.jpg)
![b0458dd9-dca9-45da-a005-bea21bf4ef2c](https://user-images.githubusercontent.com/102225659/208913561-c82bbf54-fef7-4dce-9471-47bb2b39956b.jpg)
