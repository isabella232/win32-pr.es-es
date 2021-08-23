---
title: Mensaje (servicios web de Windows)
description: Un mensaje es un objeto que encapsula los datos que se transmiten o reciben.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Servicios web de mensajes para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1722cbe4a956ef16a1b7195158b695f551419ad600c64f552e92700d3e4ee57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657105"
---
# <a name="message-windows-web-services"></a>Mensaje (servicios web de Windows)

Un mensaje es un objeto que encapsula los datos que se transmiten o reciben. SOAP define la estructura de un mensaje e incluye un conjunto de encabezados y un cuerpo. Los encabezados siempre se almacena en búfer en memoria, pero el cuerpo se lee y se escribe con una API de streaming.

![Diagrama que muestra un mensaje con el encabezado almacenado en búfer y el cuerpo que se transmite.](images/messageenvelope.png)


Los mensajes tienen un conjunto de propiedades que se pueden usar para especificar valores opcionales que controlan el comportamiento de un mensaje y para proporcionar una manera de recuperar información adicional sobre los mensajes recibidos (por ejemplo, la información de seguridad). Vea [**WS \_ MESSAGE PROPERTY ID \_ \_ (Id.**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) de propiedad de WS MESSAGE) para obtener una lista completa de las propiedades del mensaje.

Un mensaje se dirige a una dirección de [punto de conexión específica.](endpoint-address.md)

Un [**error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) es un tipo especial de contenido de mensaje que se usa para representar los errores devueltos desde un punto de conexión remoto.

Los mensajes se someten a codificación que transforma el XML en un formato de conexión lineal antes de transmitirse.

Para obtener más información sobre los mensajes, vea el tema Información general [sobre la capa de](channel-layer-overview.md) canal.

En los ejemplos siguientes se muestra el uso de mensajes en WWSAPI.

| Ejemplo                                              | Descripción                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | Muestra el uso de encabezados de mensaje personalizados.    |
| [MessageEncodingExample](messageencodingexample.md) | Muestra la codificación y la codificación de un mensaje. |
| [ForwardMessageExample](forwardmessageexample.md)   | Muestra el reenvío de un mensaje.            |



 

Los siguientes elementos de API se usan con mensajes.

| Devolución de llamada                                                        | Descripción                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ MESSAGE \_ DONE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Notifica al autor de la llamada que el mensaje ha completado su uso de la estructura WS XML READER que se proporcionó a la función WsReadEnvelopeStart o de la estructura WS XML WRITER proporcionada a la función \_ \_ \_ \_ WsWriteEnvelopeStart. |



 



| Enumeración                                                      | Descripción                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**VERSIÓN DE DIRECCIONAMIENTO DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Versión de la especificación utilizada para los encabezados de direccionamiento.                                        |
| [**VERSIÓN DEL \_ SOBRE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Versión de la especificación utilizada para la estructura de sobres.                                        |
| [**ATRIBUTOS DE ENCABEZADO DE WS \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Conjunto de marcas que representan los atributos mustUnderstand y relay de SOAP de un encabezado.                    |
| [**TIPO DE \_ ENCABEZADO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Tipo del encabezado.                                                                                  |
| [**INICIALIZACIÓN DE \_ MENSAJES WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Especifica los encabezados que [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) debe agregar al mensaje. |
| [**ID. \_ DE PROPIEDAD DEL MENSAJE \_ \_ DE WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | Identificador de cada propiedad de mensaje.                                                                         |
| [**ESTADO DEL MENSAJE DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | Estado del mensaje.                                                                                |



 



| Función                                                             | Descripción                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Asigna una dirección de destino a un mensaje.                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Comprueba que el receptor entiende correctamente los encabezados especificados.                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Crea una instancia de un [objeto WS \_ MESSAGE.](ws-message.md)                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Crea un mensaje que es adecuado para su uso con un canal específico.                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Garantiza que hay un número suficiente de bytes disponibles en un mensaje para leer.                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Vacía todos los datos acumulados del cuerpo del mensaje que se han escrito.                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Libera el recurso de memoria asociado a un mensaje.                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Busca el encabezado definido por la aplicación del mensaje y lo deserializa.                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Busca un encabezado estándar determinado en el mensaje y lo deserializa.                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Rellena un parámetro ULONG con los ATRIBUTOS [**\_ DE ENCABEZADO \_ de WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) del elemento de encabezado en el que se coloca el lector. |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Recupera una propiedad de objeto Message especificada.                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Inicializa los encabezados del mensaje como preparación para el procesamiento.                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Marca un encabezado tal como lo entiende la aplicación.                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Deserializa un valor del Lector XML del mensaje.                                                                                               |
| [**WsReadEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Lee los elementos de cierre de un mensaje.                                                                                                               |
| [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Lee los encabezados del mensaje y se prepara para leer los elementos del cuerpo.                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Quita un encabezado personalizado del mensaje.                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Quita el objeto [**WS \_ HEADER TYPE \_ estándar**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) de un mensaje.                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Establece el estado del mensaje de nuevo en **WS \_ MESSAGE STATE \_ \_ EMPTY**.                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Agrega o reemplaza el encabezado estándar especificado en el mensaje.                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Escribe un valor en el cuerpo de un mensaje.                                                                                                               |
| [**WsWriteEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Escribe los elementos de cierre de un mensaje.                                                                                                              |
| [**WsWriteEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Escribe el inicio del mensaje, incluido el conjunto actual de encabezados del mensaje, y se prepara para escribir los elementos del cuerpo.                           |



 



| Handle                        | Descripción                                         |
|-------------------------------|-----------------------------------------------------|
| [WS \_ MESSAGE](ws-message.md) | Tipo opaco utilizado para hacer referencia a un objeto de mensaje. |



 



| Estructura                                                | Descripción                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ERROR \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Valor de error que se lleva en el cuerpo de un mensaje que indica un error de procesamiento. |
| [**CÓDIGO DE ERROR DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Representa un código de error.                                                             |
| [**MOTIVO DEL ERROR DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Contiene una explicación del error.                                                |
| [**PROPIEDADES DEL MENSAJE DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Especifica un conjunto de estructuras [**\_ WS MESSAGE \_ PROPERTY.**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)  |
| [**WS \_ MESSAGE \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Especifica una configuración específica del mensaje.                                                |



 

 

 




