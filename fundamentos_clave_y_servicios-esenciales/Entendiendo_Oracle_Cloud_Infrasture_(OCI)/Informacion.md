NUBE HIBRIDA

NUBE PUBLICA

NUBE PRIVADA


# ORACLE CLOUD INFRASTURE

DEVELOPER SERVICES

APPLICATIONS
DATA & AI
ANALYTICS
DATABASES
INFRASTUCTURE

GOVERNANCE & ADMINISTRATION

CLOUD REGIONS / CLOUD"CUSTOMER / HYBRID CLOUD / MULTI-CLOUD

## DEVELOPER SERVICES: LOW CODE, APPDEV, INFRASTRUTURE AS CODE

## APPLICATIONS: SERVERLESS, APP INTEGRATION, BUSINESS & INDUSTRY SAAS

## AI & DATA: BIG DATA, AI SERVICES, GENERATIVE AI

## DATABASES: ORACLE DATA BASES, DISTRIBUTED & OSS DATABASES

## CORE INFRASTRUCTURE: COMPUTE, CONTAINERS, OS, VMWARE, STORAGE, NETWORKING

## ANALITICS: BUSINESS ANALYTICS

## GOVERNANCE & ADMINISTRATION: CLOUUD OPS, SECURITY, OBSERVABILITY

COMMERCIAL AND GOVERNMENT REGIONS / MULTICLOUD / DEDICATED REGIONS / CLOUD REGIONS

# ARQUITECTURA

## REGION: AREA GEOGRAFICA LOCALIZADA, COMPRENDIDA DE UNA O MAS DOMINIOS DE DISPONIBILIDAD

## DOMINIO DE DISPONIBILIDAD(AVAILABILITY DOMAINS): SON UNO MAS CENTROS DE DATOS TOLERANTES A FALLAS UBICADOS DENTRO DE UNA REGION PERO CONECTADOS ENTRE SI MEDIANTE UNA RED DE BAJA LATENCIA Y ALTO ANCHO DE BANDA
*   ISOLADO UNO DE CADA OTRO, TOLERANTE A FALLAS, POCO PROBABLE QUE FALLE SIMULTANEAMENTE.
*   LA INFRAESTRUCTURA NO SE COMPARTE


## DOMINIOS DE FALLA(FAULT DOMAINS): ES UNA AGRUPACION DE HARDWARE E INFRAESTRUCTURA DENTRO DE UN DOMINIO DE DISPONIBILIDAD, SON COMO CENTROS DE DATOS LOGICOS
*   CADA DOMINIO DE DISPONIBILIDAD TIENE 3 DOMINIOS DE FALLO.
*   DATA CENTER LOGICO DENTRO DE UN DOMINIO DE DISPONIBILIDAD.


## EVITAR PUNTOS UICOS DE FALLA

### DATA GUARD: GENERA UNA REPLICA DE NUESTRA APLICACION

# ESCOGIENDO UNA REGION

## LOCALIZACION: ELEGIR UNA REGION QUE ESTE CERCA DE TUS USUARIOS PARA TENER UNA BAJA LATENCIA Y UN ALTO DESEMPEÑO
## RESIDENCIA DE DATOS Y CUMPLIMIENTO: MUCHOS PAISES TIENEN REQUEISITOS ESTRICOTS SOBRE EL ALMACENAMIENTO DE DATOS.
## DISPONIBILIDAD DE SERVICIOS: lOS NUEVOS SERVICIOS EN LA NUBE SE PONEN A DISPOSICION EN FUNCION DE LA DEMANDA REGIONAL, EL CUMPLIMIENTO NORMATIVO, LA DISPONIBILIDAD DE RECURSOS Y OTROS FACTORES

# ¿Qué concepto hace referencia a estar precavidos contra fallas dentro de un dominio de disponibilidad de OCI?

Dominio de fallas - Fault Domain

Los dominios de falla proporcionan una capacidad para proteger tus aplicaciones e instancias de fallas inesperadas de hardware o interrupciones de red dentro de un Dominio de Disponibilidad. Cada dominio de falla opera en su propio conjunto de hardware físico, por lo tanto, alguna falla que afecte a un dominio de falla no afecta a las instancias en otros dominios de fallo.

# ¿Qué afirmación sobre OCI NO es cierta?
Un único dominio de fallo puede estar asociado a múltiples dominios de disponibilidad dentro de una región.

Un dominio de fallo es una subdivisión de un dominio de disponibilidad. Cada dominio de disponibilidad contiene tres dominios de falla. Los dominios de falla permiten que distribuye tus instancias para que no estén en el mismo hardware físico dentro de un único dominio de disponibilidad. Un dominio de fallo no puede estar asociado a múltiples dominios de disponibilidad.

# ¿Qué servicio de Oracle Cloud Infrastructure NO está diseñado para una solución multicloud (nube múltiple)?
Oracle Roving Edge Infrastructure

Esta es la única opcion que no tiene el nombre de alg{un otro proveedor de nube, y a pesar que no se habló en videos sobre esta tecnología, lo importante es que sepas los nombres de otros proveedores como AWS, AZURE, GCP(Google Cloud Platform).

Oracle Roving Edge Infrastructure es un servicio que proporciona un dispositivo portátil y resistente que ejecuta un subconjunto de servicios OCI, diseñado para implementación de campo fuera de un centro de datos tradicional. No es un servicio Diseñado específicamente para la implementación multicloud. Por otro lado, servicios como el Oracle Database Service for Azure y Oracle Interconnect for Azure están diseñados para permitir que Oracle Cloud Infrastructure interactúe con Azure, indicando un enfoque multicloud. Oracle MySQL HeatWave es un servicio de análisis para el servicio de base de datos MySQL que se ejecuta en AWS, pero la gestión de cuentas, la facturación y la medición se hacen a través de OCI.

# Te suscribiste a una región OCI que tiene un dominio de disponibilidad. Deseas implementar una aplicación altamente disponible con dos servidores y una base de datos de 2 nodos. ¿Cómo colocarías los componentes para mantener la alta disponibilidad de la aplicación?
Poner un servidor y un nodo de la base de datos en un dominio de falla, y el segundo servidor y nodo de la base de datos en otro dominio de fallo

En este escenario, distribuir los servidores y nodos de base de datos en diferentes dominios de fallo dentro del mismo dominio de disponibilidad proporcionaría protección contra la falla de un único dominio de falla. Si un dominio de falla deja de estar disponible, el otro permanecería activo, garantizando la alta disponibilidad de la aplicación.

# ¿Qué afirmación sobre las regiones y los dominios de disponibilidad es cierta?
Una región OCI tiene uno o más dominios de disponibilidad

Una región OCI está compuesta por uno o más dominios de disponibilidad aislados e interconectados. Cada dominio de disponibilidad es una ubicación física separado dentro de una región. El número de dominios de disponibilidad por región puede variar; algunas regiones de la OCI tienen tres dominios de disponibilidad, mientras que otras un único dominio de disponibilidad.