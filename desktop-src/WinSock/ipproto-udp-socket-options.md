---
description: En la tabla siguiente se describen las opciones de socket UDP de IPPROTO que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF INET e AF INET6) con el parámetro protocol para la función de socket especificada como \_ \_ UDP \_ (IPPROTO \_ UDP).
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: Opciones de socket IPPROTO_UDP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 763e45a78ffd8bfed15d09f4e77bc17be71ccc110499d8937b60b49294f499c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051483"
---
# <a name="ipproto_udp-socket-options"></a>Opciones de socket UDP de IPPROTO \_

En la tabla siguiente se describen las opciones de socket UDP de **IPPROTO \_** que se aplican a los sockets creados para las familias de direcciones IPv4 e IPv6 (AF INET e AF INET6) con el parámetro protocol para la función de socket especificada como \_ UDP \_ (IPPROTO  [](/windows/win32/api/Winsock2/nf-winsock2-socket) \_ UDP). Consulte las [**páginas de referencia de la función getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) y [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) para obtener más información sobre cómo obtener y establecer opciones de socket.

Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la función [**WSAEnumProtocols,**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

## <a name="options"></a>Opciones

| Opción | Obtener | Set | Tipo optval | Descripción |
|-|-|-|-|-|
| COBERTURA \_ DE SUMA DE COMPROBACIÓN UDP \_ (ws2tcpip.h) | Sí | Sí | DWORD (booleano) | Cuando **es TRUE,** los datagramas UDP se envían con una suma de comprobación. |
| UDP \_ NOCHECKSUM (ws2tcpip.h) | Sí | Sí | DWORD (booleano) | Cuando **es TRUE,** los datagramas UDP se envían con la suma de comprobación de cero. Obligatorio para los proveedores de servicios. Si un proveedor de servicios no tiene un mecanismo para deshabilitar el cálculo de suma de comprobación UDP, puede almacenar simplemente esta opción sin realizar ninguna acción. Esta opción no se admite para IPv6. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef.h; incluir ws2tcpip.h) | Sí | Sí | DWORD | Cuando se establece en un valor distinto de cero, se pueden usar varios datagramas recibidos en un solo búfer de mensajes antes de que se indiquen a la aplicación. El valor de opción representa el tamaño máximo del mensaje en bytes para los mensajes coalecidos que se pueden indicar a la aplicación. Todavía se pueden indicar mensajes sin usar mayores que el valor de opción. El valor predeterminado es 0 (sin uso). Los datagramas solo se coalirán si se originaron en la misma dirección de origen y puerto. Todos los datagramas coalesced tendrán el mismo tamaño, excepto el &mdash; último datagrama, que puede ser menor. Si la aplicación quiere recuperar los tamaños de datagrama (excepto el último datagrama, que puede diferir) que se han coalido, debe usar una API de recepción que admita información de control (como [**LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) El tamaño de todos, menos el último mensaje, se puede encontrar en el **UDP_COALESCED_INFO** de control, que es de tipo DWORD. Para la seguridad de tipos, la aplicación debe usar las funciones [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) y [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) en lugar de la opción de socket directamente. |
| UDP_SEND_MSG_SIZE (ws2ipdef.h; incluir ws2tcpip.h) | Sí | Sí | DWORD | Cuando se establece en un valor distinto de cero, los búferes enviados por la aplicación se desglosan en varios mensajes mediante la pila de redes. El valor de opción representa el tamaño de cada mensaje desglosado. El valor de la opción se representa en bytes. El tamaño del último segmento puede ser menor que el valor de la opción. El valor predeterminado es 0 (sin segmentación). La aplicación debe establecer un valor inferior a la MTU de la ruta de acceso a los destinos para evitar la fragmentación de IP. Para la seguridad de tipos, la aplicación debe usar las funciones [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) y [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) en lugar de la opción de socket directamente. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Compatibilidad de Windows heredado con las opciones UDP de IPPROTO \_

**UDP \_ CHECKSUM \_ COVERAGE** no está disponible en Windows 2000 y Windows NT4. **UDP \_ CHECKSUM \_ COVERAGE** y **UDP \_ NOCHECKSUM** no están disponibles en Windows 9x/Me. 

## <a name="remarks"></a>Comentarios

En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el nivel UDP de **IPPROTO \_** se define en el archivo de encabezado *Ws2def.h* que se incluye automáticamente en el archivo de encabezado *Winsock2.h.* Las opciones de socket UDP de **IPPROTO \_** se definen en el archivo de *encabezado Ws2tcpip.h.* El *archivo de encabezado Ws2def.h* nunca debe usarse directamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado<br/> | <dl> <dt>ws2ipdef.h (incluye ws2tcpip.h) y ws2tcpip.h</dt> <dt>Winsock2.h en Windows Server 2003, Windows XP y Windows 2000</dt> </dl> |
