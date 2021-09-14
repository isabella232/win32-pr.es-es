---
description: En la lista siguiente se proporcionan descripciones concisas de cada función Winsock. Para obtener información adicional sobre cualquier función, haga clic en el nombre de la función.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Funciones Winsock
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 9bf2205c970eeaaf4e64867565d58680b28298c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967260"
---
# <a name="winsock-functions"></a>Funciones Winsock

En la lista siguiente se proporcionan descripciones concisas de cada función Winsock. Para obtener información adicional sobre cualquier función, haga clic en el nombre de la función.

| Función | Descripción |
|-|-|
| [**Aceptar**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Permite un intento de conexión entrante en un socket. |
| [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Acepta una nueva conexión, devuelve la dirección local y remota y recibe el primer bloque de datos enviado por la aplicación cliente. |
| [**Atar**](/windows/win32/api/winsock/nf-winsock-bind) | Asocia una dirección local a un socket. |
| [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | Cierra un socket existente. |
| [**Conectar**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Establece una conexión a un socket especificado. |
| [**ConnectEx**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Establece una conexión a un socket especificado y, opcionalmente, envía datos una vez establecida la conexión. Solo se admite en sockets orientados a conexiones. |
| [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Cierra una conexión en un socket y permite reutilizar el identificador de socket. |
| [**EnumProtocols**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Recupera información sobre un conjunto especificado de protocolos de red que están activos en un host local. |
| [**freeaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Libera la información de dirección que la [**función getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) asigna dinámicamente en [**estructuras addrinfo.**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) |
| [**FreeAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Libera información de dirección que la [**función GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) asigna dinámicamente en [**estructuras addrinfoex.**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) |
| [**FreeAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Libera información de dirección que la [**función GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) asigna dinámicamente en [**estructuras addrinfoW.**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) |
| [**y \_ strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Ayuda a imprimir mensajes de error en función de los errores de EAI \_ \* devueltos por la [**función getaddrinfo.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) |
| [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Analiza los datos obtenidos de una llamada a la [**función AcceptEx.**](/windows/win32/api/mswsock/nf-mswsock-acceptex) |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Consulta un espacio de nombres o un conjunto de espacios de nombres predeterminados para recuperar información de dirección de red para un servicio de red especificado. Este proceso se conoce como resolución de nombres de servicio. Un servicio de red también puede usar la función para obtener información de dirección local que puede usar con la [**función de**](/windows/win32/api/winsock/nf-winsock-bind) enlace. |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Proporciona una traducción independiente del protocolo de un nombre de host ANSI a una dirección. |
| [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Proporciona resolución de nombres independiente del protocolo con parámetros adicionales para calificar qué proveedores de espacio de nombres deben controlar la solicitud. |
| [**GetAddrInfoExCancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Cancela una operación asincrónica mediante la [**función GetAddrInfoEx.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) |
| [**GetAddrInfoExOverlappedResult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Obtiene el código de retorno de una **estructura OVERLAPPED** utilizada por una operación asincrónica para [**la función GetAddrInfoEx.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) |
| [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Proporciona una traducción independiente del protocolo de un nombre de host Unicode a una dirección. |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Recupera la información del host correspondiente a una dirección de red. |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Recupera la información de host correspondiente a un nombre de host de una base de datos host. En desuso: use [**getaddrinfo en**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) su lugar. |
| [**gethostname**](/windows/win32/api/winsock/nf-winsock-gethostname) | Recupera el nombre de host estándar del equipo local. |
| [**GetHostNameW**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Recupera el nombre de host estándar del equipo local como una cadena Unicode. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Recupera el estado del filtro de multidifusión para un socket IPv4. |
| [**GetNameByType**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Recupera el nombre de un servicio de red para el tipo de servicio especificado. |
| [**getnameinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Proporciona resolución de nombres de una dirección IPv4 o IPv6 a un nombre de host ANSI y de un número de puerto al nombre del servicio ANSI. |
| [**GetNameInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Proporciona resolución de nombres de una dirección IPv4 o IPv6 a un nombre de host Unicode y de un número de puerto al nombre del servicio Unicode. |
| [**getpeername**](/windows/win32/api/winsock/nf-winsock-getpeername) | Recupera la dirección del mismo nivel a la que está conectado un socket. |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Recupera la información de protocolo correspondiente a un nombre de protocolo. |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Recupera la información de protocolo correspondiente a un número de protocolo. |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Recupera la información del servicio correspondiente a un nombre de servicio y un protocolo. |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Recupera la información del servicio correspondiente a un puerto y un protocolo. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Recupera información sobre un servicio de red en el contexto de un conjunto de espacios de nombres predeterminados o un espacio de nombres especificado. |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | Recupera el nombre local de un socket. |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Recupera una opción de socket. |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Recupera el estado del filtro de multidifusión para un socket IPv4 o IPv6. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Recupera un GUID de tipo de servicio para un servicio de red especificado por nombre. |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Convierte un valor **double del** host al orden de bytes de la red TCP/IP (que es big-endian). |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Convierte un valor **float del** host al orden de bytes de la red TCP/IP (que es big-endian). |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | Convierte un **valor u long \_ del** host al orden de bytes de la red TCP/IP (que es big-endian). |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Convierte un **\_ \_ int64** sin signo del host al orden de bytes de red TCP/IP (que es big-endian). |
| [**htons**](/windows/win32/api/winsock/nf-winsock-htons) | Convierte un **valor u short \_ del** host al orden de bytes de la red TCP/IP (que es big-endian). |
| [**complemento de \_ conjunto de inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Convierte una cadena que contiene una dirección de puntos de Protocolo de Internet (Ipv4) en una dirección adecuada para [**la estructura \_ del complemento**](/windows/win32/api/winsock2/ns-winsock2-in_addr) de entrada. |
| [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Convierte una dirección de red de Internet (IPv4) en una cadena en formato de puntos estándar de Internet. |
| [**InetNtop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | convierte una dirección de red de Internet IPv4 o IPv6 en una cadena en formato estándar de Internet. La versión ANSI de esta función es [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw). |
| [**InetPton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Convierte una dirección de red de Internet IPv4 o IPv6 en su formulario de presentación de texto estándar en su formato binario numérico. La versión ANSI de esta función es [**inet \_ pton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Controla el modo de E/S de un socket. |
| [**listen**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Coloca un socket en un estado en el que escucha una conexión entrante. |
| [**ntohd**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Convierte un **\_ \_ int64** sin signo del orden de red TCP/IP en el orden de bytes del host (que es little-endian en procesadores Intel) y devuelve un **valor double**. |
| [**nthhf**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Convierte un **\_ \_ int32** sin signo del orden de red TCP/IP en el orden de bytes del host (que es little-endian en procesadores Intel) y devuelve **un valor float**. |
| [**ntohl**](/windows/win32/api/winsock/nf-winsock-ntohl) | Convierte un valor u long del orden de red TCP/IP al orden de bytes del host (que es \_ little-endian en procesadores Intel). |
| [**nthhll**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Convierte un **\_ \_ int64** sin signo del orden de red TCP/IP en el orden de bytes del host (que es little-endian en procesadores Intel). |
| [**ntohs**](/windows/win32/api/winsock/nf-winsock-ntohs) | Convierte un valor u short del orden de bytes de la red TCP/IP al orden de bytes del host (que es \_ little-endian en procesadores Intel). |
| [**recv**](/windows/win32/api/winsock/nf-winsock-recv) | Recibe datos de un socket conectado o enlazado. |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Recibe un datagrama y almacena la dirección de origen. |
| [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Cierra una cola de finalización existente que se usa para la notificación de finalización de E/S mediante el envío y recepción de solicitudes con las extensiones de E/S registradas en Winsock. |
| [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Crea una cola de finalización de E/S de un tamaño específico para su uso con las extensiones de E/S registradas de Winsock. |
| [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Crea un descriptor de socket de E/S registrado mediante un socket especificado y colas de finalización de E/S para su uso con las extensiones de E/S registradas en Winsock. |
| [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Quita las entradas de una cola de finalización de E/S para usarlas con las extensiones de E/S registradas de Winsock. |
| [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Anula el registro de un búfer registrado que se usa con las extensiones de E/S registradas de Winsock. |
| [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Registra el método que se usará para el comportamiento de notificación con una cola de finalización de E/S para su uso con las extensiones de E/S registradas de Winsock. |
| [**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Recibe datos de red en un socket TCP de E/S registrado conectado o un socket UDP de E/S registrado enlazado para su uso con las extensiones de E/S registradas en Winsock. |
| [**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Recibe datos de red en un socket TCP de E/S registrado conectado o un socket UDP de E/S registrado enlazado con opciones adicionales para su uso con las extensiones de E/S registradas de Winsock. |
| [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Registra un [**\_ BUFFERID de RIO**](rio-bufferid.md), un descriptor de búfer registrado, con un búfer especificado para su uso con las extensiones de E/S registradas de Winsock. |
| [**RIOResizeCompletionQueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Cambia el tamaño de una cola de finalización de E/S para que sea mayor o menor para su uso con las extensiones de E/S registradas de Winsock. |
| [**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Cambia el tamaño de una cola de solicitudes para que sea mayor o menor para su uso con las extensiones de E/S registradas de Winsock. |
| [**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Envía datos de red en un socket TCP de E/S registrado conectado o un socket UDP de E/S registrado enlazado para su uso con las extensiones de E/S registradas en Winsock. |
| [**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Envía datos de red en un socket TCP de E/S registrado conectado o un socket UDP de E/S registrado enlazado con opciones adicionales para su uso con las extensiones de E/S registradas de Winsock. |
| [**Seleccione**](/windows/win32/api/Winsock2/nf-winsock2-select) | Determina el estado de uno o varios sockets, en espera si es necesario, para realizar E/S sincrónica. |
| [**Enviar**](/windows/win32/api/Winsock2/nf-winsock2-send) | Envía datos en un socket conectado. |
| [**sendto**](/windows/win32/api/winsock/nf-winsock-sendto) | Envía datos a un destino específico. |
| [**SetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Registra un nombre de host y servicio junto con las direcciones asociadas con un proveedor de espacio de nombres específico. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Establece el estado de filtro de multidifusión para un socket IPv4. |
| [**SetService**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Registra o quita del registro un servicio de red dentro de uno o varios espacios de nombres. También puede agregar o quitar un tipo de servicio de red dentro de uno o varios espacios de nombres. |
| [**SetSocketMediaStreamingMode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Indica si la red se va a usar para transferir medios de streaming que requieren calidad de servicio. |
| [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Establece una opción de socket. |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Establece el estado del filtro de multidifusión para un socket IPv4 o IPv6. |
| [**Apagado**](/windows/win32/api/winsock/nf-winsock-shutdown) | Deshabilita los envíos o las recibe en un socket. |
| [**Zócalo**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Crea un socket enlazado a un proveedor de servicios específico. |
| [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Transmite datos de archivo a través de un identificador de socket conectado. |
| [**TransmitPackets**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Transmite datos en memoria o datos de archivo a través de un socket conectado. |
| [**WSAAccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Acepta condicionalmente una conexión basada en el valor devuelto de una función de condición, proporciona especificaciones de flujo de calidad de servicio y permite la transferencia de datos de conexión. |
| [**WSAAddressToString**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Convierte todos los componentes de una [**estructura sockaddr**](sockaddr-2.md) en una representación de cadena legible de la dirección. |
| [**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Recupera de forma asincrónica la información del host que corresponde a una dirección. |
| [**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Recupera de forma asincrónica la información de host que corresponde a un nombre de host. |
| [**WSAAsyncGetProtoByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Recupera de forma asincrónica la información de protocolo que corresponde a un nombre de protocolo. |
| [**WSAAsyncGetProtoByNumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Recupera de forma asincrónica la información de protocolo que corresponde a un número de protocolo. |
| [**WSAAsyncGetServByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Recupera de forma asincrónica la información del servicio que corresponde a un nombre de servicio y un puerto. |
| [**WSAAsyncGetServByPort**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Recupera de forma asincrónica la información del servicio que corresponde a un puerto y un protocolo. |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | Solicita Windows notificación basada en mensajes de eventos de red para un socket. |
| [**WSACancelAsyncRequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Cancela una operación asincrónica incompleta. |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Finaliza el uso del32.DLL \_ Ws2. |
| [**WSACloseEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Cierra un identificador de objeto de evento abierto. |
| [**WSAConnect**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Establece una conexión a otra aplicación de socket, intercambia datos de conexión y especifica la calidad de servicio necesaria en función de la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) especificada. |
| [**WSAConnectByList**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Establece una conexión a uno de una colección de posibles puntos de conexión representados por un conjunto de direcciones de destino (nombres de host y puertos). |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Establece una conexión a otra aplicación de socket en un host y puerto especificados |
| [**WSACreateEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Crea un nuevo objeto de evento. |
| [**WSADeleteSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Quita la asociación entre un nombre de destino del mismo nivel y una dirección IP para un socket. |
| [**WSADuplicateSocket**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Devuelve una estructura que se puede usar para crear un nuevo descriptor de socket para un socket compartido. |
| [**WSAEnumNameSpaceProviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Recupera información sobre los espacios de nombres disponibles. |
| [**WSAEnumNameSpaceProvidersEx**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Recupera información sobre los espacios de nombres disponibles. |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Detecta repeticiones de eventos de red para el socket indicado, borra los registros de eventos de red internos y restablece los objetos de evento (opcional). |
| [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Recupera información sobre los protocolos de transporte disponibles. |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Especifica un objeto de evento que se va a asociar al conjunto especificado de eventos de red \_ XXX de FD. |
| [**\_\_WSAFDIsSet**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Especifica si un socket se incluye en un conjunto de descriptores de socket. |
| [**WSAGetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Consulta el estado de la opción [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) socket. |
| [**WSAGetIcmpErrorInfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Consulta la dirección de origen de un error ICMP recibido en un socket TCP durante la configuración de la conexión. |
| [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Recupera la MTU de la capa IP definida por el usuario para un socket. |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Devuelve el estado de error de la última operación que produjo un error. |
| [**WSAGetOverlappedResult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Recupera los resultados de una operación superpuesta en el socket especificado. |
| [**WSAGetQOSByName**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Inicializa una estructura [**qos basada**](/windows/win32/api/winsock2/ns-winsock2-qos) en una plantilla con nombre o proporciona un búfer para recuperar una enumeración de los nombres de plantilla disponibles. |
| [**WSAGetServiceClassInfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Recupera la información de clase (esquema) relativa a una clase de servicio especificada de un proveedor de espacios de nombres especificado. |
| [**WSAGetServiceClassNameByClassId**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Recupera el nombre del servicio asociado al tipo especificado. |
| [**WSAGetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Recupera el tamaño máximo de un mensaje coalesced recibido para un socket UDP. |
| [**WSAGetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Recupera el tamaño del mensaje de segmentación para un socket UDP. |
| [**WSAHtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Convierte un valor u \_ long del orden de bytes del host al orden de bytes de red. |
| [**WSAHtons**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Convierte un valor u \_ short del orden de bytes del host al orden de bytes de red. |
| [**WSAImpersonateSocketPeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Se usa para suplantar la entidad de seguridad correspondiente a un socket del mismo nivel con el fin de realizar la autorización de nivel de aplicación. |
| [**WSAInstallServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Registra un esquema de clase de servicio dentro de un espacio de nombres. |
| [**WSAIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Controla el modo de un socket. |
| [**WSAJoinLeaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Une un nodo hoja en una sesión multipunto, intercambia datos de conexión y especifica la calidad de servicio necesaria en función de las estructuras especificadas. |
| [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Inicia una consulta de cliente restringida por la información contenida en una [**estructura WSAQUERYSET.**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Libera el identificador usado por las llamadas anteriores a [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta). |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Recupere la información de servicio solicitada. |
| [**WSANSPIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Desarrolladores para realizar llamadas de control de E/S a un espacio de nombres registrado. |
| [**WSANtohl**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Convierte un valor u \_ long del orden de bytes de red al orden de bytes del host. |
| [**WSANt adheres**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Convierte un valor u \_ short del orden de bytes de red al orden de bytes del host. |
| [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Determina el estado de uno o varios sockets. |
| [**WSAProviderConfigChange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Notifica a la aplicación cuándo se cambia la configuración del proveedor. |
| [**WSAQuerySocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Consulta información sobre la seguridad aplicada a una conexión en un socket. |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Recibe datos de un socket conectado. |
| [**WSARecvDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Finaliza la recepción en un socket y recupera los datos de desconexión si el socket está orientado a la conexión. |
| [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Recibe datos de un socket conectado. |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Recibe un datagrama y almacena la dirección de origen. |
| [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Recibe datos e información de control opcional de sockets conectados y no conectados. |
| [**WSARemoveServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Quita permanentemente el esquema de clase de servicio del Registro. |
| [**WSAResetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Restablece el estado del objeto de evento especificado en nonsignaled. |
| [**WSARevertImpersonation**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Finaliza la suplantación de un socket del mismo nivel. |
| [**WSASend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Envía datos en un socket conectado. |
| [**WSASendDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Inicia la terminación de la conexión para el socket y envía los datos de desconexión. |
| [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Envía datos e información de control opcional desde sockets conectados y no conectados. |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Envía datos a un destino específico, mediante E/S superpuesta cuando corresponda. |
| [**WSASetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Establece el estado del objeto de evento especificado en señalado. |
| [**WSASetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Establece el estado de la opción [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) socket. |
| [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Establece la MTU de capa IP definida por el usuario en un socket. |
| [**WSASetLastError**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Establece el código de error. |
| [**WSASetService**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Registra o quita del registro una instancia de servicio dentro de uno o varios espacios de nombres. |
| [**WSASetSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Se usa para especificar el nombre de destino del mismo nivel (SPN) que corresponde a una dirección IP del mismo nivel. Este nombre de destino está pensado para que lo especifiquen las aplicaciones cliente para identificar de forma segura el elemento del mismo nivel que se debe autenticar. |
| [**WSASetSocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Habilita y aplica la seguridad para un socket. |
| [**WSASetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Establece el tamaño máximo de un conjunto de mensajes coalesced en un socket UDP. |
| [**WSASetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Establece el tamaño del mensaje de segmentación en un socket UDP. |
| [**WSASocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Crea un socket enlazado a un proveedor de servicios de transporte específico. |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Inicia el uso de WS2 \_32.DLL mediante un proceso. |
| [**WSAStringToAddress**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Convierte una cadena numérica en una [**estructura sockaddr.**](sockaddr-2.md) |
| [**WSAWaitForMultipleEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Devuelve cuando uno o todos los objetos de evento especificados están en estado señalado o cuando expira el intervalo de tiempo de espera. |
