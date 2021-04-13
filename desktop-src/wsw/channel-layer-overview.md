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
# <a name="channel-layer-overview"></a><span data-ttu-id="3d603-106">Introducción a la capa de canal</span><span class="sxs-lookup"><span data-stu-id="3d603-106">Channel Layer Overview</span></span>

<span data-ttu-id="3d603-107">La capa de canal proporciona una abstracción del canal de transporte, así como los mensajes enviados en el canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-107">The Channel Layer provides an abstraction of the transport channel as well as messages sent out on the channel.</span></span> <span data-ttu-id="3d603-108">También incluye funciones para la serialización de tipos de datos de C en estructuras SOAP y desde ellas.</span><span class="sxs-lookup"><span data-stu-id="3d603-108">It also includes functions for the serialization of C data types to and from SOAP structures.</span></span> <span data-ttu-id="3d603-109">La capa de canal permite el control total de las comunicaciones por medio de [mensajes](message.md) que se componen de datos enviados o recibidos y que contienen cuerpos y encabezados, y de [canales](channel.md) que abstraen los protocolos de intercambio de mensajes y proporcionan propiedades para personalizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="3d603-109">The Channel Layer enables full control of communications by means of [messages](message.md) consisting of data sent or received and containing bodies and headers, and [channels](channel.md) that abstract message exchange protocols and provide properties for customizing settings.</span></span>

## <a name="message"></a><span data-ttu-id="3d603-110">Message</span><span class="sxs-lookup"><span data-stu-id="3d603-110">Message</span></span>

<span data-ttu-id="3d603-111">Un [mensaje](message.md) es un objeto que encapsula datos de red, específicamente, datos que se transmiten o reciben a través de una red.</span><span class="sxs-lookup"><span data-stu-id="3d603-111">A [message](message.md) is an object that encapsulates network data — specifically, data that is transmitted or received over a network.</span></span> <span data-ttu-id="3d603-112">La estructura del mensaje se define mediante SOAP, con un conjunto discreto de encabezados y un cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3d603-112">The message structure is defined by SOAP, with a discrete set of headers and a message body.</span></span> <span data-ttu-id="3d603-113">Los encabezados se colocan en un búfer de memoria y el cuerpo del mensaje se lee o se escribe mediante una API de Stream.</span><span class="sxs-lookup"><span data-stu-id="3d603-113">The headers are placed in a memory buffer, and the message body is read or written using a stream API.</span></span>

![Diagrama que muestra el encabezado y el cuerpo de un mensaje.](images/messageenvelope.png)

