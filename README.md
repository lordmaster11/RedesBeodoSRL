## Redes de Computadoras - Proyecto inicial


## Objetivo

La realización de un proyecto en el cual se integren todos los temas que incumben a la
primer parte de la materia. Este trabajo será defendido y explicado individualmente en
la instancia correspondiente a la evaluación de fin de curso o en la instancia de
integración.

## Presentación del Trabajo

Este trabajo será entregado con un informe del desarrollo del mismo en el cual se
detallen las tecnologías utilizadas y se justifiquen las elecciones de diseño
seleccionadas.
Deberá contener los siguientes apartados:
• Introducción. Marco teórico.
• Diseño de las capas (Servicios, protocolos, seguridad, etc.)
• Descripción de servicios de capa de aplicación implementados.
• Emulación (red emulada, planteo de la red en esquema reducido pero que
contenga todas las redes y servicios a implementar).
• Conclusiones, dificultades encontradas, etc.
El trabajo consta de la entrega de un informe y de la emulación de la red en esquema
reducido pero que contenga todos los servicios a implementar utilizando el programa
de emulación de redes recomendado por los docentes. La confección y entrega de
cada trabajo podrá ser grupal, pero la evaluación y defensa del mismo será individual
y en forma oral. Además los docentes decidiremos la evaluación complementaria en
forma oral o escrita de cualquier otro aspecto de la materia que se corresponda con
los temas dados hasta ese momento.
La entrega se realizará enviando por correo electrónico a la lista de docentes (tpi-docred@listas.unq.edu.ar) el archivo comprimido del trabajo a entregar (informe en
formato pdf + el archivo del emulador) y entregando el día de la evaluación una copia
impresa del informe.
El archivo enviado será un .zip o .7z. preferentemente no .rar el cual sera la
compresión de una carpeta que contiene el informe y archivo del Packettracer. La
carpeta y el archivo comprimido resultante deberá ser nombrado de la siguiente
forma, “Cx_Apellido.Nombre_Apellido.nombre_TPInicial_1_2019”. Donde Cx es
la comisión a la cual pertenece ( C1 -Mañana , C2- Noche) y Apellido.Nombre , son
los nombres de los integrantes del grupo.
Se valorará el cumplimiento de los objetivos, la calidad del informe, la preparación y la
buena presentación. Se evaluará de forma individual y grupal, de tal forma que la
colaboración y el trabajo en equipo serán importantes en la evaluación final de la
presentación.

### Detalle del trabajo a realizar

Se deberá desarrollar el proyecto de una red de datos para una Bodega “Beodo S.R.L.”
que cuenta con la siguiente condición geográfica y edilicia.

### Beodo S.R.L

La empresa posee 3 sedes, la principal situada en la Ciudad Autónoma de Buenos
Aires, otra en Mendoza y la última en San Juan.
En este trabajo desarrollaremos solamente el edificio de San Juan, que es de
propiedad íntegra de Beodo S.R.L y tiene 2 pisos.
En el 1º piso se encuentran SUM (20 puestos de trabajo), Atención al Público (5
puestos de Trabajo) y Departamento Comercial (3 puestos de trabajo)
En el 2º piso se encuentran Departamento de Administración (4 puestos de trabajo) y
Cuarto de Servidores y Conectividad (alojando 6 servidores).
En esta sede se utilizará un único segmento de red IP con direcciones públicas
pertenecientes al rango 192.168.145.64/26 ( 192.168.145.64 – 192.168.145.127).

### Conectividad
La sede obtendrá conectividad a Internet por medio de un enlace dedicado punto a
punto desde un router que se encuentra instalado físicamente en el cuarto de
servidores el que se encuentra conectado a una abstracción del servicio DNS con el
cual podrán hacer la delegación de zona a su dominio.

### Servicios y equipamiento
El nombre de dominio de Beodo S.R.L. será Beodo.com.ar, administrado por el
Departamento de Sistemas en los DNS primario y secundario de Beodo. Además se
delegará la administración del subdominio prensa.Beodo.com.ar al Departamento de
Prensa que administrará sus propios servidores DNS primario y secundario. Los
servidores DNS deberán ser completamente configurados en el emulador (registros
SOA, varios registros CNAME, MX, etc.).
Todos los dispositivos (PCs, laptops, smartphones, etc.), excepto aquellos equipos que
provean servicios o por algún motivo requieran IP estática, obtendrán sus
configuraciones de red utilizando el protocolo DHCP.
La sede contará con los siguientes servicios:
I. Dos servidores Web y dos servidores Web con protocolo seguro (HTTPS).
1. El servidor Web principal contendrá como mínimo un logo (imagen),
información general sobre Beodo, un enlace al listado de servicios brindados
utilizando listas y tablas al estilo del problema 1 de la práctica 4 (World Wide
Web) y un enlace al servidor del Departamento de Prensa.
2. El otro servidor Web estará dedicado al Departamento de Prensa y contendrá
como mínimo un logo, información general, un enlace a un listado de
destinos disponibles y otro al listado de sucursales.
3. Uno de los servidores Web seguros será dedicado al Departamento de
Prensa y contendrá como mínimo la pantalla de acceso al sistema de
publicaciones.
4. El otro servidor Web seguro contendrá la Intranet del sistema administrativo.
Sólo se deberá diseñar la página de inicio. Este servidor Web deberá ser
accedido solamente por los clientes del Departamento Administrativo; para
esto se deberá configurar adecuadamente el firewall local del servidor.
Se deberán desarrollar páginas HTML acordes con la función de cada uno de los
servidores.
II. Servicio de correo electrónico.
Todas las direcciones de correo electrónico serán de la forma
usuario@Beodo.com.ar.
En el emulador se deberá configurar el servidor de correo con al menos 3
usuarios y sus respectivos clientes.
III. Dos puntos de acceso wireless con los que se ofrecerán servicios a laptops,
tablets, smartphones, etc. Su identificación en la red será “Beodo”. El acceso a
ellos será asegurado con WPA2-PSK usando AES.
IV. Varias impresoras de red. Algunas de ellas wireless y otras conectadas por cable.
Todas las oficinas contarán con al menos un teléfono IP conectado a la red y a
una PC.

Se deberá tener en cuenta la distribución de los distintos servicios en los equipos
físicos prestando atención a la distribución de la carga, la seguridad y fiabilidad de la
red. Como regla general de seguridad informática los servidores deberán tener
operativos únicamente los servicios necesarios para realizar su función.
Con el objeto de analizar el tráfico de la red se instalarán dos sniffers. Uno será
ubicado entre los servidores y los clientes. El otro de manera de poder revisar el
tráfico de la red con Internet.

Se pide que desarrolle el proyecto implementando los servicios requeridos. Describa
los servicios auxiliares necesarios para que la red sea operativa indicando las
configuraciones básicas de los mismos. En la emulación implemente todos los
servicios utilizados.

