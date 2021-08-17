---
description: Para admitir IPv4 e IPv6 en Windows XP con Service Pack 1 (SP1) y en Windows Server 2003, una aplicación tiene que crear dos sockets, uno para su uso con IPv4 y otro para su uso con IPv6.
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Dual-Stack sockets para aplicaciones IPv6 Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424580569fb3bed5e81c6232cb99dc2d53a30af1ab2c23c9b4afa6945c0a6eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132668"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Dual-Stack sockets para aplicaciones IPv6 Winsock

Para admitir IPv4 e IPv6 en Windows XP con Service Pack 1 (SP1) y en Windows Server 2003, una aplicación tiene que crear dos sockets, uno para su uso con IPv4 y otro para su uso con IPv6. La aplicación debe controlar estos dos sockets por separado.

Windows Vista y versiones posteriores ofrecen la posibilidad de crear un único socket IPv6 que pueda controlar el tráfico IPv6 e IPv4. Por ejemplo, se crea un socket de escucha TCP para IPv6, se coloca en modo de pila dual y se enlaza al puerto 5001. Este socket de doble pila puede aceptar conexiones de clientes TCP IPv6 que se conectan al puerto 5001 y desde clientes TCP IPv4 que se conectan al puerto 5001. Esta característica permite un diseño de aplicaciones muy simplificado y reduce la sobrecarga de recursos necesaria para publicar operaciones en dos sockets independientes.

## <a name="creating-a-dual-stack-socket"></a>Creación de un Dual-Stack socket

