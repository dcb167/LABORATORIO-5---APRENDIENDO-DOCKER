# LABORATORIO 5 (APRENDIENDO - DOCKER)

## Elaborado por: Laura Rodriguez y Diana Bernal

### 1. PUNTO 1

#### 1.1 Investigación de Herramientas

##### 1.1.1 Herramienta ROS
###### 1.1.1.1 Definición

Robot Operating System (ROS) es un conjunto de bibliotecas y herramientas de código abierto diseñado para facilitar el desarrollo de aplicaciones robóticas. Ofrece servicios de middleware, abstracción de hardware, comunicación entre procesos y gestión de paquetes [1]. El proyecto ROS fue impulsado inicialmente por Willow Garage y la comunidad académica, y actualmente es mantenido por Open Robotics con versiones más robustas como ROS 2, orientadas a sistemas distribuidos y entornos industriales [2], [3].

###### 1.1.1.2 Alcances en el sector loT

La combinación de robótica e IoT ha dado origen al concepto Internet of Robotic Things (IoRT), en el cual, los robots actúan como nodos inteligentes dentro de redes IoT, ejecutando tareas de sensado, procesamiento y actuación [5]. ROS proporciona la infraestructura necesaria para esta integración mediante adaptadores como ROS–MQTT y ROS Gateways, que permiten la interoperabilidad con plataformas IoT y sistemas en la nube [5], [6]. De igual manera, proyectos como FOGROS2 permiten trasladar procesos intensivos de cómputo a la nube o la niebla (FOG), optimizando el rendimiento de robots conectados en entornos IoT distribuidos [6].


###### 1.1.1.3 Aplicaciones

+ <strong> _Monitoreo ambiental y ciudades inteligentes:_</strong> Robots móviles con sensores ROS recopilan información sobre calidad del aire o ruido, y la envían a plataformas IoT para generar mapas ambientales en tiempo real [5].

+ <strong> _Agricultura de precisión:_</strong> Drones y vehículos autónomos con ROS realizan mapeo de cultivos, detección de plagas y riego automatizado, integrándose con sistemas IoT para análisis predictivo [5].

+ <strong> _Salud y asistencia remota:_</strong> Robots con ROS permiten telepresencia, transporte hospitalario y monitoreo remoto, conectados a infraestructuras médicas IoT [5].

+ <strong>_Industria 4.0 y logística:_</strong> Manipuladores industriales y AGVs controlados por ROS se integran con plataformas IIoT para mejorar la trazabilidad y la eficiencia [4], [6].

+ <strong> _Investigación y educación:_</strong> ROS sigue siendo la plataforma de referencia en universidades y centros de investigación por su modularidad y ecosistema abierto [1], [7].

##### 1.1.2 Herramienta MOVELT

###### 1.1.2.1 Definición

Movelt es un conjunto de paquetes de software open source integrados con ROS (Robot Operating System) orientados a planificación de movimiento, manipulación, cinemática, percepción de entorno, detección de colisiones, y ejecución de trayectorias para brazos robóticos. Ofrece herramientas para configurar robots, generar trayectorias, controlar manipuladores y simular movimientos [8], [9].

###### 1.1.2.2 Alcances en el sector loT

Permite que manipuladores robóticos funcionen como nodos inteligentes dentro de redes IoT, donde sus movimientos, posiciones, estados pueden ser monitoreados remotamente, y sus trayectorias planificadas teniendo en cuenta datos en tiempo real de sensores externos (IoT). En escenarios de Robótica en el Borde (Edge Robotics) o IoRT (Internet of Robotic Things), Movelt puede correr en hardware embebido o edge, recibiendo datos de sensores IoT, y realizar planificación local para reducir latencia frente a depender de la nube. A su vez, facilita integración con otros sistemas IoT mediante APIs, plugin de sensores, módulos de percepción que pueden emitir datos útiles para plataformas IoT (por ejemplo para mantenimiento predictivo, monitoreo, etc.). Para contextos de flotas de robots o automatización distribuida,  apoya la orquestación de movimientos coordinados, detección de obstáculos dinámicos, cálculos de trayectorias seguros, lo que es crítico en fábricas inteligentes, logística con robots móviles manipuladores, etc [8].

###### 1.1.2.3 Aplicaciones

+ <strong> _Industria (ensamblaje, picking, logística):_</strong> Planificación segura de trayectorias para brazos industriales en líneas de montaje y estaciones de picking.

+ <strong> _Robots de servicio y salud:_</strong>  Manipuladores que asisten en entornos asistenciales (teleoperación, entrega de medicación) integrados con sistemas hospitalarios IoT.

