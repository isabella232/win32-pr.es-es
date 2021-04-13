---
title: Introducción a la capa de canal
description: La capa de canal proporciona una abstracción del canal de transporte, así como los mensajes enviados en el canal.
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- Información general del nivel de canal servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104560657"
---
# <a name="channel-layer-overview"></a>Introducción a la capa de canal

La capa de canal proporciona una abstracción del canal de transporte, así como los mensajes enviados en el canal. También incluye funciones para la serialización de tipos de datos de C en estructuras SOAP y desde ellas. La capa de canal permite el control total de las comunicaciones por medio de [mensajes](message.md) que se componen de datos enviados o recibidos y que contienen cuerpos y encabezados, y de [canales](channel.md) que abstraen los protocolos de intercambio de mensajes y proporcionan propiedades para personalizar la configuración.

## <a name="message"></a>Message

Un [mensaje](message.md) es un objeto que encapsula datos de red, específicamente, datos que se transmiten o reciben a través de una red. La estructura del mensaje se define mediante SOAP, con un conjunto discreto de encabezados y un cuerpo del mensaje. Los encabezados se colocan en un búfer de memoria y el cuerpo del mensaje se lee o se escribe mediante una API de Stream.

![Diagrama que muestra el encabezado y el cuerpo de un mensaje.](images/messageenvelope.png)

