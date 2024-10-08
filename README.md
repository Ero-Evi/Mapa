# Mapa con Localización usando Google Maps API

Este proyecto es una aplicación Android que integra Google Maps para mostrar la ubicación actual del usuario en un mapa, con un marcador indicando "Estás aquí". También incluye una actividad principal que permite navegar al mapa a través de un botón.

## Autor

Proyecto desarrollado por Victor Llanquinao.

## Descripción del Proyecto

La aplicación cuenta con las siguientes funcionalidades principales:

1. **Pantalla principal (MainActivity)**:
   - Contiene un botón que permite al usuario acceder a la actividad del mapa.
   
2. **Pantalla de mapa (MapsActivity)**:
   - Muestra un mapa utilizando Google Maps.
   - Obtiene la ubicación actual del usuario utilizando el proveedor de ubicación `FusedLocationProviderClient`.
   - Coloca un marcador en la ubicación actual del usuario con un título "Estás aquí".
   - Mueve la cámara para centrar la vista en la ubicación del usuario con un nivel de zoom adecuado.

## Instrucciones para Ejecutar

### 1. Prerrequisitos

- Android Studio: Recordar tener Android Studio instalado.
- Google Maps API Key: Se nececita una API key que puedes obtener en [Google Cloud Console](https://console.cloud.google.com/).
  - Habilita las APIs necesarias para tu proyecto, específicamente "Maps SDK for Android".
  - Añade la API Key en el archivo `AndroidManifest.xml` dentro de la etiqueta `<application>` de la siguiente manera:
    ```xml
    <meta-data
        android:name="com.google.android.geo.API_KEY"
        android:value="Api_Here" />
    ```

### 2. Permisos Requeridos

Se requieren permisos para acceder a la ubicación del dispositivo. Asegúrate de solicitar estos permisos en el archivo `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />

