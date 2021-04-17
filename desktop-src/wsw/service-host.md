---
title: Host de servicio
description: El host de servicio es el entorno de tiempo de ejecución para hospedar un servicio dentro de un proceso.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Servicios Web de host de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105707515"
---
# <a name="service-host"></a><span data-ttu-id="e04ff-106">Host de servicio</span><span class="sxs-lookup"><span data-stu-id="e04ff-106">Service Host</span></span>

<span data-ttu-id="e04ff-107">El host de servicio es el entorno de tiempo de ejecución para hospedar un servicio dentro de un proceso.</span><span class="sxs-lookup"><span data-stu-id="e04ff-107">The service host is the runtime environment for hosting a service within a process.</span></span>


<span data-ttu-id="e04ff-108">Un servicio puede configurar uno o más puntos de conexión dentro de un host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-108">A service can configure one or more endpoints inside a service host.</span></span>

![Diagrama que muestra la estructura de un host de servicio que contiene un punto de conexión de servicio.](images/servicehost.png)

## <a name="creating-a-service-host"></a><span data-ttu-id="e04ff-110">Creación de un host de servicio</span><span class="sxs-lookup"><span data-stu-id="e04ff-110">Creating a service host</span></span>

<span data-ttu-id="e04ff-111">Antes de crear un host de servicio, un servicio debe definir sus extremos.</span><span class="sxs-lookup"><span data-stu-id="e04ff-111">Before creating a service host, a service needs to define its endpoints.</span></span> <span data-ttu-id="e04ff-112">Un punto de conexión en el host de servicio se especifica en la estructura de [**\_ punto de \_ conexión de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) y se define mediante la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="e04ff-112">An endpoint in service host is specified in the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structure and it is defined by the following information:</span></span>

