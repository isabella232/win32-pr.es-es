---
description: Se han incorporado nuevas funciones a la interfaz de Windows Sockets diseñada específicamente para facilitar la programación de Windows Sockets. Una de las ventajas de estas nuevas funciones de Windows Sockets es la compatibilidad integrada con IPv6 e IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Llamadas de función para aplicaciones Winsock de IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56fe5087e17a9a4eb1337ac803b8500b1fe9c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705620"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a><span data-ttu-id="73ed6-104">Llamadas de función para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="73ed6-104">Function Calls for IPv6 Winsock Applications</span></span>

<span data-ttu-id="73ed6-105">Se han incorporado nuevas funciones a la interfaz de Windows Sockets diseñada específicamente para facilitar la programación de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="73ed6-105">New functions have been introduced to the Windows Sockets interface specifically designed to make Windows Sockets programming easier.</span></span> <span data-ttu-id="73ed6-106">Una de las ventajas de estas nuevas funciones de Windows Sockets es la compatibilidad integrada con IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="73ed6-106">One of the benefits of these new Windows Sockets functions is integrated support for both IPv6 and IPv4.</span></span>

<span data-ttu-id="73ed6-107">Entre estas nuevas funciones de Windows Sockets se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="73ed6-107">These new Windows Sockets functions include the following:</span></span>

