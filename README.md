



# Proyecto de almacén de datos en tiempo real Snowflake para principiantes-1



En este proyecto de almacenamiento de datos de Snowflake, aprenderá a implementar la arquitectura Snowflake y a crear un almacén de datos en la nube para ofrecer valor empresarial.

¿Que aprenderás?

* Introducción al copo de nieve
* Comprender la arquitectura de los copos de nieve
* Comprender la seguridad en Snowflake
* Preparación de archivos
* Configuración de configuración para Snowflake
* Cargando datos a través de la interfaz web
* Cargando datos a través de SnowSQL
* Cargando datos usando el proveedor de la nube
* Transmisión de datos usando Snowpipe
* Visualización usando QuickSight
* Comprender el precio de Snowflake
* Viaje en el tiempo en copo de nieve
* Optimización del rendimiento en Snowflake

Descripción del Proyecto

## visión general del negocio

Data Cloud de Snowflake se basa en una plataforma de datos de vanguardia entregada como servicio (SaaS). Snowflake proporciona soluciones analíticas, de procesamiento y almacenamiento de datos que son más rápidas, fáciles de usar y más versátiles que las opciones tradicionales.

Snowflake no se basa en ninguna tecnología de base de datos actual ni en plataformas de software de grandes datos como Hadoop. Snowflake, por otro lado, combina un nuevo motor de consultas SQL con una arquitectura de nube de vanguardia. Snowflake ofrece a los usuarios todas las funciones y capacidades de una base de datos analítica empresarial, y mucho más.

* No hay hardware para elegir, instalar, configurar o administrar (virtual o real).
* No hay mucho que instalar, configurar o mantener en términos de software.
* Snowflake supervisa el mantenimiento, la administración, las actualizaciones y los ajustes continuos.

Snowflake se basa completamente en la infraestructura de la nube. A excepción de los clientes, controladores y conectores de línea de comandos opcionales, todos los componentes del servicio de Snowflake operan en infraestructuras de nube pública.

Las demandas informáticas de Snowflake se satisfacen mediante instancias informáticas virtuales y los datos se almacenan permanentemente a través de un servicio de almacenamiento. Snowflake no es compatible con entornos de nube privada (locales o alojados).

La arquitectura de Snowflake es una combinación de diseños clásicos de bases de datos de disco compartido y de nada compartido. Snowflake emplea un repositorio de datos central para datos persistentes, como arquitecturas de disco compartido, disponibles en todos los nodos informáticos de la plataforma. Snowflake ejecuta consultas utilizando clústeres de computación MPP (procesamiento masivo en paralelo), en los que cada nodo del clúster almacena una parte de todo el conjunto de datos localmente, como arquitecturas sin compartir. Este método combina la simplicidad de un diseño de disco compartido con la velocidad y las ventajas de escalamiento horizontal de una arquitectura sin compartir.

 Los componentes del copo de nieve incluyen:

* Almacén/Almacén Virtual
* Base de datos y esquema
* Mesa
* Vista
* Procedimiento almacenado
* tubo de nieve
* Arroyo
* Tarea
* Viaje en el tiempo

## **Objetivo del proyecto de análisis en tiempo real de Snowflake**

En este proyecto en tiempo real de Snowflake, aprenderá sobre la arquitectura del almacén de datos de Snowflake y en qué se diferencia de los almacenes de datos tradicionales. Aprenderá cómo implementar la arquitectura de almacén de datos Snowflake para crear un almacén de datos para aplicaciones comerciales. Además, este proyecto Snowflake le presentará varias tecnologías modernas como SnowSQL, Quicksight, etc. Cargará datos masivos desde la interfaz web, desde SnowSQL y un proveedor de la nube (Amazon S3 en este caso).

<iframe class="embed-responsive-item" title="reproductor de vídeos de youtube" src="https://www.youtube.com/embed/5IjiCo-grwI" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen" loading="lazy" speechify-initial-font-family="Montserrat" speechify-initial-font-size="16px"></iframe>

### **Pila de tecnología:**

➔ Idiomas: SQL

➔ Servicios: Amazon S3, Snowflake, SnowSQL, QuickSight, SnowPipe

### **SnowSQL**

