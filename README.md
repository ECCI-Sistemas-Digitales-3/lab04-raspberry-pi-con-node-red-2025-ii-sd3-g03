[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20745313&assignment_repo_type=AssignmentRepo)

# Universidad ECCI  
## Ingeniería Electrónica  
### Laboratorio – Corte 2  

---

## Integrantes 👥  
- **Heidy Nicol Sánchez Peña**  
- **David Mora**  
- **Federico Díaz Novoa**  

---

# Lab04: Visualización de datos en Raspberry Pi con Node-RED  

---

## 📑 Índice
1. Objetivos de aprendizaje  
2. Introducción  
3. Marco Teórico  
   - 3.1 Raspberry Pi y su importancia en IoT  
   - 3.2 Node.js y npm  
   - 3.3 Node-RED: programación visual basada en flujos  
   - 3.4 Dashboards e interfaces gráficas en Node-RED  
   - 3.5 Representación de colores en RGB  
   - 3.6 Python como herramienta de procesamiento de datos  
   - 3.7 Aplicaciones en la industria y vida real  
4. Requisitos  
5. Procedimiento  
   - 5.1 Parte 1: Instalación y configuración de Node-RED  
   - 5.2 Parte 2: Creación de un flujo en Node-RED  
   - 5.3 Script en Python para procesar valores RGB  
6. Resultados esperados  
7. Análisis y discusión de resultados  
8. Conclusiones  
9. Entregables  
10. Bibliografía  

---

## 🎯 1. Objetivos de aprendizaje
- Comprender el funcionamiento de Node-RED y su integración con Raspberry Pi.  
- Implementar un flujo en Node-RED que permita seleccionar colores y visualizar los valores RGB asociados.  
- Almacenar datos generados en un archivo de texto para su posterior análisis.  
- Desarrollar un script en Python que procese los valores RGB leídos desde un archivo.  
- Relacionar las aplicaciones prácticas de Node-RED y Python con proyectos reales de IoT e Industria 4.0.  

---

## 📘 2. Introducción
En la actualidad, la visualización y el procesamiento de datos juegan un papel esencial en proyectos de **Internet de las Cosas (IoT)**. Cada dispositivo conectado genera información que debe ser **capturada, almacenada, procesada y mostrada de forma clara** al usuario final.  

La **Raspberry Pi**, debido a su bajo costo y gran versatilidad, se ha convertido en una de las plataformas más utilizadas en proyectos de IoT. En combinación con **Node-RED**, herramienta creada por IBM para la programación visual basada en flujos, se logra una solución accesible, escalable y potente.  

Este laboratorio combina:  
1. **Node-RED** → Creación de interfaces gráficas para visualizar y manipular datos en tiempo real.  
2. **Python** → Procesamiento avanzado de los datos generados.  
3. **Raspberry Pi** → Ejecución local como servidor y punto de conexión de hardware y software.  

---

## 📚 3. Marco Teórico

### 3.1 Raspberry Pi y su importancia en IoT
La **Raspberry Pi** es una computadora de bajo costo y tamaño reducido que surgió en 2012 como iniciativa educativa. Hoy en día, es ampliamente utilizada en:  
- Automatización industrial.  
- Monitoreo ambiental.  
- Control de sistemas embebidos.  
- Aplicaciones de domótica y ciudades inteligentes.  

**Ventajas de la Raspberry Pi en IoT:**  
- Bajo consumo energético.  
- Compatibilidad con Linux y Windows IoT Core.  
- Amplio soporte de hardware y comunidad activa.  
- Capacidad para ejecutar múltiples lenguajes de programación.  

---

### 3.2 Node.js y npm
**Node.js** es un entorno de ejecución de JavaScript creado en 2009 por Ryan Dahl. Su importancia radica en:  
- Uso del motor **V8 de Google Chrome**, lo que garantiza rapidez y eficiencia.  
- Modelo **asíncrono y orientado a eventos**, ideal para sistemas en tiempo real.  
- Capacidad de manejar miles de conexiones simultáneas.  

