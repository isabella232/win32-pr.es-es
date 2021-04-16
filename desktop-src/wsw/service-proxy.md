---
title: Proxy de servicio
description: Un proxy de servicio es el proxy de cliente para un servicio.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Servicios Web de proxy de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105689616"
---
# <a name="service-proxy"></a><span data-ttu-id="36de8-106">Proxy de servicio</span><span class="sxs-lookup"><span data-stu-id="36de8-106">Service Proxy</span></span>

<span data-ttu-id="36de8-107">Un proxy de servicio es el proxy de cliente para un servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-107">A service proxy is the client side proxy for a service.</span></span> <span data-ttu-id="36de8-108">El proxy de servicio permite a las aplicaciones enviar y recibir [mensajes](message.md) a través de un [canal](channel.md) como llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="36de8-108">The service proxy enables applications to send and receive [messages](message.md) over a [channel](channel.md) as method calls.</span></span>

<span data-ttu-id="36de8-109">Los proxies de servicio se crean según sea necesario, se abren, se usan para llamar a un servicio y se cierran cuando ya no se necesitan.</span><span class="sxs-lookup"><span data-stu-id="36de8-109">Service proxies are created as needed, opened, used to call a service, and closed when no longer needed.</span></span> <span data-ttu-id="36de8-110">Como alternativa, una aplicación puede volver a usar un proxy de servicio para conectarse repetidamente al mismo servicio sin el tiempo y los recursos necesarios para inicializar un proxy de servicio más de una vez.</span><span class="sxs-lookup"><span data-stu-id="36de8-110">Alternatively, an application may reuse a service proxy to connect repeatedly to the same service without the expenditure of time and resources required for initialising a service proxy more than once.</span></span> <span data-ttu-id="36de8-111">En el diagrama siguiente se ilustra el flujo de los posibles estados del proxy de servicio y las llamadas de función o eventos que conducen de un estado a otro.</span><span class="sxs-lookup"><span data-stu-id="36de8-111">The following diagram illustrates the flow of the possible states of the service proxy and the function calls or events that lead from one state to another.</span></span>

![Diagrama que muestra los Estados de proxy de servicio y las llamadas de función o eventos que conducen de un estado a otro.](images/serviceproxystates.png)

