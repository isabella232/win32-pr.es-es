---
title: Mensaje (servicios web de Windows)
description: Un mensaje es un objeto que encapsula los datos que se transmiten o se reciben.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Servicios Web de mensajes para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704df318e10521bd56e62632af16e683b7baccfc
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104553178"
---
# <a name="message-windows-web-services"></a>Mensaje (servicios web de Windows)

Un mensaje es un objeto que encapsula los datos que se transmiten o se reciben. La estructura de un mensaje se define mediante SOAP e incluye un conjunto de encabezados y un cuerpo. Los encabezados siempre se almacenan en búfer en la memoria, pero el cuerpo se lee y se escribe con una API de streaming.

![Diagrama que muestra un mensaje con el encabezado que se almacena en búfer y el cuerpo que se transmite.](images/messageenvelope.png)


Los mensajes tienen un conjunto de propiedades que se pueden utilizar para especificar valores de configuración opcionales que controlan el comportamiento de un mensaje y para proporcionar una manera de recuperar información adicional acerca de los mensajes recibidos (como información de seguridad). Consulte identificador de la propiedad de mensaje de WS para obtener una lista completa de las propiedades del mensaje. [**\_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)

Un mensaje se dirige a una [dirección de extremo](endpoint-address.md)concreta.

Un [**\_ error de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) es una ordenación especial del contenido del mensaje que se usa para representar los errores devueltos desde un punto de conexión remoto.

Los mensajes se someten a la codificación que transforma el XML en un formato de conexión lineal antes de transmitirlo.

Para obtener más información sobre los mensajes, consulte el tema de [información general sobre capas de canales](channel-layer-overview.md) .

En los siguientes ejemplos se muestra el uso de mensajes en WWSAPI.

| Ejemplo                                              | Descripción                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | Muestra el uso de encabezados de mensaje personalizados.    |
| [MessageEncodingExample](messageencodingexample.md) | Muestra cómo codificar y descodificar un mensaje. |
| [ForwardMessageExample](forwardmessageexample.md)   | Muestra el reenvío de un mensaje.            |



 

Los siguientes elementos de API se utilizan con mensajes.

| Devolución de llamada                                                        | Descripción                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_devolución de \_ \_ llamada de mensaje WS**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Notifica al llamador que el mensaje ha completado su uso de la \_ estructura del lector XML de WS \_ que se proporcionó a la función WsReadEnvelopeStart, o de la \_ estructura del escritor XML de WS \_ proporcionada a la función WsWriteEnvelopeStart. |



 



| Enumeración                                                      | Descripción                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**versión de WS \_ Addressing \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Versión de la especificación utilizada para los encabezados de direccionamiento.                                        |
| [**\_versión de sobre de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Versión de la especificación utilizada para la estructura de sobre.                                        |
| [**\_atributos de encabezado de WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Conjunto de marcas que representan los atributos mustUnderstand y Relay de SOAP de un encabezado.                    |
| [**\_tipo de encabezado WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Tipo del encabezado.                                                                                  |
| [**\_inicialización de mensajes de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Especifica qué encabezados debe agregar el [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) al mensaje. |
| [**identificador de la propiedad de mensaje de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | IDENTIFICADOR de cada propiedad de mensaje.                                                                         |
| [**\_Estado del mensaje de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | Estado del mensaje.                                                                                |



 



| Función                                                             | Descripción                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Asigna una dirección de destino a un mensaje.                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Comprueba que el receptor ha entendido adecuadamente los encabezados especificados.                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Crea una instancia de un objeto de [ \_ mensaje de WS](ws-message.md) .                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Crea un mensaje que es adecuado para su uso con un canal específico.                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Garantiza que hay un número suficiente de bytes disponibles en un mensaje para su lectura.                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Vacía todos los datos del cuerpo del mensaje acumulado que se han escrito.                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Libera el recurso de memoria asociado a un mensaje.                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Busca el encabezado definido por la aplicación del mensaje y lo deserializa.                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Busca un encabezado estándar determinado en el mensaje y lo deserializa.                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Rellena un parámetro ULONG con los [**atributos de \_ encabezado \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) del elemento header en el que está situado el lector. |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Recupera una propiedad de objeto de mensaje especificada.                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Inicializa los encabezados del mensaje como preparación para el procesamiento.                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Marca un encabezado como entendido por la aplicación.                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Deserializa un valor del lector XML del mensaje.                                                                                               |
| [**WsReadEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Lee los elementos de cierre de un mensaje.                                                                                                               |
| [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Lee los encabezados del mensaje y se prepara para leer los elementos del cuerpo.                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Quita un encabezado personalizado del mensaje.                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Quita el objeto [**de \_ \_ tipo de encabezado WS**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) estándar de un mensaje.                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Vuelve a establecer el estado del mensaje en **\_ \_ estado \_ de mensaje WS**.                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Agrega o reemplaza el encabezado estándar especificado en el mensaje.                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Escribe un valor en el cuerpo de un mensaje.                                                                                                               |
| [**WsWriteEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Escribe los elementos de cierre de un mensaje.                                                                                                              |
| [**WsWriteEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Escribe el inicio del mensaje, incluido el conjunto actual de encabezados del mensaje y se prepara para escribir los elementos del cuerpo.                           |



 



| Handle                        | Descripción                                         |
|-------------------------------|-----------------------------------------------------|
| [\_mensaje WS](ws-message.md) | Tipo opaco que se usa para hacer referencia a un objeto de mensaje. |



 



| Estructura                                                | Descripción                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Un valor de error que se lleva a cabo en el cuerpo de un mensaje que indica un error de procesamiento. |
| [**\_código de error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Representa un código de error.                                                             |
| [**\_razón del error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Contiene una explicación del error.                                                |
| [**\_propiedades del mensaje de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Especifica un conjunto de estructuras de [**\_ \_ propiedades de mensaje de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) .  |
| [**\_propiedad WS Message \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Especifica una configuración específica del mensaje.                                                |



 

 

 




