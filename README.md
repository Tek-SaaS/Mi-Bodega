Mi Bodega

Sistema MRP Offline para Gestión de Inventario y Construcción

https://img.shields.io/badge/version-1.0.0-blue
https://img.shields.io/badge/platform-Android-green
https://img.shields.io/badge/offline-100%25-brightgreen
https://img.shields.io/badge/license-All%20Rights%20Reserved-red

---

📋 Descripción

Mi Bodega es una aplicación móvil Android 100% offline diseñada para la gestión de inventario de materiales y construcción de ítems (bodegas, oficinas, muebles, etc.) con trazabilidad completa.

La app permite:

· 📦 Gestionar materiales con fotos y nombres personalizables
· 🔨 Construir ítems usando recetas (BOM - Bill of Materials)
· 📋 Controlar stock de ítems construidos con códigos únicos manuales
· 📍 Asignar estados y ubicaciones a cada ítem
· 📝 Agregar notas e historial de cambios
· 🖼️ Personalizar completamente nombres y fotografías

Perfecta para: Carpinteros, contratistas, fabricantes de muebles, gestores de bodegas, ensambladores, y cualquier negocio que construya productos a partir de materiales.

---

📱 Capturas de Pantalla

Inventario Construcción Stock Detalle
docs/screenshots/pantalla-inventario.png docs/screenshots/pantalla-construccion.png docs/screenshots/pantalla-stock.png docs/screenshots/pantalla-detalle.png

---

🚀 Características Principales

📦 Inventario de Materiales

· ✅ Agregar, editar y eliminar materiales
· ✅ Asignar nombre, unidad (m², kg, unid, L, etc.) y foto personalizada
· ✅ Ajustar stock con motivo (compra, merma, devolución)
· ✅ Stock mínimo para alertas de reposición

🔨 Construcción de Ítems

· ✅ Seleccionar ítem a construir desde el catálogo
· ✅ Ver receta (BOM) con materiales requeridos
· ✅ Simulación: calcula stock resultante antes de construir
· ✅ Asignar código manual único (ej: OF-001, BOD-2026-01)
· ✅ Validación de stock suficiente antes de construir

📋 Stock de Ítems Construidos

· ✅ Lista completa de todos los ítems construidos
· ✅ Código único, nombre del ítem, estado y fecha
· ✅ Filtros por estado, fecha y nombre
· ✅ Trazabilidad: ver materiales usados en cada ítem

📍 Detalle y Seguimiento

· ✅ Cambiar estado: En Bodega → En Tránsito → Instalado → En Mantenimiento → Desechado
· ✅ Asignar ubicación física (texto libre)
· ✅ Agregar notas (ej: "Requiere repintar", "Entregado el 10/07")
· ✅ Historial completo de cambios
· ✅ Ver materiales usados en la construcción

🖼️ Personalización

· ✅ Cambiar nombre y foto de cualquier material
· ✅ Cambiar nombre y foto de cualquier ítem
· ✅ Agregar nuevos materiales e ítems
· ✅ Modificar recetas (agregar/quitar materiales, cambiar cantidades)

📴 Offline 100%

· ✅ Sin conexión a internet requerida
· ✅ Todos los datos almacenados localmente
· ✅ Instalación única, funciona sin dependencias externas

---

📦 Descarga

Versión Estable

Versión Fecha Descarga Tamaño
v1.0.0 26/06/2026 📲 Descargar APK ~8 MB

Verificar Integridad

```bash
# SHA256 Checksum
shasum -a 256 mibodega-v1.0.0-release.apk
# Resultado esperado:
# [Ver en archivo apk/mibodega-v1.0.0-release.sha256]
```

Requisitos del Sistema

· Android 7.0 (API 24) o superior
· Espacio: ~20 MB (app + datos)
· Permisos: Cámara (para fotos), Almacenamiento (para imágenes)

---

📱 Instalación

1. Habilitar Instalación de Fuentes Desconocidas

· Ve a Ajustes → Seguridad → Instalar desde fuentes desconocidas
· Activa la opción para tu navegador o gestor de archivos

2. Descargar el APK

· Desde tu dispositivo, descarga el archivo APK desde el enlace de arriba
· O transfiérelo desde tu computadora

3. Instalar

· Abre el archivo APK descargado
· Presiona "Instalar"
· Espera a que complete la instalación

4. ¡Listo!

· Abre la app desde el menú de aplicaciones
· La app incluye datos de ejemplo para empezar inmediatamente
· Puedes personalizar todo según tu negocio

---

🛠️ Para Desarrolladores

Estructura del Proyecto

```
Mi-Bodega/
├── /apk/                    # APK firmadas y checksums
├── /website/                # Landing page y sitio web
├── /backend/                # API para estadísticas (Node.js)
├── /android/                # Código fuente de la app
│   └── /app/src/main/java/com/mibodega/
│       ├── /data/           # Base de datos (Room) y DAOs
│       ├── /domain/         # Modelos y casos de uso
│       ├── /presentation/   # UI, ViewModels y adapters
│       └── /utils/          # Helpers y utilidades
├── /scripts/                # Scripts de automatización
└── /docs/                   # Documentación y diagramas
```

