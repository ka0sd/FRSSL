# FRSSL – Face Recognition Security System for GNU/Linux

FRSSL (Face Recognition Security System for Linux) es un sistema de autenticación facial diseñado para entornos GNU/Linux que integra reconocimiento facial con el sistema de bloqueo de pantalla (GNOME), utilizando inteligencia artificial y automatización a nivel del sistema operativo.

El objetivo del proyecto es ofrecer una alternativa o complemento a los sistemas tradicionales basados en contraseñas, reduciendo vulnerabilidades asociadas al error humano y reutilización de credenciales.

---

## 🚀 Motivación

Estadísticas globales muestran que:

- 95% de los incidentes de seguridad involucran error humano.
- 80% de los ataques están relacionados con contraseñas.
- 66% de las personas reutilizan contraseñas.
- Solo 13% utiliza contraseñas realmente únicas.

FRSSL nace como una solución experimental para mitigar estos riesgos utilizando autenticación biométrica basada en reconocimiento facial.

---

## 🏗 Arquitectura del Sistema

El flujo general del sistema es:

1. El sistema detecta cambios en el estado del ScreenSaver de GNOME mediante D-Bus.
2. Se ejecuta un script en Python cuando el sistema entra en modo de bloqueo.
3. Se captura una imagen desde la cámara.
4. Se detectan rostros en la imagen.
5. Se extraen puntos clave faciales y se codifican.
6. Se comparan con una base de datos local de rostros autorizados.
7. Si hay coincidencia, se ejecuta un comando Bash para desbloquear.

---

## 🧠 Tecnologías Utilizadas

- Python 3
- OpenCV (cv2)
- face_recognition
- NumPy
- D-Bus
- Bash scripting
- GNU/Linux (entorno GNOME)

---

## 📂 Estructura del Proyecto

- `face_reco_lockscreen.py` → Lógica principal de reconocimiento facial.
- `script.sh` → Automatización y ejecución de comandos del sistema.
- Integración con D-Bus para detección de eventos del ScreenSaver.

---

## 🔐 Características

- Integración directa con el entorno de escritorio GNOME.
- Reconocimiento facial en tiempo real.
- Comparación contra base de datos local de rostros codificados.
- Automatización del desbloqueo mediante scripting.
- Diseño modular y extensible.

---

## ⚙️ Requisitos

- GNU/Linux con GNOME
- Python 3.x
- OpenCV
- face_recognition
- NumPy
- Cámara funcional

---

## 📈 Limitaciones Actuales

- Precisión no validada con métricas estadísticas formales
- No implementa autenticación multifactor
- Dependencia de condiciones de iluminación
- Base de datos de rostros local y básica

---

## 🧪 Posibles Mejoras Futuras

- Registro automático de intentos fallidos (log de intrusos)
- Implementación de doble factor (facial + contraseña)
- Optimización de rendimiento
- Mejora de precisión con modelos más avanzados
- Interfaz gráfica de configuración

---

## 🎯 Aprendizajes del Proyecto

### Este proyecto permitió trabajar con:
- Integración entre software y sistema operativo
- Manejo de eventos en tiempo real
- Procesamiento de imágenes
- Reconocimiento de patrones faciales
- Automatización mediante scripting
- Diseño de arquitectura de seguridad

---

# 👨‍💻 Autor:

## Nicolás Garrido Novas