SnowSQL es un cliente de línea de comandos de próxima generación para conectarse a Snowflake y ejecutar consultas SQL, y realizar todas las acciones DDL y DML, como cargar y descargar datos de tablas de bases de datos. Trabajará con SnowSQL para cargar los datos para este proyecto de almacenamiento de datos en tiempo real de Snowflake. Es una base de datos 'customer_detail' que consta de varios detalles del cliente como nombre, apellido, dirección, etc. Inicialmente, carga los datos en la etapa (PIPE_CLI_STAGE), desde donde Snowflake los carga en la tabla para su posterior procesamiento.

### **SnowPipe**

SnowPipe es un servicio administrado de Snowflake que ayuda principalmente a cargar datos de transmisión, es decir, permite que Snowflake cargue datos tan pronto como estén disponibles en la etapa. SnowPipe ayuda a construir un almacén de datos de Snowflake para empresas que involucran datos de transacciones o cualquier dato que necesite procesamiento inmediato. Este proyecto Snowflake de almacenamiento de datos implica la creación de un SnowPipe para cargar el conjunto de datos de muestra en forma de transmisión en la tabla.

### **amazon s3 **

Amazon S3 es un servicio de almacenamiento de objetos que proporciona escalabilidad de fabricación, disponibilidad de datos, seguridad y rendimiento. Los usuarios pueden guardar y recuperar cualquier cantidad de datos utilizando Amazon S3 en cualquier momento y desde cualquier ubicación. Este proyecto Snowflake implica cargar datos (datos de stock reales de Tesla) en Amazon S3, que aquí se considera una etapa externa. 

### **QuickSight**

Amazon QuickSight es un servicio de inteligencia empresarial (BI) escalable, sin servidor, integrable y basado en aprendizaje automático creado para la nube. Puede conectarse a varias fuentes como Redshift, S3, Dynamo, RDS, archivos como JSON, texto, CSV, TSV, Jira, Salesforce y el servidor Oracle SQL local. Es el primer servicio de BI que ofrece precios de pago por sesión, donde solo paga cuando los usuarios acceden a sus paneles o informes, lo que lo hace rentable para implementaciones a gran escala. Este proyecto Snowflake dwh le muestra cómo aprovechar AWS Quicksight para visualizar varios patrones en el conjunto de datos. Utiliza Quicksight para crear un panel utilizando los datos de acciones de Tesla en Snowflake. Una vez que conecte Quicksight con Snowflake, podrá crear el panel cargando y analizando el conjunto de datos. Para los datos del precio de las acciones de Tesla, el tipo de gráfico más apropiado es un gráfico de líneas, ya que muestra adecuadamente el aumento y la caída de los precios de las acciones. Dependiendo de los requisitos comerciales, también puede crear diferentes paneles, como gráficos de barras verticales, gráficos de líneas de área, etc. Una vez que esté satisfecho con el panel, puede publicarlo.

## **Arquitectura**

![Proyecto de almacén de datos en tiempo real Snowflake para principiantes-1](https://projex.gumlet.io/snowflake-real-time-data-warehouse-project-for-beginners/images/image_462324121646724219297.png?w=900&dpr=1.0 "Proyecto de almacén de datos en tiempo real Snowflake para principiantes-1")

Aunque Snowflake no necesita muchas técnicas de optimización, hay algunos puntos a tener en cuenta:

* Debe haber un almacén virtual dedicado e independiente para manejar diferentes cargas de trabajo.
* El tamaño de estos almacenes virtuales debe incrementarse dependiendo del patrón de las consultas.
* Intente maximizar el uso de la caché en caso de volver a ejecutar consultas y reducir los costos de cálculo.

### **Preguntas frecuentes**

1. #### **¿Por qué es tan valioso Snowflake?**

Snowflake proporciona intercambio colaborativo de datos, lo que lo distingue de otros marcos. Tiene una escalabilidad infinita y perfecta en Amazon Web Services (AWS) y Microsoft Azure y también en otras nubes.

2. #### **¿Cómo optimiza Snowflake las consultas?**

Snowflake utiliza varios métodos para optimizar el rendimiento de las consultas, como maximizar el uso de la caché, utilizar el servicio de optimización de búsqueda, agrupar tablas, etc.
