# NFC Studio

Aplicación Android nativa para explorar etiquetas NFC compatibles, leer datos NDEF accesibles, escribir texto/URL en etiquetas compatibles y ejecutar un perfil HCE de demostración. Diseñada para funcionar sin root.

## Funciones
- Detección de tecnologías NFC expuestas por Android y presentación del ID expuesto por la etiqueta.
- Lectura de registros NDEF compatibles.
- Escritura de texto o URL en etiquetas NDEF compatibles.
- Diagnóstico de capacidad, modo de solo lectura y errores de acceso.
- Historial local de escaneos.
- HCE con AID propio de demostración: F0010203040506.

## Limitaciones
No clona credenciales de acceso o transporte, no replica UID, no intenta adivinar claves ni eludir autenticación. Android solo muestra la información expuesta y las tecnologías disponibles; las etiquetas protegidas pueden requerir protocolo o autenticación específica.

## Compilación
JDK 17, Gradle 8.13, Android Gradle Plugin 8.7.3 y Android SDK 35. Ejecuta `gradle --no-daemon clean assembleDebug`. El APK queda en `app/build/outputs/apk/debug/app-debug.apk`.

GitHub Actions compila automáticamente al actualizar `main` y publica el APK como artefacto descargable por 14 días.