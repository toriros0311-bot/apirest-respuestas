# apirest-respuestas

## Conceptos Básicos
1. ¿Qué es una API y cuál es su función principal?
   una api es una serie de conjuntos, reglas y especificaciones que permiten que los diferentes softwares se comuniquen entre si 
2. Define brevemente el estilo arquitectónico REST.
  el estilo arquitectonico REST es principalmente un estilo de comunicacion stateless (sin estado) que utiliza el protocolo http 
3. ¿Qué significa que una API sea RESTful?
  que una api sea RESTful significa que esta se maneja mediante protocolos http

## Recursos y URIs
4. ¿Qué es un recurso en el contexto de una API REST?
 un contexto en una api rest es cualquier tipo de informacion o concepto de negocio que la api expone  
5. Explica la importancia de las URIs en una API REST.
   Las Uris en una API REST son importantes por que son una direccion unica utilizada para identificar y localizar cada recurso del sistema
6. Menciona tres características importantes de las URIs.
   1: jerarquica y legible
   2: orientada a sustantivos
   3: uso de minusculas y guiones 
8. ¿Por qué es recomendable usar nombres en plural para las URIs que representan colecciones de recursos?
por que permite acceder tanto a la lista general como a un producto especifico cuando se escribe en la url, evitando asi confusion y escribir mas codigo

## Métodos HTTP
8. ¿Cuáles son los métodos HTTP principales utilizados en una API REST y cuál es la función de cada uno?
  Get: obtiene recursos sin cambiar estado
  Post: crea un nuevo recurso
  Put: reemplaza un recurso
  Patch: actualiza un campo especifico
  Delete: elimina un recurso especificado del servidor
9. Describe la diferencia entre los métodos POST y PUT.
    Post: se usa para crear nuevos recursos cuya URI sea asignada por el servidor, ejecutarlo varias veces creara varios registros

    Put: reemplaza un recurso en la URI o lo crea si no existe en esa  ubicacion fija produciendo el mismo estado sin importar cuanto se ejecute 
10. ¿Qué significa que un método HTTP sea idempotente? Da un ejemplo de un método idempotente.
que un metodo http sea idempotente quiere decir que este no realizara el mismo efecto sobre el estado del servidor

## Códigos de Estado HTTP
11. ¿Qué indican los códigos de estado en las respuestas HTTP de una API REST?
    los codigos de estado en las respuestas http suelen indicar el resultado de su solicitud  
12. Da un ejemplo de un código de estado para cada una de las siguientes categorías y explica su significado: 
    - 2xx (Éxito) 200 OK: se proceso correctamente y se devuelve el recurso solicitado 
    - 4xx (Errores del cliente): 404 Not Found: el recurso solicitado no existe en la URI especificada
    - 5xx (Errores del servidor): 500 internal error: ocurrio un error en la logica interna del servidor al intentar procesar la solicitud

## JSON
13. ¿Por qué es JSON el formato de datos más comúnmente utilizado en las APIs REST?
  por que es sencillo tanto para computadoras como para humanos, ademas de su ligero texto y amplio soporte bibliografico en casi todos los lenguajes de programacion   
14. Explica brevemente la estructura de un objeto JSON.
    los objetos JSON se delimitan entre llaves y contienen un conjunto no ordenados de pares de clave/valor, donde la clave es siempre una cadena de texto entre comillas dobles y separada de su valor por dos puntos : y los pares se separan por comas 
15. ¿Qué tipos de datos pueden representarse en JSON?
    Los tipos de datos que puede representar son:
Cadenas de texto (String)

Números (Number)

Booleans (true o false)

Nulos (null)

Objetos (Object)

Arreglos (Array)

## Postman
16. ¿Qué es Postman y para qué se utiliza en el desarrollo de APIs?
     Postman es un programa que permite simular envio de peticiones http a servidores remotos o locales, y asi comprobar y documentar, probar o automatizar el comportamiento de las APIs   
17. Menciona dos funcionalidades importantes de Postman que facilitan el trabajo con APIs.
Las dos funciones importantes del postman son:

Gestion de entornos y variables: permiten reutilizar tokens o urls base modificandolos entre entornos

Colecciones:  facilita la organizacion, guardado y ejecucion organizada de endpoints, ademas se puede agregar pruebas automatizadas 

## Ejercicios Prácticos
18. Describe cómo implementarías una operación CRUD (Crear, Leer, Actualizar, Eliminar) en una API REST.
   Operación,Método HTTP,Endpoint / URI,Descripción
Create (Crear),POST,/productos,Recibe datos JSON en el cuerpo y registra un nuevo producto en la base de datos. Retorna estado 201 Created.
Read (Leer),GET,/productos/productos/{id},Recupera la lista completa o un producto específico mediante su ID. Retorna 200 OK (o 404 si no existe).
Update (Actualizar),PUTPATCH,/productos/{id},PUT reemplaza todo el recurso. PATCH modifica solo los atributos enviados. Retorna 200 OK o 204 No Content.
Delete (Eliminar),DELETE,/productos/{id},Remueve el registro correspondiente al ID indicado de la base de datos. Retorna 200 OK o 204 No Content.
    
19. ¿Cómo usarías Postman para probar una nueva API que acabas de desarrollar?
1ro:Empezaria creando una coleccion con el nombre del proyecto
2ndo: defino una variable de entorno con la direccion base
3ro: construiria endpoints asignados al metodo http apropiado y configuraria los encabezados requeridos
4to: para los metodos como post o put  redactaria la estructura JSON  dentro de la pestaña
5to: enviaria peticiones send para y verificaria codigos de estado http
6to: escribiria aserciones simples en una pestaña de tests para automatizar comprobaciones 
    
21. Propone un ejemplo de una API REST para gestionar un catálogo de productos y describe brevemente los endpoints necesarios.

GET /api/v1/productos

Recupera el listado completo de productos. Permite filtrado o paginación por parámetros de consulta.

POST /api/v1/productos

Crea un nuevo producto recibiendo el objeto JSON con nombre, precio, descripción y stock en el cuerpo de la petición.

GET /api/v1/productos/{id}

Obtiene los detalles específicos de un único producto mediante su ID.

PUT /api/v1/productos/{id}

Sobrescribe todos los datos del producto con el ID especificado por la nueva versión recibida.

PATCH /api/v1/productos/{id}

Actualiza atributos específicos del producto (por ejemplo, ajustar únicamente el precio o el stock sin tocar el resto de campos).

DELETE /api/v1/productos/{id}

Elimina el producto indicado del sistema catálogo.
