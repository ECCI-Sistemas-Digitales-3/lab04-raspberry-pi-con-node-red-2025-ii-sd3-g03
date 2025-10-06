[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20745313&assignment_repo_type=AssignmentRepo)

# Universidad ECCI  
## Facultad de Ingeniería Electrónica  
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

En el campo de la **Ingeniería Electrónica** y el **Internet de las Cosas (IoT)**, es esencial que los estudiantes adquieran competencias en el uso de hardware y software para el diseño de soluciones tecnológicas. En este contexto, la **Raspberry Pi** se ha convertido en una herramienta clave gracias a su bajo costo, tamaño compacto y capacidad para ejecutar aplicaciones de control, monitoreo y comunicación.  

En el **Lab03**, se trabajó con la Raspberry Pi Zero W empleando **VNC Viewer** como acceso remoto al entorno gráfico. Se desarrolló un programa en **Python** para simular la lectura de un sensor y graficar datos en tiempo real con **Matplotlib**, lo que permitió comprender:  

- La captura periódica de datos.  
- La visualización dinámica en tiempo real.  
- La integración de comandos del sistema con Python.  

En el **Lab04**, se avanza hacia herramientas más profesionales mediante **Node-RED**, una plataforma de programación visual ampliamente usada en **IoT** e **Industria 4.0**. A diferencia del enfoque anterior, Node-RED permite crear **dashboards web interactivos** para visualizar y gestionar datos de forma más eficiente e intuitiva.  

El objetivo de este laboratorio es:  
- Diseñar un flujo en Node-RED con un **color picker**.  
- Mostrar los valores seleccionados en formato **RGB**.  
- Almacenar dichos valores en un archivo de texto.  
- Procesarlos en Python y convertirlos a otros formatos (como **Hexadecimal**).  

La importancia de esta práctica radica en que refleja aplicaciones reales como:  
- **Domótica** con LEDs RGB.  
- **Monitoreo ambiental** (temperatura, humedad, calidad del aire).  
- **Control de procesos industriales**.  
- **Aplicaciones educativas y de investigación**.  

✅ Mientras el **Lab03** introdujo los fundamentos de acceso remoto, lectura de datos y gráficos en Python, el **Lab04** consolida estos aprendizajes integrando **interfaces web y almacenamiento de datos**, fortaleciendo así las competencias en **IoT, automatización y sistemas embebidos modernos**.  


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

# 📷 Análisis de Imágenes – Instalación y Configuración de Node-RED

---

## Imagen 1 – Inicialización de configuración en Node-RED

En esta imagen se observa el proceso de creación del archivo de configuración **`settings.js`** dentro del directorio del usuario:


Este archivo es fundamental porque:

- Define los temas de interfaz que se usarán en el editor de Node-RED.  
- Permite seleccionar el editor de texto por defecto (en este caso **monaco**).  
- Habilita o deshabilita la opción de cargar módulos externos en los nodos de función.  

I### Figura 1
Inicialización de configuración en Node-RED  

<img width="1064" height="521" alt="Image" src="https://github.com/user-attachments/assets/7a54e9e1-f965-4c91-add6-1e3ac776382c" /> 
**Fuente:** Elaboración propia


🔑 **Importancia:** Esta etapa asegura que Node-RED quede con parámetros iniciales personalizados antes de comenzar a trabajar con flujos.  

---

## Imagen 2 – Listado de temas disponibles en Node-RED

Aquí se muestra el listado de temas que ofrece Node-RED para personalizar la interfaz gráfica del editor.  

Entre las opciones disponibles se encuentran:

- **monokai**  
- **dracula**  
- **solarized**  
- **night-owl**  
- (otros más disponibles en la configuración)  

Beneficios de esta opción:

- Mejora la **legibilidad del código** y la comodidad del usuario.  
- Facilita el trabajo en **diferentes condiciones de luz**.  
- Permite adaptar el entorno a las **preferencias del programador**.  

Listado de temas disponibles en Node-RED
<img width="1064" height="521" alt="Image" src="https://github.com/user-attachments/assets/56b18f8e-9942-48ec-88c3-d8899615b12f" />
**Fuente:** Elaboración propia

🎨 **Relevancia:** La personalización de temas contribuye a la productividad y ergonomía del entorno de desarrollo.  

---

## Imagen 3 – Recomendaciones de seguridad y archivo de configuración

En la tercera imagen se observa la inicialización de parámetros de seguridad en Node-RED.  
Se incluyen advertencias importantes como:  

- 🚫 **No exponer Node-RED directamente a Internet** sin protección.  
- 🔑 Configurar **contraseñas y autenticación** para evitar accesos no autorizados.  
- 🛠️ Modificar el archivo `/etc/sudoers.d/010_pi-nopasswd` para reforzar la seguridad en el uso de comandos administrativos.  

Además, se confirma nuevamente la generación del archivo **`settings.js`**, el cual centraliza todas las configuraciones del sistema. 

Recomendaciones de seguridad y archivo de configuración 
<img width="1064" height="521" alt="Image" src="https://github.com/user-attachments/assets/48fe6871-b947-4a13-82df-bece0e4ebdca" />
**Fuente:** Elaboración propia

🔐 **Clave:** Este paso garantiza un entorno seguro y evita vulnerabilidades al usar Node-RED en redes locales o públicas.  

---

## Imagen 4 – Proceso de instalación de Node-RED en Raspberry Pi

En esta captura se observa la ejecución del **script de instalación** de Node-RED en la Raspberry Pi.  

El procedimiento incluye:  

1. Detener Node-RED si está en ejecución.  
2. Eliminar versiones previas de **Node.js** y **Node-RED**.  
3. Instalar la versión actualizada de **Node.js**.  
4. Limpiar la caché de **npm**.  
5. Instalar el núcleo de **Node-RED**.  
6. Reconfigurar nodos existentes y añadir nodos adicionales específicos de Raspberry Pi.  
7. Crear accesos directos y actualizar el servicio en **systemd**.  

⚙️ **Duración estimada:** Entre **20 y 30 minutos** en modelos de Raspberry Pi de menor rendimiento. 

Proceso de instalación de Node-RED en Raspberry Pi
<img width="1064" height="521" alt="Image" src="https://github.com/user-attachments/assets/42bc7e3d-ebad-44c2-864b-ac7c359996b5" />
**Fuente:** Elaboración propia
✅ **Resultado esperado:** Un entorno actualizado y optimizado para trabajar con **IoT**.  

---




 ## Documentación

<!-- Incluir diagramas y adjuntar al repositorio, en una carpeta src, el flujo que crearon -->


## Conclusiones
