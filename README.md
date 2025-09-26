# ICS TP1 – Spring Boot

---

## Descripción
Este proyecto es un ejemplo desarrollado con **Spring Boot** como parte de las prácticas de Git y GitFlow en la cátedra de Ingeniería y calidad de Software.

Incluye la implementación de funcionalidades de ejemplo, manejo de versiones con **GitFlow**, commits semánticos, manejo de **releases** y **hotfixes**.

---

## Documentación con Git

### ¿Cómo podemos documentar con Git?

Git permite llevar un **historial completo y versionado** de nuestro código y documentación, incluyendo:

- **README.md**: explica el propósito del proyecto, cómo ejecutarlo, dependencias, autores y cualquier información relevante.  
- **CHANGELOG.md**: detalla los cambios por versión, siguiendo la convención [Keep a Changelog](https://keepachangelog.com/es-ES/).  
- **Commits semánticos**: cada commit debe seguir la convención [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary).  
- **Tags de versiones**: marcan puntos de release estables en el historial.  
- **Branching**: GitFlow permite mantener ramas separadas de desarrollo, features, releases y hotfixes para que la documentación siempre refleje el estado correcto del proyecto.  
- **Versionado Semántico (SemVer)**: asegura que cada versión esté etiquetada y documentada correctamente.  

> **Respuesta a la consigna 3.a:**  
> Documentaríamos en el README toda la información necesaria para entender y ejecutar el proyecto, y lo versionamos usando Git para que cualquier cambio quede registrado en el historial de commits y pueda ser revisado o revertido si es necesario.

---

### Pull Requests y contribuciones externas

> **Respuesta a la consigna 3.b:**  
> Si un externo realiza una modificación, para entender claramente el cambio necesitamos que esta persona abra un **Pull Request (PR)** y complete la información necesaria:
> 
> **Datos que se le pediría incluir:**
> - Rama de origen de la modificación.
> - Descripción detallada del cambio.
> - Motivo o issue relacionado.
> - Capturas o ejemplos si aplica.
> - Checklist de pruebas realizadas.
> 
> **Qué nos ofrece GitHub:**
> -  Visualización de todos los cambios línea por línea (diff) antes de hacer merge.
> -  Comentarios y revisión de código en línea.
> -  Verificación de estado de CI/CD si está configurado.
> -  Posibilidad de aprobar o solicitar cambios antes de integrar a `develop` o `main`.
> -  Historial completo de merges y autoría, para rastrear quién hizo qué cambio y cuándo.
> De esta manera, el equipo puede **revisar, discutir y aprobar los cambios** de forma segura, manteniendo la calidad del código y un historial limpio y documentado.

---

## Contenido del proyecto
- `src/main/java/`: código fuente Java del proyecto.  
- `src/main/resources/`: recursos de la aplicación (configuración, plantillas, etc.).  
- `CHANGELOG.md`: historial de cambios y versiones.  
- `CONTRIBUTING.md`: guía para contribuir al proyecto, incluyendo reglas.
- `README.md`: documentación del proyecto y guía de uso.  

---

## Ejecución
1. Clonar el repositorio:
```bash
git clone git@github.com:aguilarivan/ICS-TP1.git
cd TP1-ICS
````

2. Ejecutar con Maven:

```bash
./mvnw spring-boot:run
```

3. Acceder a la aplicación en `http://localhost:8080/`.


## Autores

* Aguilar Iván – [aguilarivanx@gmail.com](mailto:aguilarivanx@gmail.com)
* Rivero Lautaro – [lautiprivero@gmail.com](mailto:lautiprivero@gmail.com)
* Tessini Valentín – [valentin-tessini@hotmail.com](mailto:valentin-tessini@hotmail.com)
* Wangher Santiago – [santiago.wangher@gmail.com](mailto:santiago.wangher@gmail.com)


## Licencia

Este proyecto se encuentra bajo licencia libre para fines educativos.
