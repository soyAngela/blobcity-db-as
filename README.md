# Cliente de BlobcityDB en Docker
Este Docker Compose inicia un contenedor con una imagen de BlobCityDB (https://hub.docker.com/r/blobcity/db) y otro que ejecuta una aplicacion cliente que inserta datos en esta.
La aplicación esta encapsulada en *Docker* y puede ser construida mediante el Dockerfile o se puede encontrar en el siguiente repositorio público de *DockerHub*: https://hub.docker.com/r/soyangela/blobcity-db-client.

Para poner todo en funcionamiento sera necesario ejecutar los siguientes comandos en la carpeta contenedora del archivo *docker-compose.yml*.

**Atención**: Es necesario ejecutar el script de cambio de contraseña *password-changer-blobcitydb.sh* la primera vez que se ejecutan los contenedores para que el cliente funcione conrrectamente. 
```bash
sudo docker compose up -d
chmod +x password-changer-blobcitydb.sh
./password-changer-blobcitydb.sh
sudo docker compose down
```

Finalmente poner en marcha el cliente con:

```bash
docker compose up
```

Estos procedimeintos estan mejor explicados en el documento EntregaIndividual_AngelaGonzalez.pdf.
