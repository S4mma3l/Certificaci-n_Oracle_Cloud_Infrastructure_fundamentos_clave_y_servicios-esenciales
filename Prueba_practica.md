# Guía de Estudio de Práctica OCI Foundations Associate (40 Preguntas)

## 1. Servicios de Cómputo y Serverless 💻

| # | Pregunta | Respuesta Clave |
| :--- | :--- | :--- |
| **1** | ¿Cuál es una característica clave del servicio Oracle Cloud Infrastructure Functions? | D. Aplica automáticamente parches y actualizaciones de software del sistema operativo. |
| **2** | ¿Cuál **NO** es un tipo de instancia ofrecida por el servicio Oracle Cloud Infrastructure Compute? | A. Instancia Nano |
| **3** | ¿Cuál es una ventaja clave de usar **nodos virtuales** en un clúster de OCI Kubernetes Engine? | A. Permiten una experiencia Kubernetes *serverless*, reduciendo la sobrecarga operativa. |
| **4** | ¿A qué se refiere el término "**Formas Flexibles**" (*Flexible Shapes*) en OCI Compute? | C. La capacidad de personalizar el número de OCPUs y la cantidad de memoria para ciertas formas de VM. |
| **5** | ¿Por qué elegirías usar **contenedores** en lugar de máquinas virtuales? | D. Los contenedores permiten un tiempo de inicio más rápido y un uso de recursos más eficiente. |
| **6** | ¿Cuál **NO** es un caso de uso adecuado para las OCI Container Instances? | A. Ejecutar aplicaciones en contenedores en *Kubernetes*. (OCI Container Engine for Kubernetes - OKE es el servicio principal para esto). |
| **7** | ¿Qué afirmación describe mejor las **VMs Preemptivas** (*Preemptible VMs*) en OCI? | D. Son instancias de corta duración ofrecidas a menor costo, que pueden ser reclamadas por OCI. |

***

## 2. Redes y Balanceo de Carga 🌐

| # | Pregunta | Respuesta Clave | Explicación |
| :--- | :--- | :--- | :--- |
| **8** | ¿Cuál es el propósito principal de un **Network Security Group (NSG)** en el servicio de Redes de OCI? | D. Controlar el flujo de tráfico entre **recursos específicos** dentro de una VCN. | A diferencia de las *Security Lists*, los NSG permiten aplicar reglas de seguridad a recursos individuales, independientemente de la subred. |
| **9** | ¿Cuál es la función principal de una **Tabla de Ruta** (*Route Table*) en el servicio de Redes de OCI? | D. Definir reglas para **enrutar el tráfico** desde las subredes a destinos fuera de la VCN. | Las Tablas de Ruta dictan a dónde debe ir el tráfico saliente (*egress*) de una subred. |
| **10** | ¿Qué tipo de política de balanceo de carga es soportada por el Oracle Cloud Infrastructure Load Balancer? | C. Round Robin Ponderado (*Weighted Round Robin*) |
| **11** | ¿Cuál es una razón clave para elegir un **Network Load Balancer** en lugar del Balanceador de Carga Estándar (HTTP/HTTPS) en OCI? | A. El Network Load Balancer opera en la **Capa 4**, ofreciendo menor latencia para el tráfico TCP y UDP. | El Balanceador de Carga Estándar opera en la Capa 7 (HTTP/HTTPS). |
| **12** | ¿Qué componente del servicio de Redes de OCI permite a los recursos en una VCN acceder a los **servicios de Oracle Cloud** sin atravesar el Internet público? | C. Service Gateway |
| **13** | ¿Qué componente de red de OCI Virtual Cloud Network proporciona a las instancias de cómputo en una **subred privada** acceso de **salida a Internet**? | B. Network Address Translation (NAT) Gateway | El NAT Gateway permite tráfico saliente, pero bloquea las conexiones entrantes no solicitadas. |

***

## 3. Seguridad e IAM 🛡️