De forma predeterminada, un socket IPv6 creado en Windows Vista y versiones posteriores solo funciona a través del protocolo IPv6. Para convertir un socket IPv6 en un socket de doble pila, se debe llamar a la función [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con la opción de socket **\_ IPV6 V6ONLY** para establecer este valor en cero antes de enlazar el socket a una dirección IP. Cuando la opción de socket **\_ IPV6 V6ONLY** se establece en cero, se puede usar un socket creado para la familia de direcciones **AF \_ INET6** para enviar y recibir paquetes hacia y desde una dirección IPv6 o una dirección asignada IPv4.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>Direcciones IP con un Dual-Stack socket

Los sockets de pila doble siempre requieren direcciones IPv6. La capacidad de interactuar con una dirección IPv4 requiere el uso del formato de dirección IPv6 asignado a IPv4. Todas las direcciones IPv4 deben representarse en el formato de dirección IPv6 asignado a IPv4, lo que permite que una aplicación solo IPv6 se comunique con un nodo IPv4. El formato de dirección IPv6 asignado a IPv4 permite que la dirección IPv4 de un nodo IPv4 se represente como una dirección IPv6. La dirección IPv4 se codifica en los 32 bits de orden inferior de la dirección IPv6 y los 96 bits de orden superior tienen el prefijo fijo 0:0:0:0:0:FFFF. El formato de dirección IPv6 asignado a IPv4 se especifica en RFC 4291. Para obtener más información, [vea www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La macro SETV4MAPPED de IN6ADDR de \_ *Mstcpip.h* se puede usar para convertir una dirección IPv4 al formato de dirección IPv6 asignado a IPv4 necesario.

Si el protocolo subyacente es realmente IPv4, la dirección IPv4 se asigna a un formato de dirección IPv6 asignado a IPv4. Es decir, el campo familia de la estructura [SOCKADDR](sockaddr-2.md) indica AF INET6, pero una dirección IPv6 asignada a IPv4 se codifica en la estructura de direcciones \_ IPv6. Para un socket de doble pila en modo de escucha, esto significa que las conexiones IPv4 aceptadas devolverán una dirección IPv6 asignada a IPv4. Para un socket de doble pila que se conecta a un destino IPv4, la estructura SOCKADDR pasada para conectarse debe ser una dirección IPv6 asignada a IPv4. Las aplicaciones deben tener cuidado de controlar estas direcciones IPv6 asignadas a IPv4 correctamente y usarlas solo con sockets de pila duales. Si se va a pasar una dirección IP a un socket IPv4 normal, la dirección debe ser una dirección IPv4 normal y no una dirección IPv6 asignada a IPv4.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Posibles problemas al usar un socket Dual-Stack

Un posible problema para las aplicaciones es obtener una dirección IPv6 asignada a IPv4 en un socket de doble pila y, a continuación, intentar usar la dirección IP devuelta en otro socket solo IPv6. Por ejemplo, las [**funciones getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) o [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) pueden devolver una dirección IPv6 asignada a IPv4 cuando se usa en un socket de doble pila. Si la dirección IPv6 asignada a IPv4 devuelta se usa posteriormente en un socket diferente que no se estableció en doble pila (un socket solo IPv6 que es el comportamiento predeterminado cuando se crea un socket), se producirá un error en cualquier uso de este socket solo IPv6 con una dirección IPv6 asignada por IPv4. El formato de dirección IPv6 asignado a IPv4 solo se puede usar en un socket de doble pila.

En un socket de datagrama de doble pila, si una aplicación requiere que la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelva información de paquetes en una estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para los datagramas recibidos a través de IPv4, la opción de socket [ \_ PKTINFO](ip-pktinfo.md) de IP debe establecerse en true en el socket. Si solo la opción [ \_ PKTINFO de IPV6](ipv6-pktinfo.md) se establece en true en el socket, se proporciona información de paquetes para los datagramas recibidos a través de IPv6, pero es posible que no se proporcionan para los datagramas recibidos a través de IPv4.

Si una aplicación intenta establecer la opción de socket [ \_ PKTINFO](ip-pktinfo.md) de IP en un socket de datagrama de doble pila e IPv4 está deshabilitado en el sistema, se producirá un error en la función [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devolverá un error de [WSAEINVAL.](windows-sockets-error-codes-2.md) La función **setsockopt** también devuelve este mismo error como resultado de otros errores. Si una aplicación intenta establecer una opción de socket de nivel IPPROTO en un socket de doble pila y se produce un error con \_ [WSAEINVAL](windows-sockets-error-codes-2.md), la aplicación debe determinar si IPv4 está deshabilitado en el equipo local. Un método que se puede usar para detectar si IPv4 está habilitado o deshabilitado es llamar a la función [**de socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con el parámetro *af* establecido en AF INET para intentar crear un \_ socket IPv4. Si se **produce un** error en la función de socket y **WSAGetLastError** devuelve un error [de WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), significa que IPv4 no está habilitado. En este caso, la aplicación puede omitir un error de función **setsockopt** al intentar establecer la opción de \_ socket IP PKTINFO. De lo contrario, un error al intentar establecer la opción de \_ socket IP PKTINFO debe tratarse como un error inesperado.

Para un socket de doble pila al enviar datagramas con la función [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) y una aplicación quiere especificar una dirección de origen IP local específica que se va a usar, el método para controlar esto depende de la dirección IP de destino. Al enviar a una dirección de destino IPv4 o a una dirección de destino IPv6 asignada a IPv4, uno de los objetos de datos de control pasados en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a la que apunta el parámetro *lpMsg* debe contener una estructura [**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) que contenga la dirección de origen IPv4 local que se usará para el envío. Al enviar a una dirección de destino IPv6 que no es una dirección IPv6 asignada a IPv4, uno de los objetos de datos de control pasados en la estructura **WSAMSG** a la que apunta el parámetro *lpMsg* debe contener una estructura [**\_ in6 pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) que contiene la dirección de origen IPv6 local que se usará para el envío.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para aplicaciones Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Cambio de estructuras de datos para aplicaciones winsock de IPv6](changing-data-structures-2.md)
</dt> <dt>

[Llamadas de función para aplicaciones IPv6 Winsock](function-calls-2.md)
</dt> <dt>

[Uso de direcciones IPv4 codificadas de forma rígida](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Interfaz de usuario problemas de aplicaciones IPv6 Winsock](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones IPv6 Winsock](underlying-protocols-2.md)
</dt> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
