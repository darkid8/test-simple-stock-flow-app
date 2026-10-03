# Arquitectura del Frontend (React SPA)

Este repositorio contiene la Single Page Application (SPA) para el sistema.

## Estructura de Directorios
```text
src/
├── components/     (Botones, tablas, modales, formularios)
├── pages/          (Login, Dashboard, Productos, Ventas, Reportes)
├── services/       (Cliente HTTP / Fetch para consumir la API)
├── hooks/          (Custom hooks de estado)
└── context/        (AuthContext, Carrito/VentaContext)
```

## Reglas de Interacción
- **Capa de Servicios**: Los componentes de React (presentacionales) no deben hacer llamadas `fetch` o `axios` directamente. Todas las llamadas a la red deben encapsularse dentro del directorio `services/` (ej. `productService.js`).
- **Lógica de Dominio**: El frontend no duplica la complejidad del dominio. Su misión es interactuar fluidamente con la API, mostrando representaciones (DTOs) recibidos desde la aplicación.
