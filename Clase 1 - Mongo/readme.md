
# MONGODB

Sistema de DB NoSQL orientado a documentos de código abierto

<!-- DOCUMENTS -->

### JSON 
Java Script Object Notation

```
{
    "id": "1",
    "name": "Jhon",
    "age": 20
}

{
    "id": "2",
    "name": "Valeria",
    "surname": "Martinez",
    "age": 23
}

{
    "id": "3",
    "name": "Camila",
    "surname": "Rodriguez",
    "age": 24,
    "active": true
}

{
    "id": "4",
    "name": "Liam",
    "surname": "Sanchez",
    "age": 27,
    "active": null
}

{
    "id": "5",
    "name": "Li",
    "surname": "huan",
    "age": 40,
    "subs": ["Liam", "Camila"]
}

```

### BSON

Formato de intercambio de datos usado para almacenar y transferir datos en MongoDB

Respresentación binaria de JSON

[BSON Types](https://docs.mongodb.com/manual/reference/bson-types/)

### Collections

MongoDB guarda los documentos BSON en colecciones, y las colecciones se almacenan en la base de datos.


### Instalación

[Tutorial](https://docs.mongodb.com/manual/administration/install-community/)

[MongoDB](https://www.mongodb.com/download-center/community)

[RoboMongo](https://robomongo.org/download)

[MongoDB compass](https://www.mongodb.com/download-center/compass)

### Basic Commands

Muestra los comandos basicos y ayuda
```
help
```

Muestra las bases de datos
```
show dbs
```

Muestra las colecciones en la base de datos actual
```
show collections
```

Muestra los usuarios de la base de datos actual
```
show users
```

Selecciona la base de datos a usar (O la crea)
```
use <db_name> 
```

Muestra las bases de datos
```
show dbs
```

Crea un colección
```
db.createCollection("<name>")
```

Obtiene la colección
```
db.getCollection("<collection_name>")
```

Borra una colección
```
db.<collection_name>.drop()
```

lista los objetos de la coleccion
```
db.version()
```

lista los objetos de la coleccion
```
db.<collection_name>.find()
```

Lista los objetos de la colección donde age = 29
```
db.<collection_name>.find( { age:29 } )
```

Inserta un documento
```
db.<collection_name>.insert({"name":"foobarfoo"})
db.<collection_name>.insertOne({"name":"foobarfoo2"})
```

Inserta multiples documentos
```  
db.<collection_name>.insertMany(
    [  
      {  
        course: "JavaScript",  
        category: "Programming Language"  
      },  
      {  
        course: "NodeJS",  
        category: "Programming Language"  
      },  
      {  
        course: "Angular 8",  
        category: "Programming Language"  
      }  
    ]
);

db.<collection_name>.insert([{},{},{},{}])
```

Actualiza un dato de la colección
```
db.<collection_name>.update(SELECTIOIN_CRITERIA, UPDATED_DATA)  
db.<collection_name>.update({'course':'JavaScript'},{$set:{'course':'JS'}})  
```

Borra todos los datos de la colección
```
db.<collection_name>.remove({})
```

Borra todos los datos que cumplan la condición
```
db.<collection_name>.remove( { catergory : "programming language" } )  
```

Borra la base de datos en uso
```
db.dropDatabase()
```

Sale de la terminal de mongo (ctrl-c)
```
exit / quit()
```
