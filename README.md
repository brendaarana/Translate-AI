AI Translator App (MIT App Inventor)

Aplicación móvil de traducción de texto en tiempo real desarrollada en MIT App Inventor utilizando servicios de traducción automática con Inteligencia Artificial. La aplicación permite ingresar texto en un idioma de origen y obtener una traducción rápida y precisa en el idioma destino al pulsar un botón, destacándose por su enfoque ético en la privacidad de los datos.


Autora: Brenda Arana Gutiérrez


Descripción del Proyecto

La aplicación integra el componente no visible Traductor (servicios de traducción automática) para procesar cadenas de texto mediante peticiones asíncronas. Ofrece una interfaz intuitiva con retroalimentación visual inmediata al usuario tras procesar la solicitud de traducción.

Características Principales

Traducción Instantánea: Procesamiento automático de texto mediante un solo clic.
Manejo Ético y Privacidad de Datos: No requiere registros personales ni almacena datos en servidores o bases de datos locales. El texto ingresado se procesa de manera efímera exclusivamente para la traducción y se borra de inmediato, garantizando el respeto a la privacidad del usuario.
Interfaz de Usuario Accesible: Diseño limpio con colores personalizados, cajas de entrada de texto estructuradas y etiquetas dinámicas para los resultados.
Procesamiento Asíncrono: Captura y despliegue del evento de respuesta mediante bloques de eventos para evitar congelamiento de la interfaz.

Lógica de Programación y Bloques Implementados

La arquitectura de la aplicación en la vista de bloques se compone de dos eventos clave:
translate_button.Click: Al hacer clic en el botón de traducción, se invoca la función Traductor.SolicitarTraducción especificando el idioma destino (ej. "es" para español) y pasando el texto ingresado en text_box.Text.

Traductor.TraducciónRecibida: Evento disparado automáticamente cuando el servicio de IA devuelve el resultado. Recibe los parámetros códigoRespuesta y traducción, asignando este último a la propiedad Text de la etiqueta de resultado (translation_label).

Modelos y Flujo de Procesamiento

Flujo de Datos Asíncrono:
[Usuario ingresa texto] ➔ [Click en translate_button] ➔ [SolicitarTraducción(lenguaje, texto)] ➔ [Servicio de Traducción IA] ➔ [Evento TraducciónRecibida] ➔ [Actualización de translation_label]

