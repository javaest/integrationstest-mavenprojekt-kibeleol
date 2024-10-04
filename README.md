[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Frr2_-wj)
## Maven

Ein Maven-Projekt ist ein Software-Projekt, das mit Apache Maven verwaltet wird, einem populären Build-Management-Tool für Java-basierte Projekte. Maven erleichtert den Prozess der Projektverwaltung, indem es standardisierte Projektstrukturen, Abhängigkeitsmanagement und Automatisierung von Build- und Deploy-Prozessen bietet.

### Hauptmerkmale von Maven-Projekten

1. **Standardisierte Projektstruktur**:
   Maven definiert eine standardisierte Verzeichnisstruktur für Projekte, was es einfacher macht, neue Projekte zu starten und bestehende Projekte zu verstehen.

   Typische Verzeichnisstruktur:

2. **Projekt-Objektmodell (POM)**:
Das Herzstück eines Maven-Projekts ist die `pom.xml`-Datei (Project Object Model). Diese XML-Datei enthält Metadaten über das Projekt und Konfigurationsdetails für Maven.
### Abhängigkeitsmanagement

Maven verwaltet Abhängigkeiten (Dependencies) automatisch. Wenn eine Bibliothek benötigt wird, wird sie in der `pom.xml` definiert, und Maven lädt sie automatisch aus einem zentralen Repository herunter.

### Build-Lifecycle

Maven folgt einem definierten Build-Lifecycle, der aus Phasen wie `validate`, `compile`, `test`, `package`, `verify`, `install` und `deploy` besteht. Diese Phasen ermöglichen eine konsistente und wiederholbare Build-Prozedur.

Beispiel-Befehle:
- `mvn compile`: Kompiliert den Quellcode des Projekts.
- `mvn test`: Führt die Unit-Tests aus.
- `mvn package`: Erstellt eine ausführbare JAR- oder WAR-Datei.
- `mvn install`: Installiert das Paket in das lokale Repository.
- `mvn deploy`: Kopiert das endgültige Paket in ein entferntes Repository.

### Plugins

Maven bietet eine Vielzahl von Plugins, die verschiedene Aufgaben während des Build-Prozesses übernehmen können, wie z.B. Code-Analyse, Dokumentationserstellung, Testausführung und vieles mehr.

### Vorteile von Maven

- **Automatisierung**: Maven automatisiert viele Aspekte des Build- und Release-Prozesses.
- **Wiederverwendbarkeit**: Einmal definierte Abhängigkeiten und Build-Prozesse können in mehreren Projekten wiederverwendet werden.
- **Integration**: Maven integriert sich gut mit anderen Tools und CI/CD-Systemen.
- **Konsistenz**: Durch die Standardisierung der Projektstruktur und des Build-Prozesses bietet Maven eine konsistente Arbeitsweise.

Maven ist ein weit verbreitetes Werkzeug in der Java-Entwicklergemeinschaft und bietet zahlreiche Vorteile für die Verwaltung und den Build von Softwareprojekten.

### Integration Tests

**Definition:** 
Integration Tests überprüfen die Zusammenarbeit mehrerer Komponenten eines Systems. Im Gegensatz zu Unit-Tests, die isoliert einzelne Funktionen testen, konzentrieren sich Integrationstests auf die korrekte Interaktion und Integration der verschiedenen Teile des Systems.

**Ziel:**
Das Ziel von Integrationstests ist es, sicherzustellen, dass die verschiedenen Module oder Komponenten eines Systems ordnungsgemäß zusammenarbeiten. Sie decken Fehler auf, die durch die Interaktion zwischen Modulen entstehen könnten.

### Einsatz von Mocks in Integration Tests

**Definition:**
Mocks sind simulierte Objekte, die das Verhalten echter Objekte nachahmen. Sie werden verwendet, um die Abhängigkeiten des zu testenden Codes zu ersetzen, sodass der Test unabhängig und kontrollierbar bleibt.

**Ziel:**
Der Einsatz von Mocks in Integrationstests kann sinnvoll sein, wenn bestimmte Abhängigkeiten schwer zu steuern sind oder externe Systeme involviert sind, wie z.B. Datenbanken, Webservices oder externe APIs. Mocks helfen dabei, Tests schneller, zuverlässiger und reproduzierbarer zu machen.

**Einsatzmöglichkeiten:**

1. **Isolation von Testfällen:**
   - Wenn man eine bestimmte Komponente testet, kann man ihre Abhängigkeiten durch Mocks ersetzen, um den Test isoliert und fokussiert zu halten.
   
2. **Vermeidung externer Abhängigkeiten:**
   - Durch das Mocken von externen Systemen (z.B. Datenbanken, Webservices) kann man sicherstellen, dass der Test unabhängig von der Verfügbarkeit und dem Zustand dieser Systeme ist.

3. **Kontrolle über das Verhalten von Abhängigkeiten:**
   - Man kann das Verhalten von Abhängigkeiten präzise steuern, um bestimmte Szenarien und Randfälle zu testen.


## Aufgabe: Integrationstest für OrderService und PaymentService

Ein E-Commerce-System hat zwei Hauptkomponenten:
- OrderService: Verantwortlich für die Verwaltung von Bestellungen.
- PaymentService: Verantwortlich für die Abwicklung von Zahlungen.

Wenn eine Bestellung aufgegeben wird, muss der OrderService den PaymentService aufrufen, um die Zahlung zu verarbeiten.

#### Erklärung:

Mockito einrichten: Die Annotationen @Mock und @InjectMocks werden verwendet, um Mock-Objekte zu erstellen und diese in die zu testende Klasse (OrderService) zu injizieren.
1. Tests schreiben: Test für erfolgreichen Zahlungsvorgang: Simuliert einen erfolgreichen Zahlungsvorgang und überprüft, ob die Bestellung erfolgreich abgeschlossen wird.
2. Test für fehlgeschlagenen Zahlungsvorgang: Soll einen fehlgeschlagenen Zahlungsvorgang simulieren und überprüft, ob die Bestellung nicht abgeschlossen wird.

#### Ihre Aufgabe:
1. Binden Sie das Maven projekt in Ihrer IDE ein.
2. Implementieren Sie den 2. Test
