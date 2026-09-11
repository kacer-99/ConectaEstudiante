# Conecta Estudiante - Portal de Actividades y Talleres

**Asignatura:** Electivo Angular 22  
**Estudiante:** Kevin Carrasco  

## Descripción del Proyecto
Este proyecto es una aplicación web (SPA) desarrollada en Angular 22 para la organización "Conecta Estudiante". La app permite revisar actividades y talleres académicos, ver datos de contacto y realizar solicitudes de inscripción mediante un formulario reactivo con validaciones.

## Versión y Requisitos
- **Angular CLI:** Versión 22.x (usando Standalone Components)
- **Node.js:** v18+

## Cómo ejecutar el proyecto
1. Clonar el repositorio: `git clone https://github.com/kacer-99/ConectaEstudiante.git`
2. Instalar dependencias: `npm install`
3. Iniciar el servidor: `ng serve`
4. Abrir en el navegador: `http://localhost:4200`

## Componentes y Vistas
- **Componentes base (`src/app/components/`):**
  - `Cabecera`: Encabezado principal del sitio.
  - `Menu`: Barra de navegación con los accesos directos.
- **Páginas (`src/app/pages/`):**
  - `Inicio`: Vista principal de bienvenida.
  - `Actividades`: Muestra el catálogo de talleres recorridos con `@for`.
  - `Contacto`: Vista con información de contacto.
  - `Inscripcion`: Vista con el formulario de registro.

## Rutas configuradas (`app.routes.ts`)
- `/` e `/inicio`: Carga la página de Inicio.
- `/actividades`: Carga el catálogo de talleres.
- `/contacto`: Carga la vista de contacto.
- `/inscripcion`: Carga la vista del formulario.
Se utilizaron `routerLink` y `routerLinkActive` en el menú para navegar dentro del `<router-outlet>`.

## Formulario e Inscripción
El formulario está hecho en la vista de Inscripción con `ReactiveFormsModule` (`FormGroup` y `FormControl`). Tiene 7 campos con sus respectivas validaciones:
- **Nombre y Apellido:** Obligatorios y con un mínimo de 3 caracteres (`minLength`).
- **Correo:** Obligatorio y con formato de email válido (`email`).
- **Carrera, Actividad y Jornada:** Campos de selección obligatorios.
- **Comentario:** Campo opcional de texto libre.

Si un campo es obligatorio y el usuario lo deja vacío o mal escrito, se muestra un mensaje de error usando `@if` al marcar la casilla (`touched` e `invalid`). Al presionar enviar, se ejecuta `markAllAsTouched()` para validar todo junto.

## Registro de Etapas

### Etapa 1: Estructura inicial
- Creación del proyecto Angular Standalone con rutas habilitadas.
- Generación de los componentes en `components/` y las páginas en `pages/`.

### Etapa 2: Navegación SPA y Rutas
- Configuración del archivo `app.routes.ts`.
- Conexión de rutas con `routerLink` y despliegue del catálogo de actividades con `@for`.

### Etapa 3: Formulario Reactivo
- Integración de `ReactiveFormsModule` y lógica con `FormGroup`.
- Configuración de validaciones y mensajes de error en los campos.

### Etapa 4: Estilos y Entrega
- Aplicación de estilos CSS generales en `styles.css`.
- Compilación del proyecto con `ng build` y subida final a GitHub.
