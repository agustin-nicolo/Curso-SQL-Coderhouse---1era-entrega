# Curso-SQL-Coderhouse---1era-entrega

<img width="520" height="343" alt="image" src="https://github.com/user-attachments/assets/287388c6-8abb-4513-b0d2-166a2ce4150f" />

**Introducción:**

En esta presentación se abordará la temática comercial y crediticia de una entidad bancaria, relacionando el área comercial tanto con su propia área de créditos como con los clientes de la entidad (segmento empresas), buscando eficientizar el proceso de ventas y mejora de la comunicación. 

**Objetivo:**

El principal objetivo es lograr que el área comercial logre más ventas, por lo que se busca mejorar la comunicación tanto interna (sector comercial – sector de créditos) como externa (sector comercial – cliente) permitiendo una mejor administración de cartera y generando oportunidades de negocios. 

**Situación problemática:**

Existe una falta de eficiencia entre la comunicación interna de la entidad (sector comercial – sector de créditos), la cual provoca una pérdida de tiempo y dificulta la buena administración de la cartera de clientes. A su vez, la entidad está frente al desafió de incrementar sus ventas para continuar creciendo.  

**Modelo de Negocio:**

Dado que la entidad bancaria subsiste con la prestación y/o venta de productos crediticios y/o de dinero y por otro lado con la recepción de depósitos de dinero de sus clientes, se buscará poner a disposición un esquema ordenado de datos y un historial de comportamiento de clientes, buscando que el sector comercial tenga las herramientas necesarias para incrementar sus ventas, conociendo y administrando mejor a los clientes. 
Se utilizará la información estructural del cliente, ya sea nombre, actividad, sector económico, entre otros, como así también su legajo crediticio con información contable y financiera.  A su vez, se utilizará y relacionará información de productos disponibles para su venta como el historial de ventas realizadas. 
Se buscará la mejora de procesos, a partir de los recursos y herramientas disponibles en la entidad. 

**Descripción de la tabla:**

a)	Tabla “clientes”: Detalla la información estructural del cliente 

-	Id_ cliente (CLAVE PRIMARIA)
-	Razón social
-	Sector económico
-	Actividad
-	Línea de crédito (activo/inactivo)

b)	Tabla “legajo_crediticio”: Detalla su historial de crediticio en la entidad

-	Id_legajo (CLAVE PRIMARIA)
-	Id_ cliente (CLAVE FORANEA con Id_cliente de la TABLA CLIENTES)
-	Monto_calificado
-	Fecha_calificacion
-	Fecha_vencimiento (de la linea de crédito)
-	Fecha_informacion (ultima información presentada por el cliente y analizada)
-	Facturación (cuando vende el cliente por mes)
-	Deuda (que deuda tiene el cliente en el sistema financiero)

c)	Tabla “productos”: Detalla el listado de productos que vende la entidad

-	Id_ producto (CLAVE PRIMARIA)
-	nombre

d)	Tabla “ventas”: Detalla el historial de ventas de la entidad por cada cliente

-	Id_ venta (CLAVE PRIMARIA)
-	Id_ cliente (CLAVE FORANEA con Id_cliente de la TABLA CLIENTES)
-	Id_producto (CLAVE FORANEA con Id_producto de la TABLA PRODUCTOS)
-	Fecha_venta
-	Monto
-	Tasa
-	Plazo

