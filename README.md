# SofTron

Proyecto de software (por definir en la próxima sesión de desarrollo).

## Estructura de ramas (Gitflow con entornos)

Este repositorio sigue el patrón **Gitflow** extendido con ramas de entorno:

| Rama | Rol | Quién trabaja |
|------|-----|----------------|
| `main` | Producción. Solo código estable ya liberado. | Nadie directamente (solo merges de release). |
| `develop` | Rama de integración estable. Base de las `feature/*`. | Desarrolladores / agentes ruflo. |
| `demo` | Validación de QA sobre lo integrado en `develop`. | Testers. |
| `uat` | Pruebas manuales de aceptación previas a producción. | Validación manual antes de `main`. |

### Flujo de trabajo

```
feature/*  ->  develop  ->  demo  ->  uat  ->  main
```

- Las nuevas funcionalidades se desarrollan en ramas `feature/*` y se integran en `develop`.
- `develop` se promociona a `demo` para pruebas de QA.
- Lo validado pasa a `uat` para la prueba manual de aceptación.
- Solo lo aprobado en `uat` se fusiona en `main` (release a producción).
- Las correcciones urgentes de producción usan ramas `hotfix/*` desde `main`.