+ <strong> _Investigación y educación:_</strong>   Prototipado de planificadores, benchmarking de algoritmos de manipulación y enseñanza de cinemática y control.

+ <strong> _Robots móviles manipuladores:_</strong> Integración de planificación del brazo con la navegación base (coordinación ARM + BASE para tareas dinámicas en almacenes).

+ <strong> _Prototipado y pruebas en simulación:_</strong> Uso combinado de Movelt, RViz y Gazebo para validar comportamientos antes de desplegar en hardware.

##### 1.1.3 Herramienta Gazebo

###### 1.1.3.1 Definición

Gazebo es un simulador multi-robot 3D open-source que combina un motor físico (dinámica de cuerpos rígidos), modelos de sensores (cámaras, LIDAR, IMU, contactos), renderizado 3D y una arquitectura de plugins para extender comportamientos y conexiones a middleware como ROS. Fue presentado originalmente por Koenig y Howard (2004) y desde entonces ha evolucionado incluyendo la re-arquitectura conocida como Ignition/Gazebo para ofrecer mayor modularidad y bibliotecas reutilizables  [10], [11].

###### 1.1.3.2 Alcances en el sector loT

+ <strong> _Pruebas de interoperability y gateways IoT:_</strong> Al simular sensores y actuadores, Gazebo facilita probar pipelines que convierten datos simulados en mensajes MQTT/HTTP o en topics ROS, permitiendo validar integración con plataformas IoT sin riesgo para el hardware [12], [13].

+ <strong> _Entrenamiento y validación de IA/ML en el borde:_</strong> Conjuntos de datos sintéticos (imágenes, nubes de puntos, lecturas IMU) generados en Gazebo son útiles para entrenar modelos que luego se ejecutan en edge devices dentro de arquitecturas IoT [14].

###### 1.1.3.3 Aplicaciones

+ <strong> _Diseño y validación de gemelos digitales industriales:_</strong> Pruebas de planificación de rutas, previsión de fallos y mantenimiento predictivo usando datos simulados que replican las condiciones de planta.

+ <strong> _Desarrollo y verificación de algoritmos de navegación y percepción:_</strong> Benchmarking de SLAM, localización y evitación de obstáculos con sensores simulados (LIDAR, cámaras, sonares). 

+ <strong> _Pruebas de integración ROS / ROS 2 y despliegues CI/CD:_</strong> Integración continua de software robótico con simulación automatizada para asegurar regresiones y calidad.

### 2. PUNTO 2


### 3. PUNTO 3
#### Proceso de creación de simulación del Robot con LIDAR y SLAM en Docker:

+ Iniciamos creando la carpeta del proyecto y el Dockerfile:
<img width="1705" height="191" alt="image" src="https://github.com/user-attachments/assets/8ea5aa7d-007b-4216-88ad-eb5c40ca9cc3" />

+ Seguimos con la construcción de la imagen Docker:
<img width="1744" height="627" alt="image" src="https://github.com/user-attachments/assets/a7c9d84e-b186-421a-bf21-b0517fe2d7dd" />
<img width="1352" height="180" alt="image" src="https://github.com/user-attachments/assets/a6893aba-a9ae-4276-a328-182e6cfa7f30" />

+ Ahora, en una terminal nueva se inicia la Simulación del robot (Gazebo):
<img width="1476" height="602" alt="image" src="https://github.com/user-attachments/assets/bc32be8a-04cb-42c2-88dd-4700cf34fed6" />
+ Visualización de la simulación:
<img width="1849" height="1077" alt="image" src="https://github.com/user-attachments/assets/6dcac922-0f73-4054-aaaf-614549d866b5" />

+ Dentro del mismo contenedor, en otra terminal ejecutamos el SLAM:
<img width="1850" height="508" alt="image" src="https://github.com/user-attachments/assets/e8c8b750-1699-4ef6-912a-ecea0fcd9c56" />

+ Visualización de la ventana abierta del SLAM:
<img width="1274" height="1047" alt="image" src="https://github.com/user-attachments/assets/a57f7c75-9d69-4edf-a602-6aaa3299174b" />

+ En otra terminal, se realizara la teleoperación para  poder mover el robot:
<img width="1854" height="394" alt="image" src="https://github.com/user-attachments/assets/ffe6e8c9-a48f-44f6-be10-b9689956a799" />

+ Se visuliza que se mueve el robot:
<img width="1831" height="1010" alt="image" src="https://github.com/user-attachments/assets/5718ea26-51d4-4fd2-b5c8-2455185d0d2e" />

+ En una cuarta terminal ejecutamos el Rviz que muestra los cambios en tiempo real:
<img width="1831" height="1010" alt="image" src="https://github.com/user-attachments/assets/f91ef97c-681b-45fb-8def-38dc2caa821f" />
<img width="1831" height="1010" alt="image" src="https://github.com/user-attachments/assets/fb815d4f-ab58-41d5-949a-e42f870319ec" />

