# despr2_1

# 1.Creacion de la VM
 Crea una VM como clon enlazado de la VM ba­se Ubuntu-Server-Base.ova proporcionada en el repositorio del curso:

[Captura 1](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%201.png)

Configura la red: Adaptador 1 en NAT + Port-Forward (host 8081 → guest 80; host 2223 → guest 22):
[Captura 2](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%202.png)

# 2.Preparacion del entorno 
Inicia la VM y accede por SSH desde el host:
[Captura 3](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%203.png)
Actualiza paquetes:
[Captura 4](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%204.png)
Instala apache2:
[Captura 5](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%205.png)
Configura el firewall para permitir tráfico HTTP y HTTPS:
[Captura 6](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%206.png)
Verifica que las reglas se han aplicado:
[Captura 7](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%207.png)
está configurado, habilita el tráfico ssh, HTTP y HTTPS:
[Captura 8](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%208.png)

Habilita el firewall si no está habilitado:
[Captura 9](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%209.png)

# 3.Comprobación básica
Comprueba que el servicio está activo:
[Captura 10](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%2010.png)
Desde el host, accede a http://localhost:8081/ y comprueba que ves la página por defecto de Apache. Haz una captura de pantalla.
[Captura 11](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%2011.png)

# 4.Desplegar sitio de ejemplo
Utiliza scp desde tu máquina local:
[Captura 12](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%2012.png)
Luego, en la VM:
[Captura 13](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%2013.png)
Comprueba que si recargas http://localhost:8081/ ves una página en blanco (o error 404). Ahora, copia los archivos:
[Captura 14](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%2014.png)

La dificultad que encontre es que el sudo cp -r no se realizaba y no pude seguir la practica hasta la ultima que hice la snapshot

# 5.Comprobar

# 6.Apaga la VM y crea un snapshot llamado After-Apache-Deployment para posibles futuras prácticas.

[Captura 15](https://github.com/braiscastro/despr2_1/blob/main/img/Captura%2015.png)
