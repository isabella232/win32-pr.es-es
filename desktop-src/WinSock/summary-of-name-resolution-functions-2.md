---
description: 'Las funciones de resolución de nombres se pueden agrupar en tres categorías: instalación del servicio, consultas de cliente y aplicación auxiliar (con macros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Resumen de las funciones de resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809698"
---
# <a name="summary-of-name-resolution-functions"></a><span data-ttu-id="c4531-103">Resumen de las funciones de resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c4531-103">Summary of Name Resolution Functions</span></span>

<span data-ttu-id="c4531-104">Las funciones de resolución de nombres se pueden agrupar en tres categorías: instalación del servicio, consultas de cliente y aplicación auxiliar (con macros).</span><span class="sxs-lookup"><span data-stu-id="c4531-104">The name resolution functions can be grouped into three categories: Service installation, client queries, and helper (with macros).</span></span> <span data-ttu-id="c4531-105">Las secciones siguientes identifican las funciones de cada categoría y describen brevemente su uso previsto.</span><span class="sxs-lookup"><span data-stu-id="c4531-105">The sections that follow identify the functions in each category and briefly describe their intended use.</span></span> <span data-ttu-id="c4531-106">También se describen las estructuras de datos clave.</span><span class="sxs-lookup"><span data-stu-id="c4531-106">Key data structures are also described.</span></span>

## <a name="service-installation"></a><span data-ttu-id="c4531-107">Instalación del servicio</span><span class="sxs-lookup"><span data-stu-id="c4531-107">Service Installation</span></span>