**npm (Node Package Manager):**  
- Es el gestor de paquetes oficial de Node.js.  
- Permite instalar librerías como el **dashboard de Node-RED**.  
- Contiene más de 1.3 millones de paquetes disponibles (dato actualizado a 2025).  

---

### 3.3 Node-RED: programación visual basada en flujos
**Node-RED** fue creado por IBM en 2013 y se convirtió en una de las herramientas más utilizadas en IoT.  

**Características principales:**  
- Interfaz gráfica “drag-and-drop”.  
- Librería de nodos preinstalados para redes, almacenamiento, control y visualización.  
- Posibilidad de programar nodos personalizados en JavaScript.  
- Comunicación con APIs REST, MQTT, WebSocket y protocolos industriales.  

**Ventajas:**  
- Bajo nivel de programación requerido.  
- Escalabilidad.  
- Interfaz intuitiva.  
- Comunidad activa con miles de flujos compartidos.  

**Limitaciones:**  
- Dependencia de Node.js.  
- No está optimizado para cálculos matemáticos complejos (para eso se usa Python).  

---

### 3.4 Dashboards e interfaces gráficas en Node-RED
El **dashboard** es una extensión que permite generar interfaces gráficas de usuario accesibles desde un navegador web.  
**Ejemplos de elementos disponibles en dashboard:**  
- Gráficas de líneas y barras.  
- Botones y controles deslizantes.  
- Indicadores LED virtuales.  
- Selectores de color (color picker).  

El dashboard facilita la **interacción entre el usuario y el sistema**, permitiendo controlar dispositivos y visualizar datos en tiempo real.  

---

### 3.5 Representación de colores en RGB
El modelo **RGB (Red, Green, Blue)** es un sistema aditivo de colores basado en la mezcla de tres componentes: rojo, verde y azul.  
- Cada componente puede tomar valores entre 0 y 255.  
- Ejemplo: **RGB(255,0,0) → Rojo puro**.  
- Este sistema es el estándar en pantallas, LEDs y sensores de color.  

En este laboratorio, Node-RED captura los valores RGB seleccionados por el usuario mediante un color picker y los almacena en un archivo.  

---

### 3.6 Python como herramienta de procesamiento de datos
**Python** se ha consolidado como uno de los lenguajes más usados en IoT y análisis de datos.  
- Compatible con Raspberry Pi.  
- Amplia gama de librerías: NumPy, Pandas, Matplotlib.  
- Facilidad para integrar con APIs, bases de datos y archivos de texto.  

En este laboratorio, Python se emplea para leer el archivo con los valores RGB y procesarlos, por ejemplo:  
- Convertirlos a formato **Hexadecimal** (#FF0000).  
- Guardarlos en una base de datos.  
- Aplicar filtros o transformaciones matemáticas.  

---

### 3.7 Aplicaciones en la industria y vida real
Este mismo procedimiento puede aplicarse en:  
- **Control de iluminación LED RGB** en domótica.  
- **Interfaz de monitoreo ambiental**, donde sensores capturan datos de temperatura, humedad y se visualizan en Node-RED.  
- **Sistemas industriales de control** en tableros SCADA (Supervisión, Control y Adquisición de Datos).  
- **Salas interactivas de museos o aulas**, donde los colores representan datos en tiempo real.  

---

## 🛠️ 4. Requisitos

### Software
- Raspberry Pi OS actualizado.  
- Node.js y npm.  
- Node-RED.  
- Python 3.  

### Hardware
- Raspberry Pi (modelo 3, 4 o superior recomendado).  
- Conexión a red local (Wi-Fi o Ethernet).  
- Computadora con cliente SSH.  

---

## ⚙️ 5. Procedimiento

### 🔹 5.1 Parte 1: Instalación y configuración de Node-RED
1. Conexión por SSH:  
```bash
ssh usuario_raspberry@ip

## Documentación

<!-- Incluir diagramas y adjuntar al repositorio, en una carpeta src, el flujo que crearon -->


## Conclusiones
