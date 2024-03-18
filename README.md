# raspi-docker-stack

- Instalo Libreelec
- Configuro lenguaje, nombre equipo, etc...
- Activo ssh desde dentro de libreelec (Hay que conectarla a un monitor)
- Instalo en addon de docker en libreelec
- Abro consola 192.168.50.120
- Pruebo si el comando docker funciona.
- Instalo Portnainer
	> docker volume create portainer_data
	> docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
	
- Una vez finalice ya puedo entrar en la web http://192.168.50.120:9443
- Creo usuario y password.
- Creo un nuevo stack:
  - Transmission:
      https://hub.docker.com/r/linuxserver/transmission
  - WireGuard Easy (https://github.com/wg-easy/wg-easy):
      
    - Abrir el puerto correspondiente en el router.

  - Teamspeak (https://hub.docker.com/r/ertagh/teamspeak3-server):

    - Abrir el puerto correspondiente en el router.

    - Al iniciar el teamspeak, la primera vez que te conectas al servidor copiar el token de uno de los archivos log en /storage/data/teamspeak/save/log/
  
  - CS2 server (https://github.com/joedwards32/CS2)
       
