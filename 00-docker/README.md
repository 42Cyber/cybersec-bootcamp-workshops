# Docker for cybersecurity

### Ex00 - Docker funciona?

```docker --version```


### Ex01 - Hello World

```docker run hello-world```

### Ex02 - Ubuntu!

```docker run -it ubuntu bash```

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

