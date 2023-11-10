# pr-ctica1.2DNS


Se debe poder resolver ips en una máquina Linux con un DNS funcionando, para ello:

Instalaremos bind9 en la máquina virtual con “sudo apt install -y bind9”. Ya instalado vemos el estado de bind9 y con → “systemctl status bind9” y a continuación tenemos que ver que está activo (running).

Ahora configuramos los archivos creados en /etc/bind y /var/lib/bind. Primero configuraremos los archivos de /etc/bind, poniendo y modificando los archivos de configuración. Después iremos a /var/lib/bind y tendremos que crear la base de datos (si todo se ha hecho bien, la carpeta de dicha ruta de bind debería estar vacía).

Después de hacer esto, ponemos la máquina en adaptador puente por ejemplo en Modo Promiscuo para que otras máquinas puedan detectarla o hacer (en nuestro caso), Digs. 

Entramos en la Terminal y tendremos que ver la IP de nuestra máquina y comprobar que está con el puerto 53 (el determinado). Lo haremos con la siguiente herramienta → “netstat -ptan” para ver nuestra interfaz DNS (IP) que se creó con “adaptador puente” con el puerto 53 (es el determinado).

Finalmente, ya solo hacemos dig @[Dicha IP] test.asircastelao.int (por ejemplo) y nos debería devolver (o solucionar) la dirección IP que haya en nuestra base de datos con ese dominio.