<span data-ttu-id="36de8-113">Estos Estados de proxy de servicio se enumeran en la enumeración de [**Estado de proxy de servicio de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="36de8-113">These service proxy states are enumerated in the [**WS\_SERVICE\_PROXY\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) enumeration.</span></span>

<span data-ttu-id="36de8-114">Como se muestra en el diagrama anterior y en el código siguiente, se crea un proxy de servicio mediante una llamada a la función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="36de8-114">As the preceding diagram and the following code illustrate, a service proxy is created by a call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span> <span data-ttu-id="36de8-115">Como parámetros para esta llamada, WWSAPI proporciona las siguientes enumeraciones:</span><span class="sxs-lookup"><span data-stu-id="36de8-115">As parameters for this call, WWSAPI provides the following enumerations:</span></span>

-   [<span data-ttu-id="36de8-116">**\_tipo de canal de WS \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-116">**WS\_CHANNEL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [<span data-ttu-id="36de8-117">**\_enlace de canal de WS \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-117">**WS\_CHANNEL\_BINDING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

<span data-ttu-id="36de8-118">También acepta parámetros opcionales mediante los siguientes tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="36de8-118">It also accepts optional parameters using the following data types:</span></span>

-   [<span data-ttu-id="36de8-119">**identificador de la propiedad de proxy de WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-119">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [<span data-ttu-id="36de8-120">**Descripción de WS \_ Security \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-120">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

<span data-ttu-id="36de8-121">Una vez creado el proxy de servicio, la función **WsCreateServiceProxy** devuelve una referencia al proxy de servicio, [el \_ \_ proxy de servicio WS](ws-service-proxy.md), a través de un parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="36de8-121">When the service proxy has been created, the **WsCreateServiceProxy** function returns a reference to the service proxy, [WS\_SERVICE\_PROXY](ws-service-proxy.md), through an out parameter.</span></span>

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

<span data-ttu-id="36de8-122">Cuando se ha creado el proxy de servicio, la aplicación puede abrir el proxy de servicio para la comunicación con un servicio llamando a la función [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , pasando una estructura de [**direcciones**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contiene la dirección de red del extremo de servicio al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="36de8-122">When the service proxy has been created, the application can open the service proxy for communication to a service by calling the [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) function, passing an [**address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure containing the network address of the service endpoint to connect to.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

<span data-ttu-id="36de8-123">Cuando se ha abierto el proxy del servicio, la aplicación puede utilizarlo para realizar llamadas al servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-123">When the service proxy has been opened, the application can use it to make calls to the service.</span></span>

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

<span data-ttu-id="36de8-124">Cuando la aplicación ya no necesita el proxy del servicio, cierra el proxy del servicio mediante una llamada a la función [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="36de8-124">When the application no longer needs the service proxy, it closes the service proxy by calling the [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) function.</span></span> <span data-ttu-id="36de8-125">También libera la memoria asociada mediante una llamada a [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="36de8-125">It also frees the associated memory by calling [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span></span>

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a><span data-ttu-id="36de8-126">Reutilización del proxy de servicio</span><span class="sxs-lookup"><span data-stu-id="36de8-126">Reusing the Service Proxy</span></span>

<span data-ttu-id="36de8-127">Como alternativa, después de llamar a [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , una aplicación puede volver a usar el proxy de servicio mediante una llamada a la función [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="36de8-127">Alternatively, after calling [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) an application can reuse the service proxy by calling the [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) function.</span></span>

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

<span data-ttu-id="36de8-128">Para obtener más información sobre cómo se usan los proxies de servicio en distintos contextos, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="36de8-128">For more information on how service proxies are used in different contexts, see the following topics:</span></span>

-   [<span data-ttu-id="36de8-129">Proxy de servicio y sesiones</span><span class="sxs-lookup"><span data-stu-id="36de8-129">Service Proxy and Sessions</span></span>](service-proxy-and-sessions.md)
-   [<span data-ttu-id="36de8-130">Operación de servicio</span><span class="sxs-lookup"><span data-stu-id="36de8-130">Service Operation</span></span>](service-operation.md)
-   [<span data-ttu-id="36de8-131">Operaciones de servicio del lado cliente</span><span class="sxs-lookup"><span data-stu-id="36de8-131">Client Side Service Operations</span></span>](client-side-service-operations.md)
-   [<span data-ttu-id="36de8-132">HttpCalculatorClientExample</span><span class="sxs-lookup"><span data-stu-id="36de8-132">HttpCalculatorClientExample</span></span>](httpcalculatorclientexample.md)

### <a name="security"></a><span data-ttu-id="36de8-133">Seguridad</span><span class="sxs-lookup"><span data-stu-id="36de8-133">Security</span></span>

<span data-ttu-id="36de8-134">Las siguientes consideraciones sobre el diseño de la aplicación se deben anotar cuidadosamente al usar la API del proxy del servicio WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="36de8-134">Following application design considerations should be carefully noted when you use the WWSAPI service proxy API:</span></span>

-   <span data-ttu-id="36de8-135">El proxy de servicio no llevará a cabo ninguna validación de los datos más allá de la validación básica del perfil 2,0 y la serialización XML.</span><span class="sxs-lookup"><span data-stu-id="36de8-135">The service proxy will not perform any validation of the data beyond Basic Profile 2.0 validation and XML serialization.</span></span> <span data-ttu-id="36de8-136">Es responsabilidad de la aplicación validar los datos contenidos en los parámetros que recibe como parte de la llamada.</span><span class="sxs-lookup"><span data-stu-id="36de8-136">It is the responsibility of the application to validate the data contained in the parameters it receives back as part of the call.</span></span>
-   <span data-ttu-id="36de8-137">Al configurar el número máximo de llamadas pendientes en el proxy de servicio, se usa el valor de enumeración [**\_ \_ \_ ID. de propiedad del proxy WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) valor de enumeración de **WS \_ proxy \_ propiedad número de \_ \_ \_ llamadas pendientes**, que proporciona protección contra un servidor de ejecución lenta.</span><span class="sxs-lookup"><span data-stu-id="36de8-137">Configuring the maximum number of pending calls on the service proxy, by using the [**WS\_PROXY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) enumeration value **WS\_PROXY\_PROPERTY\_MAX\_PENDING\_CALLS**, provides protection against a slow running server.</span></span> <span data-ttu-id="36de8-138">El valor máximo predeterminado es 100.</span><span class="sxs-lookup"><span data-stu-id="36de8-138">The default maximum is 100.</span></span> <span data-ttu-id="36de8-139">Las aplicaciones deben tener cuidado al modificar los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="36de8-139">Applications must be careful in modifying the defaults.</span></span>
-   <span data-ttu-id="36de8-140">El proxy de servicio no proporciona ninguna garantía de seguridad más allá de las especificadas en la estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) usada para comunicarse con el servidor.</span><span class="sxs-lookup"><span data-stu-id="36de8-140">The service proxy provides no security guarantees beyond those specified in the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure used to communicate with the server.</span></span>
-   <span data-ttu-id="36de8-141">Tenga cuidado al modificar los valores predeterminados de [mensajes](message.md) y [canales](channel.md) en el proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-141">Take care when you modifying [message](message.md) and [channel](channel.md) defaults on the service proxy.</span></span> <span data-ttu-id="36de8-142">Lea las consideraciones de seguridad asociadas a los mensajes y canales antes de modificar cualquiera de las propiedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="36de8-142">Read the security considerations associated with messages and channels before you modify any of the related properties.</span></span>
-   <span data-ttu-id="36de8-143">El proxy del servicio cifra todas las credenciales que mantiene en la memoria.</span><span class="sxs-lookup"><span data-stu-id="36de8-143">Service proxy encrypts all credentials that it keeps in memory.</span></span>

<span data-ttu-id="36de8-144">Los siguientes elementos de la API se relacionan con los proxies de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-144">The following API elements relate to service proxies.</span></span>

| <span data-ttu-id="36de8-145">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="36de8-145">Callback</span></span>                                                          | <span data-ttu-id="36de8-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="36de8-146">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36de8-147">**\_devolución de \_ llamada de mensaje de proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-147">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | <span data-ttu-id="36de8-148">Se invoca cuando los encabezados del mensaje de entrada están a punto de enviarse a través de o cuando se reciben los encabezados de un mensaje de salida.</span><span class="sxs-lookup"><span data-stu-id="36de8-148">Invoked when the headers of the input message are about to be sent through or when an output message headers are just received.</span></span> |



 



| <span data-ttu-id="36de8-149">Enumeración</span><span class="sxs-lookup"><span data-stu-id="36de8-149">Enumeration</span></span>                                                 | <span data-ttu-id="36de8-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="36de8-150">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36de8-151">**identificador de la \_ propiedad de llamada WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-151">**WS\_CALL\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | <span data-ttu-id="36de8-152">Enumera los parámetros opcionales para configurar una llamada en una operación de servicio del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="36de8-152">Enumerates optional parameters for configuring a call on a client side service operation.</span></span> |
| [<span data-ttu-id="36de8-153">**identificador de la propiedad de proxy de WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-153">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | <span data-ttu-id="36de8-154">Enumera los parámetros opcionales para configurar el proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-154">Enumerates optional parameters for configuring the service proxy.</span></span>                         |
| [<span data-ttu-id="36de8-155">**\_Estado del \_ proxy de servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-155">**WS\_SERVICE\_PROXY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | <span data-ttu-id="36de8-156">El estado del proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-156">The state of the service proxy.</span></span>                                                           |



 



| <span data-ttu-id="36de8-157">Función</span><span class="sxs-lookup"><span data-stu-id="36de8-157">Function</span></span>                                                       | <span data-ttu-id="36de8-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="36de8-158">Description</span></span>                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="36de8-159">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="36de8-159">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | <span data-ttu-id="36de8-160">Abandona una llamada especificada en un proxy de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="36de8-160">Abandons a specified call on a specified service proxy.</span></span>                           |
| [<span data-ttu-id="36de8-161">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="36de8-161">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | <span data-ttu-id="36de8-162">Cancela todas las entradas y salidas pendientes en un proxy de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="36de8-162">Cancels all pending input and output on a specified service proxy.</span></span>                |
| [<span data-ttu-id="36de8-163">**WsCall**</span><span class="sxs-lookup"><span data-stu-id="36de8-163">**WsCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | <span data-ttu-id="36de8-164">Solo interno.</span><span class="sxs-lookup"><span data-stu-id="36de8-164">Internal only.</span></span> <span data-ttu-id="36de8-165">Serializa los argumentos en un mensaje y lo envía a través del canal.</span><span class="sxs-lookup"><span data-stu-id="36de8-165">Serializes arguments into a message and sends it over the channel.</span></span> |
| [<span data-ttu-id="36de8-166">**WsCloseServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="36de8-166">**WsCloseServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | <span data-ttu-id="36de8-167">Cierra un proxy de servicio para la comunicación.</span><span class="sxs-lookup"><span data-stu-id="36de8-167">Closes a service proxy for communication.</span></span>                                         |
| [<span data-ttu-id="36de8-168">**WsCreateServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="36de8-168">**WsCreateServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | <span data-ttu-id="36de8-169">Crea un proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-169">Creates a service proxy.</span></span>                                                          |
| [<span data-ttu-id="36de8-170">**WsFreeServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="36de8-170">**WsFreeServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | <span data-ttu-id="36de8-171">Libera la memoria asociada a un proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-171">Releases the memory associated with a service proxy.</span></span>                              |
| [<span data-ttu-id="36de8-172">**WsGetServiceProxyProperty**</span><span class="sxs-lookup"><span data-stu-id="36de8-172">**WsGetServiceProxyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | <span data-ttu-id="36de8-173">Recupera una propiedad de proxy de servicio especificada.</span><span class="sxs-lookup"><span data-stu-id="36de8-173">Retrieves a specified service proxy property.</span></span>                                     |
| [<span data-ttu-id="36de8-174">**WsOpenServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="36de8-174">**WsOpenServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | <span data-ttu-id="36de8-175">Abre un proxy de servicio en un punto de conexión de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-175">Opens a service proxy to a service endpoint.</span></span>                                      |
| [<span data-ttu-id="36de8-176">**WsResetServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="36de8-176">**WsResetServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | <span data-ttu-id="36de8-177">Restablece el proxy del servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-177">Resets service proxy.</span></span>                                                             |



 



| <span data-ttu-id="36de8-178">Handle</span><span class="sxs-lookup"><span data-stu-id="36de8-178">Handle</span></span>                                     | <span data-ttu-id="36de8-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="36de8-179">Description</span></span>                                       |
|--------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="36de8-180">\_proxy de servicio WS \_</span><span class="sxs-lookup"><span data-stu-id="36de8-180">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md) | <span data-ttu-id="36de8-181">Tipo opaco que se usa para hacer referencia a un proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="36de8-181">An opaque type used to reference a service proxy.</span></span> |



 



| <span data-ttu-id="36de8-182">Estructura</span><span class="sxs-lookup"><span data-stu-id="36de8-182">Structure</span></span>                                         | <span data-ttu-id="36de8-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="36de8-183">Description</span></span>                 |
|---------------------------------------------------|-----------------------------|
| [<span data-ttu-id="36de8-184">**\_propiedad de llamada WS \_**</span><span class="sxs-lookup"><span data-stu-id="36de8-184">**WS\_CALL\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | <span data-ttu-id="36de8-185">Especifica una propiedad de llamada.</span><span class="sxs-lookup"><span data-stu-id="36de8-185">Specifies a call property.</span></span>  |
| <span data-ttu-id="36de8-186">[**WS \_ \_propiedad de proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span><span class="sxs-lookup"><span data-stu-id="36de8-186">[**WS\_PROXY\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span></span> | <span data-ttu-id="36de8-187">Especifica una propiedad de proxy.</span><span class="sxs-lookup"><span data-stu-id="36de8-187">Specifies a proxy property.</span></span> |



 

 

 




