
# Actualización automática de GrupoOSG

Este repositorio gestiona el sistema de actualizaciones automáticas de la aplicación **GrupoOSG**.

Cada vez que se lanza una nueva versión del software, se actualiza un archivo `version.json` que contiene la versión más reciente disponible y un enlace al instalador correspondiente.


## 🛠️ ¿Cómo funciona?

Al iniciar la aplicación, esta consulta el archivo JSON para comprobar si hay una nueva versión. Si la versión disponible es mayor que la instalada localmente, el usuario podrá descargarla e instalarla automáticamente.


## 📄 Estructura del archivo `version.json`

```json
{
  "version": "1.0.0",
  "url": "https://github.com/ByRedyx/GrupoOSGApp/releases/download/v1.0.0/GrupoOSG_v1.0.0.msi"
}
```
-   `version`: versión más reciente del software (formato semántico).
-   `url`: enlace directo al archivo `.msi` publicado en la sección de Releases del repositorio de instalación.


## 🌐 URL del archivo JSON

Este archivo está disponible públicamente gracias a **GitHub Pages**:

`https://byredyx.github.io/GrupoOSGApp/version.json` 

La aplicación WPF accede a esta URL para consultar automáticamente si hay nuevas versiones disponibles.


## 🚀 Cómo lanzar una nueva versión

1.  Crear un nuevo instalador `.msi` de la aplicación GrupoOSG.
    
2.  Publicar una nueva [Release](https://github.com/ByRedyx/GrupoOSGApp/releases) con:
    
    -   El instalador adjunto
        
    -   Un nombre de versión como `v1.0.0`
        
    -   Descripción de cambios
        
3.  Actualizar el archivo `version.json` con la nueva versión y URL.


## ✅ Repositorio de instalación

Puedes encontrar los instaladores en la sección de [Releases](https://github.com/ByRedyx/GrupoOSGApp/releases).


## 🔒 Seguridad

Este sistema está pensado para distribuir actualizaciones a través de GitHub. No requiere autenticación porque el archivo `version.json` y los releases son públicos.

Para una solución privada o con control de acceso, se recomienda alojar el JSON e instaladores en un servidor propio o utilizar tokens de acceso.


## 💡 Créditos

Sistema de actualización desarrollado por el departamento de IT de **GrupoOSG**.
