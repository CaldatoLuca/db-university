# DB University

Modellizzare la struttura delle entità di un database per memorizzare tutti i dati riguardanti una università:

- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
  ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni Corso può essere tenuto da diversi Insegnanti;
- ogni Corso prevede più appelli d’Esame;
- ogni Studente è iscritto ad un solo Corso di Laurea;
- ogni Studente può iscriversi a più appelli di Esame;
- per ogni appello d’Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.

Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni.
Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

## Tipi di Relazioni

### Dipartimenti -> Corsi di Laurea

Relazione di tipo 'one to many'

Un Dipartimento avrà più Corsi di Laura ma un Corso di Laurea non avrà più Dipartmenti

### Corsi di Laurea -> Corsi

Relazione di tipo 'many to many'

Un Corso di Laurea avrà più Corsi e un Corso può esserci in più Corsi di Laurea

### Corsi -> Insegnanti

Relazione di tipo 'many to many'

La foto fa riferimenti al lavoro finale del gruppo di lavoro (in cui, erroneamente, è stata usata una relazione 'one to many')

Un Corso può avere più Insegnanti e un Insegnante può insegnare in più Corsi

### Corsi -> Appelli di Esame

Relazione di tipo 'one to many'

Un Corso può avere più Appelli ma un Appello non può essere di più Corsi

### Corsi di Laurea -> Studenti

Relazione di tipo 'one to many'

Un Corso di Laurea avrà molti studenti ma uno Studente non può iscriversi a più Corsi di Laurea

### Studenti -> Appelli di Esame

Relazione di tipo 'many to many'

Uno studente può fare più Appelli e un Appello può avere più studenti

La proprietà voti viene aggiunta alla 'tabella ponte' perchè ogni Studente ha un voto per ogni Appello
