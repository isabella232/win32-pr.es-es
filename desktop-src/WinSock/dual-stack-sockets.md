---
description: Con el fin de admitir IPv4 e IPv6 en Windows XP con Service Pack 1 (SP1) y en Windows Server 2003, una aplicación tiene que crear dos sockets, un socket para su uso con IPv4 y un socket para su uso con IPv6.
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Sockets Dual-Stack para aplicaciones Winsock de IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943d8150586bcf14a905ab32dcacaea63b7d6982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705632"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Sockets Dual-Stack para aplicaciones Winsock de IPv6

Con el fin de admitir IPv4 e IPv6 en Windows XP con Service Pack 1 (SP1) y en Windows Server 2003, una aplicación tiene que crear dos sockets, un socket para su uso con IPv4 y un socket para su uso con IPv6. La aplicación debe controlar estos dos sockets por separado.

Windows Vista y versiones posteriores ofrecen la posibilidad de crear un socket IPv6 único que pueda controlar el tráfico IPv6 e IPv4. Por ejemplo, se crea un socket de escucha TCP para IPv6, se coloca en modo de pila doble y se enlaza al puerto 5001. Este socket de doble pila puede aceptar conexiones de clientes TCP IPv6 que se conectan al puerto 5001 y desde clientes TCP IPv4 que se conectan al puerto 5001. Esta característica permite un diseño de aplicaciones enormemente simplificado y reduce la sobrecarga de recursos necesaria para las operaciones de publicación en dos sockets independientes.

## <a name="creating-a-dual-stack-socket"></a>Creación de un socket de Dual-Stack

De forma predeterminada, un socket IPv6 creado en Windows Vista y versiones posteriores solo funciona a través del protocolo IPv6. Para convertir un socket IPv6 en un socket de pila doble, se debe llamar a [**la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) llamada a la función de **\_ V6ONLY** para establecer este valor en cero antes de que el socket esté enlazado a una dirección IP. Cuando la opción de socket **\_ V6ONLY de IPv6** está establecida en cero, un socket creado para la familia de direcciones **AF \_ inet6** se puede usar para enviar y recibir paquetes a y desde una dirección IPv6 o una dirección IPv4 asignada.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>Direcciones IP con un socket Dual-Stack

