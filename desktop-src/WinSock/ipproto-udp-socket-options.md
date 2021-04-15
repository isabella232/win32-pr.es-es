---
description: En la tabla siguiente se describen \_ las opciones de socket UDP de IPPROTO que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF \_ inet y AF \_ inet6) con el parámetro Protocol a la función socket especificada como UDP (IPPROTO \_ UDP).
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: Opciones de socket IPPROTO_UDP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 6f1f25ebae34d7db4290ab23bbf799fc0e0b68df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708774"
---
# <a name="ipproto_udp-socket-options"></a>\_Opciones de socket UDP de IPPROTO

En la tabla siguiente se describen las opciones de socket **\_ UDP de IPPROTO** que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF \_ inet y AF \_ inet6) con el parámetro *Protocol* a la función [**socket**](/windows/win32/api/Winsock2/nf-winsock2-socket) especificada como UDP (IPPROTO \_ UDP). Consulte las páginas de referencia de [**la función**](/windows/win32/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) y el valor de My para obtener más información sobre cómo obtener y establecer las opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas de cada protocolo instalado, use la función [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

## <a name="options"></a>Opciones

| Opción | Obtener | Set | Tipo Optval | Descripción |
|-|-|-|-|-|
| Cobertura de la \_ suma de comprobación UDP \_ (Ws2tcpip. h) | sí | sí | DWORD (booleano) | Cuando **es true**, los datagramas UDP se envían con una suma de comprobación. |
| Nocomprobaciones de UDP \_ (Ws2tcpip. h) | sí | sí | DWORD (booleano) | Si **es true**, se envían datagramas UDP con la suma de comprobación de cero. Requerido para los proveedores de servicios. Si un proveedor de servicios no tiene un mecanismo para deshabilitar el cálculo de la suma de comprobación UDP, puede que simplemente almacene esta opción sin realizar ninguna acción. Esta opción no es compatible con IPv6. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef. h; include Ws2tcpip. h) | sí | sí | DWORD | Cuando se establece en un valor distinto de cero, varios datagramas recibidos se pueden fusionar en un solo búfer de mensajes antes de que se indiquen a la aplicación. El valor de la opción representa el tamaño máximo del mensaje en bytes para los mensajes fusionados que se pueden indicar a la aplicación. Todavía se pueden indicar los mensajes no fusionados con un tamaño mayor que el valor de opción. El valor predeterminado es 0 (sin fusión). Los datagramas solo se fusionarán si se originan en la misma dirección de origen y puerto. Todos los datagramas fusionados tendrán el mismo tamaño &mdash; , excepto el último, que puede ser menor. Si su aplicación desea recuperar los tamaños de los datagramas (excepto el último, que puede diferir) que se fusionó, debe usar una API de recepción que admita información de control (como [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)). El tamaño de todos los mensajes, excepto el último, se puede encontrar en el mensaje de control de **UDP_COALESCED_INFO** , que es de tipo DWORD. Para la seguridad de tipos, la aplicación debe usar las funciones [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) y [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) en lugar de la opción socket directamente. |
| UDP_SEND_MSG_SIZE (ws2ipdef. h; include Ws2tcpip. h) | sí | sí | DWORD | Cuando se establece en un valor distinto de cero, los búferes enviados por la aplicación se dividen en varios mensajes por la pila de red. El valor de la opción representa el tamaño de cada mensaje desactivado. El valor de la opción se representa en bytes. El tamaño del último segmento puede ser menor que el valor de la opción. El valor predeterminado es 0 (sin segmentación). La aplicación debe establecer un valor que sea menor que la MTU de la ruta de acceso a los destinos para evitar la fragmentación de IP. Para la seguridad de tipos, la aplicación debe usar las funciones [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) y [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) en lugar de la opción socket directamente. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Compatibilidad de Windows heredada con \_ las opciones de UDP de IPPROTO

**UDP \_ de La \_ cobertura** de la suma de comprobación no está disponible en Windows 2000 y en Windows NT4. **UDP \_ de La \_ cobertura** de la suma de comprobación y la **\_ nocomprobaciones UDP** no están disponibles en Windows 9x/me. 

## <a name="remarks"></a>Observaciones

En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel de **\_ UDP de IPPROTO** se define en el archivo de encabezado *Ws2def. h* que se incluye automáticamente en el archivo de encabezado *WinSock2. h* . Las opciones de socket **\_ UDP de IPPROTO** se definen en el archivo de encabezado *Ws2tcpip. h* . El archivo de encabezado *Ws2def. h* nunca debe usarse directamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado<br/> | <dl> <dt>ws2ipdef. h (incluye Ws2tcpip. h) y Ws2tcpip. h</dt> <dt>WinSock2. h en Windows Server 2003, Windows XP y Windows 2000</dt> </dl> |
