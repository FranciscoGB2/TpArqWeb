# Trabajo Practico Arquitectura Web (SoundWeb: Pagina para que artistas suban canciones)
### Introduccion
Me llamo Francisco Gonzalez Bonorino estoy cursando la materia Diseño de sistemas con el profesor: Diego Marafetti. En este repo se tratara sobre mi proyecto "SoundWeb" el cual es una pagina donde artistas podran subir sus canciones para que otras personas puedan escucharlas y opinar sobre ellas

---

### Estructura
#### Este Sistema estara formado por:
- Artista (int id_artista, String Nombre, String Contraseña)
- Cancion (int id_cancion, String Nombre, id_album, int id_artista, int contLike, int contDislike)
- Album (int id_album, int id_artista, String Nombre_album)

#### Posibles funciones
  Tendremos la posibilidad de obtener la informacion de usuarios/artistas/administradores con getUsuario(), de canciones getCancion() y de albumes del artista getAlbum();

  adicionalmente cada usuario tendra la posibilidad de comentar en canciones de los artistas y dejar un "like" o "dislike" comentar(string Comentario, int id_cancion) like(int id_cancion), dislike(int id_cancion)

  Por otro lado tambien los usuarios tendran la capacidad de usar las operaciones basicas del CRUD, entre otros podran: Agregar y eliminar: canciones y albumes obtener datos de usuarios/artistas, canciones y albumes

  #### Ejemplos

  ##### Create
  crear un usuario:
POST/Usuario/create {"id_usuario":3312,"Usuario":Dave Mustaine,"Contraseña": NoMeGustaMetallica123}
  
  ##### Read
  leer datos de un usuario (en este caso Dave Mustaine)
  GET/Usuario/{3312}

  
  ##### Update
  Actualizar datos de un usuario (en este caso Dave Mustaine)
  PUT/Usuario/{3312}  {"id_usuario":3312, "Usuario":Dave Mustaine,"Contraseña":AguanteMegadeth321}
  ##### Delete
  Por ultimo usaremos el metodo delete (entre otras cosas) para borrar un usuario:
    DELETE/Usuario/{3312}
---
### Ejemplos de Cancion
  ##### CREAR CANCION 
    POST/Cancion/create {"id_cancion":1234,"Nombre":Tornado of Souls,"id_album":1002,"id_usuario":3312,"contLike":0,"contDislike":0}
  ##### LEER DATOS DE CANCION 
     GET/Cancion/{1234}
  ##### ACTUALIZAR CANCION
    PUT/cancion/{1234}  {"id_cancion":1234,"Nombre":Tornado of Souls,"id_album":1002,"id_usuario":3312,"contLike":200000,"contDislike":2}
  ##### ELIMINAR CANCION
    DELETE/cancion/{3312}
---
### Ejemplos de Album
  ##### CREAR ALBUM
    POST/Album/create {"id_album":1002,"id_usuario":3312,"Nombre":Rust In Peace,}
  ##### LEER DATOS DE CANCION 
     GET/Album/{1002}
  ##### ACTUALIZAR CANCION
    PUT/Album/{1002}  {"id_Album":1002,"id_usuario":3312,"Nombre":Countdown To Extinction}
  ##### ELIMINAR CANCION
    DELETE/Album/{1002}