-   [<span data-ttu-id="73ed6-108">**WSAConnectByName**</span><span class="sxs-lookup"><span data-stu-id="73ed6-108">**WSAConnectByName**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [<span data-ttu-id="73ed6-109">**WSAConnectByList**</span><span class="sxs-lookup"><span data-stu-id="73ed6-109">**WSAConnectByList**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   <span data-ttu-id="73ed6-110">familia de funciones [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**función getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)y [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span><span class="sxs-lookup"><span data-stu-id="73ed6-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) family of functions (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow), and [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span></span>
-   <span data-ttu-id="73ed6-111">familia de funciones [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**getnameinfo** y [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span><span class="sxs-lookup"><span data-stu-id="73ed6-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions (**getnameinfo** and [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span></span>

<span data-ttu-id="73ed6-112">Además, se han agregado nuevas funciones auxiliares de IP con compatibilidad para IPv6 e IPv4 para simplificar la programación de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="73ed6-112">In addition, new IP Helper functions with support for both IPv6 and IPv4 have been added to simplify Windows Sockets programming.</span></span> <span data-ttu-id="73ed6-113">Entre estas nuevas funciones auxiliares de IP se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="73ed6-113">These new IP Helper functions include the following:</span></span>

-   [<span data-ttu-id="73ed6-114">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="73ed6-114">**GetAdaptersAddresses**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

<span data-ttu-id="73ed6-115">Al agregar compatibilidad con IPv6 a una aplicación, deben usarse las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="73ed6-115">When adding IPv6 support to an application the following guidelines should be used:</span></span>

-   <span data-ttu-id="73ed6-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) para establecer una conexión a un punto de conexión a partir de un nombre de host y un puerto.</span><span class="sxs-lookup"><span data-stu-id="73ed6-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) to establish a connection to an endpoint given a host name and port.</span></span> <span data-ttu-id="73ed6-117">La función **WSAConnectByName** está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="73ed6-117">The **WSAConnectByName** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="73ed6-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) para establecer una conexión a una de una colección de extremos posibles representados por un conjunto de direcciones de destino (nombres de host y puertos).</span><span class="sxs-lookup"><span data-stu-id="73ed6-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) to establish a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).</span></span> <span data-ttu-id="73ed6-119">La función **WSAConnectByList** está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="73ed6-119">The **WSAConnectByList** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="73ed6-120">Reemplace las llamadas de función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) por llamadas a una de las nuevas funciones de Windows Sockets de [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-120">Replace [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function calls with calls to one of the new [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets functions.</span></span> <span data-ttu-id="73ed6-121">La función **función getaddrinfo** compatible con el protocolo IPv6 está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="73ed6-121">The **getaddrinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="73ed6-122">El protocolo IPv6 también se admite en Windows 2000 cuando está instalado IPv6 Technology Preview para Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="73ed6-122">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>
-   <span data-ttu-id="73ed6-123">Reemplace las llamadas a la función [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) con llamadas a una de las nuevas funciones de Windows Sockets de [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-123">Replace [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function calls with calls to one of the new [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets functions.</span></span> <span data-ttu-id="73ed6-124">La función **getnameinfo** compatible con el protocolo IPv6 está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="73ed6-124">The **getnameinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="73ed6-125">El protocolo IPv6 también se admite en Windows 2000 cuando está instalado IPv6 Technology Preview para Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="73ed6-125">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>

## <a name="wsaconnectbyname"></a><span data-ttu-id="73ed6-126">WSAConnectByName</span><span class="sxs-lookup"><span data-stu-id="73ed6-126">WSAConnectByName</span></span>

<span data-ttu-id="73ed6-127">La función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) simplifica la conexión a un punto de conexión mediante un socket basado en transmisión dado el nombre de host o la dirección IP del destino (IPv4 o IPv6).</span><span class="sxs-lookup"><span data-stu-id="73ed6-127">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function simplifies connecting to an endpoint using a stream-based socket given the destination's hostname or IP address (IPv4 or IPv6).</span></span> <span data-ttu-id="73ed6-128">Esta función reduce el código fuente necesario para crear una aplicación IP que es independiente de la versión del protocolo IP que se usa.</span><span class="sxs-lookup"><span data-stu-id="73ed6-128">This function reduces the source code required to create an IP application that is agnostic to the version of the IP protocol used.</span></span> <span data-ttu-id="73ed6-129">**WSAConnectByName** reemplaza los siguientes pasos en una aplicación TCP típica a una llamada de función única:</span><span class="sxs-lookup"><span data-stu-id="73ed6-129">**WSAConnectByName** replaces the following steps in a typical TCP application to a single function call:</span></span>

-   <span data-ttu-id="73ed6-130">Resuelva un nombre de host en un conjunto de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="73ed6-130">Resolve a hostname to a set of IP addresses.</span></span>
-   <span data-ttu-id="73ed6-131">Para cada dirección IP:</span><span class="sxs-lookup"><span data-stu-id="73ed6-131">For each IP address:</span></span>
    -   <span data-ttu-id="73ed6-132">Cree un socket de la familia de direcciones adecuada.</span><span class="sxs-lookup"><span data-stu-id="73ed6-132">Create a socket of the appropriate address family.</span></span>
    -   <span data-ttu-id="73ed6-133">Intenta conectarse a la dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="73ed6-133">Attempts to connect to the remote IP address.</span></span> <span data-ttu-id="73ed6-134">Si la conexión se realizó correctamente, devuelve; de lo contrario, se intenta la siguiente dirección IP remota para el host.</span><span class="sxs-lookup"><span data-stu-id="73ed6-134">If the connection was successful, it returns; otherwise the next remote IP address for the host is tried.</span></span>

<span data-ttu-id="73ed6-135">La función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) va más allá de resolver el nombre y, a continuación, intentar conectarse.</span><span class="sxs-lookup"><span data-stu-id="73ed6-135">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function goes beyond just resolving the name and then attempting to connect.</span></span> <span data-ttu-id="73ed6-136">La función usa todas las direcciones remotas devueltas por la resolución de nombres y todas las direcciones IP de origen de la máquina local.</span><span class="sxs-lookup"><span data-stu-id="73ed6-136">The function uses all of the remote addresses returned by name resolution and all of the local machine's source IP addresses.</span></span> <span data-ttu-id="73ed6-137">Primero intenta conectarse usando pares de direcciones con la mayor probabilidad de éxito.</span><span class="sxs-lookup"><span data-stu-id="73ed6-137">It first attempts to connect using address pairs with the highest chance of success.</span></span> <span data-ttu-id="73ed6-138">Por lo tanto, **WSAConnectByName** no solo garantiza que se establecerá una conexión si es posible, sino que también minimiza el tiempo necesario para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="73ed6-138">Therefore, **WSAConnectByName** not only ensures that a connection will be established if possible, but it also minimizes the time to establish the connection.</span></span>

<span data-ttu-id="73ed6-139">Para habilitar las comunicaciones IPv6 e IPv4, use el método siguiente:</span><span class="sxs-lookup"><span data-stu-id="73ed6-139">To enable both IPv6 and IPv4 communications, use the following method:</span></span>

-   <span data-ttu-id="73ed6-140">Se debe llamar a [**la función V6ONLY**](/windows/desktop/api/winsock/nf-winsock-setsockopt) en un socket creado para la \_ familia de direcciones AF inet6 para deshabilitar la opción de socket **\_ de IPv6** antes de llamar a [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span><span class="sxs-lookup"><span data-stu-id="73ed6-140">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span></span> <span data-ttu-id="73ed6-141">Esto se logra mediante una llamada a la **función de la función de** llamada en el socket con el parámetro *Level* establecido en **IPPROTO \_ IPv6** (consulte [ \_ las opciones de socket IPv6 de IPPROTO](ipproto-ipv6-socket-options.md)), el parámetro *optname* establecido en **IPv6 \_ V6ONLY** y el valor del parámetro *optvalue* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="73ed6-141">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>

<span data-ttu-id="73ed6-142">Si una aplicación necesita enlazarse a un puerto o una dirección local específicos, no se puede usar [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) , ya que el parámetro de socket para **WSAConnectByName** debe ser un socket sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="73ed6-142">If an application needs to bind to a specific local address or port, then [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) cannot be used since the socket parameter to **WSAConnectByName** must be an unbound socket.</span></span>

<span data-ttu-id="73ed6-143">En el ejemplo de código siguiente se muestran solo algunas líneas de código que se necesitan para usar esta función con el fin de implementar una aplicación que es independiente de la versión de IP.</span><span class="sxs-lookup"><span data-stu-id="73ed6-143">The code example below shows only a few lines of code are needed to use this function to implement an application that is agnostic to the IP version.</span></span>

<span data-ttu-id="73ed6-144">Establecer una conexión mediante [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span><span class="sxs-lookup"><span data-stu-id="73ed6-144">Establish a connection using [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a><span data-ttu-id="73ed6-145">WSAConnectByList</span><span class="sxs-lookup"><span data-stu-id="73ed6-145">WSAConnectByList</span></span>

<span data-ttu-id="73ed6-146">La función [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) establece una conexión a un host dado un conjunto de hosts posibles (representado por un conjunto de puertos y direcciones IP de destino).</span><span class="sxs-lookup"><span data-stu-id="73ed6-146">The [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function establishes a connection to a host given a set of possible hosts (represented by a set of destination IP addresses and ports).</span></span> <span data-ttu-id="73ed6-147">La función toma todas las direcciones IP y los puertos para el extremo y todas las direcciones IP de la máquina local, e intenta una conexión mediante todas las combinaciones de direcciones posibles.</span><span class="sxs-lookup"><span data-stu-id="73ed6-147">The function takes all IP addresses and ports for the endpoint and all of the local machine's IP addresses, and attempts a connection using all possible address combinations.</span></span>

<span data-ttu-id="73ed6-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) está relacionado con la función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) is related to the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function.</span></span> <span data-ttu-id="73ed6-149">En lugar de tomar un nombre de host único, **WSAConnectByList** acepta una lista de hosts (direcciones de destino y pares de puertos) y se conecta a una de las direcciones y puertos de la lista proporcionada.</span><span class="sxs-lookup"><span data-stu-id="73ed6-149">Instead of taking a single hostname, **WSAConnectByList** accepts a list of hosts (destination addresses and port pairs) and connects to one of the addresses and ports in the provided list.</span></span> <span data-ttu-id="73ed6-150">Esta función está diseñada para admitir escenarios en los que una aplicación necesita conectarse a cualquier host disponible a partir de una lista de posibles hosts.</span><span class="sxs-lookup"><span data-stu-id="73ed6-150">This function is designed to support scenarios in which an application needs to connect to any available host out of a list of potential hosts.</span></span>

<span data-ttu-id="73ed6-151">De forma similar a [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), la función [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) reduce significativamente el código fuente necesario para crear, enlazar y conectar un socket.</span><span class="sxs-lookup"><span data-stu-id="73ed6-151">Similar to [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), the [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function significantly reduces the source code required to create, bind and connect a socket.</span></span> <span data-ttu-id="73ed6-152">Esta función facilita la implementación de una aplicación que es independiente de la versión de IP.</span><span class="sxs-lookup"><span data-stu-id="73ed6-152">This function makes it much easier to implement an application that is agnostic to the IP version.</span></span> <span data-ttu-id="73ed6-153">La lista de direcciones de un host aceptado por esta función puede ser direcciones IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="73ed6-153">The list of addresses for a host accepted by this function may be IPv6 or IPv4 addresses.</span></span>

<span data-ttu-id="73ed6-154">Para habilitar las direcciones IPv6 e IPv4 que se van a pasar en la lista de direcciones únicas que acepta la función, se deben realizar los siguientes pasos antes de llamar a la función:</span><span class="sxs-lookup"><span data-stu-id="73ed6-154">To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the following steps must be performed prior to calling the function:</span></span>

-   <span data-ttu-id="73ed6-155">Se debe llamar a [**la función V6ONLY**](/windows/desktop/api/winsock/nf-winsock-setsockopt) en un socket creado para la \_ familia de direcciones AF inet6 para deshabilitar la opción de socket **\_ de IPv6** antes de llamar a [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span><span class="sxs-lookup"><span data-stu-id="73ed6-155">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span></span> <span data-ttu-id="73ed6-156">Esto se logra mediante una llamada a la **función de la función de** llamada en el socket con el parámetro *Level* establecido en **IPPROTO \_ IPv6** (consulte [ \_ las opciones de socket IPv6 de IPPROTO](ipproto-ipv6-socket-options.md)), el parámetro *optname* establecido en **IPv6 \_ V6ONLY** y el valor del parámetro *optvalue* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="73ed6-156">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>
-   <span data-ttu-id="73ed6-157">Todas las direcciones IPv4 deben representarse en el formato de dirección IPv6 asignado a IPv4, lo que permite que una aplicación solo IPv6 se comunique con un nodo IPv4.</span><span class="sxs-lookup"><span data-stu-id="73ed6-157">Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.</span></span> <span data-ttu-id="73ed6-158">El formato de dirección IPv6 asignado a IPv4 permite representar la dirección IPv4 de un nodo IPv4 como una dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="73ed6-158">The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6 address.</span></span> <span data-ttu-id="73ed6-159">La dirección IPv4 se codifica en los bits 32 de orden inferior de la dirección IPv6 y los bits 96 de orden superior tienen el prefijo fijo 0:0: 0:0: FFFF.</span><span class="sxs-lookup"><span data-stu-id="73ed6-159">The IPv4 address is encoded into the low-order 32 bits of the IPv6 address, and the high-order 96 bits hold the fixed prefix 0:0:0:0:0:FFFF.</span></span> <span data-ttu-id="73ed6-160">El formato de dirección IPv6 asignado a IPv4 se especifica en RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="73ed6-160">The IPv4-mapped IPv6 address format is specified in RFC 4291.</span></span> <span data-ttu-id="73ed6-161">Para obtener más información, consulte [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span><span class="sxs-lookup"><span data-stu-id="73ed6-161">For more information, see [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span></span> <span data-ttu-id="73ed6-162">La \_ macro IN6ADDR SETV4MAPPED de *Mstcpip. h* se puede usar para convertir una dirección IPv4 en el formato de dirección IPv6 asignado a IPv4 requerido.</span><span class="sxs-lookup"><span data-stu-id="73ed6-162">The IN6ADDR\_SETV4MAPPED macro in *Mstcpip.h* can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</span></span>

<span data-ttu-id="73ed6-163">Establecer una conexión mediante [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span><span class="sxs-lookup"><span data-stu-id="73ed6-163">Establish a Connection Using [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a><span data-ttu-id="73ed6-164">getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="73ed6-164">getaddrinfo</span></span>

<span data-ttu-id="73ed6-165">La función **función getaddrinfo** también realiza el trabajo de procesamiento de muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="73ed6-165">The **getaddrinfo** function also performs the processing work of many functions.</span></span> <span data-ttu-id="73ed6-166">Anteriormente, las llamadas a un número de funciones de Windows Sockets eran necesarias para crear, abrir y enlazar una dirección a un socket.</span><span class="sxs-lookup"><span data-stu-id="73ed6-166">Previously, calls to a number of Windows Sockets functions were required to create, open, and then bind an address to a socket.</span></span> <span data-ttu-id="73ed6-167">Con la función **función getaddrinfo** , las líneas de código fuente necesarias para realizar este trabajo se pueden reducir considerablemente.</span><span class="sxs-lookup"><span data-stu-id="73ed6-167">With the **getaddrinfo** function, the lines of source code necessary to perform such work can be significantly reduced.</span></span> <span data-ttu-id="73ed6-168">En los dos ejemplos siguientes se muestra el código fuente necesario para realizar estas tareas con y sin la función **función getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="73ed6-168">The following two examples illustrate the source code necessary to perform these tasks with and without the **getaddrinfo** function.</span></span>

<span data-ttu-id="73ed6-169">Realización de una apertura, conexión y enlace mediante **función getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="73ed6-169">Perform an Open, Connect, and Bind Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="73ed6-170">Realización de una apertura, conexión y enlace sin usar **función getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="73ed6-170">Perform an Open, Connect, and Bind Without Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="73ed6-171">Observe que los dos ejemplos de código fuente realizan las mismas tareas, pero el primer ejemplo, con la función **función getaddrinfo** , requiere menos líneas de código fuente y puede controlar direcciones IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="73ed6-171">Notice that both of these source code examples perform the same tasks, but the first example, using the **getaddrinfo** function, requires fewer lines of source code, and can handle either IPv6 or IPv4 addresses.</span></span> <span data-ttu-id="73ed6-172">El número de líneas de código fuente que se eliminan mediante la función **función getaddrinfo** varía.</span><span class="sxs-lookup"><span data-stu-id="73ed6-172">The number of lines of source code eliminated by using the **getaddrinfo** function varies.</span></span>

> [!Note]  
> <span data-ttu-id="73ed6-173">En el código fuente de producción, la aplicación recorrer en iteración el conjunto de direcciones devueltas por la función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) o [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-173">In production source code, your application would iterate through the set of addresses returned by the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) or [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span> <span data-ttu-id="73ed6-174">En estos ejemplos se omite ese paso en favor de simplicidad.</span><span class="sxs-lookup"><span data-stu-id="73ed6-174">These examples omit that step in favor of simplicity.</span></span>

 

<span data-ttu-id="73ed6-175">Otro problema que debe abordar al modificar una aplicación IPv4 existente para admitir IPv6 está asociado con el orden en el que se llama a las funciones.</span><span class="sxs-lookup"><span data-stu-id="73ed6-175">Another issue you must address when modifying an existing IPv4 application to support IPv6 is associated with the order in which functions are called.</span></span> <span data-ttu-id="73ed6-176">Tanto [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) como [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) requieren que se realice una secuencia de llamadas de función en un orden específico.</span><span class="sxs-lookup"><span data-stu-id="73ed6-176">Both [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) require that a sequence of function calls are made in a specific order.</span></span>

<span data-ttu-id="73ed6-177">En las plataformas en las que se usan IPv4 e IPv6, la familia de direcciones del nombre de host remoto no se conoce de antemano.</span><span class="sxs-lookup"><span data-stu-id="73ed6-177">On platforms where both IPv4 and IPv6 are used, the address family of the remote host name is not known ahead of time.</span></span> <span data-ttu-id="73ed6-178">Por lo tanto, la resolución de direcciones con la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) debe ejecutarse primero para determinar la dirección IP y la familia de direcciones del host remoto.</span><span class="sxs-lookup"><span data-stu-id="73ed6-178">So address resolution using the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function must be executed first to determine the IP address and address family of the remote host.</span></span> <span data-ttu-id="73ed6-179">A continuación, se puede llamar a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) para abrir un socket de la familia de direcciones devuelta por [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span><span class="sxs-lookup"><span data-stu-id="73ed6-179">Then the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be called to open a socket of the address family returned by [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span></span> <span data-ttu-id="73ed6-180">Se trata de un cambio importante en la forma en que se escriben las aplicaciones de Windows Sockets, ya que muchas aplicaciones de IPv4 suelen usar un orden diferente de llamadas a funciones.</span><span class="sxs-lookup"><span data-stu-id="73ed6-180">This is an important change in how Windows Sockets applications are written, since many IPv4 applications tend to use a different order of function calls.</span></span>

<span data-ttu-id="73ed6-181">La mayoría de las aplicaciones IPv4 crean primero un socket para la familia de direcciones de AF \_ inet, después realizan la resolución de nombres y, a continuación, usan el socket para conectarse a la dirección IP resuelta.</span><span class="sxs-lookup"><span data-stu-id="73ed6-181">Most IPv4 applications first create a socket for the AF\_INET address family, then do name resolution, and then use the socket to connect to the resolved IP address.</span></span> <span data-ttu-id="73ed6-182">Al hacer que estas aplicaciones sean compatibles con IPv6, la llamada a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) se debe retrasar hasta después de la resolución de nombres cuando se deteremined la familia de direcciones.</span><span class="sxs-lookup"><span data-stu-id="73ed6-182">When making such applications IPv6-capable, the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function call must be delayed until after name resolution when the address family has been deteremined.</span></span> <span data-ttu-id="73ed6-183">Tenga en cuenta que si la resolución de nombres devuelve direcciones IPv4 e IPv6, se deben usar sockets independientes de IPv4 e IPv6 para conectarse a estas direcciones de destino.</span><span class="sxs-lookup"><span data-stu-id="73ed6-183">Note that if name resolution returns both IPv4 and IPv6 addresses, then separate IPv4 and IPv6 sockets must be used to connect to these destination addresses.</span></span> <span data-ttu-id="73ed6-184">Todas estas complejidades se pueden evitar mediante el uso de la función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) en Windows Vista y versiones posteriores, por lo que se recomienda a los desarrolladores de aplicaciones que usen esta nueva función.</span><span class="sxs-lookup"><span data-stu-id="73ed6-184">All of these complexities can be avoided by using the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function on Windows Vista and later, so application developers are encouraged to use this new function.</span></span>

<span data-ttu-id="73ed6-185">En el ejemplo de código siguiente se muestra la secuencia correcta para realizar la resolución de nombres primero (realizada en la cuarta línea del siguiente ejemplo de código fuente) y, a continuación, abrir un socket (realizado en la<sup>línea 19 del</sup> ejemplo de código siguiente).</span><span class="sxs-lookup"><span data-stu-id="73ed6-185">The following code example shows the proper sequence for performing name resolution first (performed in the fourth line in the following source code example), then opening a socket (performed in the 19<sup>th</sup> line in the following code example).</span></span> <span data-ttu-id="73ed6-186">Este ejemplo es un extracto del archivo Client. c que se encuentra en el [código de cliente habilitado para IPv6](ipv6-enabled-client-code-2.md) en el Apéndice B. La función PrintError llamada en el ejemplo de código siguiente se muestra en el ejemplo de Client. c.</span><span class="sxs-lookup"><span data-stu-id="73ed6-186">This example is an excerpt from the Client.c file found in the [IPv6-Enabled Client Code](ipv6-enabled-client-code-2.md) in Appendix B. The PrintError function called in the following code example is listed in the Client.c sample.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a><span data-ttu-id="73ed6-187">Funciones de aplicación auxiliar IP</span><span class="sxs-lookup"><span data-stu-id="73ed6-187">IP Helper Functions</span></span>

<span data-ttu-id="73ed6-188">Por último, las aplicaciones que usan la función auxiliar de IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)y su información de [**\_ adaptador de \_ IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)de estructura asociada deben reconocer que esta función y estructura están limitadas a las direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="73ed6-188">Finally, applications making use of the IP Helper function [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo), and its associated structure [**IP\_ADAPTER\_INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), must recognize that both this function and structure are limited to IPv4 addresses.</span></span> <span data-ttu-id="73ed6-189">Los reemplazos habilitados para IPv6 para esta función y estructura son la función [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) y la estructura de [**direcciones del \_ adaptador \_ de IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-189">IPv6-enabled replacements for this function and structure are the [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the [**IP\_ADAPTER\_ADDRESSES**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) structure.</span></span> <span data-ttu-id="73ed6-190">Las aplicaciones habilitadas para IPv6 que usan la API auxiliar de IP deben usar la función **GetAdaptersAddresses** y la estructura de **direcciones de \_ adaptador \_ IP** habilitada para IPv6 correspondiente, ambas definidas en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="73ed6-190">IPv6-enabled applications making use of the IP Helper API should use the **GetAdaptersAddresses** function and the corresponding IPv6-enabled **IP\_ADAPTER\_ADDRESSES** structure, both defined in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="recommendations"></a><span data-ttu-id="73ed6-191">Recomendaciones</span><span class="sxs-lookup"><span data-stu-id="73ed6-191">Recommendations</span></span>

<span data-ttu-id="73ed6-192">El mejor enfoque para asegurarse de que la aplicación usa llamadas a funciones compatibles con IPv6 es usar la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para obtener la traducción de host a dirección.</span><span class="sxs-lookup"><span data-stu-id="73ed6-192">The best approach to ensure your application is using IPv6-compatible function calls is to use the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function for obtaining host-to-address translation.</span></span> <span data-ttu-id="73ed6-193">A partir de Windows XP, la función **función getaddrinfo** hace que la función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) sea innecesaria y, por tanto, la aplicación debe usar la función **función getaddrinfo** en su lugar para futuros proyectos de programación.</span><span class="sxs-lookup"><span data-stu-id="73ed6-193">Beginning with Windows XP, the **getaddrinfo** function makes the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function unnecessary, and your application should therefore use the **getaddrinfo** function instead for future programming projects.</span></span> <span data-ttu-id="73ed6-194">Aunque Microsoft seguirá admitiendo **gethostbyname**, esta función no se extenderá para admitir IPv6.</span><span class="sxs-lookup"><span data-stu-id="73ed6-194">While Microsoft will continue to support **gethostbyname**, this function will not be extended to support IPv6.</span></span> <span data-ttu-id="73ed6-195">Para obtener compatibilidad transparente para obtener información de host IPv6 e IPv4, debe usar **función getaddrinfo**.</span><span class="sxs-lookup"><span data-stu-id="73ed6-195">For transparent support for obtaining IPv6 and IPv4 host information, you must use **getaddrinfo**.</span></span>

<span data-ttu-id="73ed6-196">En el ejemplo siguiente se muestra cómo usar mejor la función **función getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="73ed6-196">The following example shows how to best use the **getaddrinfo** function.</span></span> <span data-ttu-id="73ed6-197">Observe que la función, cuando se usa correctamente como muestra este ejemplo, controla correctamente la traducción de host a dirección de IPv6 e IPv4, pero también obtiene otra información útil sobre el host, como el tipo de sockets admitido.</span><span class="sxs-lookup"><span data-stu-id="73ed6-197">Notice that the function, when used properly as this example demonstrates, handles both IPv6 and IPv4 host-to-address translation properly, but it also obtains other useful information about the host, such as the type of sockets supported.</span></span> <span data-ttu-id="73ed6-198">Este ejemplo es un extracto del ejemplo de Client. c que se encuentra en el Apéndice B.</span><span class="sxs-lookup"><span data-stu-id="73ed6-198">This sample is an excerpt from the Client.c sample found in Appendix B.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> <span data-ttu-id="73ed6-199">La versión de la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que admite IPv6 es nueva en la versión de Windows XP de Windows.</span><span class="sxs-lookup"><span data-stu-id="73ed6-199">The version of the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function that supports IPv6 is new for the Windows XP release of Windows.</span></span>

 

<span data-ttu-id="73ed6-200">Código que se debe evitar</span><span class="sxs-lookup"><span data-stu-id="73ed6-200">Code to Avoid</span></span>

<span data-ttu-id="73ed6-201">La traducción de direcciones de host se ha logrado tradicionalmente mediante la función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-201">Host address translation has traditionally been achieved using the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function.</span></span> <span data-ttu-id="73ed6-202">A partir de Windows XP:</span><span class="sxs-lookup"><span data-stu-id="73ed6-202">Beginning with Windows XP:</span></span>

-   <span data-ttu-id="73ed6-203">La función **función getaddrinfo** hace que la función **gethostbyname** esté obsoleta.</span><span class="sxs-lookup"><span data-stu-id="73ed6-203">The **getaddrinfo** function makes the **gethostbyname** function obsolete.</span></span>
-   <span data-ttu-id="73ed6-204">Las aplicaciones deben usar la función **función getaddrinfo** en lugar de la función **gethostbyname** .</span><span class="sxs-lookup"><span data-stu-id="73ed6-204">Your applications should use the **getaddrinfo** function instead of the **gethostbyname** function.</span></span>

<span data-ttu-id="73ed6-205">Tareas de codificación</span><span class="sxs-lookup"><span data-stu-id="73ed6-205">Coding Tasks</span></span>

<span data-ttu-id="73ed6-206">**Para modificar una aplicación IPv4 existente para agregar compatibilidad con IPv6**</span><span class="sxs-lookup"><span data-stu-id="73ed6-206">**To modify an existing IPv4 application to add support for IPv6**</span></span>

1.  <span data-ttu-id="73ed6-207">Adquiera la utilidad Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="73ed6-207">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="73ed6-208">Esta utilidad se instala como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="73ed6-208">This utility is installed as part of the Windows SDK.</span></span> <span data-ttu-id="73ed6-209">El Windows SDK está disponible a través de una suscripción a MSDN y también se puede descargar desde el sitio web de Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-209">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span> <span data-ttu-id="73ed6-210">También se incluyó una versión anterior de la herramienta *Checkv4.exe* como parte de Microsoft IPv6 Technology Preview para Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="73ed6-210">An older version of the *Checkv4.exe* tool was also as included as part of the Microsoft IPv6 Technology Preview for Windows 2000.</span></span>
2.  <span data-ttu-id="73ed6-211">Ejecute la utilidad *Checkv4.exe* en el código.</span><span class="sxs-lookup"><span data-stu-id="73ed6-211">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="73ed6-212">Vea [usar la utilidad de Checkv4.exe](using-the-checkv4-exe-utility-2.md) para obtener información sobre cómo ejecutar la utilidad de versión en los archivos.</span><span class="sxs-lookup"><span data-stu-id="73ed6-212">See [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md) to learn about running the version utility against your files.</span></span>
3.  <span data-ttu-id="73ed6-213">La utilidad le alerta sobre el uso de [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)y otras funciones solo de IPv4 y proporciona recomendaciones sobre cómo reemplazarlos con la función compatible con IPv6 como [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span><span class="sxs-lookup"><span data-stu-id="73ed6-213">The utility alerts you to usage of the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and other IPv4-only functions, and provides recommendations on how to replace them with the IPv6-compatible function such as [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span></span>
4.  <span data-ttu-id="73ed6-214">Reemplace todas las instancias de la función **gethostbyname** y el código asociado según corresponda, con la función **función getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="73ed6-214">Replace any instances of the **gethostbyname** function, and associated code as appropriate, with the **getaddrinfo** function.</span></span> <span data-ttu-id="73ed6-215">En Windows Vista, use la función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) o [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="73ed6-215">On Windows Vista, use the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) or [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function when appropriate.</span></span>
5.  <span data-ttu-id="73ed6-216">Reemplace todas las instancias de la función [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) y el código asociado, según corresponda, por la función [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-216">Replace any instances of the [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function, and associated code as appropriate, with the [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) function.</span></span>

<span data-ttu-id="73ed6-217">Como alternativa, puede buscar en el código base las instancias de las funciones **gethostbyname** y [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) y cambiar todo el uso (y otros códigos asociados, según corresponda) a las funciones **función getaddrinfo** y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-217">Alternatively, you can search your code base for instances of the **gethostbyname** and [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) functions, and change all such usage (and other associated code, as appropriate) to the **getaddrinfo** and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73ed6-218">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73ed6-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73ed6-219">Guía de IPv6 para aplicaciones de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="73ed6-219">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="73ed6-220">Cambiar las estructuras de datos para IPv6 Winsock Appications</span><span class="sxs-lookup"><span data-stu-id="73ed6-220">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="73ed6-221">Sockets de doble pila para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="73ed6-221">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="73ed6-222">Uso de direcciones IPv4 codificadas</span><span class="sxs-lookup"><span data-stu-id="73ed6-222">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="73ed6-223">Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="73ed6-223">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="73ed6-224">Protocolos subyacentes para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="73ed6-224">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
