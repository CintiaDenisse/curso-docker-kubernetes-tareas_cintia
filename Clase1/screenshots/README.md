# Nombre de la aplicación - Elegi httpd y redis

# Comandos ejecutados 
a. Para el caso de Httpd ejecute el siguiente comando en ubuntu:
docker run -d --name mi-apache -p 8081:80 httpd

b. Para el caso de redis ejecute estos comandos en ubuntu:
docker run -d --name mi-apache -p 8081:80 httpd
docker logs mi-redis

# Comando docker run completo
a. para http es:
<img width="886" height="247" alt="image" src="https://github.com/user-attachments/assets/c12a44cd-0cc1-4c24-a11f-587bb7c4039a" />
<img width="886" height="264" alt="image" src="https://github.com/user-attachments/assets/43e51970-50da-4550-9db6-a4adf524ed35" />
<img width="886" height="313" alt="image" src="https://github.com/user-attachments/assets/a167e92d-498e-4324-8fb1-74ab071d65f5" />

b. Para redis es:

<img width="886" height="372" alt="image" src="https://github.com/user-attachments/assets/83025cbd-ddee-4b9b-99dd-6588aafab6c4" />
<img width="886" height="366" alt="image" src="https://github.com/user-attachments/assets/8b95f2ea-6d1c-4c00-9e15-c4a673daccdc" />
<img width="886" height="360" alt="image" src="https://github.com/user-attachments/assets/04e9801f-be6a-4b3b-aa38-78aad41281d3" />
<img width="886" height="215" alt="image" src="https://github.com/user-attachments/assets/0f34ee0b-5be0-4055-8a82-3acc59094819" />

# Comandos de verificación
<img width="1447" height="160" alt="image" src="https://github.com/user-attachments/assets/7c1c1d59-d328-43f0-9782-8135e1400b31" />
Verifica que los contenedores creados esten corriendo en el puerto correspondiente.
Para mi-redis, se verifica además con docker logs mi-redis que los logs esten en Ready  to accept connections.

# Comandos de limpieza
Primero se detiene los contenedores con: 
<img width="972" height="125" alt="image" src="https://github.com/user-attachments/assets/962e24c0-43ef-4a11-81a3-37b2ca34ee9e" />
 Luego se elimina los contenedores:
 <img width="762" height="122" alt="image" src="https://github.com/user-attachments/assets/d7a51fa3-f19f-402d-b6e5-27f9b90e37ab" />
Finalmente se elimina las imagenes:
<img width="1053" height="157" alt="image" src="https://github.com/user-attachments/assets/3eac3bae-79f6-4d0d-b678-e5178c6b313d" />

# Explicación breve de los flags usados
-d: Ejecuta el contenedor en segundo plano.
--name [nombre_contenedor]: Asigna un nombre personalizado al contenedor.
-p [puerto maquina local]:[puerto]: Mapea un puerto del contenedor a un puerto de la máquina local.
httpd o regis: Especifica la imagen que se usará.

# Conclusiones (opcional):
Este tipo de ejercicios me ayuda a comprender cómo se crean contenedores básicos y empezar a conocer su funcionamiento.

# Qué aprendi:
Con este ejercicio aprendí a desplegar contenedores de servicios básicos usando Docker y aprendi el uso de los comandos docker run, docker ps, docker logs, docker stop, docker rm y docker -d, además el poder ver este funcionamiento en el Docker desktop.

# Dificultades encontradas y cómo las resolviste
En cuanto a Docker no he tenido problemas, lo que me costo fue aprender a usar GitHup.
