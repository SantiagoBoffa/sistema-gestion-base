# Sistema de Gestión Wow

##### Probar el sistema con docker-compose:


```bash
# descargar el repositorio
git clone https://github.com/Clementina-coop/sistema-gestion-base.git

# Entrar al direcotrio del proyecto
cd sistema-gestion-base

# generar imágenes de docker
docker-compose build

# levantar el sistema
docker-compose up

# cargar datos iniciales en una nueva terminal
bash utils/restore_docker_local.sh data/bk_20200409_200353 bonsai-db
```

Abrir el navegador en [http://localhost:3000](http://localhost:3000) y loguearse con:

Usuario => admin@proyectowow.com.ar

Contraseña => 123456

##### Para desarrollo

**Backend**

El backend está desarrollado con [FeathersJS](https://feathersjs.com/) y se encuentra en la carpeta **back**.

Configurar en el archivo **.env** la variable **MONGO_DB** con la configuración de conexión a la base de datos.

Cargar el backup de la carpeta data en la base de datos mongo.

```
cd back
npm install
npm start
```

**Frontend**

El backend está desarrollado con [React Admin](https://marmelab.com/react-admin/) y se encuentra en la carpeta **front**

```
cd front
yarn install
yarn start
```
