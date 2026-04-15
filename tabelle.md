# Tabella: dipartimenti

| Nome colonna        | Tipo di Dato | Attributi                       |
| ------------------- | ------------ | ------------------------------- |
| id (PK)             | BIGINT       | NOT NULL, UNIQUE, AUTOINCREMENT |
| nome                | VARCHAR(50)  | NOT NULL                        |
| numero_corsi_laurea | VARCHAR(50)  | NOT NULL                        |
| descrizione         | TEXT         | NULL                            |
| indirizzo           | VARCHAR(50)  | NULL                            |
| email               | VARCHAR(50)  | NULL                            |
| numero              | VARCHAR(15)  | NULL                            |
| sito_web            | VARCHAR(50)  | NULL                            |

# Tabella: corsi_di_laurea

| Nome colonna         | Tipo di Dato | Attributi                       |
| -------------------- | ------------ | ------------------------------- |
| id (PK)              | BIGINT       | NOT NULL, UNIQUE, AUTOINCREMENT |
| dipartimento_id (FK) | BIGINT          |                                 |
| nome                 | VARCHAR(50)  | NOT NULL                        |
| numero_corsi         | TINYINT      | NOT NULL                        |
| durata               | TINYINT      | NULL                            |
| sede                 | VARCHAR(50)  | NULL                            |
| lingua               | VARCHAR(20)  | NULL                            |
| sito_web             | VARCHAR(50)  | NULL                            |

# Tabella: corsi

| Nome colonna            | Tipo di Dato | Attributi                       |
| ----------------------- | ------------ | ------------------------------- |
| id (PK)                 | BIGINT       | NOT NULL, UNIQUE, AUTOINCREMENT |
| corso_di_laurea_id (FK) | BIGINT          |                                 |
| nome                    | VARCHAR(50)  | NOT NULL                        |
| codice                  | TINYINT      | NULL                            |
| periodo                 | VARCHAR(20)  | NULL                            |
| cfu                     | TEXT         | NULL                            |
| settore                 | VARCHAR(50)  | NULL                            |

# Tabella: insegnanti

| Nome colonna | Tipo di Dato | Attributi                       |
| ------------ | ------------ | ------------------------------- |
| id (PK)      | BIGINT       | NOT NULL, UNIQUE, AUTOINCREMENT |
| nome         | VARCHAR(50)  | NOT NULL                        |
| cognome      | VARCHAR(50)  | NOT NULL                        |
| email        | VARCHAR(50)  | NULL                            |
| telefono     | VARCHAR(15)  | NULL                            |

# Tabella: esami

| Nome colonna | Tipo di Dato | Attributi                       |
| ------------ | ------------ | ------------------------------- |
| id (PK)      | BIGINT       | NOT NULL, UNIQUE, AUTOINCREMENT |
| data         | DATE         | NOT NULL                        |
| orario       | TIME         | NOT NULL                        |
| aula         | VARCHAR(20)  | NOT NULL                        |
| voto         | TINYINT      | NULL                            |

# Tabella: studenti

| Nome colonna            | Tipo di Dato | Attributi                       |
| ----------------------- | ------------ | ------------------------------- |
| id (PK)                 | BIGINT       | NOT NULL, UNIQUE, AUTOINCREMENT |
| corso_di_laurea_id (FK) | BIGINT          |                                 |
| nome                    | VARCHAR(50)  | NOT NULL                        |
| cognome                 | VARCHAR(50)  | NOT NULL                        |
| matricola               | INT          | NOT NULL                        |
| indirizzo               | VARCHAR(50)  | NULL                            |
| data_di_nascita         | DATE         | NULL                            |
| email                   | VARCHAR(50)  | NULL                            |
| codice_fiscale          | VARCHAR(50)  | NULL                            |
| telefono                | VARCHAR(50)  | NULL                            |
