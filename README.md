# Markdown-example

# CONSTRUIR LA IMAGEN DESDE EL DOCKERFILE
    docker build -t pern-stack-image .

# CORRER EL CONTENEDOR.
### en windows %cd%  se refiere a el directorio actual en command prompt.
    docker run -v %cd%:/app:ro -p 3000:3000 -d --name pern-stack-container pern-stack-image
### en windows ${pwd} se refiere al directorio  actual en el powershell.
    docker run -v ${pwd}:/app:ro -p 3000:3000 -d --name pern-stack-container pern-stack-image

# CORRER LA APLICACION DOCKER COMPOSE EN MODO DE DESARROLLO.
    docker-compose -f docker-compose.yml -f docker-compose.dev.yml up -d

# CORRER LA APLICACION CON DOCKER COMPOSE EN MODO DE PRODUCCION.
    docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d


esto es un testo en *italic*

esto es un esto en **negrita**

esto es un exto en  ~~tachado~~

<!--lista desordenada -->

* apple
* orange
* etc

<!--lista ordenada -->

1. apple
2. orange
3. etc

<!--lista desordenada con sub item-->

* apple
	* apple 1
	* apple 2
* orange
* etc

<!--lista ordenada con sub item -->

1. apple
	1. apple 1
	2. apple 2
2. orange
3. etc

<!-- Enlace a sitio web -->
[faztweb.com](http://faztweb.com)

[faztweb.com](http://faztweb.com "Custom Title")

> this is a qoute

<!-- crear una linea -->

---
___

<!-- Crear una linea de codigo -->

`console.log("Hello world");`

<!-- Crear bloque de codigo -->

```
const { Pool } = require('pg');

    const pool = new Pool({
        host: process.env.DB_HOST || 'localhost',
        user: process.env.DB_USER || 'postgres',
        password: process.env.DB_PASSWORD ||  '123456',
        database: process.env.DB_NAME || 'pern-stack' ,    
        port: process.env.DB_PORT ||  5432
        
    });

module.exports = pool;
```

<!-- Crear bloque de codigo con resaltado -->

```javascript
const { Pool } = require('pg');

    const pool = new Pool({
        host: process.env.DB_HOST || 'localhost',
        user: process.env.DB_USER || 'postgres',
        password: process.env.DB_PASSWORD ||  '123456',
        database: process.env.DB_NAME || 'pern-stack' ,    
        port: process.env.DB_PORT ||  5432
        
    });

module.exports = pool;
```

```python
print ("hello world")
```

```html
<h1>Hello world</h1>
```

<!-- Crear tablas en markdown -->

| nombre| apellido | salario |
| -----|:---------:| -------:|
|Vicente|Lopez|5000|
|Francisco| Lopez|5000|
|Juan|Lopez|5000|
|Paulina|Lopez|5000|

<!-- imagenes -->
![visual estudio code logo](https://upload.wikimedia.org/wikipedia/commons/9/9a/Visual_Studio_Code_1.35_icon.svg "visual studio code") 

<!-- Github markdown -->
<!-- Lista to do -->
*[x] task1
*[] task2
*[] task3
*[x] task4
