
# Guía de Contribución

¡Gracias por tu interés en contribuir a este proyecto! 🎉  
Este documento explica cómo colaborar de manera ordenada siguiendo las buenas prácticas definidas para el equipo.

---

## 📌 Flujo de trabajo (Gitflow)

Este proyecto sigue el modelo [Gitflow](https://nvie.com/posts/a-successful-git-branching-model/).  
Las ramas principales son:

- **main** → contiene la versión en producción, siempre estable.  
- **develop** → rama base para nuevas funcionalidades.  

### Ramas de soporte:
- **feature/** → para nuevas funcionalidades. Se crean desde `develop` y vuelven a `develop`.  
- **release/** → para preparar versiones. Se crean desde `develop` y se mergean en `main` y `develop`.  
- **hotfix/** → para arreglar bugs críticos en producción. Se crean desde `main` y se mergean en `main` y `develop`.

Ejemplo:
```bash
# crear una nueva feature
git checkout develop
git checkout -b feature/login

# ... trabajar en la feature

git checkout develop
git merge feature/login
git branch -d feature/login
````

---

## 📝 Commits (Conventional Commits)

Los mensajes de commit deben seguir la convención [Conventional Commits](https://www.conventionalcommits.org/).
Formato:

```
<tipo>(opcional-scope): <descripción corta>
```

### Tipos más usados:

* **feat:** nueva funcionalidad.
* **fix:** corrección de bug.
* **docs:** cambios en documentación.
* **style:** cambios de formato/código sin afectar la lógica (indentación, espacios).
* **refactor:** cambios internos sin modificar el comportamiento.
* **test:** agregar o modificar pruebas.
* **chore:** tareas de mantenimiento (ej: dependencias, configuración inicial).

Ejemplo:

```bash
feat(auth): agregar login con JWT
fix(api): corregir validación de emails
chore: agregar .gitignore y configuración inicial
```

---

## 📖 Changelog

Este proyecto mantiene un archivo `CHANGELOG.md` siguiendo [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/) y [Semantic Versioning](https://semver.org/lang/es/).

### Reglas:

* Las entradas de cambios se agregan bajo la sección `## [Unreleased]`.
* Cuando se prepara una **release**, esas entradas se mueven a una nueva sección con número de versión y fecha.

Ejemplo:

```markdown
## [Unreleased]
- Nueva API de usuarios

## [1.0.0] - 2025-09-25
- Versión inicial del proyecto
```

---

## 🏷️ Versionado y Tags

* Este proyecto usa **Semantic Versioning (SemVer)**: `MAJOR.MINOR.PATCH`.
* Cada release en `main` debe llevar un **tag** asociado a su commit.

Ejemplo:

```bash
git tag -a v1.2.0 -m "Release 1.2.0"
git push origin v1.2.0
```

---

## ✅ Checklist antes de abrir un Pull Request

* [ ] La rama parte de `develop`.
* [ ] Los commits siguen la convención **Conventional Commits**.
* [ ] El `CHANGELOG.md` fue actualizado en `[Unreleased]`.
* [ ] Se agregaron pruebas si aplica.
* [ ] El código compila y pasa los tests (`mvn clean verify`).

---

¡Gracias por contribuir! 🚀
