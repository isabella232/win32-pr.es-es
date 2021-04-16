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
# <a name="function-calls-for-ipv6-winsock-applications"></a>Llamadas de función para aplicaciones Winsock de IPv6

Se han incorporado nuevas funciones a la interfaz de Windows Sockets diseñada específicamente para facilitar la programación de Windows Sockets. Una de las ventajas de estas nuevas funciones de Windows Sockets es la compatibilidad integrada con IPv6 e IPv4.

Entre estas nuevas funciones de Windows Sockets se incluyen las siguientes:

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   familia de funciones [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**función getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)y [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   familia de funciones [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**getnameinfo** y [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

Además, se han agregado nuevas funciones auxiliares de IP con compatibilidad para IPv6 e IPv4 para simplificar la programación de Windows Sockets. Entre estas nuevas funciones auxiliares de IP se incluyen las siguientes:

-   [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

Al agregar compatibilidad con IPv6 a una aplicación, deben usarse las siguientes directrices:

-   Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) para establecer una conexión a un punto de conexión a partir de un nombre de host y un puerto. La función **WSAConnectByName** está disponible en Windows Vista y versiones posteriores.
-   Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) para establecer una conexión a una de una colección de extremos posibles representados por un conjunto de direcciones de destino (nombres de host y puertos). La función **WSAConnectByList** está disponible en Windows Vista y versiones posteriores.
-   Reemplace las llamadas de función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) por llamadas a una de las nuevas funciones de Windows Sockets de [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . La función **función getaddrinfo** compatible con el protocolo IPv6 está disponible en Windows XP y versiones posteriores. El protocolo IPv6 también se admite en Windows 2000 cuando está instalado IPv6 Technology Preview para Windows 2000.
-   Reemplace las llamadas a la función [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) con llamadas a una de las nuevas funciones de Windows Sockets de [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) . La función **getnameinfo** compatible con el protocolo IPv6 está disponible en Windows XP y versiones posteriores. El protocolo IPv6 también se admite en Windows 2000 cuando está instalado IPv6 Technology Preview para Windows 2000.

## <a name="wsaconnectbyname"></a>WSAConnectByName

La función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) simplifica la conexión a un punto de conexión mediante un socket basado en transmisión dado el nombre de host o la dirección IP del destino (IPv4 o IPv6). Esta función reduce el código fuente necesario para crear una aplicación IP que es independiente de la versión del protocolo IP que se usa. **WSAConnectByName** reemplaza los siguientes pasos en una aplicación TCP típica a una llamada de función única:

-   Resuelva un nombre de host en un conjunto de direcciones IP.
-   Para cada dirección IP:
    -   Cree un socket de la familia de direcciones adecuada.
    -   Intenta conectarse a la dirección IP remota. Si la conexión se realizó correctamente, devuelve; de lo contrario, se intenta la siguiente dirección IP remota para el host.

La función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) va más allá de resolver el nombre y, a continuación, intentar conectarse. La función usa todas las direcciones remotas devueltas por la resolución de nombres y todas las direcciones IP de origen de la máquina local. Primero intenta conectarse usando pares de direcciones con la mayor probabilidad de éxito. Por lo tanto, **WSAConnectByName** no solo garantiza que se establecerá una conexión si es posible, sino que también minimiza el tiempo necesario para establecer la conexión.

Para habilitar las comunicaciones IPv6 e IPv4, use el método siguiente:

-   Se debe llamar a [**la función V6ONLY**](/windows/desktop/api/winsock/nf-winsock-setsockopt) en un socket creado para la \_ familia de direcciones AF inet6 para deshabilitar la opción de socket **\_ de IPv6** antes de llamar a [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea). Esto se logra mediante una llamada a la **función de la función de** llamada en el socket con el parámetro *Level* establecido en **IPPROTO \_ IPv6** (consulte [ \_ las opciones de socket IPv6 de IPPROTO](ipproto-ipv6-socket-options.md)), el parámetro *optname* establecido en **IPv6 \_ V6ONLY** y el valor del parámetro *optvalue* establecido en cero.

Si una aplicación necesita enlazarse a un puerto o una dirección local específicos, no se puede usar [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) , ya que el parámetro de socket para **WSAConnectByName** debe ser un socket sin enlazar.

En el ejemplo de código siguiente se muestran solo algunas líneas de código que se necesitan para usar esta función con el fin de implementar una aplicación que es independiente de la versión de IP.

Establecer una conexión mediante [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


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



## <a name="wsaconnectbylist"></a>WSAConnectByList

La función [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) establece una conexión a un host dado un conjunto de hosts posibles (representado por un conjunto de puertos y direcciones IP de destino). La función toma todas las direcciones IP y los puertos para el extremo y todas las direcciones IP de la máquina local, e intenta una conexión mediante todas las combinaciones de direcciones posibles.

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) está relacionado con la función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) . En lugar de tomar un nombre de host único, **WSAConnectByList** acepta una lista de hosts (direcciones de destino y pares de puertos) y se conecta a una de las direcciones y puertos de la lista proporcionada. Esta función está diseñada para admitir escenarios en los que una aplicación necesita conectarse a cualquier host disponible a partir de una lista de posibles hosts.

