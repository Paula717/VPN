
<H1><div align=center>CONFIGURACION DE VPN CON MIKROTIK</H1>

<div align=center><img src="img/img01.gif"></div>

<text style = "display:block; text-align: justify"> Con la Ayuda del software **RouterOS Winbox** la cual es una aplicación que nos permite la administracion de **Mikrotik** usando una interfaz gráfica. El cual incluye una sofisticada tecnología para realizar estas conexiones basada en el sistema operativo RouterOS. Este software permite a sus usuarios realizar conexiones vía FTP, telnet y SSH.

<text style = "display:block; text-align: justify"> Utilizaremos el protrocolo IPSEC/L2TP para lograr la conexion con el VPN que vamos a configurar, ya que este protocolo estandar que ya viene
en la mayoria de dispositivos de computo y moviles actualmente y de esta forma no utilizar clientes de terceros.

Primero vamos a ir al botón de **PPP**  
<div align=center><img src="img/img02.jpg"></div>

Luego a **Profiles** y al botón **+**
<div align=center><img src="img/img03.jpg"></div>

<text style = "display:block; text-align: justify">En este apartado, crearemos un perfil de la siguiente forma:
<div align=center><img src="img/img04.jpg"></div>

<text style = "display:block; text-align: justify"> Luego vamos al apartado de **Protocols** y lo configuramos de la siguiente form (despues solo le damos en el Boton de **OK** ):
<div align=center><img src="img/img05.jpg"></div>

<text style = "display:block; text-align: justify"> Despues de terminar con la configuracion del perfil vamos a crear un usuario dandole al botón de Secrets, donde pondremos un Nombre de usuario,
contraseña, servicio y seleccionamos el Perfil que hicimos anteriormente, Ejemplo:
<div align=center><img src="img/img06.jpg"></div>

<text style = "display:block; text-align: justify"> Continuamos nuestra configuración en el botón de **Interface** luego le damos en el botón de **L2TP Server** y configuramos el apartado de la siguiente forma:
<div align=center><img src="img/img07.jpg"></div>

<text style = "display:block; text-align: justify"> Luego solo le damos en **Apply** y **OK**

De esta forma ya tendriamos configurada nuestra VPN, pero necesitamos abrir unos puertos en la parte de **Firewall** para que la VPN funcione correctamente.
Para esto nos vamos al botón de **IP**
<div align=center><img src="img/img08.jpg"></div>

<text style = "display:block; text-align: justify"> Luego damos click en el **+** y añadiremos una por una estas 2 reglas que veremos en el siguiente listado:
<div align=center><img src="img/img09.jpg"></div>

<text style = "display:block; text-align: justify"> En la primera lo configuraremos de la siguiente forma: 

En **General** <div align=center><img src="img/img10.jpg"></div>

En **Action** <div align=center><img src="img/img11.jpg"></div>

Y en al segunda Regla: 

En **General** <div align=center><img src="img/img12.jpg"></div>  

En **Action** <div align=center><img src="img/img13.jpg"></div>

<text style = "display:block; text-align: center"> **Y listo, eso seria todo ☻.**
<div align=center><img src="img/img14.gif"></div>

 Solo nos quedaria conectarnos a la VPN que hemos creado para comprobar que este funcionando. Para esto lo haremos por medio del dispositivo movil de la siguiente forma: