# Currency Conversion API

Proyecto de aprendizaje: desarrollo seguro con IA — IES Rafael Alberti

Una API REST simple para conversión de divisas, construida con prácticas seguras y generación de código asistida por IA.

## Instalación

```bash
npm install
```

## Uso

### Iniciar servidor
```bash
npm start
```

El servidor correrá en `http://localhost:3000`

### Endpoint

**GET** `/api/convert?from=USD&to=EUR`

Request:
```
/api/convert?from=USD&to=EUR
```

Response (éxito):
```json
{
  "success": true,
  "data": {
    "from": "USD",
    "to": "EUR",
    "rate": 0.9
  },
  "error": null
}
```

Response (error):
```json
{
  "success": false,
  "data": null,
  "error": "'from' parameter is required"
}
```

## Tests

```bash
npm test
```

Ejecuta **15 tests** que cubren:
- ✓ Happy path (conversiones válidas)
- ✓ Parámetros faltantes
- ✓ Inputs vacíos/nulos
- ✓ Divisas no soportadas
- ✓ Edge cases

## Cómo se usó la IA

- **Handler generado por**: ChatGPT (Claude también soportado)
- **Validación**: Cada línea fue revisada manualmente
- **Tests expandidos**: Se añadieron casos de error más allá del happy path
- **Seguridad**: Revisados con checklist RULES.md

Ver [RULES.md](RULES.md) para la política completa de código generado con IA.

## Estructura del proyecto

```
src/
  ├── api/
  │   └── handler.js          # Endpoint /convert
  ├── models/                  # (Próximamente)
  ├── middleware/              # (Próximamente)
  └── utils/                   # (Próximamente)

tests/
  ├── unit/
  │   └── handler.test.js      # Tests del handler
  └── integration/             # (Próximamente)

docs/                           # (Próximamente)
```

## Autor

Victor Manuel Romero

## Licencia

MIT
