---
title: Canal (Windows Web Services)
description: Los canales encapsulan un contexto de comunicación entre dos o más partes y se usan para enviar y recibir mensajes.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Servicios web de canal para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93819057f2de4ecf82b2def9cdc4fe14dd1b0ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262028"
---
# <a name="channel-windows-web-services"></a>Canal (Windows Web Services)

Los canales encapsulan un contexto de comunicación entre dos o más partes y se usan para enviar y recibir mensajes.


En el cliente, use [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para crear un canal. En el servidor, use [**WsCreateChannelForListener para**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) crear un canal que el cliente pueda aceptar mediante un agente de [escucha.](listener.md)

Al crear un canal, se especifica la siguiente información, que determina el comportamiento local del canal y el protocolo de conexión que se va a usar.

-   [**WS \_ CHANNEL \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type), que identifica el patrón de intercambio de mensajes del canal.
-   [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica el protocolo de transferencia que se va a usar.
-   Descripción [**de \_ seguridad \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica la seguridad utilizada para el canal. Al crear canales para su uso en un servidor, se especifica una vez para todos los canales que se aceptarán para un agente de escucha determinado.
-   Un conjunto de propiedades de canal de [**WS, \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)que especifican opciones opcionales adicionales (para obtener una lista de estas opciones, vea las enumeraciones de id. de propiedad del canal de [**WS). \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)

Antes de usar el canal, debe abrirlo llamando a la función [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) y especificando el canal y la dirección del punto de [conexión,](endpoint-address.md)junto con otra información opcional.

Para obtener información sobre las transiciones de estado de un canal, consulte el [**tema Estados del**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) canal.

Para obtener más información sobre los canales, consulte el tema [Información general sobre la capa de](channel-layer-overview.md) canal.

Los siguientes elementos de API se usan con canales.

| Devolución de llamada                                                                                  | Descripción                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ ABANDON \_ MESSAGE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Controla la [**llamada WsAbandoneMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) para un canal con enlace de canal personalizado.                                              |
| [**WS \_ ABORT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Controla la [**llamada a WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) para un canal con enlace de canal personalizado.                                                  |
| [**DEVOLUCIÓN DE LLAMADA DEL CANAL WS \_ CLOSE \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Controla la [**llamada de WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) para un canal con enlace de canal personalizado.                                                  |
| [**WS \_ CREATE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Controla la [**llamada de WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) para un canal con enlace de canal personalizado.                                                  |
| [**WS \_ CREATE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Controla la creación de una instancia de descodificador.                                                                                                                  |
| [**WS \_ CREATE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Controla la creación de una instancia del codificador.                                                                                                                 |
| [**DESCODIFICADOR WS \_ \_ DESCODIFICACIÓN \_ DE DEVOLUCIÓN DE LLAMADA**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Descodifica un mensaje.                                                                                                                                    |
| [**DEVOLUCIÓN DE LLAMADA \_ \_ FINAL DEL \_ DESCODIFICADOR DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Descodifica el final de un mensaje.                                                                                                                         |
| [**DEVOLUCIÓN DE LLAMADA \_ DEL TIPO DE CONTENIDO GET DEL \_ \_ \_ \_ DESCODIFICADOR DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Obtiene el tipo de contenido del mensaje.                                                                                                                 |
| [**DEVOLUCIÓN DE LLAMADA \_ \_ DE INICIO DEL \_ DESCODIFICADOR DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Inicia la decodificación de un mensaje.                                                                                                                            |
| [**DEVOLUCIÓN DE \_ LLAMADA \_ DE CODIFICACIÓN DEL \_ CODIFICADOR WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Codifica un mensaje.                                                                                                                                    |
| [**DEVOLUCIÓN DE LLAMADA \_ DEL \_ EXTREMO DEL CODIFICADOR WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Codifica el final de un mensaje.                                                                                                                         |
| [**WS \_ ENCODER \_ GET \_ CONTENT \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Obtiene el tipo de contenido del mensaje.                                                                                                                 |
| [**DEVOLUCIÓN DE \_ LLAMADA DE INICIO DEL \_ CODIFICADOR WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Inicia la codificación de un mensaje.                                                                                                                            |
| [**WS \_ FREE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Controla la [**llamada de WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) para un canal con enlace de canal personalizado.                                                    |
| [**DEVOLUCIÓN DE \_ LLAMADA DEL \_ \_ DESCODIFICADOR LIBRE DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Controla la liberación de una instancia de descodificador.                                                                                                                   |
| [**WS \_ FREE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Controla la liberación de una instancia del codificador.                                                                                                                  |
| [**WS \_ GET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Controla la [**llamada a WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) para un canal con enlace de canal personalizado.                                      |
| [**DEVOLUCIÓN DE \_ LLAMADA \_ DE REDIRECCIONAMIENTO HTTP \_ DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Se invoca cuando un mensaje está a punto de redirigirse automáticamente a otro servicio mediante la funcionalidad de redireccionamiento automático HTTP, tal y como se describe en RFC2616. |
| [**WS \_ OPEN \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Controla la [**llamada a WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) para un canal con enlace de canal personalizado.                                                    |
| [**WS \_ READ \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Controla la [**llamada a WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) para un canal con enlace de canal personalizado.                                              |
| [**WS \_ READ \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Controla la [**llamada a WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) para un canal con enlace de canal personalizado.                                              |
| [**WS \_ RESET \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Controla la [**llamada a WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) para un canal con enlace de canal personalizado.                                                  |
| [**WS \_ SET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Controla la [**llamada a WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) para un canal con enlace de canal personalizado.                                      |
| [**WS \_ SHUTDOWN \_ SESSION \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Controla la [**llamada WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) para un canal con enlace de canal personalizado.                              |
| [**WS \_ WRITE \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Controla la [**llamada WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) para un canal con enlace de canal personalizado.                                            |
| [**WS \_ WRITE \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Controla la [**llamada WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) para un canal con enlace de canal personalizado.                                        |



 



| Enumeración                                                 | Descripción                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENLACE DE \_ CANAL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Indica la pila de protocolos que se usará para el canal.                                                                                      |
| [**IDENTIFICADOR DE PROPIEDAD \_ \_ DEL CANAL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifica cada propiedad de canal mediante un identificador.                                                                                                |
| [**ESTADO DEL \_ CANAL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | Estado del canal.                                                                                                                 |
| [**TIPO DE \_ CANAL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Indica las características básicas del canal, como si es con sesión y qué direcciones de comunicación se admiten. |
| [**WS \_ ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Las distintas codificaciones (formatos de mensaje).                                                                                                |
| [**WS \_ RECEIVE \_ OPTION**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Especifica si se requiere un mensaje al recibir desde un canal.                                                                    |
| [**MODO DE TRANSFERENCIA DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Especifica si los mensajes que se envían o reciben se transmiten o se almacena en búfer.                                                            |



 



| Función                                                         | Descripción                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbanntesMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Omite el resto de un mensaje para un canal.                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Anula todas las E/S pendientes en un canal especificado y establece el estado del canal en **WS \_ CHANNEL STATE \_ \_ FAULTED**. |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Cierra un canal cuando ya no es necesario.                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Crea un canal.                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Crea un canal para un agente de escucha.                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Libera los recursos de memoria asociados a un canal.                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Recupera una propiedad del canal al que hace referencia el parámetro channel.                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Abre un canal en un punto de conexión.                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Lee los elementos de cierre de un mensaje de un canal.                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Lee los encabezados del siguiente mensaje del canal y se prepara para leer los elementos del cuerpo.               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Recibe un mensaje y deserializa el cuerpo del mensaje como un valor.                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Envía un mensaje de solicitud y recibe un mensaje de respuesta correlacionado.                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Restablezca un canal para que se pueda reutilizar.                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Envía un mensaje en un canal mediante la serialización para escribir el elemento body.                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Envía un mensaje que es una respuesta a un mensaje recibido.                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Establece una propiedad de un canal.                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Establece una propiedad de un mensaje.                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Escribe los elementos de cierre de un mensaje en el canal.                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Escribe los encabezados de un mensaje en el canal y se prepara para escribir los elementos del cuerpo.                   |



 



| Handle                        | Descripción                                 |
|-------------------------------|---------------------------------------------|
| [CANAL \_ WS](ws-channel.md) | Tipo opaco que se usa para hacer referencia a un canal. |



 



| Estructura                                                                          | Descripción                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DESCODIFICADOR \_ DE CANAL WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Conjunto de devoluciones de llamada que transforman el tipo de contenido y los bytes codificados de un mensaje recibido.                                                                                                      |
| [**CODIFICADOR DEL CANAL WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Conjunto de devoluciones de llamada que pueden transformar el tipo de contenido y los bytes codificados de un mensaje enviado.                                                                                                      |
| [**PROPIEDADES DEL \_ CANAL WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Conjunto de estructuras [**WS \_ CHANNEL \_ PROPERTY.**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                                                                                                                        |
| [**WS \_ CHANNEL \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Una configuración específica del canal.                                                                                                                                                                      |
| [**DEVOLUCIONES DE \_ LLAMADA DE CANAL PERSONALIZADO DE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Conjunto de devoluciones de llamada que forman la implementación de un canal personalizado.                                                                                                                             |
| [**PROXY HTTP PERSONALIZADO DE WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | se usa para especificar el proxy personalizado para el canal, utilizando el valor **WS \_ CHANNEL PROPERTY CUSTOM \_ \_ \_ HTTP** PROXY de la enumeración \_ [**\_ WS CHANNEL PROPERTY \_ \_ ID.**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) |
| [**ASIGNACIÓN DE \_ ENCABEZADO HTTP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Representa un encabezado individual que se asigna como parte de [**WS \_ HTTP MESSAGE \_ \_ MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).                                                                         |
| [**ASIGNACIÓN DE \_ MENSAJES HTTP \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Información sobre cómo se debe representar una solicitud o respuesta HTTP en un objeto de mensaje.                                                                                                     |
| [**CONTEXTO DE DEVOLUCIÓN \_ DE LLAMADA DE REDIRECCIÓN HTTP \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Especifica la función de devolución de llamada y el estado para controlar el comportamiento de redireccionamiento automático http.                                                                                               |
| [**DESCRIPCIÓN DEL MENSAJE DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | Esquema del [WS \_ MESSAGE](ws-message.md) de entrada y salida para una descripción de operación determinada.                                                                                             |



 

 

 




