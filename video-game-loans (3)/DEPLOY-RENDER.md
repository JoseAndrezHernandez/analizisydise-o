# 🚀 Guía de Despliegue en Render

## Pasos para desplegar tu proyecto en Render:

### 1. Preparar el repositorio
1. Sube todo el código a GitHub
2. Asegúrate de que todos los archivos estén incluidos

### 2. Crear cuenta en Render
1. Ve a [render.com](https://render.com)
2. Regístrate con tu cuenta de GitHub
3. Conecta tu repositorio

### 3. Configurar el servicio
1. Haz clic en "New +" → "Web Service"
2. Conecta tu repositorio de GitHub
3. Configura los siguientes valores:

**Configuración básica:**
- **Name**: `video-game-loans` (o el nombre que prefieras)
- **Environment**: `Node`
- **Region**: `Oregon` (o el más cercano)
- **Branch**: `main` (o tu rama principal)

**Build & Deploy:**
- **Build Command**: `npm install && npm run build`
- **Start Command**: `npm start`

**Plan:**
- Selecciona **Free** (suficiente para tu proyecto universitario)

### 4. Variables de entorno (opcional)
En la sección "Environment Variables", puedes agregar:
- `NODE_ENV` = `production`

### 5. Configurar almacenamiento persistente
1. En "Settings" → "Disks"
2. Haz clic en "Add Disk"
3. Configura:
   - **Name**: `data-storage`
   - **Mount Path**: `/opt/render/project/src/data`
   - **Size**: `1 GB` (más que suficiente)

### 6. Desplegar
1. Haz clic en "Create Web Service"
2. Render automáticamente:
   - Clonará tu repositorio
   - Instalará las dependencias
   - Construirá la aplicación
   - La desplegará

### 7. ¡Listo! 🎉
- Tu aplicación estará disponible en una URL como: `https://tu-app.onrender.com`
- Los datos se guardarán permanentemente
- Funcionará para múltiples usuarios simultáneamente

## 🔧 Solución de problemas

### Si el build falla:
1. Verifica que `package.json` tenga todas las dependencias
2. Asegúrate de que la versión de Node sea >= 18

### Si los datos no se guardan:
1. Verifica que el disco persistente esté configurado
2. Revisa los logs en el dashboard de Render

### Si hay errores de permisos:
1. Los archivos se crearán automáticamente en el primer uso
2. El script `init-data.js` se ejecuta automáticamente

## 📱 Usuarios de prueba para demostrar:
- **Admin**: admin@gameloans.com / 123456
- **Usuario**: juan@email.com / 123456
- **Usuario**: maria@email.com / 123456

## ✅ Características que funcionarán:
- ✅ Agregar/eliminar juegos permanentemente
- ✅ Sistema de préstamos completo
- ✅ Múltiples usuarios simultáneos
- ✅ Datos persistentes entre sesiones
- ✅ Modo oscuro/claro
- ✅ Responsive design

¡Tu proyecto estará listo para presentar! 🎮
\`\`\`

Vamos a crear también un archivo de configuración para asegurar que Next.js funcione correctamente en producción:
