-- Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
SELECT students.id, students.name, students.surname, degrees.name
FROM students
JOIN degrees ON degrees.id = students.degree_id
WHERE degrees.name = "Corso di Laurea in Economia";


-- Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
SELECT departments.name AS dipartimento, degrees.name AS nome_corso
FROM departments
JOIN degrees ON departments.id = degrees.department_id
WHERE departments.name = 'Dipartimento di Neuroscienze'
AND degrees.level = 'magistrale';


-- Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
SELECT teachers.id, teachers.name, courses.name, courses.period, courses.year 
FROM courses
JOIN course_teacher ON course_teacher.course_id = courses.id
JOIN teachers ON teacher_id = course_teacher.teacher_id
WHERE teachers.id = 44;


-- Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome
SELECT students.*, degrees.id, degrees.name, departments.id, departments.name
FROM students
JOIN degrees ON degrees.id = students.degree_id
JOIN departments ON departments.id = degrees.department_id
ORDER BY students.surname ASC, students.name ASC;