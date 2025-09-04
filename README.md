# TrackFit – Nutzerhandbuch

TrackFit ist eine Fullstack-App zur Verwaltung von Workouts und Fitnessdaten.
Hier findest du die Anleitung, wie du das Projekt lokal starten und nutzen kannst.

---

## 📌 Technische Voraussetzungen

Um die App zum Laufen zu bringen, brauchst du:

* eine Entwicklungsumgebung (z. B. IntelliJ IDEA oder VS Code),
* **Docker Desktop** installiert und gestartet,
* eine aktive Internetverbindung.

---

## ⚙️ Installation & Start

### 1. Projekt entpacken

Entpacke die `.zip`-Datei mit dem Quellcode.

### 2. Quellcode öffnen

Öffne den Code in deiner IDE (z. B. IntelliJ).
→ Markiere das Projekt als **Maven-Projekt**, damit die Abhängigkeiten geladen werden.

### 3. Docker starten

Starte Docker Desktop.

### 4. Docker-Images laden

Öffne ein Terminal im Ordner `TrackFit` und führe diese Befehle aus:

```bash
docker load -i backend.tar
docker load -i frontend.tar
```

Damit werden die vorbereiteten Docker-Images für Backend und Frontend in dein Docker geladen.

### 5. Container hochfahren

Starte alles mit:

```bash
docker compose up
```

Dadurch werden über die `docker-compose.yml`:

* eine **MySQL-Datenbank** (inkl. Mail-Service),
* das **Backend**
* und das **Frontend** gestartet.

### 6. Läuft alles?

Check, ob alle drei Container laufen:

* `backend`
* `frontend`
* `mysql:5.7`

Das geht entweder in Docker Desktop oder mit:

```bash
docker ps
```

Falls ein Container gestoppt wurde, kannst du ihn manuell starten:

```bash
docker start <container_id>
```

Hinweis: Beim ersten Start kann es sein, dass etwas stoppt. Ab dem zweiten Mal läuft es meistens stabil.

### 7. App nutzen

* **Frontend**: im Browser erreichbar ([http://localhost:8081](http://localhost:8081) oder [http://localhost:4200](http://localhost:4200), je nach Setup).
* **Backend**: läuft auf [http://localhost:8080](http://localhost:8080).
* **Datenbank**: MySQL 5.7 auf Port 3306.

---

## ⚠️ Wichtiger Hinweis

* Die Datenbank startet leer.
* Es werden keine Daten automatisch eingespielt.
* Wenn du Beispieldaten brauchst, musst du sie per SQL-Skripte oder über die API hinzufügen.

---

## 📸 Screenshots

## Login mit auth
![1](https://github.com/user-attachments/assets/49f79dcc-04c8-45de-ba45-1abaa77aea96)

## Profilseite
![4](https://github.com/user-attachments/assets/96d04253-11e3-48dd-b7be-0abd82579c7e)

## Freunde Hinzufügen
![2](https://github.com/user-attachments/assets/38cc316d-3671-49b1-a7e0-08ff27d314f3)

## Aktivität visualisiert
![5](https://github.com/user-attachments/assets/3fa631f9-5354-4ab8-9c64-8e3ba85f4cc3)



