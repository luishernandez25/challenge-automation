# ChallengeQa

<h1> Front End </h1>

Se tiene la siguiente Web siendo un Ecommerce B2C, el cual se requiere automatizar una serie de pruebas de regresion para validar una 
serie de funcionalidades la casuistica es la siguiente:

1)Validar la funcionalidad de crear cuenta la cual estara vinculada a una cuenta de correo y luego se rellena un formulario, y el alta se realice correctamente

2)Validar poder realizar la compra de cualquier producto de la web, donde se debe cumplir el flujo funcional de seleccionar la prenda, agregarla al carrito, proceder al pago (3 veces)
luego aceptar los terminos de servicio, seleccionar cualquiera de los 2 metodos de pago disponibles, confirmar la orden y luego volver a la orden y poder capturar la evidencia del historico del carrito

3)Validar intentar crear una cuenta con un correo ya registrado, donde se debe capturar el error y para que dar el ok al test se debe hacer un equals al error textual"An account using this email address has already been registered. Please enter a valid password or request a new one." 

<h1> Back End </h1>

1) Se tiene un desarrollo de Backend con 4 servicios externalizados GET

servicio de persona que devuelve un status 200 {"response": {"nombre": "ezequiel","apellido":"hermoso"}}
https://back-qa.herokuapp.com/persona/ezequiel
  
servicio de persona que devuelve un status error 500 {"error": "Error interno del servidor"}
https://back-qa.herokuapp.com/persona/error/500/ezequiel

servicio de persona que devuelve un status error 404 {"error": "Error endpoint no encontrado"}
https://back-qa.herokuapp.com/persona/error/404/ezequiel

servicio de persona que devuelve un status error 401 {"error": "Error acceso no autorizado"}
https://back-qa.herokuapp.com/persona/error/401/ezequiel

2) 4 servicios externalizados POST

servicio de persona se le envía un request {"nombre": "ezequiel", "apellido":"hermoso"} que devuelve un status 200
https://back-qa.herokuapp.com/persona/

servicio de persona se le envía un request {"nombre": "ezequiel", "apellido":"hermoso"} que devuelve un status error 500
https://back-qa.herokuapp.com/persona/error/500/

servicio de persona se le envía un request {"nombre": "ezequiel", "apellido":"hermoso"} que devuelve un status error 404
https://back-qa.herokuapp.com/persona/error/404/

servicio de persona se le envía un request {"nombre": "ezequiel", "apellido":"hermoso"} que devuelve un status error 401
https://back-qa.herokuapp.com/persona/error/401/

3) <h2> 4 servicios externalizados PUT </h2>

servicio de persona se le envía un request {"apellido":"hermoso2"} que devuelve un status 200
https://back-qa.herokuapp.com/persona/ezequiel

servicio de persona se le envía un request {"apellido":"hermoso2"} que devuelve un status error 500
https://back-qa.herokuapp.com/persona/error/500/ezequiel

servicio depersona se le envía un request {"apellido":"hermoso2"} que devuelve un status error 404
https://back-qa.herokuapp.com/persona/error/404/ezequiel

servicio de persona se le envía un request {"apellido":"hermoso2"} que devuelve un status error 401
https://back-qa.herokuapp.com/persona/error/401/ezequiel

para verificar que se modificó con el put se debe ejecutar el siguiente servicio
servicio de persona que devuelve un status 200 {"response": {"nombre": "ezequiel","apellido":"hermoso2"}}
https://back-qa.herokuapp.com/persona/ezequiel

servicio de persona se le envía un request {"nombre: ezequiel", "apellido:hermoso"} que
devuelve un status error 500
https://back-qa.herokuapp.com/persona/ezequiel

<h1> Criterios de aceptacion </h1>

Para el desarrollo de la automatizacion del front el postulante es libre de seleccionar cualquier herramienta openSource que desee, lo minimo que se solicita es que siga el patron de Page Object
Para las apis se requiere el desarrollo con RestAssured o Karate siendo la primera la mas deseable, en caso que todo el desarrollo(Front + Back) sea hecho en JAVA ambas soluciones deben estar en el mismo repo pero en diferentes sources
en este mismo caso se solicita en las apis validar todos los status code para poder dar como resultado un OK en la prueba. se debera subir todo a este repo y agregar la documentacion de los comandos necesarios para la ejecucion 

