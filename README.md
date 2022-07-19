# Real World Vue 3

Creación de un proyecto mediante **CLI** (Command Line Interface) vista por **UI** (User Interface)

La **Vue CLI** es un sistema completo para el rápido desarrollo con Vue. Nos permite seleccionar las librerías a usar en nuestro proyecto, incorporándose automáticamente al mismo. Configura un _Webpack_ donde archivos _Javascript_, _CSS_ y sus dependencias, se agrupan correctamente y se optimizan en el momento de la implementación.
Permite **HMR**(Hot Module Replacement): App se actualiza automáticamente al guardar un cambio.

Instalación con comando:

```bash
npm install -g @vue/cli
```

Si la instalación tira los siguientes problemas o similares:

```bash
npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
npm WARN deprecated source-map-url@0.4.1: See https://github.com/lydell/source-map-url#deprecated
npm WARN deprecated source-map-resolve@0.5.3: See https://github.com/lydell/source-map-resolve#deprecated
npm WARN deprecated subscriptions-transport-ws@0.11.0: The `subscriptions-transport-ws` package is no longer maintained. We recommend you use `graphql-ws` instead. For help migrating Apollo software to `graphql-ws`, see https://www.apollographql.com/docs/apollo-server/data/subscriptions/#switching-from-subscriptions-transport-ws    For general help using `graphql-ws`, see https://github.com/enisdenjo/graphql-ws/blob/master/README.md

added 848 packages, and audited 849 packages in 39s

64 packages are looking for funding
  run `npm fund` for details

9 vulnerabilities (7 moderate, 2 high)

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
```

Intentar correr los siguientes comandos:

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt autoremove
npm prune
npm audit --only=prod
npm audit fix --force
```

lo cual debería resultar en lo siguiente:

```bash
npm WARN using --force Recommended protections disabled.

up to date, audited 1 package in 254ms

found 0 vulnerabilities
```


## Creación de proyecto Vue

Luego de instalar la CLI, ejecutar en consola:

```bash
vue create project-name
```

Elegimos la opción para seleccionar manualmente las características, marcando:

* Router
* VueX

* ESLint + Prettier
* Lint on save
* dedicate files

Se levanta el entorno local de desarrollo con siguientes comandos que nos mostrará la consola:

```bash
$ cd project-name
$ npm run serve
```

Si los ejecutamos:

```bash
  App running at:
  - Local:   http://localhost:8080/ 
  - Network: http://192.168.1.37:8080/

  Note that the development build is not optimized.
  To create a production build, run npm run build.
```

Para esta configuración en interfaz, ejecutar:

```bash
vue ui
```


## Project Tour

* **node_modules:** Dependencias necesarias en la construcción de nuestro proyecto;
* **public:** Albergar archivos que no se procesen a traves del _Webpack_;
* **src:** Código de la aplicación
* **assets:** Imágenes, fonts..
* **components:** bloques que construyan la app;
* **router:** para la navegación en la app;
* **store:** state management;
* **views:** guarda los componentes para nuestras diferentes vistas de la página;
* **App.vue:** componente root;
* **main.js:** renderiza nuestra app y la monta en el DOM html;

En archivo **main.js** importo la aplicación, creo la app y la monto: argumento de _mount_ en _/public/index.html_/, donde comienza nuestra aplicación.


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

