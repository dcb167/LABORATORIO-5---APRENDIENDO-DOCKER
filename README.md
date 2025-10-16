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

Diseño y validación de gemelos digitales industriales: pruebas de planificación de rutas, previsión de fallos y mantenimiento predictivo usando datos simulados que replican las condiciones de planta.

Desarrollo y verificación de algoritmos de navegación y percepción: benchmarking de SLAM, localización y evitación de obstáculos con sensores simulados (LIDAR, cámaras, sonares). 

Pruebas de integración ROS / ROS 2 y despliegues CI/CD: integración continua de software robótico con simulación automatizada para asegurar regresiones y calidad.

### 2. PUNTO 2

### 3. PUNTO 3

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
