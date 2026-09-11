# Conecta Estudiante - Portal de Actividades y Talleres
**Asignatura:** Electivo Angular 22  
**Estudiante:** Kevin Carrasco  

## Descripción del Proyecto
Aplicación SPA desarrollada en Angular para la organización "Conecta Estudiante". Permite revisar actividades y talleres académicos, consultar datos de contacto y registrar solicitudes de inscripción mediante un formulario reactivo con validaciones.

## Instrucciones de Ejecución
1. Clonar el repositorio: `git clone <URL_REPOSITORIO>`
2. Instalar dependencias: `npm install`
3. Ejecutar servidor local: `ng serve`
4. Abrir en el navegador: `http://localhost:4200`

## Registro de Etapas y Commits

### Etapa 1: Estructura inicial
- Creación del proyecto Angular Standalone con routing habilitado.
- Generación de componentes base: Cabecera y Menu en `components/`.
- Generación de componentes de vista: Inicio, Actividades, Contacto e Inscripcion en `pages/`.

### Etapa 2: Navegación SPA y Rutas
- Configuración de `app.routes.ts` para navegación dinámica.
- Uso de `routerLink`, `routerLinkActive` y `<router-outlet>`.
- Creación de vistas `Inicio`, `Actividades` (con interpolación y `@for`), y `Contacto`.

### Etapa 3: Formulario Reactivo y Validaciones
- Implementación de `ReactiveFormsModule`, `FormGroup`, `FormControl` y `Validators`.
- Integración de los 7 campos requeridos con validación en tiempo real.
- Feedback al usuario con mensajes de error dinámicos (`@if`, `touched`, `invalid`).
- Manejo de envío con `markAllAsTouched()`, `console.log()` y `reset()`.

### Etapa 4: Estilos CSS e Integración Final
- Diseño e integración de estilos CSS globales en `styles.css`.
- Prueba y verificación de compilación limpia con `ng build`.
- Preparación final del proyecto y publicación en GitHub.
