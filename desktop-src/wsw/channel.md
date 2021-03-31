---
title: Canal (servicios Web de Windows)
description: Los canales encapsulan un contexto de comunicación entre dos o más entidades y se usan para enviar y recibir mensajes.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Servicios Web de canal para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93819057f2de4ecf82b2def9cdc4fe14dd1b0ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995860"
---
# <a name="channel-windows-web-services"></a>Canal (servicios Web de Windows)

Los canales encapsulan un contexto de comunicación entre dos o más entidades y se usan para enviar y recibir mensajes.


En el cliente, use [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para crear un canal. En el servidor, use [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) para crear un canal que el cliente pueda aceptar mediante un agente de [escucha](listener.md).

Cuando se crea un canal, se especifica la siguiente información, que determina el comportamiento local del canal y el protocolo de conexión que se va a utilizar.

-   Un [**\_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type), que identifica el patrón de intercambio de mensajes del canal.
-   Un [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica el protocolo de transferencia que se va a usar.
-   Una [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica la seguridad utilizada para el canal. Al crear canales para su uso en un servidor, se especifica una vez para todos los canales que se aceptarán para un agente de escucha determinado.
-   Una [**\_ \_ propiedad Set WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, que especifica una configuración adicional opcional (para obtener una lista de estas opciones, consulte enumeraciones de [**identificador de propiedad de canal de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ).

Antes de usar el canal, debe abrirlo llamando a la función [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) y especificando el canal y la [dirección del punto de conexión](endpoint-address.md), junto con otra información opcional.

Para obtener información sobre las transiciones de estado de un canal, consulte el tema [**Estados del canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) .

Para obtener más información sobre los canales, vea el tema [información general](channel-layer-overview.md) de la capa de canal.

Los siguientes elementos de API se usan con canales.

| Devolución de llamada                                                                                  | Descripción                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_devolución de \_ llamada de mensajes de abandono de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Controla la llamada a [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) para un canal con enlace de canal personalizado.                                              |
| [**\_devolución de \_ llamada de canal de ANULAción WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Controla la llamada a [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) para un canal con enlace de canal personalizado.                                                  |
| [**\_devolución de \_ llamada de canal de cierre WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Controla la llamada a [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) para un canal con enlace de canal personalizado.                                                  |
| [**\_devolución de \_ llamada de canal de creación WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Controla la llamada a [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) para un canal con enlace de canal personalizado.                                                  |
| [**\_devolución de \_ llamada del descodificador de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Controla la creación de una instancia del descodificador.                                                                                                                  |
| [**\_devolución de \_ llamada del codificador de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Controla la creación de una instancia de codificador.                                                                                                                 |
| [**devolución de llamada de descodificación de WS \_ DEScodificador \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Descodifica un mensaje.                                                                                                                                    |
| [**devolución de llamada de final del \_ DEScodificador de WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Descodifica el final de un mensaje.                                                                                                                         |
| [**devolución de llamada de \_ \_ tipo de \_ contenido de \_ decodificador WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Obtiene el tipo de contenido del mensaje.                                                                                                                 |
| [**devolución de llamada de inicio del \_ DEScodificador de WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Inicia la descodificación de un mensaje.                                                                                                                            |
| [**devolución de llamada de codificación de WS \_ Encoder \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Codifica un mensaje.                                                                                                                                    |
| [**devolución de llamada de final del \_ codificador de WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Codifica el final de un mensaje.                                                                                                                         |
| [**devolución de llamada de \_ \_ tipo de contenido get del codificador de WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Obtiene el tipo de contenido del mensaje.                                                                                                                 |
| [**devolución de llamada de inicio del \_ codificador WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Inicia la codificación de un mensaje.                                                                                                                            |
| [**\_devolución de \_ llamada de canal gratis de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Controla la llamada a [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) para un canal con enlace de canal personalizado.                                                    |
| [**\_devolución de \_ llamada del descodificador gratuito de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Controla la liberación de una instancia del descodificador.                                                                                                                   |
| [**\_devolución de \_ llamada del codificador gratis de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Controla la liberación de una instancia de codificador.                                                                                                                  |
| [**devolución de llamada de la propiedad de canal WS \_ Get \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Controla la llamada a [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) para un canal con enlace de canal personalizado.                                      |
| [**\_devolución de \_ llamada de redirección http de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Se invoca cuando un mensaje está a punto de redirigirse automáticamente a otro servicio mediante la funcionalidad de redirección HTTP automática, tal y como se describe en RFC2616. |
| [**\_devolución de \_ llamada de canal abierto de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Controla la llamada a [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) para un canal con enlace de canal personalizado.                                                    |
| [**\_devolución de \_ llamada de final del mensaje \_ \_ de WS**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Controla la llamada a [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) para un canal con enlace de canal personalizado.                                              |
| [**\_devolución de \_ llamada de inicio de mensaje \_ \_ de WS**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Controla la llamada a [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) para un canal con enlace de canal personalizado.                                              |
| [**\_devolución de \_ llamada de canal de restablecimiento de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Controla la llamada a [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) para un canal con enlace de canal personalizado.                                                  |
| [**\_devolución de \_ llamada de propiedad de canal \_ \_ de WS**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Controla la llamada a [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) para un canal con enlace de canal personalizado.                                      |
| [**\_devolución de \_ llamada de canal de sesión de cierre de \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Controla la llamada a [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) para un canal con enlace de canal personalizado.                              |
| [**\_devolución de \_ llamada de final del mensaje de escritura de \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Controla la llamada a [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) para un canal con enlace de canal personalizado.                                            |
| [**\_devolución de \_ llamada de inicio del mensaje de escritura de \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Controla la llamada a [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) para un canal con enlace de canal personalizado.                                        |



 



| Enumeración                                                 | Descripción                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_enlace de canal de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Indica la pila de protocolos que se va a utilizar para el canal.                                                                                      |
| [**identificador de la propiedad de canal de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifica cada propiedad del canal mediante un identificador.                                                                                                |
| [**Estado de WS \_ Channel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | Estado del canal.                                                                                                                 |
| [**\_tipo de canal de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Indica las características básicas del canal, como si se trata de una sesión y qué direcciones de comunicación se admiten. |
| [**\_codificación WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Las distintas codificaciones (formatos de mensaje).                                                                                                |
| [**\_opción de recepción de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Especifica si se requiere un mensaje cuando se recibe de un canal.                                                                    |
| [**\_modo de transferencia de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Especifica si los mensajes enviados o recibidos se transmiten o se almacenan en búfer.                                                            |



 



| Función                                                         | Descripción                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Omite el resto de un mensaje para un canal.                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Anula todas las e/s pendientes en un canal especificado y establece el estado del canal en **Estado de canal de WS con \_ \_ \_ errores**. |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Cierra un canal cuando ya no se necesita.                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Crea un canal.                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Crea un canal para un agente de escucha.                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Libera los recursos de memoria asociados a un canal.                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Recupera una propiedad del canal al que hace referencia el parámetro de canal.                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Abre un canal en un extremo.                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Lee los elementos de cierre de un mensaje de un canal.                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Lee los encabezados del mensaje siguiente del canal y se prepara para leer los elementos del cuerpo.               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Recibe un mensaje y deserializa el cuerpo del mensaje como un valor.                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Envía un mensaje de solicitud y recibe un mensaje de respuesta correlacionado.                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Restablecer un canal para que se pueda volver a usar.                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Envía un mensaje en un canal utilizando la serialización para escribir el elemento de cuerpo.                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Envía un mensaje que es una respuesta a un mensaje recibido.                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Establece una propiedad de un canal.                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Establece una propiedad de un mensaje.                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Escribe los elementos de cierre de un mensaje en el canal.                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Escriba los encabezados de un mensaje en el canal y prepárese para escribir los elementos del cuerpo.                   |



 



| Handle                        | Descripción                                 |
|-------------------------------|---------------------------------------------|
| [canal de WS \_](ws-channel.md) | Tipo opaco que se usa para hacer referencia a un canal. |



 



| Estructura                                                                          | Descripción                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**descodificador de canal de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Conjunto de devoluciones de llamada que transforman el tipo de contenido y los bytes codificados de un mensaje recibido.                                                                                                      |
| [**\_codificador de canal de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Conjunto de devoluciones de llamada que puede transformar el tipo de contenido y los bytes codificados de un mensaje enviado.                                                                                                      |
| [**\_propiedades de canal de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Un conjunto de estructuras de [**\_ \_ propiedades de canal de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) .                                                                                                                        |
| [**\_propiedad de canal de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Configuración específica del canal.                                                                                                                                                                      |
| [**\_devoluciones de llamada de canal personalizado de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Un conjunto de devoluciones de llamada que forman la implementación de un canal personalizado.                                                                                                                             |
| [**\_ \_ proxy HTTP personalizado de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | se usa para especificar el proxy personalizado para el canal mediante la propiedad de canal de WS valor de proxy **\_ \_ \_ \_ http personalizado** \_ de la enumeración de [**identificador de propiedad de canal de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) . |
| [**\_asignación de \_ encabezados \_ http de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Representa un encabezado individual que se asigna como parte de [**la \_ \_ \_ asignación de mensajes HTTP de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).                                                                         |
| [**\_asignación de \_ mensajes \_ http de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Información sobre cómo se debe representar una solicitud o respuesta HTTP en un objeto de mensaje.                                                                                                     |
| [**\_contexto de \_ devolución de llamada de redirección de WS http \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Especifica la función de devolución de llamada y el estado para controlar el comportamiento de la redirección automática de HTTP.                                                                                               |
| [**\_Descripción del mensaje de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | El esquema para el [ \_ mensaje WS](ws-message.md) de entrada y salida para una descripción de operación determinada.                                                                                             |



 

 

 




