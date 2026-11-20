<p align="center">
  <b>Español</b> | <a href="CONTRIBUTING.en.md">English</a>
</p>

# Guía de contribución

Normas de trabajo del repositorio: ramas, commits y Pull Requests. Las hacen cumplir los rulesets de GitHub y las acciones de GitHub Actions.

## Ramas

| Rama | Uso |
|---|---|
| `main` | Entrega final. Está bloqueada y no se toca hasta la entrega. |
| `develop` | Integración. Es la rama por defecto y solo cambia mediante Pull Request. |
| `feature/pablo` | Rama de trabajo de Pablo. |
| `feature/alvaro` | Rama de trabajo de Álvaro. |

Cada persona trabaja únicamente en su rama `feature`. Esas ramas no se borran ni se reescriben: no hay force push.

## Flujo de trabajo

1. Actualiza tu rama con los últimos cambios de `develop`.
2. Haz commits pequeños en tu rama y súbelos.
3. Abre una Pull Request de tu rama a `develop` y rellena la plantilla (Summary, Changes y Notes).
4. Asígnate la PR y comprueba que **Validate commits** y **Validate PR title** están en verde.
5. El propietario del repositorio mergea con **Create a merge commit**.
6. Al terminar el trabajo, una única PR de `develop` a `main`.

## Commits y títulos de PR

Se usa [Conventional Commits](https://www.conventionalcommits.org/) en inglés: `tipo(ámbito): descripción en imperativo`. El ámbito es opcional.

| Tipo | Uso |
|---|---|
| `feat` | Nueva funcionalidad |
| `fix` | Corrección de un error |
| `docs` | Documentación |
| `style` | Formato, sin cambio de lógica |
| `refactor` | Reestructurar sin cambiar el comportamiento |
| `test` | Pruebas |
| `chore` | Configuración y mantenimiento |
| `ci` | Automatizaciones (GitHub Actions) |

Ejemplos: `feat(expenses): add receipt upload`, `docs(readme): update branding paths`.

Un propósito por commit y por PR.

## Comprobación automática

Dos acciones de GitHub Actions revisan las Pull Requests:

| Acción | Job | Qué comprueba |
|---|---|---|
| **Commit messages** | `Validate commits` | Que todos los commits de la PR sigan Conventional Commits. Solo en PRs hacia `develop`. |
| **PR title** | `Validate PR title` | Que el título de la PR siga Conventional Commits. |

De dónde sale cada PR (solo desde `feature/pablo` o `feature/alvaro` hacia `develop`, y solo desde `develop` hacia `main`) es una norma del equipo: no la comprueba ninguna acción.

## Estilo de archivos

`.editorconfig` define la codificación, la indentación y el salto de línea final. Todos los archivos terminan con una línea vacía.