Tecnologías Utilizadas

Componente Tecnología
Lenguaje Java / Kotlin
Base de Datos Room (SQLite)
Arquitectura MVVM + Repository Pattern
Dependencias ViewModel, LiveData, Navigation, Glide
Backend (Landing) Node.js + Express
Frontend (Landing) HTML, CSS, JavaScript

Clonar y Compilar

```bash
# Clonar el repositorio
git clone https://github.com/Tek-SaaS/Mi-Bodega.git
cd Mi-Bodega

# Compilar la APK
cd android
./gradlew clean
./gradlew assembleRelease

# La APK estará en:
# android/app/build/outputs/apk/release/app-release.apk
```

Scripts de Automatización

Script Función
scripts/build-apk.sh Compila, firma y mueve la APK a las carpetas correspondientes
scripts/generate-hash.sh Genera SHA256 para verificación de integridad
scripts/deploy-website.sh Despliega el sitio web a GitHub Pages o Vercel
scripts/generate-sample-data.sh Genera datos de ejemplo en JSON

---

📖 Documentación

Documento Descripción
Manual de Usuario Guía completa para usuarios finales
Manual Técnico Documentación técnica para desarrolladores
Arquitectura Diagramas y decisiones arquitectónicas
API Documentation Endpoints del backend (estadísticas)
Diagrama de BD Modelo de base de datos

---

🔄 Flujo de Trabajo

Construir un Ítem

```
1. Seleccionar Ítem
   ↓
2. Ver Receta (BOM)
   ↓
3. Simular (revisar stock)
   ↓
4. Asignar código manual
   ↓
5. Construir (resta materiales, crea ítem)
   ↓
6. Ítem en estado "En Bodega"
```

Seguir un Ítem Construido

```
1. Ir a "Stock"
   ↓
2. Buscar por código o nombre
   ↓
3. Hacer clic en el ítem
   ↓
4. Ver: Estado, Ubicación, Notas, Materiales usados, Historial
   ↓
5. Editar: Estado, Ubicación, Notas
   ↓
6. Guardar cambios (se registra en historial)
```

---

🗺️ Hoja de Ruta

Versión 1.1.0 (Próxima)

· Exportar datos a CSV/PDF
· Búsqueda avanzada con filtros
· Escaneo de códigos QR para identificación rápida
· Notificaciones de stock mínimo

Versión 1.2.0 (Futura)

· Sincronización entre dispositivos (opcional)
· Modo oscuro
· Widgets en pantalla de inicio
· Mapa de ubicaciones de ítems

Versión 2.0.0 (Ideal)

· Multi-empresa
· Roles de usuario (admin, operador, visualizador)
· Dashboard con gráficos estadísticos
· Integración con impresoras Bluetooth

---

🤝 Contribuir

¡Las contribuciones son bienvenidas! Por favor:

1. Haz un Fork del proyecto
2. Crea una rama para tu feature (git checkout -b feature/AmazingFeature)
3. Commit de tus cambios (git commit -m 'Add some AmazingFeature')
4. Push a la rama (git push origin feature/AmazingFeature)
5. Abre un Pull Request

Nota: Este proyecto usa Semantic Versioning.

---

📝 Changelog

v1.0.0 (2026-06-26)

· ✨ Lanzamiento inicial
· ✅ Gestión completa de inventario de materiales
· ✅ Construcción de ítems con recetas (BOM)
· ✅ Stock de ítems construidos con trazabilidad
· ✅ Personalización de nombres y fotos
· ✅ Estados y ubicaciones de ítems
· ✅ Historial de cambios
· ✅ Datos de ejemplo para empezar rápido
· ✅ Landing page con descarga

---

🐛 Reportar Problemas

Si encuentras un bug o tienes una sugerencia:

1. Revisa los issues existentes
2. Si no existe, abre uno nuevo
3. Incluye:
   · Versión de la app
   · Dispositivo y versión de Android
   · Pasos para reproducir el problema
   · Capturas de pantalla (si aplica)

---

📧 Contacto

Canal Enlace
Soporte support@mibodega.app
Sitio Web https://mibodega.app
GitHub https://github.com/Tek-SaaS/Mi-Bodega
Issues GitHub Issues

---

📄 Licencia

Todos los derechos reservados © 2026

Este software es propiedad de Tek-SaaS. No se permite su uso, copia, modificación o distribución sin autorización expresa del propietario.

Para licencias comerciales, contactar a: license@mibodega.app

---

🙏 Agradecimientos

· A todos los usuarios que confían en Mi Bodega para gestionar su inventario
· A la comunidad open-source por las herramientas que hacen esto posible
· A los primeros adoptantes que ayudaron a pulir la experiencia

---

Hecho con ❤️ para quienes construyen el mundo con sus manos

---

<p align="center">
  <a href="https://github.com/Tek-SaaS/Mi-Bodega">
    <img src="website/assets/img/logo.png" alt="Mi Bodega" width="120">
  </a>
  <br>
  <strong>Mi Bodega</strong> — Tu inventario, tu construcción, tu control
</p>