Aunque el modelo de datos de un mensaje siempre es el modelo de datos XML, el formato de conexión real es flexible. Antes de transmitir un mensaje, se codifica mediante una codificación determinada (como texto, binario o MTOM). Para obtener más información sobre las codificaciones, consulte [**\_ codificación de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .

![Diagrama que muestra varios formatos de codificación de mensajes.](images/messageandencodings.png)

## <a name="channel"></a>Canal

Un [canal](channel.md) es un objeto que se usa para enviar y recibir mensajes en una red entre dos o más extremos.

Los canales tienen datos asociados que describen cómo [tratar](endpoint-address.md) el mensaje cuando se envía. Enviar un mensaje en un canal es como colocarlo en un tobogán; el canal incluye la información donde debe ir el mensaje y cómo obtenerlo.

![Diagrama que muestra los canales para los mensajes.](images/channelsaschute.png)

Los canales se clasifican en [**tipos de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Un tipo de canal especifica qué dirección pueden fluir los mensajes. El tipo de canal también identifica si el canal tiene sesión o sin sesión. Una sesión se define como una forma abstracta de correlacionar los mensajes entre dos o más entidades. Un ejemplo de canal con sesión es un canal TCP, que usa la conexión TCP como la implementación de la sesión concreta. Un ejemplo de canal sin sesión es UDP, que no tiene un mecanismo de sesión subyacente. Aunque HTTP sí tiene conexiones TCP subyacentes, este hecho no se expone directamente a través de esta API y, por lo tanto, HTTP también se considera un canal sin sesión.

![Diagrama que muestra los tipos de canal con sesión y con sesión.](images/channeltypes.png)

Aunque los tipos de canales describen la dirección y la información de la sesión de un canal, no especifican cómo se implementa el canal. ¿Qué protocolo debe usar el canal? ¿Qué dificultad debe tener el canal al intentar enviar el mensaje? ¿Qué tipo de seguridad se usa? ¿Es de unidifusión o multidifusión? Esta configuración se conoce como el "enlace" del canal. El enlace se compone de lo siguiente:

-   Un [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica el protocolo de transferencia que se va a usar (TCP, UDP, http, NAMEDPIPE).
-   Una [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica cómo proteger el canal.
-   Una [**\_ \_ propiedad Set WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, que especifica valores opcionales adicionales. Consulte identificador de la propiedad de canal de WS para ver la lista de propiedades. [**\_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)

![Diagrama que muestra una lista de propiedades de canal.](images/channelsandbindings.png)

## <a name="listener"></a>Agente de escucha

Para iniciar la comunicación, el cliente crea un objeto de canal. Pero ¿cómo obtiene el servicio su objeto de canal? Para ello, crea un [agente de escucha](listener.md). La creación de un agente de escucha requiere la misma información de enlace necesaria para crear un canal. Una vez que se ha creado un agente de escucha, la aplicación puede aceptar canales del agente de escucha. Dado que la aplicación puede quedar atrás en la aceptación de canales, los agentes de escucha suelen mantener una cola de canales que están preparados para aceptar (hasta alguna cuota).

![Diagrama que muestra los canales en la cola del agente de escucha.](images/channelaccept.png)

## <a name="initiating-communication-client"></a>Iniciando comunicación (cliente)

Para iniciar la comunicación en el cliente, use la siguiente secuencia.

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

## <a name="accepting-communication-server"></a>Aceptación de la comunicación (servidor)

Para aceptar las comunicaciones entrantes en el servidor, use la siguiente secuencia.

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

Para enviar mensajes, utilice la siguiente secuencia.

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La función [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) no permite la transmisión por secuencias y presupone que el cuerpo contiene un solo elemento. Para evitar estas restricciones, utilice la siguiente secuencia en lugar de **WsSendMessage**.

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

La función [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) usa la serialización para escribir los elementos del cuerpo. Para escribir los datos directamente en el escritor de XML, utilice la siguiente secuencia en lugar de **WsWriteBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

La función [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) usa la serialización para establecer los encabezados en el búfer de encabezado del mensaje. Para usar el escritor de XML para escribir un encabezado, use la siguiente secuencia en lugar de **WsAddCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a>Recibir mensajes (cliente o servidor)

Para recibir mensajes, utilice la siguiente secuencia.

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

La función [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) no permite la transmisión por secuencias y supone que el cuerpo contiene solo un elemento, y que el tipo de mensaje (acción y esquema del cuerpo) se conoce por adelantado. Para evitar estas restricciones, utilice la siguiente secuencia en lugar de **WsReceiveMessage**.

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

La función [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) usa la serialización para leer los elementos del cuerpo. Para leer los datos directamente desde el [lector XML](xml-reader.md), utilice la siguiente secuencia en lugar de **WsReadBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

Las funciones [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) usan la serialización para obtener los encabezados del búfer de encabezado del mensaje. Para usar el [lector XML](xml-reader.md) para leer un encabezado, use la siguiente secuencia en lugar de **WsGetCustomHeader**.

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

## <a name="request-reply-client"></a>Solicitar respuesta (cliente)

La realización de una solicitud-respuesta en el cliente se puede realizar con la siguiente secuencia.

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

La función [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) asume un único elemento para el cuerpo de los mensajes de solicitud y respuesta, y que el tipo de mensaje (acción y esquema del cuerpo) se conoce por adelantado. Para evitar estas limitaciones, el mensaje de solicitud y de respuesta se puede enviar manualmente, tal y como se muestra en la siguiente secuencia. Esta secuencia coincide con la secuencia anterior para enviar y recibir un mensaje, excepto donde se indique.

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

## <a name="request-reply-server"></a>Solicitar respuesta (servidor)

Para recibir un mensaje de solicitud en el servidor, use la misma secuencia que se describe en la sección anterior sobre la recepción de mensajes.

Para enviar un mensaje de respuesta o de error, use la siguiente secuencia.

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La función [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) asume un único elemento en el cuerpo y no permite la transmisión por secuencias. Para evitar estas limitaciones, utilice la siguiente secuencia. Es lo mismo que la secuencia anterior para enviar un mensaje, pero utiliza el [**\_ \_ mensaje de respuesta WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) en lugar **del \_ \_ mensaje en blanco de WS** al inicializarse.

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

El [**\_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) indica el patrón de intercambio de mensajes posible para un canal determinado. El tipo admitido varía según el enlace, como se indica a continuación:

-   [**WS \_ El \_ \_ enlace de canal http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite la [**\_ \_ \_ solicitud de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y el tipo de **\_ canal WS \_ \_ reply** en el servidor.
-   [**WS \_ El \_ \_ enlace de canal TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite la [**\_ \_ \_ \_ sesión dúplex de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y la **\_ \_ \_ \_ sesión dúplex de tipo WS Channel** en el servidor.
-   [**WS \_ El \_ \_ enlace de canal de UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite el [**\_ \_ tipo \_ dúplex de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y la **\_ \_ \_ entrada de tipo de canal de WS** en el servidor.
-   [**WS \_ El \_ \_ enlace de canal de NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite el [**\_ \_ tipo \_ dúplex de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y la **\_ \_ \_ entrada de tipo de canal de WS** en el servidor.

## <a name="message-loops"></a>Bucles de mensajes

Para cada patrón de intercambio de mensajes, hay un "bucle" específico que se puede usar para enviar o recibir mensajes. El bucle describe el orden legal de las operaciones necesarias para enviar o recibir varios mensajes. Los bucles se describen a continuación como producciones gramaticales. El término "fin" es una recepción en la que se devuelve **WS \_ \_ -End** (vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md)), que indica que no hay más mensajes disponibles en el canal. La producción paralela especifica que para Parallel (x & y) que la operación x se puede realizar simultáneamente con y.

En el cliente se utilizan los siguientes bucles:

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

En el servidor se usan los siguientes bucles:

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

El uso [**del \_ \_ enlace de \_ \_ seguridad de \_ mensaje de contexto de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) en el servidor requiere una recepción correcta antes de que se permita el envío, incluso con un canal de tipo [**WS \_ Channel \_ Type \_ \_ Session dúplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Después de la primera recepción. se aplica el bucle normal.

Tenga en cuenta que los canales de tipo [**WS \_ Channel \_ Type \_ request**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) y **WS \_ Channel \_ Type \_ reply** se pueden usar para enviar y recibir mensajes unidireccionales (así como el patrón de solicitud-respuesta estándar). Esto se logra cerrando el canal de respuesta sin enviar una respuesta. En este caso, no se recibirá ninguna respuesta en el canal de solicitud. El valor devuelto **WS \_ S \_ End** que usa el [**enlace de seguridad de mensaje de contexto de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) en el servidor requiere una recepción correcta antes de que se permita el envío, incluso con un canal de tipo **WS \_ Channel \_ Type \_ \_ sesión dúplex**. Después de la primera recepción, se aplica el bucle normal.

se devolverá, lo que indica que no hay ningún mensaje disponible.

Los bucles de cliente o servidor se pueden realizar en paralelo entre sí mediante el uso de varias instancias de canal.

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>Filtrado de mensajes

Un canal de servidor puede filtrar los mensajes recibidos que no estén destinados a la aplicación, como los mensajes que establecen un [contexto de seguridad](security-context.md). En ese caso, se devolverá **WS \_ S \_ End** de [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) y no habrá mensajes de aplicación disponibles en ese canal. Sin embargo, esto no indica que el cliente ha previsto finalizar la comunicación con el servidor. Puede haber más mensajes disponibles en otro canal. Vea [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).

## <a name="cancellation"></a>Cancelación

La función [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) se usa para cancelar la e/s pendiente para un canal. Esta API no esperará a que se completen las operaciones de e/s. Consulte el diagrama de estado de [**\_ \_ Estado de WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) y la documentación de **WsAbortChannel** para obtener más información.

La API de [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) se usa para cancelar la e/s pendiente para un agente de escucha. Esta API no esperará a que se completen las operaciones de e/s. La anulación de un agente de escucha hará que se anulen también las aceptaciones pendientes. Consulte el diagrama de estado de [**Estado del agente de \_ escucha \_ de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) y **WsAbortListener** para obtener más información.

## <a name="tcp"></a>TCP

El [**\_ enlace de \_ canales \_ TCP de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP sobre TCP. La especificación SOAP sobre TCP se basa en el mecanismo de tramas .NET.

No se admite el uso compartido de puertos en esta versión. Cada agente de escucha que se abre debe usar un número de puerto diferente.

## <a name="udp"></a>UDP

El [**\_ enlace de \_ canal \_ de WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP sobre UDP.

Hay una serie de limitaciones con el enlace UDP:

-   No se admite la seguridad.
-   Los mensajes se pueden perder o duplicar.
-   Solo se admite una codificación: [**WS \_ codificación \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).
-   Los mensajes se limitan fundamentalmente a 64k y, con frecuencia, pueden perderse si el tamaño supera la MTU de la red.

## <a name="http"></a>HTTP

El [**\_ enlace de \_ canal \_ de WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP sobre http.

Para controlar los encabezados específicos de HTTP en el cliente y en el servidor, consulte [**\_ \_ \_ asignación de mensajes HTTP de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).

Para enviar y recibir mensajes que no son SOAP en el servidor, use la codificación [**WS \_ \_ sin formato**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) para la [**codificación de propiedades de canal de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

## <a name="namedpipes"></a>NAMEDPIPES

El [**\_ enlace de \_ canal \_ de WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP a través de canalizaciones con nombre, lo que permite la comunicación con el servicio Windows Communication Foundation (WCF) mediante NetNamedPipeBinding.

## <a name="correlating-requestreply-messages"></a>Correlación de mensajes de solicitud/respuesta

Los mensajes de solicitud/respuesta se correlacionan de una de estas dos maneras:

-   La correlación se realiza utilizando el canal como mecanismo de correlación. Por ejemplo, al usar [**el \_ \_ \_ transporte de versión WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) y el [**\_ \_ \_ enlace de canal WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , la respuesta del mensaje de solicitud se correlaciona con la solicitud por el hecho de que es el cuerpo de la entidad de la respuesta http.
-   La correlación se realiza mediante los encabezados MessageID y más recientes. Este mecanismo se usa con [**WS \_ Addressing \_ versión \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) y **WS \_ Addressing \_ version \_ 0 \_ 9** (incluso cuando se usa el [**\_ enlace de \_ canal \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)). En este caso, el mensaje de solicitud incluye el encabezado MessageID. El mensaje de respuesta incluye un encabezado de actualizador que tiene el valor del encabezado MessageID de la solicitud. El encabezado de latesto permite al cliente correlacionar una respuesta con una solicitud enviada.

Las siguientes API de nivel de canal usan automáticamente los mecanismos de correlación adecuados en función de la [**versión de WS \_ Addressing \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) del canal.

-   [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

Si no se usan estas API, los encabezados se pueden agregar manualmente y se puede acceder a ellos mediante [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) o [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).

## <a name="custom-channels-and-listeners"></a>Canales y agentes de escucha personalizados

Si el conjunto predefinido de enlaces de canal no satisface las necesidades de la aplicación, se puede definir una implementación de canal personalizado y de agente de escucha mediante la especificación de un [**\_ \_ \_ enlace de canal personalizado de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) al crear el canal o el agente de escucha. La implementación real del canal/agente de escucha se especifica como un conjunto de devoluciones de llamada a través de las devoluciones de llamada de canal [**\_ \_ \_ personalizado \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) de propiedades de canal de WS o de las propiedades de las [**\_ \_ \_ \_ \_ devoluciones de llamada del agente**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) de escucha de WS. Una vez que se crea un canal personalizado o un agente de escucha, el resultado es un objeto [WS \_ Channel](ws-channel.md) o [WS \_ Listener](ws-listener.md) que se puede usar con las API existentes.

También se puede usar un canal personalizado y un agente de escucha con el proxy de servicio y el [host de servicio](service-host.md) especificando el valor de **\_ \_ \_ enlace de canal personalizado** de WS en la enumeración de [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) y las propiedades de las devoluciones de llamada de [**\_ \_ \_ \_ \_ canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) personalizadas de la propiedad de canal de servicio o el proxy de servicio de la propiedad WS Channel. [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)

## <a name="security"></a>Seguridad

El canal permite limitar la cantidad de memoria utilizada para diversos aspectos de las operaciones a través de propiedades como:

-   [**WS \_ \_ \_ tamaño máximo de los \_ \_ mensajes almacenados \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)en la propiedad del canal,
-   [**WS \_ \_ \_ tamaño máximo del \_ \_ \_ mensaje transmitido**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)por la propiedad de canal
-   [**WS \_ \_ \_ tamaño máximo de \_ \_ Inicio \_ de secuencia**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propiedad del canal,
-   [**WS \_ propiedad de canal \_ \_ tamaño máximo del \_ \_ búfer de encabezados de solicitud \_ \_ \_ http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ tamaño máximo del \_ \_ Diccionario de \_ sesión**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propiedad de canal.

Estas propiedades tienen valores predeterminados que son conservador y seguros para la mayoría de los escenarios. Los valores predeterminados y cualquier modificación que se realicen en ellos deben evaluarse detenidamente frente a posibles vectores de ataque que pueden provocar la denegación de servicio por parte de un usuario remoto.

El canal permite establecer los valores de tiempo de espera para varios aspectos de las operaciones a través de propiedades como:

-   [**WS \_ \_tiempo de \_ \_ espera de conexión**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propiedad de canal
-   [**WS \_ \_tiempo de \_ \_ espera de envío de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)
-   [**WS \_ \_tiempo de \_ \_ \_ espera de respuesta de recepción de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_tiempo de \_ \_ espera de recepción de propiedades de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_tiempo de \_ \_ espera de resolución de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)
-   [**WS \_ \_tiempo de \_ \_ espera de cierre de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Estas propiedades tienen valores predeterminados que son conservador y seguros para la mayoría de los escenarios. Aumentar los valores de tiempo de espera aumenta la cantidad de tiempo que una parte remota puede tener un recurso local activo, como la memoria, los sockets y los subprocesos que realizan la e/s sincrónica. Una aplicación debe evaluar los valores predeterminados y tener cuidado al aumentar el tiempo de espera, ya que puede abrir posibles vectores de ataque que pueden provocar la denegación de servicio desde un equipo remoto.

Algunas de las otras opciones de configuración y consideraciones de diseño de aplicaciones que se deben evaluar cuidadosamente al usar WWSAPI Channel API:

-   Cuando se usa el nivel de canal/escucha, depende de la aplicación crear y aceptar canales en el lado servidor. Del mismo modo, depende de la aplicación crear y abrir canales en el lado cliente. Una aplicación debe poner un límite superior en estas operaciones porque cada canal consume memoria y otros recursos limitados, como los sockets. Una aplicación debe ser especialmente cuidadosa cuando se crea un canal en respuesta a cualquier acción desencadenada por una parte remota.
-   Depende de la aplicación escribir la lógica para crear canales y aceptarlos. Cada canal consume recursos limitados, como la memoria y los sockets. Una aplicación debe tener un límite superior en el número de canales que está dispuesto a aceptar, o una parte remota puede realizar muchas conexiones, lo que conduce a OOM y, por tanto, a la denegación de servicio. También debe recibir activamente los mensajes de esas conexiones mediante un tiempo de espera pequeño. Si no se recibe ningún mensaje, se agotará el tiempo de espera de la operación y se liberará la conexión.
-   Es una aplicación la que envía una respuesta o un error mediante la interpretación de los encabezados SOAP ReplyTo o FaultTo. La práctica segura consiste en respetar solo un encabezado ReplyTo o FaultTo, que es "Anonymous", lo que significa que se debe usar la conexión existente (TCP, HTTP) o la IP de origen (UDP) para enviar la respuesta SOAP. Las aplicaciones deben extremar las precauciones al crear recursos (por ejemplo, un canal) para responder a una dirección diferente, a menos que la firma del mensaje sea una entidad que pueda hablar de la dirección a la que se envía la respuesta.
-   La validación realizada en la capa del canal no sustituye a la integridad de los datos obtenida a través de la seguridad. Una aplicación debe basarse en las características de seguridad de WWSAPI para asegurarse de que se comunica con una entidad de confianza y también debe confiar en la seguridad para garantizar la integridad de los datos.

Del mismo modo, hay opciones de configuración de mensajes y consideraciones de diseño de aplicaciones que se deben evaluar cuidadosamente al usar WWSAPI Message API:

-   El tamaño del montón utilizado para almacenar los encabezados de un mensaje se puede configurar mediante la propiedad de [**\_ \_ \_ \_ propiedades del montón**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) de propiedades del mensaje de WS. Aumentar este valor permite que los encabezados del mensaje consuman más memoria, lo que puede conducir a OOM.
-   El usuario del objeto de mensaje debe saber que las API de acceso de encabezado son O (n) con respecto al número de encabezados del mensaje, ya que comprueban si hay duplicados. Los diseños que requieren muchos encabezados en un mensaje pueden provocar un uso excesivo de la CPU.
-   El número máximo de encabezados en un mensaje se puede configurar mediante la propiedad [**WS \_ Message \_ propiedad \_ Max \_ Processed \_ headers**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . También hay un límite implícito basado en el tamaño del montón del mensaje. Aumentar ambos valores permite que haya más encabezados presentes, lo que agrava el tiempo necesario para buscar un encabezado (cuando se usan las API de acceso de encabezado).

 

 




