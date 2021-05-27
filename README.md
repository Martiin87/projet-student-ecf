# ECF projet-student

Prérequis:
PhPMyAdmin

- Tout d'abord créer l'utilisateur de la BDD
- Créer la BDD
- Créer la structure de la BDD :
### user
- id : clé primaire
- email : varchar 190, unique
- roles : text
- password : varchar 190
- firstname : varchar 190
- lastname : varchar 190
- phone : varchar 20, nullable
- school_year_id : clé étrangère qui pointe vers school_year.id

### school_year

- id : clé primaire
- name : varchar 190
- date_start : datetime, nullable
- date_end : datetime, nullable

### project

- id : clé primaire
- name : varchar 190
- description : text, nullable

### project_user

- project_id : clé étrangère qui pointe vers project.id
- user_id : clé étrangère qui pointe vers user.id


- Injecter les données indispensables :

| id | email               | roles          | password                                                     | firstname | lastname | phone | school_year_id |
|----|---------------------|----------------|--------------------------------------------------------------|-----------|----------|-------|----------------|
| 1  | foo.foo@example.com | ["ROLE_ADMIN"] | $2y$10$/H2ChUxriH.0Q33g3EUEx.S2s4j/rGJH2G88jK9nCP60GbUW8mi5K | Foo       | Foo      | NULL  | NULL           |

- Injecter les données de test:

- 60 user ayant le rôle `ROLE_STUDENT`
- 5 user ayant le rôle `ROLE_TEACHER`
- 15 user ayant le rôle `ROLE_CLIENT`

- 3 school years dont les données sont générées aléatoirement

- 20 projets dont les données sont générées aléatoirement

 
