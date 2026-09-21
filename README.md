# Aesthetic-Haus

> Progressive Web App (PWA) para registrar, organizar y consultar entrenamientos de fuerza.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-222?style=for-the-badge&logo=github)](#-demo)
[![PWA](https://img.shields.io/badge/PWA-Ready-5A0FC8?style=for-the-badge)](#-pwa)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111)](#-tecnologías)

## 📌 Sobre el proyecto

**Aesthetic-Haus** es una aplicación web orientada al seguimiento de entrenamientos de fuerza.

El proyecto nació con un objetivo práctico: disponer de una herramienta sencilla para registrar entrenamientos y consultar el progreso desde el móvil, manteniendo la información del usuario incluso después de cerrar la aplicación.

Además de resolver el problema funcional, el proyecto está planteado como un ejercicio de desarrollo y aprendizaje dentro de **2º DAM**, aplicando conceptos de desarrollo web, persistencia de datos, PWA y control de versiones.

## ✨ Funcionalidades

- 👤 Perfil personalizable.
- 🏋️ Registro de ejercicios y series.
- ⚖️ Peso, repeticiones y RPE.
- 📊 Seguimiento del volumen/tonelaje registrado.
- ⏱️ Temporizador y control de la sesión.
- 🎨 Personalización visual.
- 🖼️ Avatar/perfil.
- 💾 Persistencia local de los datos.
- 📱 Diseño adaptado a móvil.
- 📲 Instalación como aplicación desde Safari en iPhone.
- 📴 Funcionamiento offline después de cargar la aplicación.
- 🔄 Sistema preparado para detectar nuevas versiones.
- 👥 Cada dispositivo mantiene su propio perfil y sus propios entrenamientos.

## 📱 PWA

Aesthetic-Haus está preparada como **Progressive Web App**.

Desde Safari en iPhone se puede utilizar:

**Compartir → Añadir a pantalla de inicio → Abrir como app web**

La aplicación utiliza un `manifest.webmanifest` y un Service Worker para proporcionar una experiencia más cercana a una aplicación instalada.

## 💾 Persistencia de datos

El proyecto utiliza almacenamiento local del navegador:

- **LocalStorage** como almacenamiento principal.
- **IndexedDB** como respaldo.
- Guardado automático de los datos relevantes.
- Recuperación del estado al volver a abrir la aplicación.

Los datos personales y de entrenamiento se mantienen localmente en el dispositivo. Por ello, dos personas pueden utilizar la misma aplicación publicada y mantener perfiles independientes en sus respectivos dispositivos.

> **Nota:** al ser almacenamiento local, los datos no se sincronizan automáticamente entre dispositivos.

## 🔄 Sistema de actualizaciones

La PWA incorpora un sistema de versiones para evitar que una caché antigua impida recibir cambios publicados.

El flujo previsto es:

```text
Nueva versión
     ↓
Publicación en GitHub Pages
     ↓
La aplicación detecta la actualización
     ↓
El usuario actualiza
     ↓
Se descarga la nueva versión
     ↓
Los datos locales se mantienen
```

## 🛠️ Tecnologías

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura de la aplicación |
| CSS3 | Diseño, responsive y temas |
| JavaScript | Lógica e interacción |
| LocalStorage | Persistencia rápida |
| IndexedDB | Persistencia de respaldo |
| Service Worker | Caché y funcionamiento offline |
| Web App Manifest | Instalación como PWA |
| Git | Control de versiones |
| GitHub | Repositorio y colaboración |
| GitHub Pages | Publicación de la aplicación |

## 🧠 Decisiones técnicas

### Persistencia local

Se optó por almacenamiento local porque la aplicación puede funcionar sin una cuenta de usuario ni un servidor para las funciones básicas.

Esto permite mantener la aplicación sencilla y, al mismo tiempo, conservar los entrenamientos después de cerrar el navegador.

### PWA

La aplicación está orientada principalmente al uso móvil, por lo que una PWA permite acceder rápidamente desde la pantalla de inicio sin desarrollar una aplicación nativa específica para iOS y Android.

### Offline-first

El Service Worker permite almacenar los recursos necesarios para que la aplicación pueda seguir utilizándose cuando no haya conexión, una vez que los recursos hayan sido cargados previamente.

## 📂 Estructura

```text
aesthetic-haus/
├── index.html
├── manifest.webmanifest
├── sw.js
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
├── README.md
└── LICENSE
```

## 🚀 Publicar con GitHub Pages

1. Crear un repositorio llamado `aesthetic-haus`.
2. Subir los archivos del proyecto a la raíz del repositorio.
3. Ir a **Settings → Pages**.
4. Seleccionar la rama `main` y la carpeta `/ (root)`.
5. Guardar la configuración.
6. GitHub Pages generará la URL pública del proyecto.

Ejemplo:

```text
https://TU-USUARIO.github.io/aesthetic-haus/
```

## 🧪 Cómo ejecutar localmente

Para desarrollo, los archivos pueden servirse mediante un servidor HTTP local.

Por ejemplo, con VS Code y una extensión como Live Server.

> Para probar correctamente las características PWA/Service Worker, es preferible utilizar `http://localhost` o una URL HTTPS en lugar de abrir directamente `index.html` con `file://`.

## 🔮 Próximas mejoras

Algunas posibles evoluciones del proyecto:

- [ ] Historial avanzado de entrenamientos.
- [ ] Gráficas de progresión.
- [ ] Exportación e importación de datos.
- [ ] Gestión de rutinas.
- [ ] Sistema de objetivos.
- [ ] Backend y API REST.
- [ ] Autenticación de usuarios.
- [ ] Sincronización entre dispositivos.
- [ ] Base de datos remota.
- [ ] Tests automatizados.
- [ ] Arquitectura frontend/backend más modular.

## 🎓 Contexto académico

Proyecto desarrollado como parte del aprendizaje de **2º de Desarrollo de Aplicaciones Multiplataforma (DAM)**.

El objetivo no es únicamente crear una interfaz, sino aplicar conceptos de desarrollo de software a un proyecto funcional que pueda evolucionar progresivamente.

## 👨‍💻 Autor

**Alejandro Mosquete Mendoza**

Estudiante de **2º DAM**.

Este repositorio forma parte de mi portfolio personal y documenta la evolución de uno de mis proyectos prácticos.

---

### 📄 Licencia

Este proyecto se distribuye bajo la licencia incluida en `LICENSE`.
