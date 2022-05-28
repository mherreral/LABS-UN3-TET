# EMR
## Creando el clúster
Para crear un clúster EMR debemos ingresar a la consola EMR de AWS y darle en nuevo clúster, allí nos vamos por opciones avanzadas de configuración
![imagen](https://user-images.githubusercontent.com/53027815/170834900-0c049bd0-fd6c-4d37-bde9-b914a242a9d5.png)
![imagen](https://user-images.githubusercontent.com/53027815/170834918-decc2f5b-d92b-400d-8641-f13fe993ce22.png)

Luego seleccionamos la versión 6.3.1 de EMR y las aplicaciones que usaremos
![imagen](https://user-images.githubusercontent.com/53027815/170835015-a553b1b8-281d-45e7-8e3b-57e0daa1c0c8.png)

Especificamos los catálogos de datos a usar
![imagen](https://user-images.githubusercontent.com/53027815/170835037-f4364c27-cb28-446d-a6a8-554fec13d927.png)

Asociamos un bucket a nuestro EMR
![imagen](https://user-images.githubusercontent.com/53027815/170835063-ac138fe4-d2f3-47f4-8b45-187a5b734ad3.png)

Luego vamos a la consola de S3 Y creamos un bucket con el mismo nombre

Importante: en las configuraciones de hardware debemos cambiar las instancias a m4.xlarge y por instancias spot.

Luego le damos guardar y crear clúster.

## Utilizando EMR
Cuando el clúster esté corriendo, vamos y editamos el security group del máster, agregándole los puertos que usan las aplicaciones mencionadas anteriormente, además verificamos que tengamos acceso vía SSH al máster (puerto 22)
![imagen](https://user-images.githubusercontent.com/53027815/170835082-5753f394-5c68-4a7a-a87b-1fbc9ffce7e2.png)

Una vez tengamos esto, podemos ir a la definición del clúster, y allí accedemos a las aplicaciones, inicialmente vamos con HUE, allí debemos crear un usuario hadoop con cualquier contraseña, y esto nos lanzará la siguiente consola
![imagen](https://user-images.githubusercontent.com/53027815/170835233-f621989c-afd8-4c61-88de-9fd177c81e17.png)

Luego podemos entrar a jupyterhub, allí también necesitaremos un usuario por defecto, que es jovyan, con clave jupyter, allí podremos crear notebooks
![imagen](https://user-images.githubusercontent.com/53027815/170835271-8d9fbfed-ca21-4628-b162-f416ad785e5b.png)

Los notebooks creados se guardarán en nuestro bucket
![imagen](https://user-images.githubusercontent.com/53027815/170835284-59739598-edaa-4ab5-b92f-d5d80eaad159.png)