Los sockets de doble pila siempre requieren direcciones IPv6. La capacidad de interactuar con una dirección IPv4 requiere el uso del formato de dirección IPv6 asignado a IPv4. Todas las direcciones IPv4 deben representarse en el formato de dirección IPv6 asignado a IPv4, lo que permite que una aplicación solo IPv6 se comunique con un nodo IPv4. El formato de dirección IPv6 asignado a IPv4 permite representar la dirección IPv4 de un nodo IPv4 como una dirección IPv6. La dirección IPv4 se codifica en los bits 32 de orden inferior de la dirección IPv6 y los bits 96 de orden superior tienen el prefijo fijo 0:0: 0:0: FFFF. El formato de dirección IPv6 asignado a IPv4 se especifica en RFC 4291. Para obtener más información, consulte [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La \_ macro IN6ADDR SETV4MAPPED de *Mstcpip. h* se puede usar para convertir una dirección IPv4 en el formato de dirección IPv6 asignado a IPv4 requerido.

Si el protocolo subyacente es en realidad IPv4, la dirección IPv4 se asigna a un formato de dirección IPv6 asignado a IPv4. Es decir, el campo Family de la estructura [SOCKADDR](sockaddr-2.md) indica AF \_ inet6, pero una dirección IPv6 asignada por IPv4 se codifica en la estructura de la dirección IPv6. En el caso de un socket de doble pila en modo de escucha, esto significa que cualquier conexión IPv4 aceptada devolverá una dirección IPv6 asignada a IPv4. Para un socket de doble pila que se está conectando a un destino IPv4, la estructura SOCKADDR que se pasa a Connect debe ser una dirección IPv6 asignada a IPv4. Las aplicaciones deben tener cuidado de administrar estas direcciones IPv6 asignadas por IPv4 de manera adecuada y solo usarlas con sockets de pila duales. Si se va a pasar una dirección IP a un socket IPv4 normal, la dirección debe ser una dirección IPv4 normal, no una dirección IPv6 asignada a IPv4.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Posibles problemas con un socket de Dual-Stack

Un posible error en las aplicaciones es obtener una dirección IPv6 asignada por IPv4 en un socket de doble pila y, a continuación, intentar usar la dirección IP devuelta en otro socket solo IPv6. Por ejemplo, las funciones [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) o [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) pueden devolver una dirección IPv6 asignada a IPv4 cuando se usa en un socket de doble pila. Si la dirección IPv6 asignada a IPv4 devuelta se usa posteriormente en un socket diferente que no se estableció en una pila dual (un socket solo IPv6 que es el comportamiento predeterminado cuando se crea un socket), se producirá un error al usar este socket solo IPv6 con una dirección IPv6 asignada por IPv4. El formato de dirección IPv6 asignado a IPv4 solo se puede usar en un socket de pila doble.

En un socket de datagrama de pila doble, si una aplicación requiere la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) para devolver información de paquetes en una estructura de [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para los datagramas recibidos a través de IPv4, la opción de socket de [IP \_ PKTINFO](ip-pktinfo.md) debe establecerse en true en el socket. Si solo la [opción \_ PKTINFO de IPv6](ipv6-pktinfo.md) está establecida en true en el socket, se proporcionará información de paquetes para los datagramas recibidos a través de IPv6, pero es posible que no se proporcionen para los datagramas recibidos a través de IPv4.

Si una aplicación intenta establecer la opción de socket [ \_ PKTINFO de IP](ip-pktinfo.md) en un socket de datagrama de pila doble e IPv4 está deshabilitado en el sistema, se producirá un error en [**la función MUTE**](/windows/desktop/api/winsock/nf-winsock-setsockopt) y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devolverá un error de [WSAEINVAL](windows-sockets-error-codes-2.md). Este mismo error **también lo devuelve la función** My como resultado de otros errores. Si una aplicación intenta establecer una \_ opción de socket de nivel IP de IPPROTO en un socket de doble pila y se produce un error con [WSAEINVAL](windows-sockets-error-codes-2.md), la aplicación debe determinar si IPv4 está deshabilitado en el equipo local. Un método que se puede usar para detectar si IPv4 está habilitado o deshabilitado es llamar a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con el parámetro *AF* establecido en AF \_ inet para probar y crear un socket IPv4. Si se produce un error en la función de **socket** y **WSAGetLastError** devuelve un error de [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), significa que IPv4 no está habilitado. En este caso, la aplicación puede pasar por alto **un error de la** función de r al intentar establecer la \_ opción de socket PKTINFO de IP. De lo contrario, un error al intentar establecer la \_ opción de socket PKTINFO de IP debe tratarse como un error inesperado.

Para un socket de doble pila cuando se envían datagramas con la función [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) y una aplicación desea especificar la dirección IP local específica que se va a usar, el método para controlar esto depende de la dirección IP de destino. Cuando se envía a una dirección de destino IPv4 o a una dirección de destino IPv6 asignada por IPv4, uno de los objetos de datos de control pasados en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) señalada por el parámetro *lpMsg* debe contener una estructura [**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) que contenga la dirección de origen IPv4 local que se va a usar para el envío. Cuando se envía a una dirección de destino IPv6 que no es una dirección IPv6 asignada por IPv4, uno de los objetos de datos de control pasados en la estructura **WSAMSG** señalada por el parámetro *lpMsg* debe contener una estructura [**IN6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) que contenga la dirección de origen IPv6 local que se va a usar para el envío.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para aplicaciones de Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Cambiar las estructuras de datos para IPv6 Winsock Appications](changing-data-structures-2.md)
</dt> <dt>

[Llamadas de función para aplicaciones Winsock de IPv6](function-calls-2.md)
</dt> <dt>

[Uso de direcciones IPv4 codificadas](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones Winsock de IPv6](underlying-protocols-2.md)
</dt> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**IN6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[\_PKTINFO IP](ip-pktinfo.md)
</dt> <dt>

[\_PKTINFO IPv6](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
