# Using HDFS

Inicialmente debemos ingresar a nuestro master node vía ssh
- Creamos directorio para cargar datos

```
hdfs dfs -mkdir /user/hadoop/datasets
```

- Cargamos los datasets desde local hasta la instancia
![imagen](https://user-images.githubusercontent.com/53027815/170852525-b1ac16af-221a-4016-a38e-ed1956567592.png)

- Una vez cargados en la instancia, las agregamos a hdfs
![imagen](https://user-images.githubusercontent.com/53027815/170852539-e60c12fa-501a-4884-bae4-962940a2cf62.png)

- Listamos lo que hay en el directorio
![imagen](https://user-images.githubusercontent.com/53027815/170852551-a74ba07b-550c-42b4-a455-9779c74b67f7.png)

# Using HUE

- Vamos a HUE, y creamos los directorios ~/datasets/hue
![imagen](https://user-images.githubusercontent.com/53027815/170852616-3d227fa5-5316-42cb-801a-6a988ffdb524.png)

- Luego cargamos los datasets
![imagen](https://user-images.githubusercontent.com/53027815/170852630-1b8b0ba2-095d-4e41-b39d-328aec9081fd.png)

- Vemos los datos desde HUE
![imagen](https://user-images.githubusercontent.com/53027815/170852643-4990fc4a-2ce8-4b12-8771-d4952ecd7b2c.png)

# Using S3

- Vamos a la opción de S3 de HUE y creamos en el bucket los directorios datasets/hue
![imagen](https://user-images.githubusercontent.com/53027815/170852659-c6f23e6b-9375-4704-aa74-a98e285e1be3.png)

- Luego cargamos los datasets
![imagen](https://user-images.githubusercontent.com/53027815/170852687-65a70efe-7f96-48a0-941b-9b7d93931e44.png)

# Using HDFS + S3

- Ingresamos a la consola de hadoop
![imagen](https://user-images.githubusercontent.com/53027815/170852730-d43b0b3f-537f-4fc8-bd3a-9548047f4127.png)

- Copiamos de hdfs a s3
![imagen](https://user-images.githubusercontent.com/53027815/170852745-2a5c7a78-a337-4032-99e0-87bc4ba58ca5.png)

- Así queda desde s3
![imagen](https://user-images.githubusercontent.com/53027815/170852767-2798e85a-caaf-4629-abf0-a16c864b59f1.png)


- Para hacer el bucket público vamos a permissions
![imagen](https://user-images.githubusercontent.com/53027815/170852789-20f9a24e-d441-4d1d-ba40-25a4cc99f974.png)

- Quitamos el block public access
![imagen](https://user-images.githubusercontent.com/53027815/170852801-33351d77-4222-4a22-8138-bd5edbcbc0d8.png)

- Editamos la policy

Y así quedan nuestros buckets:
- https://notebooksmhl.s3.amazonaws.com/datasets_from_hadoop/
- https://notebooksmhl.s3.amazonaws.com/datasets/

