# Lab4.3


Buen dia para poder ejecutar el laboratorio se tiene que instalar node js y despues ir a la carpate del proyecto y ejecutar node indez


Ej:
cd Lab4.3
node index

Comando para que cuando el balandeador de carga cree instancias y active la pagina web
#!/bin/bash

cd /home/ec2-user/Lab4.3

/home/ec2-user/.nvm/versions/node/v12.4.0/bin/node index.js

El proyecto se creo de la siguiente manera

Se creo una instancia en aws y se cargo el proyecto instalando node js
Despues se creo una imagen de la instancia que tenia el proyecto instalado.
Se procedio a crear un grupo de autoescalado que utilizaba esa instancia ahi se definio Cuando se inician las instancias, si especificó varias Zonas de disponibilidad, la capacidad deseada se distribuye a través de estas Zonas de disponibilidad. Si se produce una acción de escala, Amazon EC2 Auto Scaling mantiene automáticamente el equilibrio en todas las zonas de disponibilidad que especifique.

Despues se creo el ELB que es el balanceador de carga del autoscaling group aqui se definen cuando es que las instancias deben ser creadas o eliminadas distribuyendo la carga entre las instancias con un DNS que distribuye a las ips de las instancias las cargas depues de haber creado el ELB se tiene que adjuntar al grupo de auto escalado para que funcione

Despues de haber realizado el ELB se procede a realizar una prueba de stress sobre los cpus con un programa y se verifica el funcionamiento del autoescalado ascendente y descendente es muy interesante como funciona el laboratorio.


