# HamlibNet to Cloudlog CAT by CE3MRO (v1.0.0)

**HamlibNet to Cloudlog CAT** es una aplicación de escritorio liviana y eficiente diseñada para radioaficionados que utilizan **710 Console** (o cualquier servidor Hamlib Net TCP) y desean sincronizar de manera automática la frecuencia, modo y potencia de transmisión con su instancia de **Cloudlog**.

---

## 🚀 Novedades y Características en v1.0.0

* **Sincronización Inteligente (Debounce):**
  * Detecta el movimiento continuo de la perilla del dial (`⏳ DIAL EN MOVIMIENTO...`) y aguarda el tiempo configurado antes de realizar la llamada API a Cloudlog.
  * Previene sobrecargas en el servidor enviando datos únicamente cuando la frecuencia se estabiliza.

* **Soporte para Operación en Split (RX/TX):**
  * Lectura concurrente de VFO A y VFO B.
  * Envío automático del parámetro `frequency_rx` a la API de Cloudlog cuando se activa la operación en Split.

* **Control Directo de Potencia:**
  * Entrada rápida para la potencia de salida (W) desde la pantalla principal.
  * Botón **OK** / tecla **Enter** para aplicar e informar inmediatamente los cambios de potencia a Cloudlog.

* **Reconexión Automática y Resiliencia TCP:**
  * Gestión activa de pérdida de conexión con Hamlib Net.
  * Reset automático de estados en caso de cierre inesperado de 710 Console, mostrando la alerta `✕ BUSCANDO HAMLIB`.

* **Integración con el Sistema Windows:**
  * Soporte para minimizar a la **Bandeja del Sistema (System Tray)**.
  * Opción de **Iniciar automáticamente con Windows** accesible desde el panel de configuración.
  * Almacenamiento seguro del archivo `config.json` en `%LOCALAPPDATA%` (no requiere permisos de administrador para ejecutarse o instalarse).

---

## 💻 Requisitos del Sistema

* **Sistema Operativo:** Windows 10 / Windows 11 (32 bits y 64 bits).
* **Servidor CAT:** 710 Console o servidor `rigctl` con interfaz Hamlib Net habilitada (Puerto por defecto: `4533`).
* **Servidor Log:** Instancia activa de Cloudlog con API Key habilitada para control de radio.

---

## 📦 Instalación

1. Descarga el instalador **`HamlibNet_Cloudlog_CAT_Installer_v1.0.0.exe`** desde la sección de **Assets** al final de esta publicación.
2. Ejecuta el instalador y sigue los pasos del asistente.
3. Abre la aplicación desde el acceso directo creado en el escritorio o el menú Inicio.
4. Completa la **URL de tu Cloudlog**, la **API Key** y la **IP/Puerto de Hamlib Net** en la pantalla de Configuración.

---

### 📝 Notas de Versión
* **Autor:** CE3MRO
* **Versión:** 1.0.0 (Primera Edición Pública)
* **Licencia:** Open Source