| # | Pregunta | Respuesta Clave |
| :--- | :--- | :--- |
| **14** | ¿Qué característica **NO** es proporcionada por las Oracle Cloud Infrastructure **Security Zones**? | D. Almacenamiento y gestión de claves de cifrado y secretos. (Esto lo hace **Vault**). |
| **15** | ¿Cómo garantiza OCI el cifrado de datos almacenados y transmitidos? | A. OCI proporciona **cifrado predeterminado** para datos en reposo y en tránsito. |
| **16** | ¿Qué servicio de OCI es responsable de almacenar y gestionar de forma segura **claves de cifrado y secretos**? | C. Vault |
| **17** | ¿Cuál es la ventaja de almacenar **secretos** en un Vault en OCI? | A. Proporciona mayor seguridad que almacenarlos en código o archivos de configuración. |
| **18** | ¿Qué servicio de seguridad en OCI ayuda a proteger contra ataques de **Denegación de Servicio Distribuido (DDoS)**? | D. OCI Web Application Firewall (WAF) |
| **30** | ¿Cuál es la mejor práctica recomendada para los **Administradores de Tenencia** de OCI? | D. Aplicar siempre la Autenticación Multifactor (**MFA**) para mayor seguridad. |
| **31** | ¿Cuál **NO** es un componente de una sentencia de política de **IAM** en OCI? | D. Frecuencia de copia de seguridad de datos (*Data backup frequency*) |
| **32** | ¿Qué afirmación **NO** es verdadera acerca de los **compartimentos** en OCI? | D. Los compartimentos son un recurso global. (**Son regionales o globales a la región del home compartment**). |
| **33** | ¿Qué afirmación describe mejor el comportamiento de **Authz** por defecto para usuarios y grupos en IAM de OCI? | C. El acceso a los recursos se concede **explícitamente** en las políticas; de lo contrario, se **deniega por defecto**. |
| **36** | En el **Modelo de Seguridad Compartida** de Oracle Cloud, ¿de qué es responsable Oracle? | D. Gestionar y asegurar la **infraestructura física** y los servicios de nube subyacentes. |

***

## 4. Almacenamiento (*Storage*) y Transferencia de Datos 💾

| # | Pregunta | Respuesta Clave |
| :--- | :--- | :--- |
| **23** | ¿Cuál es el propósito principal del **Servicio de Transferencia de Datos** (*Data Transfer Service*) de OCI? | A. Facilitar la **transferencia masiva de datos fuera de línea** a OCI utilizando discos o dispositivos. |
| **24** | En el servicio **Block Volume** de OCI, ¿qué característica te permite **aumentar el tamaño** de un volumen en bloque sin tiempo de inactividad? | D. Redimensionamiento en Línea (*Online Resizing*) |
| **25** | En el servicio **Object Storage** de OCI, ¿qué nivel de almacenamiento está diseñado para datos de **acceso poco frecuente** que se pueden **restaurar en horas**? | B. Almacenamiento de Archivo (*Archive Storage*) |
| **27** | ¿Cuál es el propósito principal de la característica **Auto-Tiering** en OCI Object Storage? | C. Reducir los costos de almacenamiento **moviendo objetos** entre los niveles Estándar y Acceso Infrecuente. |
| **28** | ¿Qué tipo de almacenamiento de OCI se adjunta típicamente **localmente** a una instancia de cómputo y ofrece **IOPS muy altas**, pero **no es persistente**? | C. Local NVMe |
| **29** | ¿Qué característica del servicio **Object Storage** de OCI permite a los usuarios mover objetos automáticamente entre niveles de almacenamiento según reglas predefinidas? | C. Gestión del Ciclo de Vida de Objetos (*Object Lifecycle Management*) |

***

## 5. Fundamentos y Modelos de Negocio 💰

| # | Pregunta | Respuesta Clave |
| :--- | :--- | :--- |
| **37** | ¿Cuál es el propósito principal de los **Dominios de Falla** (*fault domains*) en OCI? | B. Distribuir instancias a través de **diferentes hardware físico** dentro de un Dominio de Disponibilidad. |
| **38** | ¿Qué es un **Dominio de Disponibilidad** (*availability domain*) en OCI? | C. Uno o más **centros de datos** ubicados dentro de una región. |
| **39** | ¿Por qué los Dominios de Disponibilidad dentro de la misma Región de OCI están conectados por una red de **baja latencia y alto ancho de banda**? | B. Para permitir **conectividad de alta disponibilidad** y construir sistemas replicados. |
| **40** | ¿Por qué es importante elegir una **Región de OCI cercana a tus usuarios**? | D. Para **minimizar la latencia** y mejorar el rendimiento de la aplicación. |
| **19** | ¿Qué oferta de OCI te permite ejecutar servicios en la nube en **tu propio centro de datos** mientras mantienes el cumplimiento normativo? | C. OCI Dedicated Region |
| **20** | ¿Qué servicio de OCI **NO** está diseñado para usarse con **múltiples proveedores de nube** (*Multicloud*)? | B. Oracle Roving Edge Infrastructure |
| **21** | ¿Con qué te ayuda **Oracle Cloud Advisor**? | C. Recomendaciones de **gestión de costos**, rendimiento y alta disponibilidad. |
| **22** | ¿Cómo se aplican las **cuotas de compartimento** en OCI? | C. Por compartimento. |
| **34** | ¿Qué factor **NO** impacta el costo de ejecutar una instancia de máquina virtual en OCI? | D. El sistema operativo utilizado por la instancia VM. (Aunque puede haber costos de licencia, la forma, región y número son los principales impulsores). |
| **35** | En OCI, ¿qué permite a los clientes el modelo de precios de **Créditos Universales** (*Universal Credits*)? | C. Usar **créditos prepagos** para cualquier servicio de nube elegible. |