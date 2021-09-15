---
title: Información general sobre la capa de canal
description: La capa de canal proporciona una abstracción del canal de transporte, así como los mensajes enviados en el canal.
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- Channel Layer Overview Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573104"
---
# <a name="channel-layer-overview"></a>Información general sobre la capa de canal

La capa de canal proporciona una abstracción del canal de transporte, así como los mensajes enviados en el canal. También incluye funciones para la serialización de tipos de datos de C hacia y desde estructuras SOAP. La capa de canal permite el [](message.md) control total de las comunicaciones mediante mensajes [](channel.md) que constan de datos enviados o recibidos y que contienen cuerpos y encabezados, y canales que abstraen los protocolos de intercambio de mensajes y proporcionan propiedades para personalizar la configuración.

## <a name="message"></a>Message

Un [mensaje](message.md) es un objeto que encapsula los datos de red, en concreto, los datos que se transmiten o reciben a través de una red. SOAP define la estructura del mensaje, con un conjunto discreto de encabezados y un cuerpo del mensaje. Los encabezados se colocan en un búfer de memoria y el cuerpo del mensaje se lee o escribe mediante una API de secuencia.

![Diagrama que muestra el encabezado y el cuerpo de un mensaje.](images/messageenvelope.png)

Aunque el modelo de datos de un mensaje siempre es el modelo de datos XML, el formato de conexión real es flexible. Antes de transmitir un mensaje, se codifica mediante una codificación determinada (como Text, Binary o MTOM). Consulte [**WS \_ ENCODING para**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) obtener más información sobre las codificaciones.

![Diagrama que muestra varios formatos de codificación de mensajes.](images/messageandencodings.png)

## <a name="channel"></a>Canal

Un [canal](channel.md) es un objeto que se usa para enviar y recibir mensajes en una red entre dos o más puntos de conexión.

Los canales tienen datos asociados que describen [cómo abordar](endpoint-address.md) el mensaje cuando se envía. Enviar un mensaje en un canal es como colocarlo en una cadena: el canal incluye la información a la que debe ir el mensaje y cómo obtenerlo.

![Diagrama que muestra los canales de los mensajes.](images/channelsaschute.png)

Los canales se clasifican en [**tipos de canal.**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) Un tipo de canal especifica qué dirección pueden fluir los mensajes. El tipo de canal también identifica si el canal tiene sesión o no tiene sesión. Una sesión se define como una manera abstracta de correlacionar mensajes entre dos o más partes. Un ejemplo de un canal con sesión es un canal TCP, que usa la conexión TCP como implementación de sesión concreta. Un ejemplo de un canal sin sesión es UDP, que no tiene un mecanismo de sesión subyacente. Aunque HTTP tiene conexiones TCP subyacentes, este hecho no se expone directamente a través de esta API y, por tanto, HTTP también se considera un canal sin sesión.

![Diagrama que muestra los tipos de canal con sesión y sin sesión.](images/channeltypes.png)

Aunque los tipos de canal describen la dirección y la información de sesión de un canal, no especifican cómo se implementa el canal. ¿Qué protocolo debe usar el canal? ¿Con qué esfuerzo debe intentar el canal entregar el mensaje? ¿Qué tipo de seguridad se usa? ¿Es una difusión única o multidifusión? Esta configuración se conoce como el "enlace" del canal. El enlace consta de lo siguiente:

-   [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica el protocolo de transferencia que se va a usar (TCP, UDP, HTTP, NAMEDPIPE).
-   Descripción [**de \_ WS SECURITY \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica cómo proteger el canal.
-   Propiedad de [**WS \_ CHANNEL \_ establecida,**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)que especifica valores opcionales adicionales. Consulte [**WS \_ CHANNEL PROPERTY ID \_ \_ (Id. de propiedad**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) del canal de WS) para obtener la lista de propiedades.

![Diagrama que muestra una lista de propiedades del canal.](images/channelsandbindings.png)

## <a name="listener"></a>Agente de escucha

Para empezar a comunicarse, el cliente crea un objeto Channel. ¿Pero cómo obtiene el servicio su objeto Channel? Para ello, crea un agente [de escucha.](listener.md) La creación de un agente de escucha requiere la misma información de enlace necesaria para crear un canal. Una vez creado un agente de escucha, la aplicación puede aceptar canales del agente de escucha. Puesto que la aplicación puede quedarse atrás en la aceptación de canales, los agentes de escucha normalmente mantienen una cola de canales que están listos para aceptar (hasta alguna cuota).

![Diagrama que muestra los canales de la cola del agente de escucha.](images/channelaccept.png)

## <a name="initiating-communication-client"></a>Iniciar comunicación (cliente)

Para iniciar la comunicación en el cliente, use la secuencia siguiente.

``` syntax
WsCreateChannel
for each address being sent to
{
    WsOpenChannel           // open channel to address
    // send and/or receive messages
    WsCloseChannel          // close channel
    WsResetChannel?         // reset if opening again
}
WsFreeChannel
```

## <a name="accepting-communication-server"></a>Aceptar comunicación (servidor)

Para aceptar comunicaciones entrantes en el servidor, use la secuencia siguiente.

``` syntax
WsCreateListener
WsOpenListener
for each channel being accepted (can be done in parallel)
{
    WsCreateChannelForListener
    for each accept
    {
        WsAcceptChannel     // accept the channel
        // send and/or receive messages
        WsCloseChannel      // close the channel
        WsResetChannel?     // reset if accepting again
    }
    WsFreeChannel
}
WsCloseListener
WsFreeListener
```

## <a name="sending-messages-client-or-server"></a>Envío de mensajes (cliente o servidor)

Para enviar mensajes, use la secuencia siguiente.

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La [**función WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) no permite el streaming y supone que el cuerpo contiene solo un elemento. Para evitar estas restricciones, use la siguiente secuencia en lugar de **WsSendMessage**.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

La [**función WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) usa la serialización para escribir los elementos del cuerpo. Para escribir los datos directamente en el sistema de escritura XML, use la secuencia siguiente en lugar de **WsWriteBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

La [**función WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) usa la serialización para establecer los encabezados en el búfer de encabezado del mensaje. Para usar el objeto de escritura XML para escribir un encabezado, use la siguiente secuencia en lugar de **WsAddCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a>Recepción de mensajes (cliente o servidor)

Para recibir mensajes, use la secuencia siguiente.

``` syntax
WsCreateMessageForChannel
for each message being received
{
    WsReceiveMessage            // receive a message
    WsGetHeader*                // optionally access standard headers such as To or Action
    WsResetMessage              // reset if reading another message
}
WsFreeMessage
```

La función [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) no permite el streaming y supone que el cuerpo contiene solo un elemento y que el tipo del mensaje (acción y esquema del cuerpo) se conoce por adelantado. Para evitar estas restricciones, use la siguiente secuencia en lugar de **WsReceiveMessage**.

``` syntax
WsReadMessageStart              // read all headers into header buffer
for each standard header
{
    WsGetHeader                 // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader           // deserialize application defined header
}
for each element of the body
{
    WsFillBody?                 // optionally fill the body
    WsReadBody                  // deserialize element of body
}
WsReadMessageEnd                // read end of message
```

La [**función WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) usa la serialización para leer los elementos del cuerpo. Para leer los datos directamente desde el Lector [XML](xml-reader.md), use la siguiente secuencia en lugar de **WsReadBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

Las [**funciones WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) usan la serialización para obtener los encabezados del búfer de encabezado del mensaje. Para usar el [Lector XML para](xml-reader.md) leer un encabezado, use la siguiente secuencia en lugar de **WsGetCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateReader                      // create an xml reader
WsSetInputToBuffer                  // specify input of reader should be buffer
WsMoveReader*                       // move to inside header element
while looking for header to read
{
    WsReadToStartElement            // see if the header matches the application header
    if header matched
    {
        WsGetHeaderAttributes?      // get the standard header attributes
        WsReadStartElement          // consume the start of the header element
        // use the read functions to read the contents of the header element
        WsReadEndElement            // consume the end of the header element
    }
    else
    {
        WsSkipNode                  // skip the header element
    }
}                
```

## <a name="request-reply-client"></a>Solicitud de respuesta (cliente)

La realización de una solicitud-respuesta en el cliente se puede realizar con la secuencia siguiente.

``` syntax
WsCreateMessageForChannel               // create request message 
WsCreateMessageForChannel               // create reply message 
for each request reply
{
    WsRequestReply                      // send request, receive reply
    WsResetMessage?                     // reset request message (if repeating)
    WsResetMessage?                     // reset reply message (if repeating)
}
WsFreeMessage                           // free request message
WsFreeMessage                           // free reply message
```

La [**función WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) asume un único elemento para el cuerpo de los mensajes de solicitud y respuesta, y que el tipo del mensaje (acción y esquema del cuerpo) se conoce por adelantado. Para evitar estas limitaciones, el mensaje de solicitud y respuesta se puede enviar manualmente, como se muestra en la secuencia siguiente. Esta secuencia coincide con la secuencia anterior para enviar y recibir un mensaje, excepto donde se indica.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message

// the following block is specific to sending a request
{
    generate a unique MessageID for request
    WsSetHeader         // set the message ID            
}

for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message

WsReadMessageStart      // read all headers into header buffer

// the following is specific to receiving a reply
{
    WsGetHeader         // deserialize RelatesTo ID of reply
    verify request MessageID is equal to RelatesTo ID
}

for each standard header
{
    WsGetHeader         // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader   // deserialize application defined header
}
for each element of the body
{
    WsFillBody?         // optionally fill the body
    WsReadBody          // deserialize element of body
}
WsReadMessageEnd        // read end of message                
```

## <a name="request-reply-server"></a>Solicitud de respuesta (servidor)

Para recibir un mensaje de solicitud en el servidor, use la misma secuencia que se describe en la sección anterior sobre la recepción de mensajes.

Para enviar un mensaje de respuesta o error, use la secuencia siguiente.

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La [**función WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) asume un único elemento en el cuerpo y no permite el streaming. Para evitar estas limitaciones, use la secuencia siguiente. Esto es igual que la secuencia anterior para enviar un mensaje, pero usa [**WS \_ REPLY \_ MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) en lugar de **WS \_ BLANK \_ MESSAGE** al inicializar.

``` syntax
// the following block is specific to sending a reply
{
    WsInitializeMessage // initialize message to WS_REPLY_MESSAGE
}
WsSetHeader             // serialize action header into header buffer                                
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

## <a name="message-exchange-patterns"></a>Modelos de intercambio de mensajes

[**WS \_ CHANNEL TYPE \_ dicta**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) el patrón de intercambio de mensajes posible para un canal determinado. El tipo admitido varía según el enlace, como se muestra a continuación:

-   [**WS \_ HTTP \_ CHANNEL \_ BINDING admite**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) [**WS CHANNEL TYPE \_ \_ \_ REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y **WS CHANNEL TYPE \_ \_ \_ REPLY** en el servidor.
-   [**WS \_ ENLACE \_ DE \_ CANAL TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite [**WS CHANNEL TYPE DUPLEX \_ \_ \_ \_ SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y **\_ WS CHANNEL TYPE DUPLEX \_ \_ \_ SESSION** en el servidor.
-   [**WS \_ UDP \_ CHANNEL \_ BINDING admite**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) [**WS CHANNEL TYPE \_ \_ \_ DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y **WS CHANNEL TYPE \_ \_ \_ INPUT** en el servidor.
-   [**WS \_ NAMEDPIPE \_ CHANNEL \_ BINDING admite**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) [**WS CHANNEL TYPE \_ \_ \_ DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y **WS CHANNEL TYPE \_ \_ \_ INPUT** en el servidor.

## <a name="message-loops"></a>Bucles de mensajes

Para cada patrón de intercambio de mensajes, hay un "bucle" específico que se puede usar para enviar o recibir mensajes. El bucle describe el orden legal de las operaciones necesarias para enviar o recibir varios mensajes. Los bucles se describen a continuación como producciones gramaticales. El término "end" es una recepción en la que se devuelve **WS \_ S \_ END** (consulte los valores devueltos de Windows [Web Services),](windows-web-services-return-values.md)lo que indica que no hay más mensajes disponibles en el canal. La producción paralela especifica que para parallel(x & y) esa operación x se puede realizar simultáneamente con y.

Los bucles siguientes se usan en el cliente:

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

Los bucles siguientes se usan en el servidor:

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

El uso del ENLACE DE SEGURIDAD DE MENSAJES DE CONTEXTO DE SEGURIDAD de WS en el servidor requiere una recepción correcta antes de permitir el envío incluso con un canal de tipo [**WS \_ CHANNEL TYPE DUPLEX \_ \_ \_ SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) Después de la primera recepción. se aplica el bucle normal.

Tenga en cuenta que los canales de tipo [**WS \_ CHANNEL TYPE \_ \_ REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) y **WS CHANNEL TYPE \_ \_ \_ REPLY** se pueden usar para enviar y recibir mensajes un solo sentido (así como el patrón de solicitud-respuesta estándar). Esto se logra cerrando el canal de respuesta sin enviar una respuesta. En este caso, no se recibirá ninguna respuesta en el canal de solicitud. El valor devuelto **WS \_ S \_ END** Using the WS SECURITY CONTEXT MESSAGE SECURITY BINDING on the server requires a successful [**\_ \_ \_ \_ \_ receive**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) before sending is allowed even with a channel of type **WS \_ CHANNEL TYPE DUPLEX \_ \_ \_ SESSION**. Después de la primera recepción, se aplica el bucle normal.

se devolverá , lo que indica que no hay ningún mensaje disponible.

Los bucles de cliente o servidor se pueden realizar en paralelo entre sí mediante el uso de varias instancias de canal.

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>Filtrado de mensajes

Un canal de servidor puede filtrar los mensajes recibidos que no están diseñados para la aplicación, como los mensajes que establecen un [contexto de seguridad](security-context.md). En ese **caso, WS \_ S \_ END** se devolverá desde [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) y no habrá ningún mensaje de aplicación disponible en ese canal. Sin embargo, esto no indica que el cliente pretende finalizar la comunicación con el servidor. Es posible que haya más mensajes disponibles en otro canal. Vea [**WsShutdownSessionChannel.**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel)

## <a name="cancellation"></a>Cancelación

La [**función WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) se usa para cancelar la E/S pendiente de un canal. Esta API no esperará a que se completen las operaciones de E/S. Consulte el [**diagrama de estado de \_ \_ WS CHANNEL STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) y la documentación de **WsAbortChannel** para obtener más información.

La [**API WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) se usa para cancelar la E/S pendiente de un agente de escucha. Esta API no esperará a que se completen las operaciones de E/S. La anulación de un agente de escucha hará que también se anulen las aceptaciones pendientes. Consulte el diagrama [**de estado del \_ \_ agente**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) de escucha de WS y **WsAbortListener** para obtener más información.

## <a name="tcp"></a>TCP

[**WS \_ TCP CHANNEL \_ \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP a través de TCP. La especificación SOAP sobre TCP se basa en el mecanismo de tramas de .NET.

No se admite el uso compartido de puertos en esta versión. Cada agente de escucha que se abre debe usar un número de puerto diferente.

## <a name="udp"></a>UDP

El [**ENLACE DE CANAL UDP \_ de WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP a través de UDP.

Hay una serie de limitaciones con el enlace UDP:

-   No hay compatibilidad con la seguridad.
-   Los mensajes se pueden perder o duplicar.
-   Solo se admite una codificación: [**WS \_ ENCODING XML \_ \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).
-   Los mensajes se limitan fundamentalmente a 64 000 y, con frecuencia, tienen una mayor probabilidad de perderse si el tamaño supera la MTU de la red.

## <a name="http"></a>HTTP

[**WS \_ HTTP CHANNEL BINDING \_ \_ admite**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) SOAP a través de HTTP.

Para controlar los encabezados específicos de HTTP en el cliente y el servidor, vea [**WS \_ HTTP MESSAGE \_ \_ MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).

Para enviar y recibir mensajes que no son SOAP en el servidor, use [**WS \_ ENCODING \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) para [**WS \_ CHANNEL PROPERTY \_ \_ ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

## <a name="namedpipes"></a>NAMEDPIPES

[**WS \_ NAMEDPIPE \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP sobre canalizaciones con nombre, lo que permite la comunicación con el servicio Windows Communication Foundation (WCF) mediante NetNamedPipeBinding.

## <a name="correlating-requestreply-messages"></a>Correlación de mensajes de solicitud/respuesta

Los mensajes de solicitud/respuesta se correlacionan de una de estas dos maneras:

-   La correlación se realiza mediante el canal como mecanismo de correlación. Por ejemplo, al usar [**WS \_ ADDRESSING \_ VERSION \_ TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) y [**WS \_ HTTP CHANNEL \_ \_ BINDING,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) la respuesta del mensaje de solicitud se correlaciona con la solicitud por el hecho de que es el cuerpo de la entidad de la respuesta HTTP.
-   La correlación se realiza mediante los encabezados MessageID y RelatesTo. Este mecanismo se usa con [**WS \_ ADDRESSING \_ VERSIÓN \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) y **WS \_ ADDRESSING \_ VERSIÓN \_ 0 \_ 9** (incluso cuando se usa [**WS HTTP CHANNEL \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)). En este caso, el mensaje de solicitud incluye el encabezado MessageID. El mensaje de respuesta incluye un encabezado RelatesTo que tiene el valor del encabezado MessageID de la solicitud. El encabezado RelatesTo permite al cliente correlacionar una respuesta con una solicitud que envió.

Las SIGUIENTES API de nivel de canal usan automáticamente los mecanismos de correlación adecuados en función de la versión de [**WS \_ ADDRESSING \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) del canal.

-   [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

Si no se usan estas API, se puede agregar manualmente los encabezados y acceder a ellos mediante [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) o [**WsGetHeader.**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)

## <a name="custom-channels-and-listeners"></a>Canales y agentes de escucha personalizados

Si el conjunto predefinido de enlaces de canal no satisface las necesidades de la aplicación, se puede definir un canal personalizado y una implementación del agente de escucha especificando [**WS \_ CUSTOM CHANNEL \_ \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) al crear el canal o agente de escucha. La implementación real del canal o agente de escucha se especifica como un conjunto de devoluciones de llamada a través de las propiedades [**\_ CUSTOM CHANNEL \_ \_ \_ \_ CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) o [**WS LISTENER PROPERTY CUSTOM \_ \_ LISTENER \_ \_ \_ CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) de WS CHANNEL PROPERTY. Una vez creado un canal personalizado o un agente de escucha, el resultado es un objeto [WS \_ CHANNEL](ws-channel.md) o [WS \_ LISTENER](ws-listener.md) que se puede usar con las API existentes.

Un canal personalizado y un agente de escucha también se pueden usar con el proxy de servicio y el [host](service-host.md) de servicio especificando el valor de ENLACE DE CANAL PERSONALIZADO de WS en la enumeración [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) y las propiedades CUSTOM [**CHANNEL \_ \_ \_ \_ \_ CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) de WS CHANNEL PROPERTY y [**WS \_ LISTENER PROPERTY CUSTOM LISTENER \_ \_ \_ \_ CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) al crear el proxy de servicio o el host de servicio. **\_ \_ \_**

## <a name="security"></a>Seguridad

El canal permite limitar la cantidad de memoria usada para varios aspectos de las operaciones a través de propiedades como:

-   [**WS \_ TAMAÑO MÁXIMO DE MENSAJE ALMACENADO EN BÚFER DE LA \_ \_ PROPIEDAD \_ \_ \_ CHANNEL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TAMAÑO \_ MÁXIMO DE MENSAJE TRANSMITIDO POR \_ \_ \_ SECUENCIAS DE \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)LA PROPIEDAD CHANNEL ,
-   [**WS \_ CHANNEL \_ PROPERTY MAX STREAMED START \_ \_ \_ \_ SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TAMAÑO DE \_ BÚFER \_ MÁXIMO DE \_ ENCABEZADOS DE SOLICITUD HTTP \_ DE LA PROPIEDAD \_ \_ \_ CHANNEL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TAMAÑO \_ MÁXIMO DE DICCIONARIO DE SESIÓN DE LA PROPIEDAD \_ \_ \_ \_ CHANNEL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Estas propiedades tienen valores predeterminados que son conservadores y seguros para la mayoría de los escenarios. Los valores predeterminados y las modificaciones realizadas en ellos deben evaluarse cuidadosamente frente a posibles vectores de ataque que pueden provocar la denegación de servicio por parte de un usuario remoto.

El canal permite establecer valores de tiempo de espera para varios aspectos de las operaciones a través de propiedades como:

-   [**WS \_ TIEMPO DE \_ ESPERA DE CONEXIÓN DE LA PROPIEDAD \_ \_ CHANNEL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TIEMPO DE \_ ESPERA DE ENVÍO DE PROPIEDAD DE \_ \_ CANAL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TIEMPO DE \_ ESPERA DE RESPUESTA DE RECEPCIÓN DE LA PROPIEDAD \_ \_ \_ CHANNEL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TIEMPO DE \_ ESPERA DE RECEPCIÓN DE PROPIEDAD DE \_ \_ CANAL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TIEMPO DE \_ ESPERA DE RESOLUCIÓN DE PROPIEDAD DE \_ \_ CANAL**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ TIEMPO DE \_ ESPERA DE CIERRE DE PROPIEDAD DE \_ \_ CANAL.**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)

Estas propiedades tienen valores predeterminados que son conservadores y seguros para la mayoría de los escenarios. Aumentar los valores de tiempo de espera aumenta la cantidad de tiempo que una entidad remota puede mantener activo un recurso local, como memoria, sockets y subprocesos que hacen E/S sincrónica. Una aplicación debe evaluar los valores predeterminados y tener precaución al aumentar el tiempo de espera, ya que puede abrir posibles vectores de ataque que pueden provocar la denegación de servicio desde un equipo remoto.

Algunas de las otras opciones de configuración y consideraciones de diseño de aplicaciones que se deben evaluar cuidadosamente al usar la API de canal WWSAPI:

-   Cuando se usa la capa de canal/agente de escucha, es responsabilidad de la aplicación crear y aceptar canales en el lado servidor. De forma similar, depende de la aplicación crear y abrir canales en el lado cliente. Una aplicación debe colocar un límite superior en estas operaciones porque cada canal consume memoria y otros recursos limitados, como sockets. Una aplicación debe tener especial cuidado al crear un canal en respuesta a cualquier acción desencadenada por una entidad remota.
-   Es responsabilidad de la aplicación escribir la lógica para crear canales y aceptarlos. Cada canal consume recursos limitados, como memoria y sockets. Una aplicación debe tener un límite superior en el número de canales que está dispuesto a aceptar, o una parte remota podría realizar muchas conexiones, lo que conduce a OOM y, por tanto, denegación de servicio. También debe recibir activamente mensajes de esas conexiones con un tiempo de espera pequeño. Si no se recibe ningún mensaje, se tiempo de espera de la operación y se debe liberar la conexión.
-   Una aplicación debe enviar una respuesta o un error mediante la interpretación de los encabezados SOAP ReplyTo o FaultTo. La práctica segura es respetar solo un encabezado ReplyTo o FaultTo que sea "anónimo", lo que significa que se debe usar la conexión existente (TCP, HTTP) o la dirección IP de origen (UDP) para enviar la respuesta SOAP. Las aplicaciones deben tener mucha precaución al crear recursos (como un canal) para responder a otra dirección, a menos que el mensaje esté firmado por una parte que pueda hablar de la dirección a la que se envía la respuesta.
-   La validación realizada en la capa de canal no sustituye a la integridad de los datos lograda a través de la seguridad. Una aplicación debe basarse en las características de seguridad de WWSAPI para asegurarse de que se comunica con una entidad de confianza y también debe confiar en la seguridad para garantizar la integridad de los datos.

Del mismo modo, hay opciones de configuración de mensajes y consideraciones de diseño de aplicaciones que se deben evaluar cuidadosamente al usar WWSAPI Message API:

-   El tamaño del montón utilizado para almacenar los encabezados de un mensaje se puede configurar mediante la propiedad PROPIEDADES DEL MONTÓN DE LA PROPIEDAD DEL MENSAJE de [**WS. \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) Aumentar este valor permite que los encabezados del mensaje consuman más memoria, lo que puede dar lugar a OOM.
-   El usuario del objeto de mensaje debe tener en cuenta que las API de acceso de encabezado son O(n) con respecto al número de encabezados del mensaje, ya que comprueban si hay duplicados. Los diseños que requieren muchos encabezados en un mensaje pueden provocar un uso excesivo de la CPU.
-   El número máximo de encabezados de un mensaje se puede configurar mediante la propiedad [**\_ WS MESSAGE \_ PROPERTY MAX \_ \_ PROCESSED \_ HEADERS.**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) También hay un límite implícito basado en el tamaño del montón del mensaje. El aumento de ambos valores permite que haya más encabezados presentes, lo que aumenta el tiempo necesario para encontrar un encabezado (al usar las API de acceso de encabezado).

 

 




