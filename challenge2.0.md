# Podman Tarea 1: Contenerice una aplicacion JBoss
Escriba un Dockerfile para contener una aplicacion JBoss EAP 7.4 para cumplir con todos los siguientes requisitos:

 - Utilice la ultima version de Red Hat Universal Base Image 8 ubi8 del registro registry.access.redhat.com como base.
 - Instale el paquete java-1.8.0-openjdk-devel.
 - Cree un grupo de sistema para jboss con un GID de 1100.
 - Cree un usuario del sistema para jboss con un UID 1100.
 - Establezca el directorio de inicio del usuario de jboss en /opt/jboss.
 - Establezca el directorio de trabajo en el directorio de inicio del usuario de jboss.
 - Cambie recursivamente la propiedad del directorio de inicio del usuario de jboss a jboss:jboss.
 - Exponga el puerto 8080.
 - Haga que el contenedor se ejecute como usuario de jboss.
 - Descomprima el archivo jboss-eap-7.4.0.zip en el directorio /opt/jboss.
 - Establezca la variable de entorno JBOSS_HOME en /opt/jboss/jboss-eap-7.4.
 - Inicie el contenedor con el siguiente ejecutable: /opt/jboss/jboss-eap-7.4/bin/standalone.sh -b 0.0.0.0 -c standalone-full-ha.xml.
Antes de comenzar, inicie sesion en el portal de desarrolladores de Red Hat y descargue el archivo jboss-eap-7.4.0.zip en su directorio de trabajo. Consulte el enlace web a continuacion (se requiere una cuenta de Red Hat):
https://developers.redhat.com/content-gateway/file/jboss-eap-7.4.0.zip

# Podman Tarea 2: Construir una imagen de contenedor JBoss y corra un contenedor
Use el comando podman para crear una imagen de contenedor con Dockerfile de la tarea 1 y cree un nuevo contenedor a partir de la imagen para cumplir con todos los requisitos siguientes:

 - Etiquete la imagen del contenedor como jboss-eap:7.4.0.
 - Cree un nuevo contenedor en detached mode.
 - Nombre el contenedor jboss-from-dockerfile.
 - Reenvio de puerto desde el puerto de host 38080 al puerto de contenedor 8080.
 - Inspeccione el contenedor en ejecucion para determinar sus argumentos (Args). Puede utilizar el siguiente formato JSON: '{{.Args}}'.
 - Recupere las ultimas 15 lineas de los registros del contenedor en ejecucion.

# Podman Tarea 3: Guarde la imagen de contenedor
Realice las siguientes tareas:

 - Guarde la imagen del contenedor jboss-eap:7.4.0 en el archivo jboss-eap-7.4.0-backup.tar.
 - Actualice el contenedor jboss-from-dockerfile en ejecucion y reemplace el contenido del archivo /opt/jboss/jboss-eap-7.4/welcome-content/index.html con una sola palabra JBOSS.
 - Detenga el contenedor jboss-from-dockerfile en ejecucion y confirme sus cambios para crear una nueva imagen de contenedor.
 - La nueva imagen del contenedor debe llamarse jboss-eap y tener una etiqueta de 7.4.0-dev.
 - El nombre del autor de la nueva imagen del contenedor debe establecerse en "Home Lab".


## No olvides enviar un documento con los comandos que ejecutaste para darle OK al reto
## Exitos !!!