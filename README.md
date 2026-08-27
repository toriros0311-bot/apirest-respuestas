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
    
15. ¿Qué tipos de datos pueden representarse en JSON?

## Postman
16. ¿Qué es Postman y para qué se utiliza en el desarrollo de APIs?
17. Menciona dos funcionalidades importantes de Postman que facilitan el trabajo con APIs.

## Ejercicios Prácticos
18. Describe cómo implementarías una operación CRUD (Crear, Leer, Actualizar, Eliminar) en una API REST.
19. ¿Cómo usarías Postman para probar una nueva API que acabas de desarrollar?
20. Propone un ejemplo de una API REST para gestionar un catálogo de productos y describe brevemente los endpoints necesarios.