-   <span data-ttu-id="e04ff-113">Una dirección, que es el URI físico en el que se hospedará el servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-113">An address, which is the physical URI on which the service will be hosted.</span></span>
-   <span data-ttu-id="e04ff-114">Estructura [**de \_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que especifica el tipo del canal subyacente para el extremo.</span><span class="sxs-lookup"><span data-stu-id="e04ff-114">A [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) structure that specifies the type of the underlying channel for the endpoint.</span></span>
-   <span data-ttu-id="e04ff-115">Una estructura de [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) que especifica el enlace del canal.</span><span class="sxs-lookup"><span data-stu-id="e04ff-115">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) structure that specifies the binding of the channel.</span></span>
-   <span data-ttu-id="e04ff-116">Una estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contiene la descripción de seguridad para el extremo.</span><span class="sxs-lookup"><span data-stu-id="e04ff-116">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure that contains the security description for the endpoint.</span></span>
-   <span data-ttu-id="e04ff-117">Estructura [**del \_ \_ contrato de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) que representa el contrato de [servicio](contract.md) para el extremo.</span><span class="sxs-lookup"><span data-stu-id="e04ff-117">A [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure that represents the [service contract](contract.md) for the endpoint.</span></span>
-   <span data-ttu-id="e04ff-118">Una estructura de [**devolución de llamada de \_ seguridad del servicio \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) que especifica una función de devolución de llamada de autorización para el extremo.</span><span class="sxs-lookup"><span data-stu-id="e04ff-118">A [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) structure that specifies an authorization callback function for the endpoint.</span></span>
-   <span data-ttu-id="e04ff-119">Una estructura de [**\_ propiedad de punto de \_ conexión \_ de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) que contiene una matriz de propiedades de punto de conexión de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-119">A [**WS\_SERVICE\_ENDPOINT\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) structure that contains an array of service endpoint properties.</span></span>

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

<span data-ttu-id="e04ff-120">Solo se admiten contratos unidireccionales para SOAP a través de UDP, representado por el [**enlace de canal de WS \_ UDP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) en la enumeración de **enlace de \_ canal \_ de WS** .</span><span class="sxs-lookup"><span data-stu-id="e04ff-120">Only one-way contracts are supported for SOAP over UDP, represented by [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in the **WS\_CHANNEL\_BINDING** enumeration.</span></span>

<span data-ttu-id="e04ff-121">Una vez definido un punto de conexión, se puede pasar a la función [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , que toma una matriz de punteros a estructuras de punto de [**conexión de \_ servicio \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .</span><span class="sxs-lookup"><span data-stu-id="e04ff-121">After an endpoint is defined, it can be passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function, which takes an array of pointers to [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures.</span></span>

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

<span data-ttu-id="e04ff-122">Una aplicación puede proporcionar opcionalmente una matriz de [**propiedades de servicio**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) a [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) para configurar las opciones personalizadas en el host del servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-122">An application can optionally provide an array of [**service properties**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) to [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) to configure custom settings on the service host.</span></span>

<span data-ttu-id="e04ff-123">Una aplicación abre el host del servicio para iniciar la aceptación de solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="e04ff-123">An application opens the service host to start accepting client requests.</span></span>

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="e04ff-124">Después de abrir el host de servicio, la aplicación puede cerrarlo si no hay más operaciones que lo requieran.</span><span class="sxs-lookup"><span data-stu-id="e04ff-124">After opening the service host, the application can close it if there are no more operations that require it.</span></span> <span data-ttu-id="e04ff-125">Tenga en cuenta que esto no libera sus recursos y que se puede volver a abrir con una llamada subsiguiente a [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span><span class="sxs-lookup"><span data-stu-id="e04ff-125">Note that this does not release its resources, and that it can be reopened with a subsequent call to [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span></span>

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="e04ff-126">Después de cerrar el host de servicio, una aplicación puede restablecer el host de servicio para su reutilización.</span><span class="sxs-lookup"><span data-stu-id="e04ff-126">After closing the service host, an application may reset the service host for reuse.</span></span>

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

<span data-ttu-id="e04ff-127">Cuando la aplicación se realiza con el host de servicio, puede liberar los recursos asociados al host de servicio llamando a la función [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) .</span><span class="sxs-lookup"><span data-stu-id="e04ff-127">When the application is done with the service host it can free the resources associated with the service host by calling the [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) function.</span></span> <span data-ttu-id="e04ff-128">Tenga en cuenta que se debe llamar a [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="e04ff-128">Note that [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) must be called before calling this function.</span></span>

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

<span data-ttu-id="e04ff-129">Para obtener información sobre cómo asociar un estado personalizado al host de servicio, consulte [Estado de host de usuario](user-host-state.md) .</span><span class="sxs-lookup"><span data-stu-id="e04ff-129">For information on attaching a custom state to the service host, see [User Host State](user-host-state.md)</span></span>

<span data-ttu-id="e04ff-130">Para obtener información sobre la autorización en un host de servicio para un punto de conexión determinado, consulte [autorización del servicio](service-authorization.md).</span><span class="sxs-lookup"><span data-stu-id="e04ff-130">For information on authorization in a service host for a given endpoint, see [Service Authorization](service-authorization.md).</span></span>

<span data-ttu-id="e04ff-131">Para Iinformation sobre la implementación de operaciones de servicio y contratos de servicio para un servicio, consulte los temas sobre [operaciones](server-side-service-operations.md) de servicio y [contrato de servicio](contract.md).</span><span class="sxs-lookup"><span data-stu-id="e04ff-131">For iinformation on implementing service operations and service contracts for a service, see the [service operations](server-side-service-operations.md) and [service contract](contract.md)topics.</span></span>

## <a name="security"></a><span data-ttu-id="e04ff-132">Seguridad</span><span class="sxs-lookup"><span data-stu-id="e04ff-132">Security</span></span>

<span data-ttu-id="e04ff-133">Una aplicación puede usar las propiedades de seguimiento para controlar la cantidad de recursos que el host de servicio asigna en nombre de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="e04ff-133">An application can use the followin properties to control the amount of resources the service host allocates on behalf of the application:</span></span>

-   <span data-ttu-id="e04ff-134">[**WS \_ propiedad de punto de conexión de servicio \_ \_ \_ número máximo de \_ \_ canales de aceptación**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)</span><span class="sxs-lookup"><span data-stu-id="e04ff-134">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_ACCEPTING\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="e04ff-135">[**WS \_ propiedad de punto de conexión de servicio \_ \_ \_ Max \_ Concurrency**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="e04ff-135">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="e04ff-136">[**WS \_ \_ \_ \_ número máximo de \_ canales de propiedad de punto de conexión de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)</span><span class="sxs-lookup"><span data-stu-id="e04ff-136">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="e04ff-137">[**WS \_ \_ \_ \_ \_ \_ \_ tamaño máximo del montón del cuerpo de la propiedad del extremo de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="e04ff-137">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_BODY\_HEAP\_MAX\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="e04ff-138">[**WS \_ \_ \_ \_ tamaño máximo del \_ grupo de \_ llamadas \_ de propiedad de punto de conexión de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)</span><span class="sxs-lookup"><span data-stu-id="e04ff-138">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CALL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="e04ff-139">[**WS \_ \_ \_ \_ tamaño máximo de \_ grupo de \_ canales \_ de propiedad de punto de conexión de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span><span class="sxs-lookup"><span data-stu-id="e04ff-139">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNEL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span></span>

<span data-ttu-id="e04ff-140">Se eligen los valores predeterminados seguros para cada una de estas propiedades. una aplicación debe tener cuidado si desea modificar estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e04ff-140">Secure defaults are chosen for each of these properties, an application must be careful if it wishes to modify these properties.</span></span> <span data-ttu-id="e04ff-141">Además de las propiedades mencionadas anteriormente, la aplicación también puede modificar las propiedades específicas del [canal](channel.md), el [agente de escucha](listener.md) y el [mensaje](message.md) .</span><span class="sxs-lookup"><span data-stu-id="e04ff-141">Beyond the above-mentioned properties, [channel](channel.md), [listener](listener.md) and [message](message.md) specific properties can also be modified by the application.</span></span> <span data-ttu-id="e04ff-142">Consulte las consideraciones de seguridad de estos componentes antes de modificar cualquiera de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e04ff-142">Refer to the security considerations of these components before modifying any of these settings.</span></span>

<span data-ttu-id="e04ff-143">Además, las siguientes consideraciones sobre el diseño de la aplicación deben evaluarse cuidadosamente al usar la API del host del servicio WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="e04ff-143">In addition, the following application design considerations should be carefully evaluated when using WWSAPI service host API:</span></span>

-   <span data-ttu-id="e04ff-144">Al usar MEX, las aplicaciones deben tener cuidado de no divulgar los datos confidenciales.</span><span class="sxs-lookup"><span data-stu-id="e04ff-144">When using MEX, applications should be careful not to disclose any sensitive data.</span></span> <span data-ttu-id="e04ff-145">Como medida de mitigación, si la naturaleza de los datos que se exponen a través de MEX es sensible, las aplicaciones pueden optar por configurar el punto de conexión MEX con un enlace seguro que requiera autenticación al menos e implementar la autorización como parte del punto de conexión mediante la [**devolución de llamada de \_ seguridad del servicio \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="e04ff-145">As a mitigation, if the nature of the data being exposed through MEX is sensitive, applications may choose to configure the MEX endpoint with a secure binding requiring authentication at the very least and implement authorization as part of the endpoint using the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="e04ff-146">De forma predeterminada, la información de error enriquecida a través de errores está deshabilitada en el host de servicio mediante la propiedad de divulgación de errores de la [**\_ propiedad de servicio \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="e04ff-146">By default rich error information through faults is disabled on service host by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span> <span data-ttu-id="e04ff-147">Es el momento en que la aplicación envía información de error enriquecida como parte del error.</span><span class="sxs-lookup"><span data-stu-id="e04ff-147">It is upon the discretion of the application to send rich error information as part of the fault.</span></span> <span data-ttu-id="e04ff-148">Sin embargo, esto puede dar lugar a la divulgación de información y, por tanto, se recomienda que esta configuración solo se cambie para escenarios de depuración.</span><span class="sxs-lookup"><span data-stu-id="e04ff-148">However, this can result in information disclosure and thus it is recommended that this setting is only changed for debugging scenarios.</span></span>
-   <span data-ttu-id="e04ff-149">Además de la validación realizada para la serialización básica de perfiles 2,0 y XML, el host de servicio no realiza ninguna validación en el contenido de datos recibido como parte de los parámetros de operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-149">Beyond validation performed for Basic Profile 2.0 and XML serialization, service host performs no validation on the data content received as part of service operation parameters.</span></span> <span data-ttu-id="e04ff-150">Es responsabilidad de la aplicación realizar todas las validaciones de parámetros por sí misma.</span><span class="sxs-lookup"><span data-stu-id="e04ff-150">It is the responsibility of the application to perform all parameter validations on its own.</span></span>
-   <span data-ttu-id="e04ff-151">La autorización no se implementa como parte del host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-151">Authorization is not implemented as part of service host.</span></span> <span data-ttu-id="e04ff-152">Sin embargo, las aplicaciones pueden implementar su propio esquema de autorización mediante la [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) y la [**devolución de llamada de \_ \_ seguridad \_ del servicio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="e04ff-152">However, applications can implement their own authorization scheme using [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) and the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="e04ff-153">Es responsabilidad de la aplicación usar enlaces seguros en su punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="e04ff-153">It is the responsibility of the application to use secure bindings on its endpoint.</span></span> <span data-ttu-id="e04ff-154">El host de servicio no proporciona ninguna seguridad más allá de lo que se configura en el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="e04ff-154">Service host does not provide any security beyond what is configured on the endpoint.</span></span>

<span data-ttu-id="e04ff-155">Los siguientes elementos de API se usan con el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-155">The following API elements are used with the service host.</span></span>

| <span data-ttu-id="e04ff-156">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="e04ff-156">Callback</span></span>                                                                             | <span data-ttu-id="e04ff-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="e04ff-157">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="e04ff-158">**servicio WS- \_ \_ devolución de \_ llamada de canal \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-158">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | <span data-ttu-id="e04ff-159">Se invoca cuando el host de servicio acepta un canal en un agente de escucha del extremo.</span><span class="sxs-lookup"><span data-stu-id="e04ff-159">Invoked when a channel is accepted on an endpoint listener by the service host.</span></span> |
| [<span data-ttu-id="e04ff-160">**\_devolución de \_ llamada de canal de cierre de servicio WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | <span data-ttu-id="e04ff-161">Se invoca cuando se cierra o se anula un canal en un extremo.</span><span class="sxs-lookup"><span data-stu-id="e04ff-161">Invoked when a channel is closed or aborted on an endpoint.</span></span>                     |



 



| <span data-ttu-id="e04ff-162">Enumeración</span><span class="sxs-lookup"><span data-stu-id="e04ff-162">Enumeration</span></span>                                                                    | <span data-ttu-id="e04ff-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="e04ff-163">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e04ff-164">**identificador de la \_ propiedad de punto de conexión de servicio WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-164">**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | <span data-ttu-id="e04ff-165">Parámetros opcionales para configurar un [**\_ punto de \_ conexión de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="e04ff-165">Optional parameters for configuring a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span> |
| [<span data-ttu-id="e04ff-166">**\_Estado de \_ host de servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-166">**WS\_SERVICE\_HOST\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | <span data-ttu-id="e04ff-167">Los Estados en los que puede estar un host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-167">The states that a service host can be in.</span></span>                                                   |
| [<span data-ttu-id="e04ff-168">**identificador de la \_ propiedad de servicio WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-168">**WS\_SERVICE\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | <span data-ttu-id="e04ff-169">Parámetros opcionales para configurar el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-169">Optional parameters for configuring the service host.</span></span>                                       |



 



| <span data-ttu-id="e04ff-170">Función</span><span class="sxs-lookup"><span data-stu-id="e04ff-170">Function</span></span>                                                     | <span data-ttu-id="e04ff-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="e04ff-171">Description</span></span>                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e04ff-172">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="e04ff-172">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | <span data-ttu-id="e04ff-173">Interrumpe y suspende las operaciones actuales en el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-173">Interrupts and discontinues current operations on the service host.</span></span>                          |
| [<span data-ttu-id="e04ff-174">**WsCloseServiceHost**</span><span class="sxs-lookup"><span data-stu-id="e04ff-174">**WsCloseServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | <span data-ttu-id="e04ff-175">Cierra todos los agentes de escucha para que no se acepte ningún canal nuevo desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="e04ff-175">Closes all listeners so that no new channels are accepted from the client.</span></span>                   |
| [<span data-ttu-id="e04ff-176">**WsCreateServiceHost**</span><span class="sxs-lookup"><span data-stu-id="e04ff-176">**WsCreateServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | <span data-ttu-id="e04ff-177">Crea un host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-177">Creates a service host.</span></span>                                                                      |
| [<span data-ttu-id="e04ff-178">**WsFreeServiceHost**</span><span class="sxs-lookup"><span data-stu-id="e04ff-178">**WsFreeServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | <span data-ttu-id="e04ff-179">Libera la memoria asociada a un objeto host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-179">Releases the memory associated with a service host object.</span></span>                                   |
| [<span data-ttu-id="e04ff-180">**WsGetServiceHostProperty**</span><span class="sxs-lookup"><span data-stu-id="e04ff-180">**WsGetServiceHostProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | <span data-ttu-id="e04ff-181">Recupera una propiedad de host de servicio especificada.</span><span class="sxs-lookup"><span data-stu-id="e04ff-181">Retrieves a specified Service Host property.</span></span>                                                 |
| [<span data-ttu-id="e04ff-182">**WsOpenServiceHost**</span><span class="sxs-lookup"><span data-stu-id="e04ff-182">**WsOpenServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | <span data-ttu-id="e04ff-183">Abre un host de servicio para la comunicación e inicia los agentes de escucha en todos los extremos.</span><span class="sxs-lookup"><span data-stu-id="e04ff-183">Opens a service host for communication and starts the listeners on all the endpoints.</span></span>        |
| [<span data-ttu-id="e04ff-184">**WsResetServiceHost**</span><span class="sxs-lookup"><span data-stu-id="e04ff-184">**WsResetServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | <span data-ttu-id="e04ff-185">Restablece el host de servicio para reutilizarlo y restablece el canal subyacente y los agentes de escucha para su reutilización.</span><span class="sxs-lookup"><span data-stu-id="e04ff-185">Resets the service host for reuse and resets the underlying channel and listeners for reuse.</span></span> |



 



| <span data-ttu-id="e04ff-186">Handle</span><span class="sxs-lookup"><span data-stu-id="e04ff-186">Handle</span></span>                                       | <span data-ttu-id="e04ff-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="e04ff-187">Description</span></span>                                      |
|----------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="e04ff-188">**\_host de servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-188">**WS\_SERVICE\_HOST**</span></span>](ws-service-host.md) | <span data-ttu-id="e04ff-189">Tipo opaco que se usa para hacer referencia a un host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-189">An opaque type used to reference a service host.</span></span> |



 



| <span data-ttu-id="e04ff-190">Estructura</span><span class="sxs-lookup"><span data-stu-id="e04ff-190">Structure</span></span>                                                                              | <span data-ttu-id="e04ff-191">Descripción</span><span class="sxs-lookup"><span data-stu-id="e04ff-191">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="e04ff-192">**\_extremo de servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-192">**WS\_SERVICE\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | <span data-ttu-id="e04ff-193">Representa un punto de conexión individual en un host de servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-193">Represents an individual endpoint on a service host.</span></span>                            |
| [<span data-ttu-id="e04ff-194">**\_propiedad de \_ punto de conexión de servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-194">**WS\_SERVICE\_ENDPOINT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | <span data-ttu-id="e04ff-195">Especifica una configuración específica del servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-195">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="e04ff-196">**\_propiedad de servicio WS \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-196">**WS\_SERVICE\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | <span data-ttu-id="e04ff-197">Especifica una configuración específica del servicio.</span><span class="sxs-lookup"><span data-stu-id="e04ff-197">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="e04ff-198">**devolución de llamada de la \_ \_ propiedad de servicio WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-198">**WS\_SERVICE\_PROPERTY\_ACCEPT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | <span data-ttu-id="e04ff-199">Especifica la devolución de llamada a la que se llama cuando un canal se acepta correctamente.</span><span class="sxs-lookup"><span data-stu-id="e04ff-199">Specifies the callback which is called when a channel is successfully accepted.</span></span> |
| [<span data-ttu-id="e04ff-200">**\_devolución de \_ llamada de cierre de propiedad de servicio WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e04ff-200">**WS\_SERVICE\_PROPERTY\_CLOSE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | <span data-ttu-id="e04ff-201">Especifica la devolución de llamada a la que se llama cuando un canal está a punto de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="e04ff-201">Specifies the callback which is called when a channel is about to be closed.</span></span>    |



 

 

 




