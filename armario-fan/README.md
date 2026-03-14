# armario-fan

Controlador de ventiladores para armario basado en **ESP32** y **ESPHome**, con control **PID**, modo **manual/automático** y monitorización desde **Home Assistant**.

## Características

- Control de **dos ventiladores PWM**
- Lectura de temperatura y humedad desde **Home Assistant**
- Controladores **PID independientes** para cada ventilador
- Ajuste en caliente de:
  - `kp`, `ki`, `kd`
  - parámetros de banda muerta
  - velocidad mínima y máxima en modo automático
- Modo manual y automático
- Servidor web integrado
- Reinicio programado diario
- Sensores de diagnóstico:
  - RPM
  - salida PWM
  - términos P / I / D
  - error
  - estado de banda muerta

## Estructura

- `armario-fan.yaml` — configuración principal de ESPHome

## Notas

Este subproyecto está orientado a refrigeración de armario/rack ligero usando ventiladores PWM de 4 pines y un ESP32.

La lógica usa una arquitectura de `proxy_output` para separar el control manual del control automático PID y permitir limitar el rango de actuación sin modificar directamente el output hardware.

## Pendiente

- Añadir esquema de conexiones
- Añadir imágenes del montaje
- Añadir explicación de ajuste del PID
- Añadir publicación técnica/resumen del proyecto