+ Por ultimo se guarda el mapa y hacer la copia en la maquina:

Copia del mapa:
<img width="1849" height="155" alt="image" src="https://github.com/user-attachments/assets/c4be156d-ee2a-4e09-ba11-cd2f2a49650a" />

Copia del mapa en la maquina:
<img width="1849" height="155" alt="image" src="https://github.com/user-attachments/assets/1a550c62-88dd-443d-92b1-18f38349977c" />

+ Para finalizar se comprueba que los archivos del mapa quedaron guardados en la carpeta correctamente:
<img width="1827" height="82" alt="image" src="https://github.com/user-attachments/assets/0f003a32-fceb-423e-adfb-aa20d30045e4" />

+ Se termina de comprobrar abriendo el mapa para verlo:
<img width="1865" height="629" alt="image" src="https://github.com/user-attachments/assets/d2d111a7-7891-4967-add4-e49ae2620a5b" />

### Referencias

[1] M. Quigley, K. Conley, B. Gerkey, J. Faust, T. Foote, J. Leibs, R. Wheeler, and A. Y. Ng, “ROS: an open-source Robot Operating System,” ICRA Workshop on Open Source Software, 2009. [Online]. Available: https://ai.stanford.edu/~mquigley/papers/icra2009-ros.pdf

[2] Open Robotics, “Robot Operating System (ROS),” ROS.org, 2025. [Online]. Available: https://www.ros.org/

[3] Wikipedia, “Robot Operating System,” Wikipedia: The Free Encyclopedia, 2025. [Online]. Available: https://en.wikipedia.org/wiki/Robot_Operating_System

[4] M. Biggs, J. Peralta, and C. Hernández, “Software Engineering Research on the Robot Operating System,” Journal of Systems and Software, vol. 190, 2022. [Online]. Available: https://doi.org/10.1016/j.jss.2022.111431

[5] C. Eze, “Internet of Things Meets Robotics: A Survey of Cloud-Based Robots,” arXiv preprint arXiv:2306.02586, 2023. [Online]. Available: https://arxiv.org/abs/2306.02586

[6] J. Ichnowski et al., “FogROS2: An Adaptive Platform for Cloud and Fog Robotics Using ROS 2,” arXiv preprint arXiv:2205.09778, 2022. [Online]. Available: https://arxiv.org/abs/2205.09778

[7] A. Testa, A. Camisa, and G. Notarstefano, “ChoiRbot: A ROS 2 Toolbox for Cooperative Robotics,” arXiv preprint arXiv:2010.13431, 2020. [Online]. Available: https://arxiv.org/abs/2010.13431

[8] D. Coleman, I. Sucan, S. Chitta, N. Correll, “Reducing the Barrier to Entry of Complex Robotic Software: a MoveIt! Case Study,” arXiv preprint arXiv:1404.3785, 2014. [Online]. Available: https://arxiv.org/abs/1404.3785

[9] PickNik Robotics, “PickNik Robotics releases MoveIt Studio Developer Platform and SDK,” The Robot Report, 2022. [Online]. Available: https://www.therobotreport.com/picknik-robotics-releases-movelt-developer-platform-and-sdk/

[10] N. Koenig and A. Howard, “Design and Use Paradigms for Gazebo, An Open-Source Multi-Robot Simulator,” Proc. IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), Sendai, Japan, Sep. 2004, pp. 2149–2154. Available: https://robotics.usc.edu/publications/media/uploads/pubs/394.pdf

[11] Gazebo Sim, “Gazebo Sim — Open Source Robotics Simulator,” GazeboSim.org, 2025. [Online]. Available: https://gazebosim.org/libs/sim/
[Accessed: 16-Oct-2025].

[12] Open Robotics / Gazebo community discussion, “Updates in Ignition Gazebo Documentation,” OpenRobotics Discourse, 2023. [Online]. Available: https://discourse.openrobotics.org/t/updates-in-ignition-gazebo-documentation/48400
[Accessed: 16-Oct-2025].

[13] Gazebo Libraries, “Sensors, Physics and Tools — Gazebo Documentation,” GazeboSim.org, 2025. [Online]. Available: https://gazebosim.org/libs/
[Accessed: 16-Oct-2025].

[14] “Setting up a robot simulation (Gazebo) — ROS Documentation,” docs.ros.org, 2025. [Online]. Available: https://docs.ros.org/en/humble/Tutorials/Advanced/Simulators/Gazebo/Gazebo.html
[Accessed: 16-Oct-2025].
