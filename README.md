# TP4 Backlog – Integración Continua con GitHub Actions (Proyecto Académico)

Trabajo práctico académico desarrollado para la materia **Ingeniería y Calidad de Software**  
(Ingeniería en Sistemas – UTN Facultad Regional Mendoza).

Este repositorio se publica con fines de **portfolio personal**, con el objetivo de mostrar la aplicación práctica de **Integración Continua (CI)**, testing automatizado y buenas prácticas de calidad de software.

---

## Descripción

El proyecto consiste en la implementación de un pipeline de **Integración Continua** utilizando **GitHub Actions** sobre un proyecto Java administrado con **Gradle**.

Cada cambio en el repositorio es validado automáticamente mediante:
- compilación del proyecto,
- ejecución de pruebas unitarias,
- verificación de dependencias.

El objetivo principal es garantizar calidad, estabilidad y detección temprana de errores durante el desarrollo.

---

## Estructura del proyecto

El sistema incluye dos clases principales utilizadas como base para el testing.

### Usuario
Implementa lógica relacionada a:
- validación de email,
- validación de nombre (formato correcto),
- comportamiento de usuario premium,
- métodos de acceso (getters y setters).

### Pato
Simula comportamientos y propiedades:
- acciones (`walk`, `swim`, `fly`),
- región,
- tamaño válido,
- migración,
- formato de nombre para ficha descriptiva.

---

## Pruebas unitarias

Se desarrollaron pruebas unitarias para validar el correcto funcionamiento del sistema.

### Tests de Usuario
- Validación de usuario premium.
- Validación básica de email.
- Validación de formato de nombre.
- Verificación de setters y getters.

### Tests de Pato
- Validación de métodos de comportamiento.
- Comprobación de región y migración.
- Control de tamaño dentro de rangos válidos.
- Verificación de formato de nombre.
- Setters y getters.

Las pruebas aseguran que los cambios no rompan funcionalidades existentes.

---

## Integración Continua con GitHub Actions

Se configuró un workflow de CI en `.github/workflows/ci.yml` que:

- Se ejecuta automáticamente en cada push y pull request.
- Configura JDK 17 (Temurin).
- Utiliza Gradle con cacheo para optimizar tiempos de ejecución.
- Ejecuta el comando `./gradlew build`, que compila el proyecto y ejecuta los tests unitarios.
- Publica el grafo de dependencias para alertas de seguridad.

Este proceso garantiza que solo código validado pueda integrarse al proyecto.

---

## Tecnologías utilizadas

- Java  
- Gradle  
- GitHub Actions  
- JUnit  
- Git / GitHub  

---

## Estado del proyecto

Proyecto académico finalizado.  
El foco estuvo puesto en la correcta implementación de:
- testing automatizado,
- Integración Continua,
- buenas prácticas de calidad de software.

---

## Autoría

Trabajo práctico desarrollado en grupo para la materia  
Ingeniería y Calidad de Software  
UTN – Facultad Regional Mendoza