De forma similar a [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), la función [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) reduce significativamente el código fuente necesario para crear, enlazar y conectar un socket. Esta función facilita la implementación de una aplicación que es independiente de la versión de IP. La lista de direcciones de un host aceptado por esta función puede ser direcciones IPv6 o IPv4.

Para habilitar las direcciones IPv6 e IPv4 que se van a pasar en la lista de direcciones únicas que acepta la función, se deben realizar los siguientes pasos antes de llamar a la función:

-   Se debe llamar a [**la función V6ONLY**](/windows/desktop/api/winsock/nf-winsock-setsockopt) en un socket creado para la \_ familia de direcciones AF inet6 para deshabilitar la opción de socket **\_ de IPv6** antes de llamar a [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist). Esto se logra mediante una llamada a la **función de la función de** llamada en el socket con el parámetro *Level* establecido en **IPPROTO \_ IPv6** (consulte [ \_ las opciones de socket IPv6 de IPPROTO](ipproto-ipv6-socket-options.md)), el parámetro *optname* establecido en **IPv6 \_ V6ONLY** y el valor del parámetro *optvalue* establecido en cero.
-   Todas las direcciones IPv4 deben representarse en el formato de dirección IPv6 asignado a IPv4, lo que permite que una aplicación solo IPv6 se comunique con un nodo IPv4. El formato de dirección IPv6 asignado a IPv4 permite representar la dirección IPv4 de un nodo IPv4 como una dirección IPv6. La dirección IPv4 se codifica en los bits 32 de orden inferior de la dirección IPv6 y los bits 96 de orden superior tienen el prefijo fijo 0:0: 0:0: FFFF. El formato de dirección IPv6 asignado a IPv4 se especifica en RFC 4291. Para obtener más información, consulte [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La \_ macro IN6ADDR SETV4MAPPED de *Mstcpip. h* se puede usar para convertir una dirección IPv4 en el formato de dirección IPv6 asignado a IPv4 requerido.

Establecer una conexión mediante [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


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



## <a name="getaddrinfo"></a>getaddrinfo

La función **función getaddrinfo** también realiza el trabajo de procesamiento de muchas funciones. Anteriormente, las llamadas a un número de funciones de Windows Sockets eran necesarias para crear, abrir y enlazar una dirección a un socket. Con la función **función getaddrinfo** , las líneas de código fuente necesarias para realizar este trabajo se pueden reducir considerablemente. En los dos ejemplos siguientes se muestra el código fuente necesario para realizar estas tareas con y sin la función **función getaddrinfo** .

Realización de una apertura, conexión y enlace mediante **función getaddrinfo**


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



Realización de una apertura, conexión y enlace sin usar **función getaddrinfo**


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



Observe que los dos ejemplos de código fuente realizan las mismas tareas, pero el primer ejemplo, con la función **función getaddrinfo** , requiere menos líneas de código fuente y puede controlar direcciones IPv6 o IPv4. El número de líneas de código fuente que se eliminan mediante la función **función getaddrinfo** varía.

> [!Note]  
> En el código fuente de producción, la aplicación recorrer en iteración el conjunto de direcciones devueltas por la función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) o [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . En estos ejemplos se omite ese paso en favor de simplicidad.

 

Otro problema que debe abordar al modificar una aplicación IPv4 existente para admitir IPv6 está asociado con el orden en el que se llama a las funciones. Tanto [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) como [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) requieren que se realice una secuencia de llamadas de función en un orden específico.

En las plataformas en las que se usan IPv4 e IPv6, la familia de direcciones del nombre de host remoto no se conoce de antemano. Por lo tanto, la resolución de direcciones con la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) debe ejecutarse primero para determinar la dirección IP y la familia de direcciones del host remoto. A continuación, se puede llamar a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) para abrir un socket de la familia de direcciones devuelta por [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo). Se trata de un cambio importante en la forma en que se escriben las aplicaciones de Windows Sockets, ya que muchas aplicaciones de IPv4 suelen usar un orden diferente de llamadas a funciones.

La mayoría de las aplicaciones IPv4 crean primero un socket para la familia de direcciones de AF \_ inet, después realizan la resolución de nombres y, a continuación, usan el socket para conectarse a la dirección IP resuelta. Al hacer que estas aplicaciones sean compatibles con IPv6, la llamada a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) se debe retrasar hasta después de la resolución de nombres cuando se deteremined la familia de direcciones. Tenga en cuenta que si la resolución de nombres devuelve direcciones IPv4 e IPv6, se deben usar sockets independientes de IPv4 e IPv6 para conectarse a estas direcciones de destino. Todas estas complejidades se pueden evitar mediante el uso de la función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) en Windows Vista y versiones posteriores, por lo que se recomienda a los desarrolladores de aplicaciones que usen esta nueva función.

