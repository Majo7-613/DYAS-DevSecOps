# Cambios

Formato basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/). Desde la 1.1.0, cada versión se publica con
un tag `vX.Y.Z`. El pipeline de CD publica la imagen `ghcr.io/majo7-613/dyas-devsecops` con las etiquetas `X.Y.Z` y
`sha-<commit>`, y la despliega por su digest.

## [1.1.0] - 2026-10-27

### Agregado

- Regla de arquitectura `dominioNoAccedeARedNiBaseDeDatos`: el dominio no puede usar `java.net` ni `java.sql`
  (resultado del ejercicio 7, PR #9 y #10).
- `integrantes.txt`, badges de CI y CD y enlace al Wiki en el README.

## [1.0.0] - 2026-10-18

Versión base del taller (sin tag). Se publicó en GHCR como `1.0.0` y `sha-788439c` con el primer push a este
repositorio, el 2026-10-27.

### Agregado

- Servicio de reservas de salas con arquitectura hexagonal, Spring Boot 4.1 y PostgreSQL.
- Pipeline de CI con build, pruebas, cobertura, ArchUnit, CodeQL, Trivy y Gitleaks.
- Pipeline de CD con publicación en GHCR, SBOM, firma con cosign, despliegue en el runner autohospedado,
  prueba de humo, SLO con k6 y reversión.