-   [<span data-ttu-id="c4531-108">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="c4531-108">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [<span data-ttu-id="c4531-109">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="c4531-109">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [<span data-ttu-id="c4531-110">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="c4531-110">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

<span data-ttu-id="c4531-111">Cuando la clase de servicio necesaria todavía no existe, una aplicación utiliza [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) para instalar una nueva clase de servicio proporcionando un nombre de clase de servicio, un GUID para el identificador de clase de servicio y una serie de estructuras [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="c4531-111">When the required service class does not already exist, an application uses [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="c4531-112">Estas estructuras son específicas de un espacio de nombres determinado y proporcionan valores comunes, como los números de puerto TCP recomendados o los identificadores de SAP SAP.</span><span class="sxs-lookup"><span data-stu-id="c4531-112">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="c4531-113">Se puede quitar una clase de servicio llamando a [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) y proporcionando el GUID correspondiente al identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="c4531-113">A service class can be removed by calling [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="c4531-114">Una vez que existe una clase de servicio, se pueden instalar o quitar instancias específicas de un servicio a través de [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span><span class="sxs-lookup"><span data-stu-id="c4531-114">Once a service class exists, specific instances of a service can be installed or removed through [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span></span> <span data-ttu-id="c4531-115">Esta función toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como parámetro de entrada junto con un código de operación y marcas de operación.</span><span class="sxs-lookup"><span data-stu-id="c4531-115">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="c4531-116">El código de operación indica si el servicio se está instalando o quitando.</span><span class="sxs-lookup"><span data-stu-id="c4531-116">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="c4531-117">La estructura **WSAQUERYSET** proporciona toda la información relevante sobre el servicio, incluido el identificador de clase de servicio, el nombre de servicio (para esta instancia), la información del protocolo y el identificador de espacio de nombres aplicable, y un conjunto de direcciones de transporte en el que el servicio realiza escuchas.</span><span class="sxs-lookup"><span data-stu-id="c4531-117">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses at which the service listens.</span></span> <span data-ttu-id="c4531-118">Los servicios deben invocar **WSASetService** cuando se inicializan para anunciar su presencia en espacios de nombres dinámicos.</span><span class="sxs-lookup"><span data-stu-id="c4531-118">Services should invoke **WSASetService** when they initialize to advertise their presence in dynamic namespaces.</span></span>

## <a name="client-query"></a><span data-ttu-id="c4531-119">Consulta de cliente</span><span class="sxs-lookup"><span data-stu-id="c4531-119">Client Query</span></span>

-   [<span data-ttu-id="c4531-120">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="c4531-120">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [<span data-ttu-id="c4531-121">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="c4531-121">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [<span data-ttu-id="c4531-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="c4531-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [<span data-ttu-id="c4531-123">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="c4531-123">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

<span data-ttu-id="c4531-124">La función [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) permite a una aplicación detectar los espacios de nombres a los que se puede tener acceso a través de las funciones de resolución de nombres de Winsock.</span><span class="sxs-lookup"><span data-stu-id="c4531-124">The [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) function allows an application to discover which namespaces are accessible through Winsock name resolution facilities.</span></span> <span data-ttu-id="c4531-125">También permite que una aplicación determine si un espacio de nombres determinado es compatible con más de un proveedor de espacios de nombres y para detectar el identificador de proveedor para cualquier proveedor de espacio de nombres concreto.</span><span class="sxs-lookup"><span data-stu-id="c4531-125">It also allows an application to determine whether a given namespace is supported by more than one namespace provider, and to discover the provider identifier for any particular namespace provider.</span></span> <span data-ttu-id="c4531-126">Mediante el uso de un identificador de proveedor, la aplicación puede restringir una operación de consulta a un proveedor de espacio de nombres especificado.</span><span class="sxs-lookup"><span data-stu-id="c4531-126">Using a provider identifier, the application can restrict a query operation to a specified namespace provider.</span></span>

<span data-ttu-id="c4531-127">Espacio de nombres Winsock: las operaciones de consulta implican una serie de llamadas: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), seguidas de una o varias llamadas a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) y finalizando con una llamada a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="c4531-127">Winsock namespace–query operations involve a series of calls: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), followed by one or more calls to [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) and ending with a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="c4531-128">**WSALookupServiceBegin** toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir los parámetros de consulta junto con un conjunto de marcas para proporcionar un mayor control sobre la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c4531-128">**WSALookupServiceBegin** takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="c4531-129">Devuelve un identificador de consulta que se utiliza en las llamadas subsiguientes a **WSALookupServiceNext** y **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="c4531-129">It returns a query handle which is used in the subsequent calls to **WSALookupServiceNext** and **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="c4531-130">La aplicación llama a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) para obtener los resultados de la consulta, con los resultados proporcionados en un búfer de [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4531-130">The application invokes [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) to obtain query results, with results supplied in an application-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="c4531-131">La aplicación continúa llamando a **WSALookupServiceNext** hasta que se devuelve el código de error WSA \_ E, lo que indica que se han \_ \_ recuperado todos los resultados.</span><span class="sxs-lookup"><span data-stu-id="c4531-131">The application continues to call **WSALookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="c4531-132">La búsqueda se termina con una llamada a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="c4531-132">The search is then terminated by a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="c4531-133">La función **WSALookupServiceEnd** también se puede usar para cancelar un **WSALookupServiceNext** pendiente actualmente cuando se llama desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="c4531-133">The **WSALookupServiceEnd** function can also be used to cancel a currently pending **WSALookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="c4531-134">En Windows Sockets 2, se definen códigos de error conflictivos para WSAENOMORE (10102) y WSA \_ e \_ no \_ más (10110).</span><span class="sxs-lookup"><span data-stu-id="c4531-134">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="c4531-135">El código de error WSAENOMORE se quitará en una versión futura y solo \_ \_ \_ se conservará WSA E.</span><span class="sxs-lookup"><span data-stu-id="c4531-135">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="c4531-136">En el caso de Windows Sockets 2, sin embargo, las aplicaciones deben comprobar tanto WSAENOMORE como WSA \_ e \_ no \_ más para la compatibilidad más amplia posible con proveedores de espacio de nombres que usan cualquiera de ellos.</span><span class="sxs-lookup"><span data-stu-id="c4531-136">For Windows Sockets 2, however, applications should check for both WSAENOMORE and WSA\_E\_NO\_MORE for the widest possible compatibility with namespace providers that use either one.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="c4531-137">Funciones del asistente</span><span class="sxs-lookup"><span data-stu-id="c4531-137">Helper Functions</span></span>

-   [<span data-ttu-id="c4531-138">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="c4531-138">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [<span data-ttu-id="c4531-139">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="c4531-139">**WSAAddressToString**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [<span data-ttu-id="c4531-140">**WSAStringToAddress**</span><span class="sxs-lookup"><span data-stu-id="c4531-140">**WSAStringToAddress**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [<span data-ttu-id="c4531-141">**WSAGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="c4531-141">**WSAGetServiceClassInfo**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

<span data-ttu-id="c4531-142">Las funciones auxiliares de resolución de nombres incluyen una función para recuperar un nombre de clase de servicio a partir de un identificador de clase de servicio, un par de funciones que se usan para traducir una dirección de transporte entre una estructura [**SOCKADDR**](sockaddr-2.md) y una representación de cadena ASCII, una función para recuperar la información de esquema de la clase de servicio para una clase de servicio determinada y un conjunto de macros para asignar servicios</span><span class="sxs-lookup"><span data-stu-id="c4531-142">The name resolution helper functions include a function to retrieve a service class name given a service class identifier, a pair of functions used to translate a transport address between a [**SOCKADDR**](sockaddr-2.md) structure and an ASCII string representation, a function to retrieve the service class schema information for a given service class, and a set of macros for mapping well known services to preallocated GUIDs.</span></span>

<span data-ttu-id="c4531-143">Las siguientes macros de WinSock2. h ayudan a asignar entre las clases de servicio conocidas y los espacios de nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4531-143">The following macros from Winsock2.h aid in mapping between well known service classes and these namespaces:</span></span>

| <span data-ttu-id="c4531-144">Macro</span><span class="sxs-lookup"><span data-stu-id="c4531-144">Macro</span></span>                                                                                                            | <span data-ttu-id="c4531-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4531-145">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4531-146">SVCID \_ TCP (puerto) SVCID \_ UDP (puerto)</span><span class="sxs-lookup"><span data-stu-id="c4531-146">SVCID\_TCP(Port) SVCID\_UDP(Port)</span></span><br/> <span data-ttu-id="c4531-147">SVCID \_ NetWare (tipo de objeto)</span><span class="sxs-lookup"><span data-stu-id="c4531-147">SVCID\_NETWARE(Object Type)</span></span><br/>                              | <span data-ttu-id="c4531-148">Dado un puerto para TCP/IP o UDP/IP, o el tipo de objeto en el caso de NetWare, devuelve el GUID (número de puerto en el orden del host).</span><span class="sxs-lookup"><span data-stu-id="c4531-148">Given a port for TCP/IP or UDP/IP or the object type in the case of NetWare, returns the GUID (port number in host order).</span></span> |
| <span data-ttu-id="c4531-149">IS \_ SVCID \_ TCP (GUID) \_ SVCID \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="c4531-149">IS\_SVCID\_TCP(GUID)IS\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="c4531-150">ES \_ SVCID \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="c4531-150">IS\_SVCID\_NETWARE(GUID)</span></span><br/>                          | <span data-ttu-id="c4531-151">Devuelve **true** si el GUID está dentro del intervalo permitido.</span><span class="sxs-lookup"><span data-stu-id="c4531-151">Returns **TRUE** if the GUID is within the allowable range.</span></span>                                                                |
| <span data-ttu-id="c4531-152">ESTABLECER \_ TCP \_ SVCID (GUID, puerto) establecer \_ UDP \_ SVCID (GUID, puerto)</span><span class="sxs-lookup"><span data-stu-id="c4531-152">SET\_TCP\_SVCID(GUID, port)SET\_UDP\_SVCID(GUID, port)</span></span><br/>                                                | <span data-ttu-id="c4531-153">Inicializa una estructura GUID con el GUID equivalente para un número de puerto TCP o UDP (el número de puerto debe estar en el orden del host).</span><span class="sxs-lookup"><span data-stu-id="c4531-153">Initializes a GUID structure with the GUID equivalent for a TCP or UDP port number (port number must be in host order).</span></span>    |
| <span data-ttu-id="c4531-154">Puerto \_ del \_ \_ puerto TCP de SVCID (GUID) \_ de \_ SVCID \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="c4531-154">PORT\_FROM\_SVCID\_TCP(GUID)PORT\_FROM\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="c4531-155">SAPID \_ de \_ SVCID \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="c4531-155">SAPID\_FROM\_SVCID\_NETWARE(GUID)</span></span><br/> | <span data-ttu-id="c4531-156">Devuelve el puerto o el tipo de objeto asociado al GUID (número de puerto en el orden del host).</span><span class="sxs-lookup"><span data-stu-id="c4531-156">Returns the port or object type associated with the GUID (port number in host order).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="c4531-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4531-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4531-158">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="c4531-158">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="c4531-159">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="c4531-159">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[<span data-ttu-id="c4531-160">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="c4531-160">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[<span data-ttu-id="c4531-161">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="c4531-161">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[<span data-ttu-id="c4531-162">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="c4531-162">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[<span data-ttu-id="c4531-163">Estructuras de datos de resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c4531-163">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="c4531-164">Modelo de resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c4531-164">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="c4531-165">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="c4531-165">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="c4531-166">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c4531-166">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="c4531-167">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="c4531-167">**SOCKADDR**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="c4531-168">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="c4531-168">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[<span data-ttu-id="c4531-169">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="c4531-169">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="c4531-170">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="c4531-170">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="c4531-171">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="c4531-171">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="c4531-172">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="c4531-172">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="c4531-173">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="c4531-173">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="c4531-174">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="c4531-174">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[<span data-ttu-id="c4531-175">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="c4531-175">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[<span data-ttu-id="c4531-176">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="c4531-176">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="c4531-177">**WSANSCLASSINFO**</span><span class="sxs-lookup"><span data-stu-id="c4531-177">**WSANSCLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




