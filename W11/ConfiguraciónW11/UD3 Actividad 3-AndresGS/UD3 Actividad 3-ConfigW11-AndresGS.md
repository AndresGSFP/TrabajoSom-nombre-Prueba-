En la actividad anterior instalamos Windows 11 en una máquina virtual. Ahora vamos a realizar algunos pasos de configuración inicial.

Siguiendo las indicaciones y redacta un documento haciendo capturas de pantalla comentadas donde se indique.

Recuerda que todas las capturas de pantalla deben incluir la barra de título de VirtualBox donde aparezca tu nombre de usuario.

1. Configuración previa.

Con la máquina virtual apagada, cambia la configuración para que el sistema utilice 1024 MB de RAM y 1 CPU

📷 Haz una captura de pantalla del resumen de la máquina donde se vean los cambios aplicados.![](Aspose.Words.87ef8405-a365-439d-a2ef-a5c80706286f.001.png)

2. Configurar actualizaciones.

Inicia la máquina virtual, y una vez en el escritorio pulsa el botón de "Inicio" y ve a "Configuración"

En el panel de configuración podemos gestionar la mayoría de opciones de Windows. Ve a las opciones de "Windows Update"

Si has hecho bien la actividad anterior, la máquina virtual no debe tener acceso a Internet, al poner el adaptador de red en "Red interna". Esto lo hicimos para que Windows no empiece a descargar actualizaciones en nuestra máquina virtual sin nuestro permiso.

Entre las distintas opciones que aparecen, no hay ninguna que nos permita desactivar las actualizaciones, lo único que podemos hacer es pausar las actualizaciones.

📷 Cambia la configuración para pausar las actualizaciones durante 5 semanas y haz una captura de pantalla.

![](Aspose.Words.87ef8405-a365-439d-a2ef-a5c80706286f.002.png)

Otra cosa que podemos hacer es configurar las horas activas, para que el sistema no realice actualizaciones entre un rango determinado de horas.

Ahora, ve a "Opciones avanzadas" configura las "Horas activas" "Manualmente":

Hora de inicio: 8:00

Hora de finalización: 21:00

📷 Haz una captura de pantalla donde se vea el cambio

![](Aspose.Words.87ef8405-a365-439d-a2ef-a5c80706286f.003.png)

3. Desactivar por completo las actualizaciones.

Como hemos visto, desde el panel de configuración es imposible desactivar las actualizaciones, esto lo hace Microsoft por seguridad. Aunque para nuestra máquina virtual no necesitamos este nivel de seguridad y es más una molestia que una ayuda. Por esto vamos a desactivar por completo las actualizaciones automáticas. Esto lo haremos a través del editor de directivas de grupo, que permite un mayor control sobre el funcionamiento del sistema operativo.

Abre la ventana "Ejecutar" con la combinación de teclas Windows + R escribe la orden gpedit.msc y pulsa intro:

Se abrirá una nueva ventana, el "Editor de directivas de grupo local". En el panel izquierdo despliega:

Configuración del equipo

Plantillas administrativas

Componentes de Windows

Windows Update

Administrar la experiencia del usuario final

Haz doble clic en "Configurar Actualizaciones automáticas" y marca "Deshabilitada". 

Deshabilita también "Quitar acceso a la característica 'Pausar actualizaciones'" y "Permitir la descarga automática de actualizaciones sobre conexiones de uso medio"

📷 Haz una captura de pantalla donde se vean los cambios.

![](Aspose.Words.87ef8405-a365-439d-a2ef-a5c80706286f.004.png)

4. Instalar VirtualBox Guest Additions

VirtualBox Guest Additions es un software que puede instalarse en máquinas virtuales que aporta algunas características de accesibilidad mejorada y mejora el rendimiento del sistema invitado. En concreto, las ventajas que obtenemos al instalarlo son las siguientes:

Integración del puntero del ratón: Permite mover el ratón con libertad entre el sistema operativo anfitrión y el invitado.

Carpetas compartidas: Ofrece la posibilidad de acceder desde el sistema operativo invitado a una o varias carpetas del sistema operativo anfitrión, simplificando el intercambio de información entre ambos.

Soporte de vídeo mejorado: Permite que el sistema invitado se beneficie de los modos de vídeo avanzados y la aceleración gráfica del anfitrión (tanto 2D como 3D). Además, si el sistema invitado es Windows, GNU/Linux o Solaris, podremos elegir cualquier resolución de vídeo, sea o no estándar.

Ventanas integradas: Permite mostrar las ventanas del escritorio de la máquina virtual integradas en el escritorio del anfitrión, como si se tratara de sus propias ventanas.

Canal de comunicación genérico entre el invitado y el anfitrión: Permite el control y seguimiento del sistema invitado. Esto permite, por ejemplo, iniciar aplicaciones en el invitado desde el anfitrión.

Sincronización del reloj del sistema: Se mejora la sincronización del reloj del sistema entre el anfitrión y el invitado

Portapapeles compartido: Permite compartir el contenido del portapapeles del sistema invitado con el del anfitrión y a la inversa.

Arrastrar y soltar: Permite arrastrar archivos desde el ordenador anfitrión al invitado o a la inversa. Autenticación automática: Ofrece la posibilidad de iniciar sesión con una cuenta de usuario del sistema invitado desde el sistema anfitrión.

📷 Para instalar Guest Additions sigue los siguientes pasos:

Con la máquina virtual encendida, vé al menú de VirtualBox "Dispositivos" y "Insertar imagen de CD de las «Guest Additions»"

Ve al Explorador de archivos abre la unidad D: y ejecuta VBoxWindowsAdditions

Acepta todas las opciones por defecto del instalador y reinicia la máquina al final. Ahora en "Dispositivos" activa las opciones:

Portapapeles compartido : Bidireccional

Arrastrar y soltar : Bidireccional

Reduce el tamaño de la ventana de la máquina virtual para comprobar que el escritorio se adapta y no aparecen barras de desplazamiento.

Haz una captura de pantalla donde se vea el ajuste del escritorio al reducir el tamaño de la ventana.

*Al ser importada la máquina virtual hay que añadir una unidad de almacenamiento para que deje Insertar imagen de CD de las «Guest Additions*

![](Aspose.Words.87ef8405-a365-439d-a2ef-a5c80706286f.005.png)

5. Deshabilitar algunas aplicaciones del arranque.

Por último, vamos a desactivar algunas aplicaciones que se inician automáticamente al arrancar el sistema.

Ve al panel de "Configuración" > "Aplicaciones" > "Inicio" y deshabilita: "OneDrive" y "Microsoft Teams"

📷 Haz una captura de pantalla donde se vean los cambios.

![](Aspose.Words.87ef8405-a365-439d-a2ef-a5c80706286f.006.png)
