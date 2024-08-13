# Security Hardening

Nuestros dispositivos y redes están constantemente en riesgo de ser atacadas por hackers maliciosos vamos a ver la forma de protegernos. 

Entendemos como **endurecimiento de la seguridad o mejora de la seguridad** como: El proceso de **fortalecer** un sistema para **reducir su vulnerabilidad y superficie de ataque**.

La superficie de ataque son las vulnerabilidades potenciales que un agente de amenazas podría explotar.

- ¿Por qué es importante el endurecimiento de la seguridad?
  - Minimiza las vulnerabilidades y mantiene las redes seguras.
  - Se puede aplicar a cualquier dispositivo o sistema, incluyendo hardware, software y redes.
  - La seguridad física también forma parte del endurecimiento.
- Tipos mas comunes de endurecimiento:
  - Actualizaciones de software (parches) y cambios en la configuración de los dispositivos.
  - Exigir contraseñas más fuertes y cambios más frecuentes.
  - Actualizar los estándares de cifrado para el almacenamiento de datos.
  - Eliminar aplicaciones y servicios no utilizados.
  - Deshabilitar puertos no utilizados.
  - Reducir los permisos de acceso.
  - Minimizar la superficie de ataque hace que la supervisión sea más eficiente.



## OS Hardening o Endurecimiento de los sistemas operativos

Tipos de prácticas de endurecimiento del sistema operativo:

- Tareas realizadas regularmente:
  - *Instalación de parches (actualizaciones para abordar vulnerabilidades)*
  - *Copias de seguridad*
  - *Mantenimiento de una lista actualizada de dispositivos y usuarios autorizados*
- Tareas realizadas una sola vez:
  - *Configurar los ajustes del dispositivo para cumplir con los estándares de cifrado seguro*



------



- **Actualizaciones de parches:**
  - Abordan las vulnerabilidades de seguridad en el software y los sistemas operativos.
  - Deben aplicarse tan pronto como se publiquen para evitar la explotación por parte de actores maliciosos.
  - El sistema operativo actualizado debe añadirse a la configuración de referencia para futuras referencias.
- **Configuración predeterminada**:
  - Un conjunto documentado de especificaciones que se utiliza como base para futuras compilaciones, lanzamientos y actualizaciones.
  - Puede incluir reglas de cortafuegos, puertos permitidos/no permitidos, etc.
  - Permite a los equipos de seguridad comparar las configuraciones actuales e identificar los cambios.
- **Eliminación de hardware y software**:
  - Asegurar la eliminación y el borrado adecuados del hardware antiguo.
  - Eliminar las aplicaciones de software no utilizadas para evitar vulnerabilidades.
- **Política de contraseñas seguras**:
  - Impone reglas específicas para las contraseñas (longitud mínima, caracteres, etc.).
  - Limita los intentos de acceso para evitar el acceso no autorizado.
  - Puede requerir la autenticación multifactor (MFA) para mayor seguridad.

### BRUTE FORCE ATACK O ATAQUE POR FUERZA BRUTA

Es un método de prueba y error utilizado para adivinar información privada, como contraseñas. Los atacantes prueban diferentes combinaciones de nombres de usuario y contraseñas hasta que encuentran una que funciona.

- **Tipos de ataques:** Ataques de fuerza bruta simples y ataques de diccionario.
- **Herramientas utilizadas:** Los atacantes utilizan diversas herramientas para automatizar el proceso.
- **Evaluación de vulnerabilidades:** Las empresas pueden utilizar máquinas virtuales y entornos sandbox para probar las vulnerabilidades antes de que se produzca un ataque.
- **Medidas de prevención:**
  - ***Salting and hashing:** Añadir caracteres aleatorios a las contraseñas para hacerlas más seguras.*
  - ***Autenticación multifactor (MFA):** Requerir múltiples formas de verificación para acceder a un sistema.*
  - ***CAPTCHA y reCAPTCHA:** Pruebas que distinguen a los humanos de los bots.*
  - ***Políticas de contraseñas:** Directrices para crear contraseñas seguras.*

## Network Hardening o Endurecimiento de Redes

Tipos de **practicas mas usadas** para el endurecimiento de redes:

- **Mantenimiento de las reglas del cortafuegos:** Revise y actualice periódicamente las reglas del cortafuegos para garantizar que sean eficaces y estén actualizadas.
- **Análisis de registros de red:** Analice los registros de red para identificar actividades sospechosas y posibles amenazas a la seguridad.
- **Actualizaciones de parches:** Aplique los parches de seguridad a los sistemas operativos y aplicaciones con prontitud para solucionar las vulnerabilidades.
- **Copias de seguridad del servidor:** Realice copias de seguridad de sus servidores con regularidad para garantizar la recuperación de datos en caso de un incidente de seguridad.

**Tareas que se realizan una vez:**

- **Filtrado de puertos:** Bloquee los puertos innecesarios en los cortafuegos para evitar el acceso no autorizado.
- **Privilegios de acceso a la red:** Conceda privilegios de acceso a la red basándose en el principio de mínimo privilegio, garantizando que los usuarios sólo tengan acceso a los recursos que necesitan.
- **Cifrado:** Cifre todas las comunicaciones de red para proteger la confidencialidad e integridad de los datos.



**Dispositivos para la seguridad y endurecimiento de la red:**