<span data-ttu-id="3d603-115">Aunque el modelo de datos de un mensaje siempre es el modelo de datos XML, el formato de conexión real es flexible.</span><span class="sxs-lookup"><span data-stu-id="3d603-115">Although the data model of a message is always the XML data model, the actual wire format is flexible.</span></span> <span data-ttu-id="3d603-116">Antes de transmitir un mensaje, se codifica mediante una codificación determinada (como texto, binario o MTOM).</span><span class="sxs-lookup"><span data-stu-id="3d603-116">Before a message is transmitted, it is encoded using a particular encoding (such as Text, Binary, or MTOM).</span></span> <span data-ttu-id="3d603-117">Para obtener más información sobre las codificaciones, consulte [**\_ codificación de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .</span><span class="sxs-lookup"><span data-stu-id="3d603-117">See [**WS\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for more information on encodings.</span></span>

![Diagrama que muestra varios formatos de codificación de mensajes.](images/messageandencodings.png)

## <a name="channel"></a><span data-ttu-id="3d603-119">Canal</span><span class="sxs-lookup"><span data-stu-id="3d603-119">Channel</span></span>

<span data-ttu-id="3d603-120">Un [canal](channel.md) es un objeto que se usa para enviar y recibir mensajes en una red entre dos o más extremos.</span><span class="sxs-lookup"><span data-stu-id="3d603-120">A [channel](channel.md) is an object used to send and receive messages on a network between two or more endpoints.</span></span>

<span data-ttu-id="3d603-121">Los canales tienen datos asociados que describen cómo [tratar](endpoint-address.md) el mensaje cuando se envía.</span><span class="sxs-lookup"><span data-stu-id="3d603-121">Channels have associated data that describes how to [address](endpoint-address.md) the message when it is sent.</span></span> <span data-ttu-id="3d603-122">Enviar un mensaje en un canal es como colocarlo en un tobogán; el canal incluye la información donde debe ir el mensaje y cómo obtenerlo.</span><span class="sxs-lookup"><span data-stu-id="3d603-122">Sending a message on a channel is like placing it in a chute — the channel includes the information where the message should go and how to get it there.</span></span>

![Diagrama que muestra los canales para los mensajes.](images/channelsaschute.png)

<span data-ttu-id="3d603-124">Los canales se clasifican en [**tipos de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="3d603-124">Channels are categorized into [**channel types**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="3d603-125">Un tipo de canal especifica qué dirección pueden fluir los mensajes.</span><span class="sxs-lookup"><span data-stu-id="3d603-125">A channel type specifies which direction messages can flow.</span></span> <span data-ttu-id="3d603-126">El tipo de canal también identifica si el canal tiene sesión o sin sesión.</span><span class="sxs-lookup"><span data-stu-id="3d603-126">The channel type also identifies whether the channel is sessionful, or sessionless.</span></span> <span data-ttu-id="3d603-127">Una sesión se define como una forma abstracta de correlacionar los mensajes entre dos o más entidades.</span><span class="sxs-lookup"><span data-stu-id="3d603-127">A session is defined as an abstract way of correlating messages between two or more parties.</span></span> <span data-ttu-id="3d603-128">Un ejemplo de canal con sesión es un canal TCP, que usa la conexión TCP como la implementación de la sesión concreta.</span><span class="sxs-lookup"><span data-stu-id="3d603-128">An example of a sessionful channel is a TCP channel, which uses the TCP connection as the concrete session implementation.</span></span> <span data-ttu-id="3d603-129">Un ejemplo de canal sin sesión es UDP, que no tiene un mecanismo de sesión subyacente.</span><span class="sxs-lookup"><span data-stu-id="3d603-129">An example of a sessionless channel is UDP, which does not have an underlying session mechanism.</span></span> <span data-ttu-id="3d603-130">Aunque HTTP sí tiene conexiones TCP subyacentes, este hecho no se expone directamente a través de esta API y, por lo tanto, HTTP también se considera un canal sin sesión.</span><span class="sxs-lookup"><span data-stu-id="3d603-130">Although HTTP does have underlying TCP connections, this fact is not directly exposed through this API and therefore HTTP is also considered a sessionless channel.</span></span>

![Diagrama que muestra los tipos de canal con sesión y con sesión.](images/channeltypes.png)

<span data-ttu-id="3d603-132">Aunque los tipos de canales describen la dirección y la información de la sesión de un canal, no especifican cómo se implementa el canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-132">Although channel types describe the direction and session information for a channel, they do not specify how the channel is implemented.</span></span> <span data-ttu-id="3d603-133">¿Qué protocolo debe usar el canal?</span><span class="sxs-lookup"><span data-stu-id="3d603-133">What protocol should the channel use?</span></span> <span data-ttu-id="3d603-134">¿Qué dificultad debe tener el canal al intentar enviar el mensaje?</span><span class="sxs-lookup"><span data-stu-id="3d603-134">How hard should the channel try to deliver the message?</span></span> <span data-ttu-id="3d603-135">¿Qué tipo de seguridad se usa?</span><span class="sxs-lookup"><span data-stu-id="3d603-135">What kind of security is used?</span></span> <span data-ttu-id="3d603-136">¿Es de unidifusión o multidifusión?</span><span class="sxs-lookup"><span data-stu-id="3d603-136">Is it singlecast or multicast?</span></span> <span data-ttu-id="3d603-137">Esta configuración se conoce como el "enlace" del canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-137">These settings are referred to as the "binding" of the channel.</span></span> <span data-ttu-id="3d603-138">El enlace se compone de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3d603-138">The binding consists of the following:</span></span>

-   <span data-ttu-id="3d603-139">Un [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica el protocolo de transferencia que se va a usar (TCP, UDP, http, NAMEDPIPE).</span><span class="sxs-lookup"><span data-stu-id="3d603-139">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use (TCP, UDP, HTTP, NAMEDPIPE).</span></span>
-   <span data-ttu-id="3d603-140">Una [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica cómo proteger el canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-140">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="3d603-141">Una [**\_ \_ propiedad Set WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, que especifica valores opcionales adicionales.</span><span class="sxs-lookup"><span data-stu-id="3d603-141">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings.</span></span> <span data-ttu-id="3d603-142">Consulte identificador de la propiedad de canal de WS para ver la lista de propiedades. [**\_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="3d603-142">See [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) for the list of properties.</span></span>

![Diagrama que muestra una lista de propiedades de canal.](images/channelsandbindings.png)

## <a name="listener"></a><span data-ttu-id="3d603-144">Agente de escucha</span><span class="sxs-lookup"><span data-stu-id="3d603-144">Listener</span></span>

<span data-ttu-id="3d603-145">Para iniciar la comunicación, el cliente crea un objeto de canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-145">To start communicating, the client creates a Channel object.</span></span> <span data-ttu-id="3d603-146">Pero ¿cómo obtiene el servicio su objeto de canal?</span><span class="sxs-lookup"><span data-stu-id="3d603-146">But how does the service get its Channel object?</span></span> <span data-ttu-id="3d603-147">Para ello, crea un [agente de escucha](listener.md).</span><span class="sxs-lookup"><span data-stu-id="3d603-147">It does so by creating a [Listener](listener.md).</span></span> <span data-ttu-id="3d603-148">La creación de un agente de escucha requiere la misma información de enlace necesaria para crear un canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-148">Creating a listener requires the same binding information that is necessary to create a channel.</span></span> <span data-ttu-id="3d603-149">Una vez que se ha creado un agente de escucha, la aplicación puede aceptar canales del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="3d603-149">Once a Listener has been created, the application can Accept Channels from the Listener.</span></span> <span data-ttu-id="3d603-150">Dado que la aplicación puede quedar atrás en la aceptación de canales, los agentes de escucha suelen mantener una cola de canales que están preparados para aceptar (hasta alguna cuota).</span><span class="sxs-lookup"><span data-stu-id="3d603-150">Since the application may fall behind in accepting channels, listeners typically keep a queue of channels that are ready to accept (up to some quota).</span></span>

![Diagrama que muestra los canales en la cola del agente de escucha.](images/channelaccept.png)

## <a name="initiating-communication-client"></a><span data-ttu-id="3d603-152">Iniciando comunicación (cliente)</span><span class="sxs-lookup"><span data-stu-id="3d603-152">Initiating Communication (client)</span></span>

<span data-ttu-id="3d603-153">Para iniciar la comunicación en el cliente, use la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-153">To initiate communication on the client, use the following sequence.</span></span>

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

## <a name="accepting-communication-server"></a><span data-ttu-id="3d603-154">Aceptación de la comunicación (servidor)</span><span class="sxs-lookup"><span data-stu-id="3d603-154">Accepting Communication (server)</span></span>

<span data-ttu-id="3d603-155">Para aceptar las comunicaciones entrantes en el servidor, use la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-155">To accept incoming communications on the server, use the following sequence.</span></span>

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

## <a name="sending-messages-client-or-server"></a><span data-ttu-id="3d603-156">Envío de mensajes (cliente o servidor)</span><span class="sxs-lookup"><span data-stu-id="3d603-156">Sending Messages (client or server)</span></span>

<span data-ttu-id="3d603-157">Para enviar mensajes, utilice la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-157">To send messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="3d603-158">La función [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) no permite la transmisión por secuencias y presupone que el cuerpo contiene un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="3d603-158">The [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) function does not allow for streaming, and assumes that the body contains only one element.</span></span> <span data-ttu-id="3d603-159">Para evitar estas restricciones, utilice la siguiente secuencia en lugar de **WsSendMessage**.</span><span class="sxs-lookup"><span data-stu-id="3d603-159">To avoid these constraints, use the following sequence instead of **WsSendMessage**.</span></span>

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

<span data-ttu-id="3d603-160">La función [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) usa la serialización para escribir los elementos del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="3d603-160">The [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) function uses serialization to write the body elements.</span></span> <span data-ttu-id="3d603-161">Para escribir los datos directamente en el escritor de XML, utilice la siguiente secuencia en lugar de **WsWriteBody**.</span><span class="sxs-lookup"><span data-stu-id="3d603-161">To write the data directly to the XML Writer, use the following sequence instead of **WsWriteBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

<span data-ttu-id="3d603-162">La función [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) usa la serialización para establecer los encabezados en el búfer de encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3d603-162">The [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) function uses serialization to set the headers to the header buffer of the message.</span></span> <span data-ttu-id="3d603-163">Para usar el escritor de XML para escribir un encabezado, use la siguiente secuencia en lugar de **WsAddCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="3d603-163">To use the XML Writer to write a header, use the following sequence instead of **WsAddCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a><span data-ttu-id="3d603-164">Recibir mensajes (cliente o servidor)</span><span class="sxs-lookup"><span data-stu-id="3d603-164">Receiving Messages (client or server)</span></span>

<span data-ttu-id="3d603-165">Para recibir mensajes, utilice la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-165">To receive messages, use the following sequence.</span></span>

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

<span data-ttu-id="3d603-166">La función [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) no permite la transmisión por secuencias y supone que el cuerpo contiene solo un elemento, y que el tipo de mensaje (acción y esquema del cuerpo) se conoce por adelantado.</span><span class="sxs-lookup"><span data-stu-id="3d603-166">The [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) function does not allow for streaming, and assumes that the body contains only one element, and that the type of the message (action and schema of the body) is known up front.</span></span> <span data-ttu-id="3d603-167">Para evitar estas restricciones, utilice la siguiente secuencia en lugar de **WsReceiveMessage**.</span><span class="sxs-lookup"><span data-stu-id="3d603-167">To avoid these constraints, use the following sequence instead of **WsReceiveMessage**.</span></span>

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

<span data-ttu-id="3d603-168">La función [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) usa la serialización para leer los elementos del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="3d603-168">The [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) function uses serialization to read the body elements.</span></span> <span data-ttu-id="3d603-169">Para leer los datos directamente desde el [lector XML](xml-reader.md), utilice la siguiente secuencia en lugar de **WsReadBody**.</span><span class="sxs-lookup"><span data-stu-id="3d603-169">To read the data directly from the [XML Reader](xml-reader.md), use the following sequence instead of **WsReadBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

<span data-ttu-id="3d603-170">Las funciones [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) usan la serialización para obtener los encabezados del búfer de encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3d603-170">The [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) functions use serialization to get the headers from the header buffer of the message.</span></span> <span data-ttu-id="3d603-171">Para usar el [lector XML](xml-reader.md) para leer un encabezado, use la siguiente secuencia en lugar de **WsGetCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="3d603-171">To use the [XML Reader](xml-reader.md) to read a header, use the following sequence instead of **WsGetCustomHeader**.</span></span>

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

## <a name="request-reply-client"></a><span data-ttu-id="3d603-172">Solicitar respuesta (cliente)</span><span class="sxs-lookup"><span data-stu-id="3d603-172">Request Reply (client)</span></span>

<span data-ttu-id="3d603-173">La realización de una solicitud-respuesta en el cliente se puede realizar con la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-173">Performing a request-reply on the client can be done with the following sequence.</span></span>

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

<span data-ttu-id="3d603-174">La función [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) asume un único elemento para el cuerpo de los mensajes de solicitud y respuesta, y que el tipo de mensaje (acción y esquema del cuerpo) se conoce por adelantado.</span><span class="sxs-lookup"><span data-stu-id="3d603-174">The [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) function assumes a single element for the body of the request and reply messages, and that the type of the message (action and schema of the body) are known up front.</span></span> <span data-ttu-id="3d603-175">Para evitar estas limitaciones, el mensaje de solicitud y de respuesta se puede enviar manualmente, tal y como se muestra en la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-175">To avoid these limitations, the request and reply message can be sent manually, as shown in the following sequence.</span></span> <span data-ttu-id="3d603-176">Esta secuencia coincide con la secuencia anterior para enviar y recibir un mensaje, excepto donde se indique.</span><span class="sxs-lookup"><span data-stu-id="3d603-176">This sequence matches the earlier sequence for sending and receiving a message, except where noted.</span></span>

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

## <a name="request-reply-server"></a><span data-ttu-id="3d603-177">Solicitar respuesta (servidor)</span><span class="sxs-lookup"><span data-stu-id="3d603-177">Request Reply (server)</span></span>

<span data-ttu-id="3d603-178">Para recibir un mensaje de solicitud en el servidor, use la misma secuencia que se describe en la sección anterior sobre la recepción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3d603-178">To receive a request message on the server, use the same sequence as outlined in the previous section on receiving messages.</span></span>

<span data-ttu-id="3d603-179">Para enviar un mensaje de respuesta o de error, use la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-179">To send a reply or fault message, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="3d603-180">La función [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) asume un único elemento en el cuerpo y no permite la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="3d603-180">The [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) function assumes a single element in the body and does not allow for streaming.</span></span> <span data-ttu-id="3d603-181">Para evitar estas limitaciones, utilice la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d603-181">To avoid these limitations, use the following sequence.</span></span> <span data-ttu-id="3d603-182">Es lo mismo que la secuencia anterior para enviar un mensaje, pero utiliza el [**\_ \_ mensaje de respuesta WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) en lugar **del \_ \_ mensaje en blanco de WS** al inicializarse.</span><span class="sxs-lookup"><span data-stu-id="3d603-182">This is the same as the earlier sequence for sending a message, but uses [**WS\_REPLY\_MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) instead of **WS\_BLANK\_MESSAGE** when initializing.</span></span>

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

## <a name="message-exchange-patterns"></a><span data-ttu-id="3d603-183">Modelos de intercambio de mensajes</span><span class="sxs-lookup"><span data-stu-id="3d603-183">Message Exchange Patterns</span></span>

<span data-ttu-id="3d603-184">El [**\_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) indica el patrón de intercambio de mensajes posible para un canal determinado.</span><span class="sxs-lookup"><span data-stu-id="3d603-184">The [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) dictates the message exchange pattern possible for a given channel.</span></span> <span data-ttu-id="3d603-185">El tipo admitido varía según el enlace, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="3d603-185">The type supported, varies according to the binding, as follows:</span></span>

-   <span data-ttu-id="3d603-186">[**WS \_ El \_ \_ enlace de canal http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite la [**\_ \_ \_ solicitud de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y el tipo de **\_ canal WS \_ \_ reply** en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3d603-186">[**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_REPLY** on the server.</span></span>
-   <span data-ttu-id="3d603-187">[**WS \_ El \_ \_ enlace de canal TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite la [**\_ \_ \_ \_ sesión dúplex de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y la **\_ \_ \_ \_ sesión dúplex de tipo WS Channel** en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3d603-187">[**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION** on the server.</span></span>
-   <span data-ttu-id="3d603-188">[**WS \_ El \_ \_ enlace de canal de UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite el [**\_ \_ tipo \_ dúplex de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y la **\_ \_ \_ entrada de tipo de canal de WS** en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3d603-188">[**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>
-   <span data-ttu-id="3d603-189">[**WS \_ El \_ \_ enlace de canal de NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite el [**\_ \_ tipo \_ dúplex de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) en el cliente y la **\_ \_ \_ entrada de tipo de canal de WS** en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3d603-189">[**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>

## <a name="message-loops"></a><span data-ttu-id="3d603-190">Bucles de mensajes</span><span class="sxs-lookup"><span data-stu-id="3d603-190">Message Loops</span></span>

<span data-ttu-id="3d603-191">Para cada patrón de intercambio de mensajes, hay un "bucle" específico que se puede usar para enviar o recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="3d603-191">For each message exchange pattern, there is a specific "loop" that can be used to send or receive messages.</span></span> <span data-ttu-id="3d603-192">El bucle describe el orden legal de las operaciones necesarias para enviar o recibir varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="3d603-192">The loop describes the legal order of operations necessary to send/receive multiple messages.</span></span> <span data-ttu-id="3d603-193">Los bucles se describen a continuación como producciones gramaticales.</span><span class="sxs-lookup"><span data-stu-id="3d603-193">The loops are describes below as grammar productions.</span></span> <span data-ttu-id="3d603-194">El término "fin" es una recepción en la que se devuelve **WS \_ \_ -End** (vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md)), que indica que no hay más mensajes disponibles en el canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-194">The 'end' term is a receive where **WS\_S\_END** is returned (See [Windows Web Services Return Values](windows-web-services-return-values.md)), indicating no more messages are available on the channel.</span></span> <span data-ttu-id="3d603-195">La producción paralela especifica que para Parallel (x & y) que la operación x se puede realizar simultáneamente con y.</span><span class="sxs-lookup"><span data-stu-id="3d603-195">The parallel production specifies that for parallel(x & y) that operation x may be done concurrently with y.</span></span>

<span data-ttu-id="3d603-196">En el cliente se utilizan los siguientes bucles:</span><span class="sxs-lookup"><span data-stu-id="3d603-196">The following loops are used on the client:</span></span>

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

<span data-ttu-id="3d603-197">En el servidor se usan los siguientes bucles:</span><span class="sxs-lookup"><span data-stu-id="3d603-197">The following loops are used on the server:</span></span>

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

<span data-ttu-id="3d603-198">El uso [**del \_ \_ enlace de \_ \_ seguridad de \_ mensaje de contexto de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) en el servidor requiere una recepción correcta antes de que se permita el envío, incluso con un canal de tipo [**WS \_ Channel \_ Type \_ \_ Session dúplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="3d603-198">Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="3d603-199">Después de la primera recepción.</span><span class="sxs-lookup"><span data-stu-id="3d603-199">After the first receive.</span></span> <span data-ttu-id="3d603-200">se aplica el bucle normal.</span><span class="sxs-lookup"><span data-stu-id="3d603-200">the regular loop applies.</span></span>

<span data-ttu-id="3d603-201">Tenga en cuenta que los canales de tipo [**WS \_ Channel \_ Type \_ request**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) y **WS \_ Channel \_ Type \_ reply** se pueden usar para enviar y recibir mensajes unidireccionales (así como el patrón de solicitud-respuesta estándar).</span><span class="sxs-lookup"><span data-stu-id="3d603-201">Note that channels of type [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) and **WS\_CHANNEL\_TYPE\_REPLY** can be used to send and receive one-way messages (as well as the standard request-reply pattern).</span></span> <span data-ttu-id="3d603-202">Esto se logra cerrando el canal de respuesta sin enviar una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d603-202">This is accomplished by closing the reply channel without sending a reply.</span></span> <span data-ttu-id="3d603-203">En este caso, no se recibirá ninguna respuesta en el canal de solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d603-203">In this case, there will be no reply received on the request channel.</span></span> <span data-ttu-id="3d603-204">El valor devuelto **WS \_ S \_ End** que usa el [**enlace de seguridad de mensaje de contexto de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) en el servidor requiere una recepción correcta antes de que se permita el envío, incluso con un canal de tipo **WS \_ Channel \_ Type \_ \_ sesión dúplex**.</span><span class="sxs-lookup"><span data-stu-id="3d603-204">The return value **WS\_S\_END** Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**.</span></span> <span data-ttu-id="3d603-205">Después de la primera recepción, se aplica el bucle normal.</span><span class="sxs-lookup"><span data-stu-id="3d603-205">After the first receive the regular loop applies.</span></span>

<span data-ttu-id="3d603-206">se devolverá, lo que indica que no hay ningún mensaje disponible.</span><span class="sxs-lookup"><span data-stu-id="3d603-206">will be returned, indicating no message available.</span></span>

<span data-ttu-id="3d603-207">Los bucles de cliente o servidor se pueden realizar en paralelo entre sí mediante el uso de varias instancias de canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-207">Client or server loops may be done in parallel with each other by using multiple channel instances.</span></span>

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a><span data-ttu-id="3d603-208">Filtrado de mensajes</span><span class="sxs-lookup"><span data-stu-id="3d603-208">Message Filtering</span></span>

<span data-ttu-id="3d603-209">Un canal de servidor puede filtrar los mensajes recibidos que no estén destinados a la aplicación, como los mensajes que establecen un [contexto de seguridad](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="3d603-209">A server channel may filter received messages that are not intended for the application, such as messages that establish a [security context](security-context.md).</span></span> <span data-ttu-id="3d603-210">En ese caso, se devolverá **WS \_ S \_ End** de [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) y no habrá mensajes de aplicación disponibles en ese canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-210">In that case **WS\_S\_END** will be returned from [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) and no application messages will be available on that channel.</span></span> <span data-ttu-id="3d603-211">Sin embargo, esto no indica que el cliente ha previsto finalizar la comunicación con el servidor.</span><span class="sxs-lookup"><span data-stu-id="3d603-211">However, this does not signal that the client intended to end communication with the server.</span></span> <span data-ttu-id="3d603-212">Puede haber más mensajes disponibles en otro canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-212">More messages may be available on another channel.</span></span> <span data-ttu-id="3d603-213">Vea [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span><span class="sxs-lookup"><span data-stu-id="3d603-213">See [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span></span>

## <a name="cancellation"></a><span data-ttu-id="3d603-214">Cancelación</span><span class="sxs-lookup"><span data-stu-id="3d603-214">Cancellation</span></span>

<span data-ttu-id="3d603-215">La función [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) se usa para cancelar la e/s pendiente para un canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-215">The [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) function is used to cancel pending IO for a channel.</span></span> <span data-ttu-id="3d603-216">Esta API no esperará a que se completen las operaciones de e/s.</span><span class="sxs-lookup"><span data-stu-id="3d603-216">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="3d603-217">Consulte el diagrama de estado de [**\_ \_ Estado de WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) y la documentación de **WsAbortChannel** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3d603-217">See the [**WS\_CHANNEL\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) state diagram and documentation for **WsAbortChannel** for more information.</span></span>

<span data-ttu-id="3d603-218">La API de [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) se usa para cancelar la e/s pendiente para un agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="3d603-218">The [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API is used to cancel pending IO for a listener.</span></span> <span data-ttu-id="3d603-219">Esta API no esperará a que se completen las operaciones de e/s.</span><span class="sxs-lookup"><span data-stu-id="3d603-219">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="3d603-220">La anulación de un agente de escucha hará que se anulen también las aceptaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="3d603-220">Aborting a listener will cause any pending accepts to be aborted as well.</span></span> <span data-ttu-id="3d603-221">Consulte el diagrama de estado de [**Estado del agente de \_ escucha \_ de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) y **WsAbortListener** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3d603-221">See the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) state diagram and **WsAbortListener** for more information.</span></span>

## <a name="tcp"></a><span data-ttu-id="3d603-222">TCP</span><span class="sxs-lookup"><span data-stu-id="3d603-222">TCP</span></span>

<span data-ttu-id="3d603-223">El [**\_ enlace de \_ canales \_ TCP de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP sobre TCP.</span><span class="sxs-lookup"><span data-stu-id="3d603-223">The [**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over TCP.</span></span> <span data-ttu-id="3d603-224">La especificación SOAP sobre TCP se basa en el mecanismo de tramas .NET.</span><span class="sxs-lookup"><span data-stu-id="3d603-224">The SOAP over TCP specification builds upon the .NET Framing mechanism.</span></span>

<span data-ttu-id="3d603-225">No se admite el uso compartido de puertos en esta versión.</span><span class="sxs-lookup"><span data-stu-id="3d603-225">Port sharing is not supported in this version.</span></span> <span data-ttu-id="3d603-226">Cada agente de escucha que se abre debe usar un número de puerto diferente.</span><span class="sxs-lookup"><span data-stu-id="3d603-226">Each listener that is opened must use a different port number.</span></span>

## <a name="udp"></a><span data-ttu-id="3d603-227">UDP</span><span class="sxs-lookup"><span data-stu-id="3d603-227">UDP</span></span>

<span data-ttu-id="3d603-228">El [**\_ enlace de \_ canal \_ de WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP sobre UDP.</span><span class="sxs-lookup"><span data-stu-id="3d603-228">The [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over UDP.</span></span>

<span data-ttu-id="3d603-229">Hay una serie de limitaciones con el enlace UDP:</span><span class="sxs-lookup"><span data-stu-id="3d603-229">There are a number of limitations with the UDP binding:</span></span>

-   <span data-ttu-id="3d603-230">No se admite la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3d603-230">There is no support for security.</span></span>
-   <span data-ttu-id="3d603-231">Los mensajes se pueden perder o duplicar.</span><span class="sxs-lookup"><span data-stu-id="3d603-231">Messages may be lost or duplicated.</span></span>
-   <span data-ttu-id="3d603-232">Solo se admite una codificación: [**WS \_ codificación \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span><span class="sxs-lookup"><span data-stu-id="3d603-232">Only one encoding is supported: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span></span>
-   <span data-ttu-id="3d603-233">Los mensajes se limitan fundamentalmente a 64k y, con frecuencia, pueden perderse si el tamaño supera la MTU de la red.</span><span class="sxs-lookup"><span data-stu-id="3d603-233">Messages are fundamentally limited to 64k, and frequently have a greater chance being lost if the size exceeds the MTU of the network.</span></span>

## <a name="http"></a><span data-ttu-id="3d603-234">HTTP</span><span class="sxs-lookup"><span data-stu-id="3d603-234">HTTP</span></span>

<span data-ttu-id="3d603-235">El [**\_ enlace de \_ canal \_ de WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP sobre http.</span><span class="sxs-lookup"><span data-stu-id="3d603-235">The [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over HTTP.</span></span>

<span data-ttu-id="3d603-236">Para controlar los encabezados específicos de HTTP en el cliente y en el servidor, consulte [**\_ \_ \_ asignación de mensajes HTTP de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span><span class="sxs-lookup"><span data-stu-id="3d603-236">To control HTTP specific headers on the client and server, see [**WS\_HTTP\_MESSAGE\_MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span></span>

<span data-ttu-id="3d603-237">Para enviar y recibir mensajes que no son SOAP en el servidor, use la codificación [**WS \_ \_ sin formato**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) para la [**codificación de propiedades de canal de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="3d603-237">To send and receive non-SOAP messages on the server, use [**WS\_ENCODING\_RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

## <a name="namedpipes"></a><span data-ttu-id="3d603-238">NAMEDPIPES</span><span class="sxs-lookup"><span data-stu-id="3d603-238">NAMEDPIPES</span></span>

<span data-ttu-id="3d603-239">El [**\_ enlace de \_ canal \_ de WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) admite SOAP a través de canalizaciones con nombre, lo que permite la comunicación con el servicio Windows Communication Foundation (WCF) mediante NetNamedPipeBinding.</span><span class="sxs-lookup"><span data-stu-id="3d603-239">The [**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over named pipes, allowing communication with the Windows Communication Foundation (WCF) service using NetNamedPipeBinding.</span></span>

## <a name="correlating-requestreply-messages"></a><span data-ttu-id="3d603-240">Correlación de mensajes de solicitud/respuesta</span><span class="sxs-lookup"><span data-stu-id="3d603-240">Correlating Request/Reply Messages</span></span>

<span data-ttu-id="3d603-241">Los mensajes de solicitud/respuesta se correlacionan de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="3d603-241">Request/Reply messages are correlated in one of two ways:</span></span>

-   <span data-ttu-id="3d603-242">La correlación se realiza utilizando el canal como mecanismo de correlación.</span><span class="sxs-lookup"><span data-stu-id="3d603-242">Correlation is done using the channel as the correlation mechanism.</span></span> <span data-ttu-id="3d603-243">Por ejemplo, al usar [**el \_ \_ \_ transporte de versión WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) y el [**\_ \_ \_ enlace de canal WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , la respuesta del mensaje de solicitud se correlaciona con la solicitud por el hecho de que es el cuerpo de la entidad de la respuesta http.</span><span class="sxs-lookup"><span data-stu-id="3d603-243">For example, when using [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) the reply for the request message is correlated to the request by the fact that is it is the entity body of the HTTP response.</span></span>
-   <span data-ttu-id="3d603-244">La correlación se realiza mediante los encabezados MessageID y más recientes.</span><span class="sxs-lookup"><span data-stu-id="3d603-244">Correlation is done using the MessageID and RelatesTo headers.</span></span> <span data-ttu-id="3d603-245">Este mecanismo se usa con [**WS \_ Addressing \_ versión \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) y **WS \_ Addressing \_ version \_ 0 \_ 9** (incluso cuando se usa el [**\_ enlace de \_ canal \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span><span class="sxs-lookup"><span data-stu-id="3d603-245">This mechanism is used with [**WS\_ADDRESSING\_VERSION\_1\_0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and **WS\_ADDRESSING\_VERSION\_0\_9** (even when using [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span></span> <span data-ttu-id="3d603-246">En este caso, el mensaje de solicitud incluye el encabezado MessageID.</span><span class="sxs-lookup"><span data-stu-id="3d603-246">In this case, the request message includes the MessageID header.</span></span> <span data-ttu-id="3d603-247">El mensaje de respuesta incluye un encabezado de actualizador que tiene el valor del encabezado MessageID de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d603-247">The response message includes a RelatesTo header that has the value of the request's MessageID header.</span></span> <span data-ttu-id="3d603-248">El encabezado de latesto permite al cliente correlacionar una respuesta con una solicitud enviada.</span><span class="sxs-lookup"><span data-stu-id="3d603-248">The RelatesTo header allows the client to correlate a response with a request it sent.</span></span>

<span data-ttu-id="3d603-249">Las siguientes API de nivel de canal usan automáticamente los mecanismos de correlación adecuados en función de la [**versión de WS \_ Addressing \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) del canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-249">The following channel layer APIs automatically use the appropriate correlation mechanisms based on the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) of the channel.</span></span>

-   [<span data-ttu-id="3d603-250">**WsRequestReply**</span><span class="sxs-lookup"><span data-stu-id="3d603-250">**WsRequestReply**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [<span data-ttu-id="3d603-251">**WsSendReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="3d603-251">**WsSendReplyMessage**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [<span data-ttu-id="3d603-252">**WsSendFaultMessageForError**</span><span class="sxs-lookup"><span data-stu-id="3d603-252">**WsSendFaultMessageForError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

<span data-ttu-id="3d603-253">Si no se usan estas API, los encabezados se pueden agregar manualmente y se puede acceder a ellos mediante [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) o [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span><span class="sxs-lookup"><span data-stu-id="3d603-253">If these APIs are not used, the headers can be manually added and accessed using [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) or [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span></span>

## <a name="custom-channels-and-listeners"></a><span data-ttu-id="3d603-254">Canales y agentes de escucha personalizados</span><span class="sxs-lookup"><span data-stu-id="3d603-254">Custom Channels and Listeners</span></span>

<span data-ttu-id="3d603-255">Si el conjunto predefinido de enlaces de canal no satisface las necesidades de la aplicación, se puede definir una implementación de canal personalizado y de agente de escucha mediante la especificación de un [**\_ \_ \_ enlace de canal personalizado de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) al crear el canal o el agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="3d603-255">If the predefined set of channel bindings do not meet the needs of the application, then a custom channel and listener implementation can be defined by specifying [**WS\_CUSTOM\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) when creating the channel or listener.</span></span> <span data-ttu-id="3d603-256">La implementación real del canal/agente de escucha se especifica como un conjunto de devoluciones de llamada a través de las devoluciones de llamada de canal [**\_ \_ \_ personalizado \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) de propiedades de canal de WS o de las propiedades de las [**\_ \_ \_ \_ \_ devoluciones de llamada del agente**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) de escucha de WS.</span><span class="sxs-lookup"><span data-stu-id="3d603-256">The actual implementation of the channel/listener is specified as a set of callbacks via [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) or [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties.</span></span> <span data-ttu-id="3d603-257">Una vez que se crea un canal personalizado o un agente de escucha, el resultado es un objeto [WS \_ Channel](ws-channel.md) o [WS \_ Listener](ws-listener.md) que se puede usar con las API existentes.</span><span class="sxs-lookup"><span data-stu-id="3d603-257">Once a custom channel or listener are created, the result is a [WS\_CHANNEL](ws-channel.md) or [WS\_LISTENER](ws-listener.md) object that can be used with existing APIs.</span></span>

<span data-ttu-id="3d603-258">También se puede usar un canal personalizado y un agente de escucha con el proxy de servicio y el [host de servicio](service-host.md) especificando el valor de **\_ \_ \_ enlace de canal personalizado** de WS en la enumeración de [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) y las propiedades de las devoluciones de llamada de [**\_ \_ \_ \_ \_ canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) personalizadas de la propiedad de canal de servicio o el proxy de servicio de la propiedad WS Channel. [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)</span><span class="sxs-lookup"><span data-stu-id="3d603-258">A custom channel and listener can also be used with Service Proxy and [Service Host](service-host.md) by specifying the **WS\_CUSTOM\_CHANNEL\_BINDING** value in the [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) enumeration and the [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) and [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties when creating the Service Proxy or Service Host.</span></span>

## <a name="security"></a><span data-ttu-id="3d603-259">Seguridad</span><span class="sxs-lookup"><span data-stu-id="3d603-259">Security</span></span>

<span data-ttu-id="3d603-260">El canal permite limitar la cantidad de memoria utilizada para diversos aspectos de las operaciones a través de propiedades como:</span><span class="sxs-lookup"><span data-stu-id="3d603-260">The channel allows limiting the amount of memory used for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="3d603-261">[**WS \_ \_ \_ tamaño máximo de los \_ \_ mensajes almacenados \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)en la propiedad del canal,</span><span class="sxs-lookup"><span data-stu-id="3d603-261">[**WS\_CHANNEL\_PROPERTY\_MAX\_BUFFERED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-262">[**WS \_ \_ \_ tamaño máximo del \_ \_ \_ mensaje transmitido**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)por la propiedad de canal</span><span class="sxs-lookup"><span data-stu-id="3d603-262">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-263">[**WS \_ \_ \_ tamaño máximo de \_ \_ Inicio \_ de secuencia**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propiedad del canal,</span><span class="sxs-lookup"><span data-stu-id="3d603-263">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_START\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-264">[**WS \_ propiedad de canal \_ \_ tamaño máximo del \_ \_ búfer de encabezados de solicitud \_ \_ \_ http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="3d603-264">[**WS\_CHANNEL\_PROPERTY\_MAX\_HTTP\_REQUEST\_HEADERS\_BUFFER\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-265">[**WS \_ \_ \_ tamaño máximo del \_ \_ Diccionario de \_ sesión**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propiedad de canal.</span><span class="sxs-lookup"><span data-stu-id="3d603-265">[**WS\_CHANNEL\_PROPERTY\_MAX\_SESSION\_DICTIONARY\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="3d603-266">Estas propiedades tienen valores predeterminados que son conservador y seguros para la mayoría de los escenarios.</span><span class="sxs-lookup"><span data-stu-id="3d603-266">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="3d603-267">Los valores predeterminados y cualquier modificación que se realicen en ellos deben evaluarse detenidamente frente a posibles vectores de ataque que pueden provocar la denegación de servicio por parte de un usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="3d603-267">Default values and any modifications to them should be carefully evaluated against potential attack vectors which may cause denial of service by a remote user.</span></span>

<span data-ttu-id="3d603-268">El canal permite establecer los valores de tiempo de espera para varios aspectos de las operaciones a través de propiedades como:</span><span class="sxs-lookup"><span data-stu-id="3d603-268">The channel allows setting timeout values for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="3d603-269">[**WS \_ \_tiempo de \_ \_ espera de conexión**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propiedad de canal</span><span class="sxs-lookup"><span data-stu-id="3d603-269">[**WS\_CHANNEL\_PROPERTY\_CONNECT\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-270">[**WS \_ \_tiempo de \_ \_ espera de envío de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="3d603-270">[**WS\_CHANNEL\_PROPERTY\_SEND\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-271">[**WS \_ \_tiempo de \_ \_ \_ espera de respuesta de recepción de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="3d603-271">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_RESPONSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-272">[**WS \_ \_tiempo de \_ \_ espera de recepción de propiedades de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="3d603-272">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-273">[**WS \_ \_tiempo de \_ \_ espera de resolución de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="3d603-273">[**WS\_CHANNEL\_PROPERTY\_RESOLVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="3d603-274">[**WS \_ \_tiempo de \_ \_ espera de cierre de propiedad de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="3d603-274">[**WS\_CHANNEL\_PROPERTY\_CLOSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="3d603-275">Estas propiedades tienen valores predeterminados que son conservador y seguros para la mayoría de los escenarios.</span><span class="sxs-lookup"><span data-stu-id="3d603-275">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="3d603-276">Aumentar los valores de tiempo de espera aumenta la cantidad de tiempo que una parte remota puede tener un recurso local activo, como la memoria, los sockets y los subprocesos que realizan la e/s sincrónica.</span><span class="sxs-lookup"><span data-stu-id="3d603-276">Increasing timeout values increases the amount of time that a remote party can hold a local resource alive, such as memory, sockets, and threads doing synchronous I/O.</span></span> <span data-ttu-id="3d603-277">Una aplicación debe evaluar los valores predeterminados y tener cuidado al aumentar el tiempo de espera, ya que puede abrir posibles vectores de ataque que pueden provocar la denegación de servicio desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="3d603-277">An application should evaluate the default values and use caution when increasing a timeout as it may open up potential attack vectors which may cause denial of service from a remote computer.</span></span>

<span data-ttu-id="3d603-278">Algunas de las otras opciones de configuración y consideraciones de diseño de aplicaciones que se deben evaluar cuidadosamente al usar WWSAPI Channel API:</span><span class="sxs-lookup"><span data-stu-id="3d603-278">Some of the other configuration options and application design considerations that should be carefully evaluated when using WWSAPI Channel API:</span></span>

-   <span data-ttu-id="3d603-279">Cuando se usa el nivel de canal/escucha, depende de la aplicación crear y aceptar canales en el lado servidor.</span><span class="sxs-lookup"><span data-stu-id="3d603-279">When using the channel/listener layer, it is up to the application to create and accept channels on the server side.</span></span> <span data-ttu-id="3d603-280">Del mismo modo, depende de la aplicación crear y abrir canales en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="3d603-280">Similarly, it is up to the application to create and open channels on the client side.</span></span> <span data-ttu-id="3d603-281">Una aplicación debe poner un límite superior en estas operaciones porque cada canal consume memoria y otros recursos limitados, como los sockets.</span><span class="sxs-lookup"><span data-stu-id="3d603-281">An application should put an upper bound on these operations because each channel consumes memory and other limited resources such as sockets.</span></span> <span data-ttu-id="3d603-282">Una aplicación debe ser especialmente cuidadosa cuando se crea un canal en respuesta a cualquier acción desencadenada por una parte remota.</span><span class="sxs-lookup"><span data-stu-id="3d603-282">An application should be especially careful when create a channel in response to any action triggered by a remote party.</span></span>
-   <span data-ttu-id="3d603-283">Depende de la aplicación escribir la lógica para crear canales y aceptarlos.</span><span class="sxs-lookup"><span data-stu-id="3d603-283">It is up to the application to write the logic to create channels and accept them.</span></span> <span data-ttu-id="3d603-284">Cada canal consume recursos limitados, como la memoria y los sockets.</span><span class="sxs-lookup"><span data-stu-id="3d603-284">Each channel consumes limited resources such as memory and sockets.</span></span> <span data-ttu-id="3d603-285">Una aplicación debe tener un límite superior en el número de canales que está dispuesto a aceptar, o una parte remota puede realizar muchas conexiones, lo que conduce a OOM y, por tanto, a la denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="3d603-285">An application should have an upper bound on the number of channels it is willing to accept, or a remote party could make many connections, leading to OOM and hence denial of service.</span></span> <span data-ttu-id="3d603-286">También debe recibir activamente los mensajes de esas conexiones mediante un tiempo de espera pequeño.</span><span class="sxs-lookup"><span data-stu-id="3d603-286">It should also actively receive messages from those connections using a small timeout.</span></span> <span data-ttu-id="3d603-287">Si no se recibe ningún mensaje, se agotará el tiempo de espera de la operación y se liberará la conexión.</span><span class="sxs-lookup"><span data-stu-id="3d603-287">If no messages are received, then the operation will time out and the connection should be released.</span></span>
-   <span data-ttu-id="3d603-288">Es una aplicación la que envía una respuesta o un error mediante la interpretación de los encabezados SOAP ReplyTo o FaultTo.</span><span class="sxs-lookup"><span data-stu-id="3d603-288">It is up to an application to send a reply or fault by interpreting the ReplyTo or FaultTo SOAP headers.</span></span> <span data-ttu-id="3d603-289">La práctica segura consiste en respetar solo un encabezado ReplyTo o FaultTo, que es "Anonymous", lo que significa que se debe usar la conexión existente (TCP, HTTP) o la IP de origen (UDP) para enviar la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="3d603-289">The secure practice is to only honor a ReplyTo or FaultTo header which is "anonymous", meaning that the existing connection (TCP, HTTP) or source IP (UDP) should be used to send the SOAP reply.</span></span> <span data-ttu-id="3d603-290">Las aplicaciones deben extremar las precauciones al crear recursos (por ejemplo, un canal) para responder a una dirección diferente, a menos que la firma del mensaje sea una entidad que pueda hablar de la dirección a la que se envía la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d603-290">Applications should exercise extreme caution when creating resources (such as a channel) in order to reply to a different address, unless the message was signed by a party that can speak for the address that the reply is being sent to.</span></span>
-   <span data-ttu-id="3d603-291">La validación realizada en la capa del canal no sustituye a la integridad de los datos obtenida a través de la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3d603-291">The validation done in the channel layer is no replacement for data integrity achieved through security.</span></span> <span data-ttu-id="3d603-292">Una aplicación debe basarse en las características de seguridad de WWSAPI para asegurarse de que se comunica con una entidad de confianza y también debe confiar en la seguridad para garantizar la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="3d603-292">An application must rely on security features of the WWSAPI to ensure that it is communicating with a trusted entity, and must also rely on security to ensure data integrity.</span></span>

<span data-ttu-id="3d603-293">Del mismo modo, hay opciones de configuración de mensajes y consideraciones de diseño de aplicaciones que se deben evaluar cuidadosamente al usar WWSAPI Message API:</span><span class="sxs-lookup"><span data-stu-id="3d603-293">Similarly, there are message configuration options and application design considerations that should be carefully evaluated when using WWSAPI Message API:</span></span>

-   <span data-ttu-id="3d603-294">El tamaño del montón utilizado para almacenar los encabezados de un mensaje se puede configurar mediante la propiedad de [**\_ \_ \_ \_ propiedades del montón**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) de propiedades del mensaje de WS.</span><span class="sxs-lookup"><span data-stu-id="3d603-294">The size of the heap used to store the headers of a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_HEAP\_PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="3d603-295">Aumentar este valor permite que los encabezados del mensaje consuman más memoria, lo que puede conducir a OOM.</span><span class="sxs-lookup"><span data-stu-id="3d603-295">Increasing this value allows more memory to be consumed by the headers of the message, which can lead to OOM.</span></span>
-   <span data-ttu-id="3d603-296">El usuario del objeto de mensaje debe saber que las API de acceso de encabezado son O (n) con respecto al número de encabezados del mensaje, ya que comprueban si hay duplicados.</span><span class="sxs-lookup"><span data-stu-id="3d603-296">The user of the message object must realize that the header access APIs are O(n) with respect to the number of headers in the message, since they check for duplicates.</span></span> <span data-ttu-id="3d603-297">Los diseños que requieren muchos encabezados en un mensaje pueden provocar un uso excesivo de la CPU.</span><span class="sxs-lookup"><span data-stu-id="3d603-297">Designs which require many headers in a message may lead to excessive CPU usage.</span></span>
-   <span data-ttu-id="3d603-298">El número máximo de encabezados en un mensaje se puede configurar mediante la propiedad [**WS \_ Message \_ propiedad \_ Max \_ Processed \_ headers**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="3d603-298">The maximum number of headers in a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_MAX\_PROCESSED\_HEADERS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="3d603-299">También hay un límite implícito basado en el tamaño del montón del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3d603-299">There is also an implicit limit based on the size of the heap of the message.</span></span> <span data-ttu-id="3d603-300">Aumentar ambos valores permite que haya más encabezados presentes, lo que agrava el tiempo necesario para buscar un encabezado (cuando se usan las API de acceso de encabezado).</span><span class="sxs-lookup"><span data-stu-id="3d603-300">Increasing both of these values allows more headers to be present, which compounds the time necessary to find a header (when using the header access APIs).</span></span>

 

 




