# Docker for cybersecurity

### Ex00 - Docker funciona?

```docker --version```

### Ex01 - Hello World

```docker run hello-world```

### Ex02 - Ubuntu!

```docker run -it debian bash```

### Ex03 - Una página web!

```docker build -t miweb ex03```

-t : nombre de la imagen

```docker run -p 80:80 miweb```

-p puerto:puerto

```docker run -p 80:80 -d miweb```

-d : "detached" o en segundo plano

```docker ps```

### Ex04 - Volúmenes

```docker build -t miweb ex04```

```docker run -v "$(pwd)":/usr/share/nginx/html -p 80:80 miweb```

### Ex05 - Mi propio sistema operativo

Puedes crear un SO con tus propias dependencias:
    Ejemplos:

- net-tools
- vim
- python3
- nmap
- john
- ...


```docker

FROM debian:bullseye
RUN apt-get update && apt-get install -y net-tools vim python3 nmap john
CMD ["/bin/bash"] 

```

### Ex06 - Comandos útiles

Ver contenedores en uso: 

``docker ps``

Detener un contenedor:

``docker stop <id>``


Ejecutar un comando en un contenedor que ya está corriendo
    
    ``docker exec -it <id> <comando>``

    ``docker exec -it ubuntu bash``

Detener todos los contenedores en uso:

``docker stop $(docker ps -a -q)``

Eliminar todos los contenedores (botón rojo)

``docker system prune -af``

El MEJOR comando de todos:

``docker help``

``docker help start``

...

``docker help <<comando>>``