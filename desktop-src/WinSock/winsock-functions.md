---
description: En la lista siguiente se proporcionan descripciones concisas de cada función de Winsock. Para obtener información adicional sobre cualquier función, haga clic en el nombre de la función.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Funciones Winsock
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 9bf2205c970eeaaf4e64867565d58680b28298c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716434"
---
# <a name="winsock-functions"></a>Funciones Winsock

En la lista siguiente se proporcionan descripciones concisas de cada función de Winsock. Para obtener información adicional sobre cualquier función, haga clic en el nombre de la función.

| Función | Descripción |
|-|-|
| [**acept**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Permite un intento de conexión entrante en un socket. |
| [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Acepta una nueva conexión, devuelve la dirección local y remota, y recibe el primer bloque de datos enviado por la aplicación cliente. |
| [**volver**](/windows/win32/api/winsock/nf-winsock-bind) | Asocia una dirección local a un socket. |
| [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | Cierra un socket existente. |
| [**conéctelo**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Establece una conexión con un socket especificado. |
| [**ConnectEx**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Establece una conexión con un socket especificado y, opcionalmente, envía datos una vez establecida la conexión. Solo se admite en sockets orientados a conexiones. |
| [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Cierra una conexión en un socket y permite reutilizar el identificador de socket. |
| [**EnumProtocols**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Recupera información sobre un conjunto especificado de protocolos de red que están activos en un host local. |
| [**freeaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Libera información de dirección que la función [**función getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) asigna dinámicamente en estructuras [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) . |
| [**FreeAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Libera información de dirección que la función [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) asigna dinámicamente en estructuras [**addrinfoex**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) . |
| [**FreeAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Libera información de dirección que la función [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) asigna dinámicamente en estructuras [**addrinfoW**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) . |
| [**Gai \_ strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Ayuda en la impresión de mensajes de error en función de los \_ \* errores EAI devueltos por la función [**función getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Analiza los datos obtenidos de una llamada a la función [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) . |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Consulta un espacio de nombres, o un conjunto de espacios de nombres predeterminados, para recuperar la información de dirección de red de un servicio de red especificado. Este proceso se conoce como resolución de nombres de servicio. Un servicio de red también puede utilizar la función para obtener información de la dirección local que se puede usar con la función de [**enlace**](/windows/win32/api/winsock/nf-winsock-bind) . |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Proporciona una traducción independiente del protocolo desde un nombre de host ANSI a una dirección. |
| [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Proporciona la resolución de nombres independiente del Protocolo con parámetros adicionales para calificar qué proveedores de espacio de nombres deben controlar la solicitud. |
| [**GetAddrInfoExCancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Cancela una operación asincrónica mediante la función [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**GetAddrInfoExOverlappedResult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Obtiene el código de retorno para una estructura **superpuesta** utilizada por una operación asincrónica para la función [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Proporciona una traducción independiente del protocolo desde un nombre de host Unicode a una dirección. |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Recupera la información de host correspondiente a una dirección de red. |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Recupera información de host correspondiente a un nombre de host de una base de datos host. En desuso: use [**función getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) en su lugar. |
| [**GetHostName (**](/windows/win32/api/winsock/nf-winsock-gethostname) | Recupera el nombre de host estándar para el equipo local. |
| [**GetHostNameW**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Recupera el nombre de host estándar para el equipo local como una cadena Unicode. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Recupera el estado de filtro de multidifusión para un socket IPv4. |
| [**GetNameByType**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Recupera el nombre de un servicio de red para el tipo de servicio especificado. |
| [**getnameinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Proporciona la resolución de nombres de una dirección IPv4 o IPv6 a un nombre de host ANSI y de un número de puerto al nombre del servicio ANSI. |
| [**GetNameInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Proporciona la resolución de nombres de una dirección IPv4 o IPv6 a un nombre de host Unicode y de un número de puerto al nombre del servicio Unicode. |
| [**getpeername**](/windows/win32/api/winsock/nf-winsock-getpeername) | Recupera la dirección del elemento del mismo nivel al que está conectado un socket. |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Recupera la información de protocolo correspondiente a un nombre de protocolo. |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Recupera la información de protocolo correspondiente a un número de protocolo. |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Recupera la información de servicio correspondiente a un nombre de servicio y protocolo. |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Recupera la información de servicio correspondiente a un puerto y un protocolo. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Recupera información sobre un servicio de red en el contexto de un conjunto de espacios de nombres predeterminados o un espacio de nombres especificado. |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | Recupera el nombre local de un socket. |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Recupera una opción de socket. |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Recupera el estado de filtro de multidifusión para un socket IPv4 o IPv6. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Recupera un GUID de tipo de servicio para un servicio de red especificado por el nombre. |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Convierte un **valor Double** de host en el orden de bytes de la red TCP/IP (que es Big-endian). |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Convierte un valor **float** del host al orden de bytes de la red TCP/IP (que es Big-endian). |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | Convierte un objeto **u \_ Long** del host al orden de bytes de la red TCP/IP (que es Big-endian). |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Convierte un **\_ \_ Int64 sin signo** del host al orden de bytes de la red TCP/IP (que es Big-endian). |
| [**htons**](/windows/win32/api/winsock/nf-winsock-htons) | Convierte un objeto **u \_ Short** del host al orden de bytes de la red TCP/IP (que es Big-endian). |
| [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Convierte una cadena que contiene una dirección de puntos de protocolo de Internet (IPv4) en una dirección adecuada para la estructura [**in \_ addr**](/windows/win32/api/winsock2/ns-winsock2-in_addr) . |
| [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Convierte una dirección de red de Internet (IPv4) en una cadena en formato de puntos estándar de Internet. |
| [**InetNtop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | convierte una dirección de red de Internet IPv4 o IPv6 en una cadena en formato estándar de Internet. La versión ANSI de esta función es [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw). |
| [**InetPton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Convierte una dirección de red de Internet IPv4 o IPv6 en su formato de presentación de texto estándar en su forma binaria numérica. La versión ANSI de esta función es [**inet \_ PTON**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Controla el modo de e/s de un socket. |
| [**escuchar**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Coloca un socket en un estado en el que está escuchando una conexión entrante. |
| [**ntohd**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Convierte un **\_ \_ Int64 sin signo** del orden de la red TCP/IP al orden de bytes del host (que es Little-endian en procesadores Intel) y devuelve un **valor Double**. |
| [**ntohf**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Convierte un **\_ \_ Int32 sin signo** del orden de la red TCP/IP al orden de bytes del host (que es Little-endian en procesadores Intel) y devuelve un valor **float**. |
| [**ntohl**](/windows/win32/api/winsock/nf-winsock-ntohl) | Convierte un objeto u \_ Long del orden de la red TCP/IP al orden de bytes del host (que es Little-endian en procesadores Intel). |
| [**ntohll**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Convierte un **\_ \_ Int64 sin signo** del orden de la red TCP/IP al orden de bytes del host (que es Little-endian en procesadores Intel). |
| [**ntohs**](/windows/win32/api/winsock/nf-winsock-ntohs) | Convierte un objeto u \_ Short del orden de bytes de la red TCP/IP en el orden de bytes del host (que es Little-endian en procesadores Intel). |
| [**recv**](/windows/win32/api/winsock/nf-winsock-recv) | Recibe datos de un socket conectado o enlazado. |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Recibe un datagrama y almacena la dirección de origen. |
| [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Cierra una cola de finalización existente utilizada para la notificación de finalización de e/s mediante el envío y la recepción de solicitudes con las extensiones de e/s registradas de Winsock. |
| [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Crea una cola de finalización de e/s de un tamaño específico para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Crea un descriptor de sockets de e/s registrado mediante el socket especificado y las colas de finalización de e/s para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Quita las entradas de una cola de finalización de e/s para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Anula el registro de un búfer registrado utilizado con las extensiones de e/s registradas de Winsock. |
| [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Registra el método que se va a usar para el comportamiento de notificación con una cola de finalización de e/s para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Recibe datos de red en un socket TCP de e/s registrado conectado o un socket UDP de e/s registrado enlazado para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Recibe datos de red en un socket TCP de e/s registrado conectado o un socket UDP de e/s registrado enlazado con opciones adicionales para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Registra un [**río \_ BUFFERID**](rio-bufferid.md), un descriptor de búfer registrado, con un búfer especificado para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIOResizeCompletionQueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Cambia el tamaño de una cola de finalización de e/s para que sea mayor o menor para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Cambia el tamaño de una cola de solicitudes para que sea mayor o menor para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Envía datos de red en un socket TCP de e/s registrado conectado o un socket UDP de e/s registrado enlazado para su uso con las extensiones de e/s registradas de Winsock. |
| [**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Envía datos de red en un socket TCP de e/s registrado conectado o un socket UDP de e/s registrado enlazado con opciones adicionales para su uso con las extensiones de e/s registradas de Winsock. |
| [**no**](/windows/win32/api/Winsock2/nf-winsock2-select) | Determina el estado de uno o varios sockets, esperando si es necesario, para realizar la e/s sincrónica. |
| [**Enviar**](/windows/win32/api/Winsock2/nf-winsock2-send) | Envía datos a un socket conectado. |
| [**sendto**](/windows/win32/api/winsock/nf-winsock-sendto) | Envía datos a un destino específico. |
| [**SetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Registra un host y un nombre de servicio junto con las direcciones asociadas con un proveedor de espacios de nombres específico. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Establece el estado de filtro de multidifusión para un socket IPv4. |
| [**SetService**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Registra o quita del registro un servicio de red dentro de uno o varios espacios de nombres. También puede Agregar o quitar un tipo de servicio de red en uno o varios espacios de nombres. |
| [**SetSocketMediaStreamingMode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Indica si la red se va a usar para transferir el contenido multimedia de streaming que requiere calidad de servicio. |
| [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Establece una opción de socket. |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Establece el estado de filtro de multidifusión para un socket IPv4 o IPv6. |
| [**apagado**](/windows/win32/api/winsock/nf-winsock-shutdown) | Deshabilita los envíos o recepciones en un socket. |
| [**tomacorriente**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Crea un socket que está enlazado a un proveedor de servicios específico. |
| [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Transmite datos de archivo a través de un identificador de socket conectado. |
| [**TransmitPackets**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Transmite datos en memoria o datos de archivo a través de un socket conectado. |
| [**WSAAccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Acepta condicionalmente una conexión basada en el valor devuelto de una función de condición, proporciona especificaciones de flujo de calidad de servicio y permite la transferencia de datos de conexión. |
| [**WSAAddressToString**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Convierte todos los componentes de una estructura [**sockaddr**](sockaddr-2.md) en una representación de cadena legible para el usuario de la dirección. |
| [**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Recupera asincrónicamente la información del host que corresponde a una dirección. |
| [**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Recupera asincrónicamente la información del host que corresponde a un nombre de host. |
| [**WSAAsyncGetProtoByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Recupera asincrónicamente la información del protocolo que corresponde a un nombre de protocolo. |
| [**WSAAsyncGetProtoByNumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Recupera asincrónicamente la información del protocolo que corresponde a un número de protocolo. |
| [**WSAAsyncGetServByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Recupera de forma asincrónica la información del servicio que corresponde a un nombre de servicio y a un puerto. |
| [**WSAAsyncGetServByPort**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Recupera de forma asincrónica la información del servicio que corresponde a un puerto y un protocolo. |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | Solicita la notificación basada en mensajes de Windows de eventos de red para un socket. |
| [**WSACancelAsyncRequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Cancela una operación asincrónica incompleta. |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Termina el uso de la \_32.DLL Ws2. |
| [**WSACloseEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Cierra un identificador de objeto de evento abierto. |
| [**WSAConnect**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Establece una conexión a otra aplicación de socket, intercambia datos de conexión y especifica la calidad de servicio necesaria basada en la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) especificada. |
| [**WSAConnectByList**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Establece una conexión a una de una colección de extremos posibles representados por un conjunto de direcciones de destino (nombres de host y puertos). |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Establece una conexión a otra aplicación de socket en un host y puerto especificados. |
| [**WSACreateEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Crea un nuevo objeto de evento. |
| [**WSADeleteSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Quita la asociación entre un nombre de destino del mismo nivel y una dirección IP de un socket. |
| [**WSADuplicateSocket**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Devuelve una estructura que se puede usar para crear un nuevo descriptor de socket para un socket compartido. |
| [**WSAEnumNameSpaceProviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Recupera información sobre los espacios de nombres disponibles. |
| [**WSAEnumNameSpaceProvidersEx**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Recupera información sobre los espacios de nombres disponibles. |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Detecta los repeticiones de eventos de red para el socket indicado, borrar los registros de eventos de red interna y restablecer los objetos de evento (opcional). |
| [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Recupera información acerca de los protocolos de transporte disponibles. |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Especifica un objeto de evento que se va a asociar al conjunto especificado de \_ eventos de red FD xxx. |
| [**\_\_WSAFDIsSet**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Especifica si un socket está incluido en un conjunto de descriptores de socket. |
| [**WSAGetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Consulta el estado de la opción de socket [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) . |
| [**WSAGetIcmpErrorInfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Consulta la dirección de origen de un error ICMP recibido en un socket TCP durante la configuración de la conexión. |
| [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Recupera la MTU del nivel de IP definido por el usuario para un socket. |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Devuelve el estado de error de la última operación en la que se produjo un error. |
| [**WSAGetOverlappedResult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Recupera los resultados de una operación superpuesta en el socket especificado. |
| [**WSAGetQOSByName**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Inicializa una estructura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) basada en una plantilla con nombre o proporciona un búfer para recuperar una enumeración de los nombres de plantilla disponibles. |
| [**WSAGetServiceClassInfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Recupera la información de clase (esquema) que pertenece a una clase de servicio especificada de un proveedor de espacio de nombres especificado. |
| [**WSAGetServiceClassNameByClassId**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Recupera el nombre del servicio asociado al tipo especificado. |
| [**WSAGetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Recupera el tamaño máximo de un mensaje recibido y fusionado para un socket UDP. |
| [**WSAGetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Recupera el tamaño del mensaje de segmentación para un socket UDP. |
| [**WSAHtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Convierte un objeto u \_ Long del orden de bytes del host al orden de bytes de la red. |
| [**WSAHtons**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Convierte un objeto u \_ Short del orden de bytes del host al orden de bytes de la red. |
| [**WSAImpersonateSocketPeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Se utiliza para suplantar la entidad de seguridad correspondiente a un socket del mismo nivel para realizar la autorización en el nivel de la aplicación. |
| [**WSAInstallServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Registra un esquema de clase de servicio dentro de un espacio de nombres. |
| [**WSAIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Controla el modo de un socket. |
| [**WSAJoinLeaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Une un nodo hoja en una sesión Multipoint, intercambia los datos y especifica la calidad de servicio necesaria en función de las estructuras especificadas. |
| [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Inicia una consulta de cliente restringida por la información contenida en una estructura [**WSAQUERYSET**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) . |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Libera el identificador usado por las llamadas anteriores a [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta). |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Recuperar la información de servicio solicitada. |
| [**WSANSPIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Desarrolladores para realizar llamadas de control de e/s a un espacio de nombres registrado. |
| [**WSANtohl**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Convierte un objeto u \_ Long del orden de bytes de la red al orden de bytes del host. |
| [**WSANtohs**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Convierte un objeto u \_ Short del orden de bytes de la red al orden de bytes del host. |
| [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Determina el estado de uno o varios Sockets. |
| [**WSAProviderConfigChange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Notifica a la aplicación cuando se cambia la configuración del proveedor. |
| [**WSAQuerySocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Consulta información acerca de la seguridad que se aplica a una conexión en un socket. |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Recibe datos de un socket conectado. |
| [**WSARecvDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Finaliza la recepción en un socket y recupera los datos de desconexión si el socket está orientado a la conexión. |
| [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Recibe datos de un socket conectado. |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Recibe un datagrama y almacena la dirección de origen. |
| [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Recibe datos e información de control opcional de sockets conectados y no conectados. |
| [**WSARemoveServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Quita de forma permanente el esquema de clase de servicio del registro. |
| [**WSAResetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Restablece el estado del objeto de evento especificado en no señalado. |
| [**WSARevertImpersonation**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Finaliza la suplantación de un socket del mismo nivel. |
| [**WSASend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Envía datos a un socket conectado. |
| [**WSASendDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Inicia la terminación de la conexión para el socket y envía los datos de desconexión. |
| [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Envía datos e información de control opcional de sockets conectados y no conectados. |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Envía datos a un destino específico, utilizando e/s superpuestas cuando proceda. |
| [**WSASetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Establece el estado del objeto de evento especificado en señalado. |
| [**WSASetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Establece el estado de la opción de socket de [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) . |
| [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Establece la MTU del nivel de IP definido por el usuario en un socket. |
| [**WSASetLastError**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Establece el código de error. |
| [**WSASetService**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Registra o quita del registro una instancia de servicio en uno o varios espacios de nombres. |
| [**WSASetSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Se usa para especificar el nombre de destino del mismo nivel (SPN) que corresponde a una dirección IP del mismo nivel. Este nombre de destino está pensado para que lo especifiquen las aplicaciones cliente para identificar de forma segura el elemento del mismo nivel que se debe autenticar. |
| [**WSASetSocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Habilita y aplica la seguridad de un socket. |
| [**WSASetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Establece el tamaño máximo de un conjunto de mensajes fusionado en un socket UDP. |
| [**WSASetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Establece el tamaño del mensaje de segmentación en un socket UDP. |
| [**WSASocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Crea un socket que está enlazado a un proveedor de servicios de transporte específico. |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Inicia el uso de32.DLL de WS2 \_ por parte de un proceso. |
| [**WSAStringToAddress**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Convierte una cadena numérica en una estructura [**sockaddr**](sockaddr-2.md) . |
| [**WSAWaitForMultipleEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Devuelve cuando uno o todos los objetos de evento especificados están en el estado señalado o cuando expira el intervalo de tiempo de espera. |