En el ejemplo de código siguiente se muestra la secuencia correcta para realizar la resolución de nombres primero (realizada en la cuarta línea del siguiente ejemplo de código fuente) y, a continuación, abrir un socket (realizado en la<sup>línea 19 del</sup> ejemplo de código siguiente). Este ejemplo es un extracto del archivo Client. c que se encuentra en el [código de cliente habilitado para IPv6](ipv6-enabled-client-code-2.md) en el Apéndice B. La función PrintError llamada en el ejemplo de código siguiente se muestra en el ejemplo de Client. c.


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



## <a name="ip-helper-functions"></a>Funciones de aplicación auxiliar IP

Por último, las aplicaciones que usan la función auxiliar de IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)y su información de [**\_ adaptador de \_ IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)de estructura asociada deben reconocer que esta función y estructura están limitadas a las direcciones IPv4. Los reemplazos habilitados para IPv6 para esta función y estructura son la función [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) y la estructura de [**direcciones del \_ adaptador \_ de IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) . Las aplicaciones habilitadas para IPv6 que usan la API auxiliar de IP deben usar la función **GetAdaptersAddresses** y la estructura de **direcciones de \_ adaptador \_ IP** habilitada para IPv6 correspondiente, ambas definidas en el kit de desarrollo de software (SDK) de Microsoft Windows.

## <a name="recommendations"></a>Recomendaciones

El mejor enfoque para asegurarse de que la aplicación usa llamadas a funciones compatibles con IPv6 es usar la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para obtener la traducción de host a dirección. A partir de Windows XP, la función **función getaddrinfo** hace que la función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) sea innecesaria y, por tanto, la aplicación debe usar la función **función getaddrinfo** en su lugar para futuros proyectos de programación. Aunque Microsoft seguirá admitiendo **gethostbyname**, esta función no se extenderá para admitir IPv6. Para obtener compatibilidad transparente para obtener información de host IPv6 e IPv4, debe usar **función getaddrinfo**.

En el ejemplo siguiente se muestra cómo usar mejor la función **función getaddrinfo** . Observe que la función, cuando se usa correctamente como muestra este ejemplo, controla correctamente la traducción de host a dirección de IPv6 e IPv4, pero también obtiene otra información útil sobre el host, como el tipo de sockets admitido. Este ejemplo es un extracto del ejemplo de Client. c que se encuentra en el Apéndice B.


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
> La versión de la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que admite IPv6 es nueva en la versión de Windows XP de Windows.

 

Código que se debe evitar

La traducción de direcciones de host se ha logrado tradicionalmente mediante la función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) . A partir de Windows XP:

-   La función **función getaddrinfo** hace que la función **gethostbyname** esté obsoleta.
-   Las aplicaciones deben usar la función **función getaddrinfo** en lugar de la función **gethostbyname** .

Tareas de codificación

**Para modificar una aplicación IPv4 existente para agregar compatibilidad con IPv6**

1.  Adquiera la utilidad Checkv4.exe. Esta utilidad se instala como parte de la Windows SDK. El Windows SDK está disponible a través de una suscripción a MSDN y también se puede descargar desde el sitio web de Microsoft ( https://msdn.microsoft.com) . También se incluyó una versión anterior de la herramienta *Checkv4.exe* como parte de Microsoft IPv6 Technology Preview para Windows 2000.
2.  Ejecute la utilidad *Checkv4.exe* en el código. Vea [usar la utilidad de Checkv4.exe](using-the-checkv4-exe-utility-2.md) para obtener información sobre cómo ejecutar la utilidad de versión en los archivos.
3.  La utilidad le alerta sobre el uso de [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)y otras funciones solo de IPv4 y proporciona recomendaciones sobre cómo reemplazarlos con la función compatible con IPv6 como [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).
4.  Reemplace todas las instancias de la función **gethostbyname** y el código asociado según corresponda, con la función **función getaddrinfo** . En Windows Vista, use la función [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) o [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) cuando corresponda.
5.  Reemplace todas las instancias de la función [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) y el código asociado, según corresponda, por la función [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Como alternativa, puede buscar en el código base las instancias de las funciones **gethostbyname** y [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) y cambiar todo el uso (y otros códigos asociados, según corresponda) a las funciones **función getaddrinfo** y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para aplicaciones de Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Cambiar las estructuras de datos para IPv6 Winsock Appications](changing-data-structures-2.md)
</dt> <dt>

[Sockets de doble pila para aplicaciones Winsock de IPv6](dual-stack-sockets.md)
</dt> <dt>

[Uso de direcciones IPv4 codificadas](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones Winsock de IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