- **Cortafuegos:** Permiten o bloquean el tráfico según reglas, generalmente inspeccionando las cabeceras de los paquetes.
- **Sistemas de detección de intrusiones (IDS):** Monitorean la actividad del sistema y alertan sobre posibles intrusiones basadas en firmas de ataques conocidas o anomalías.
- **Sistemas de prevención de intrusiones (IPS):** Detienen activamente las intrusiones bloqueando el tráfico sospechoso.
- **Gestión de información y eventos de seguridad (SIEM):** Recopila y analiza los datos de registro de varios dispositivos de red para proporcionar una monitorización e información centralizadas.



| Dispositivos / Herramientas                              | Ventajas                                                     | Desventajas                                                  |
| -------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Firewall**                                             | Un firewall permite o bloquea el tráfico basado en un conjunto de reglas. | Un firewall solo puede filtrar paquetes basándose en la información proporcionada en el encabezado de los paquetes. |
| **Sistema de Detección de Intrusos (IDS)**               | Un IDS detecta y alerta a los administradores sobre posibles intrusiones, ataques y otro tráfico malicioso. | Un IDS solo puede escanear ataques conocidos o anomalías obvias; ataques nuevos y sofisticados podrían no ser detectados. No detiene el tráfico entrante. |
| **Sistema de Prevención de Intrusos (IPS)**              | Un IPS monitorea la actividad del sistema en busca de intrusiones y anomalías y toma medidas para detenerlas. | Un IPS es un dispositivo en línea. Si falla, la conexión entre la red privada y el internet se interrumpe. Puede detectar falsos positivos y bloquear tráfico legítimo. |
| **Gestión de Información y Eventos de Seguridad (SIEM)** | Una herramienta SIEM recopila y analiza datos de registros de múltiples máquinas de la red. Agrega eventos de seguridad para su monitoreo en un tablero central. | Una herramienta SIEM solo informa sobre posibles problemas de seguridad. No toma ninguna acción para detener o prevenir eventos sospechosos. |



**Ubicación de los dispositivos de seguridad:**

- **IDS:** Se coloca detrás del cortafuegos para analizar el tráfico después de que éste haya sido filtrado por el cortafuegos.
- **IPS:** Se coloca detrás del cortafuegos y antes de la LAN para evitar que el tráfico afectado llegue a las áreas sensibles.



**Medidas adicionales de endurecimiento:**

- **Segmentación de la red:** Cree subredes aisladas para diferentes departamentos o zonas de seguridad para limitar el impacto de los incidentes de seguridad.
- **Deshabilitacion de los protocolos obsoletos:** Deshabilite los protocolos inalámbricos antiguos y menos seguros y utilice los protocolos más recientes disponibles.
- **Implemente estándares de cifrado sólidos:** Utilice estándares de cifrado sólidos, especialmente para los datos de las zonas restringidas.



## Cloud Hardening o endurecimiento de la nube

**Consideraciones:**

Al igual que cualquier otra infraestructura de TI, una infraestructura en la nube necesita ser asegurada. Esto incluye la gestión de identidades, la configuración correcta de servicios, la comprensión de la superficie de ataque, la defensa contra ataques de día cero, y la visibilidad y seguimiento de los datos.

- **Gestión de acceso e identidad (IAM)**

  La IAM es un conjunto de procesos y tecnologías que ayuda a las organizaciones a gestionar identidades digitales y autorizar el uso de recursos en la nube. Un problema común es la configuración incorrecta de roles de usuario, lo que aumenta el riesgo de acceso no autorizado.

- **Superficie de ataque**

  Cada servicio o aplicación en una red presenta riesgos y vulnerabilidades, aumentando la superficie de ataque de una organización. Es esencial implementar medidas de seguridad adicionales para compensar esta ampliación.

- **Zero days Atacks o Ataques de día cero**

  Los ataques de día cero son exploits previamente desconocidos. Los proveedores de servicios en la nube (CSP ) suelen detectar y mitigar estos ataques antes que las organizaciones de TI tradicionales, asegurando que los clientes no se vean afectados.

- **Visibilidad y seguimiento**

  Los administradores de red pueden inspeccionar los datos en tránsito tanto en redes locales como en la nube mediante registros de flujo y herramientas como el mirroring de paquetes. Aunque los CSPs protegen su infraestructura, no permiten a las organizaciones monitorizar el tráfico en sus servidores, lo que puede ser preocupante para aquellas acostumbradas a tener acceso completo.

- **Modelo de responsabilidad compartida**

  El principio de responsabilidad compartida establece que el CSP es responsable de la seguridad de la infraestructura de la nube, mientras que la organización usuaria es responsable de los activos y procesos que opera en la nube. Es crucial que ambas partes entiendan claramente sus responsabilidades para evitar malentendidos y problemas de seguridad.



**Técnicas de endurecimiento de la seguridad en la nube:**

- **Gestión de identidades y accesos (IAM):** Controla el acceso a los recursos en la nube y autoriza las acciones de los usuarios.
- **Hypervisors o Hipervisores (Virtualización):** Abstraen el hardware del sistema operativo, mejorando la seguridad.
- **Base Line o Configuración predeterminada:** Establece un punto de referencia para la configuración y la instalación del entorno en la nube.
- **Criptografía:** Cifra los datos para garantizar la confidencialidad y la integridad.
- **Borrado criptográfico:** Destruye las claves de cifrado para borrar los datos de forma permanente.

