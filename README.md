# Student Enrollment System — Java + JDBC

A desktop CRUD application for managing student enrollments at a university, built with Java Swing and raw JDBC connecting to a MySQL database.

---

## Features

- **Register** students with full personal and medical data
- **Search** students by name or ID
- **Update** existing enrollment records
- **Remove** students from the system

**Fields per enrollment:**
- Full name, address, phone number
- Emergency contact name and phone
- Blood type and Rh factor

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java |
| UI | Swing (`JFrame`, buttons, text fields, combo boxes) |
| Database | MySQL |
| Data access | JDBC (`Connection`, `PreparedStatement`, `ResultSet`) |
| Schema | MySQL Workbench (`.mwb` included) |

---

## Architecture

```
InterfaceGrafica.java       → Swing UI, event handling (Insert/Remove/Update/Search)
Matricula.java              → Data model holding enrollment fields
ConexaoBancoDeDados.java    → JDBC layer: connection management + SQL execution
Principal.java              → Entry point, initializes the window
```

Flow: user fills form → `Matricula` object is populated → `ConexaoBancoDeDados` executes the SQL → result is displayed in the UI.

---

## Running Locally

**Requirements:** Java 8+, MySQL

```bash
git clone https://github.com/cherohn/AppointmentSystem-Java-JDBC.git
```

1. Import `matricula.mwb` into MySQL Workbench to create the schema
2. Update DB credentials in `ConexaoBancoDeDados.java`:
```java
// default: localhost:3306/matricula, user: root
```
3. Compile and run `Principal.java`

---

## Author

**Matheus Garcez** — [github.com/cherohn](https://github.com/cherohn)
