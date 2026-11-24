# NEXO · Android

App Android (Kotlin) que lleva las 6 pantallas de NEXO dentro de un WebView y funciona sin internet.
La interfaz está en `app/src/main/assets/www/` (HTML/CSS/JS); `MainActivity.kt` la carga y maneja el botón "atrás".

## Opción A · APK automático con GitHub (sin instalar nada)

1. Sube **todo el contenido de esta carpeta** a un repositorio de GitHub (rama `main`).
2. Ve a la pestaña **Actions → "Compilar APK" → Run workflow** (también corre solo en cada push).
3. Al terminar, abre la ejecución y descarga el artefacto **NEXO-apk** (contiene `app-debug.apk`).
4. Pásalo al teléfono, ábrelo y permite "instalar apps de orígenes desconocidos".

## Opción B · Android Studio

1. Abre Android Studio → **Open** → selecciona esta carpeta.
2. Espera a que sincronice Gradle (descarga lo necesario).
3. Conecta tu teléfono (depuración USB) o usa un emulador y pulsa **Run ▶**.
4. Para un APK: **Build → Build APK(s)**.

## Cambiar el diseño

Edita los archivos en `app/src/main/assets/www/` (`js/data.js` tiene los perfiles y publicaciones de demo).

## Datos técnicos

- `applicationId`: `app.nexo` · minSdk 26 (Android 8.0) · targetSdk 34
- El APK de depuración sirve para probar; para publicar en Google Play hay que firmar un build *release*.
