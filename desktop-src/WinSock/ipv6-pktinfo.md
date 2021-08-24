---
description: Permite que una aplicación habilite o deshabilite la devolución de información de paquetes mediante la función WSARecvMsg en un socket IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: IPV6_PKTINFO de socket (Ws2ipdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1bee015e7a73b803d78ae914e71a863dec83e4f40fc1aea9f631a54b37c586a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733775"
---
# <a name="ipv6_pktinfo-socket-option"></a>Opción de socket \_ PKTINFO de IPV6

La opción de socket PKTINFO de IPV6 permite que una aplicación habilite o deshabilite la devolución de información de paquetes mediante la función \_ [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) en un socket IPv6.

Para consultar el estado de esta opción de socket, llame a [**la función getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Para establecer esta opción, llame a la [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.

## <a name="socket-option-value"></a>Valor de opción de socket

La constante que representa esta opción de socket es 19.

## <a name="syntax"></a>Sintaxis


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* \[ en\]
</dt> <dd>

Descriptor que identifica el socket.

</dd> <dt>

*level* \[ En\]
</dt> <dd>

Nivel en el que se define la opción. Use **IPPROTO \_ IPV6** para esta operación.

</dd> <dt>

*optname* \[ En\]
</dt> <dd>

Opción de socket para la que se va a obtener o establecer el valor. Use IPV6 \_ PKTINFO para esta operación.

</dd> <dt>

*optval* \[ out\]
</dt> <dd>

Puntero al búfer que contiene el valor de la opción que se debe establecer. Este parámetro debe apuntar al búfer igual o mayor que el tamaño de un **valor DWORD.**

Este valor se trata como un valor booleano con 0 usado para indicar **FALSE** (deshabilitado) y un valor distinto de cero para indicar **TRUE** (habilitado).

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Puntero al tamaño, en bytes, del *búfer optval.* Este tamaño debe ser igual o mayor que el tamaño de un **valor DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, la [**función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) devuelve cero.

Si se produce un error en la operación, se devuelve un valor de SOCKET ERROR y se puede recuperar un código de error específico llamando \_ a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código de error                                                                                                                                              | Significado                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Debe [**producirse una llamada correcta a WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) antes de usar esta función.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Error en el subsistema de red.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno de los *parámetros optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario. Este error también se devuelve si el valor al que apunta el *parámetro optlen* es menor que el tamaño de **un valor DWORD.**<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Hay un bloqueo Windows llamada a Sockets 1.1 en curso o el proveedor de servicios sigue procesando una función de devolución de llamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Se proporcionó un argumento no válido. Este error se devuelve si el *parámetro level* es desconocido o no es válido. En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La familia de protocolos indicada desconoce o no admite la opción. Este error se devuelve si el parámetro *de tipo* para el descriptor de socket pasado en el parámetro *s* no era **SOCK \_ DGRAM** o **SOCK \_ RAW.** <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) a la que se llama con la opción de socket PKTINFO de IPV6 permite a una aplicación determinar si la función \_ [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)va a devolver información de paquetes para un socket IPv6.

La [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) a la que se llama con la opción de socket PKTINFO de IPV6 permite que una aplicación habilite o deshabilite la devolución de información de paquetes por parte de la función \_ LPFN_WSARECVMSG [**(WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) La opción PKTINFO de IPV6 \_ para un socket está deshabilitada (se establece en **FALSE)** de forma predeterminada.

Cuando esta opción de socket está habilitada en un socket IPv6 de tipo **SOCK \_ DGRAM** o **SOCK \_ RAW,** la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelve información de paquetes en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a la que apunta el *parámetro lpMsg.* Uno de los objetos de datos de control de la estructura **WSAMSG** devuelta contendrá una estructura [**\_ pktinfo in6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) que se usa para almacenar la información de la dirección de paquete recibida.

Para los datagramas recibidos por la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sobre IPv6, el miembro **Control** de la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recibida contendrá una estructura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contiene una estructura **WSACMSGHDR.** El miembro de nivel **cmsg \_** de esta estructura **WSACMSGHDR** contendrá **IPPROTO \_ IPV6,** el miembro de tipo **cmsg \_** de esta estructura contendrá **IPV6 \_ PKTINFO** y el miembro de datos **cmsg \_** contendrá una estructura [**\_ pktinfo in6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) que se usa para almacenar la información de direcciones de paquete IPv6 recibidas. La dirección IPv6 de la estructura **\_ pktinfo in6** es la dirección IPv6 desde la que se recibió el paquete.

Para un socket de datagrama de doble pila, si una aplicación requiere que la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelva información de paquetes en una estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para los datagramas recibidos a través de IPv4, la opción de socket [ \_ PKTINFO](ip-pktinfo.md) de IP debe establecerse en true en el socket. Si solo la opción PKTINFO de IPV6 se establece en true en el socket, se proporciona información de paquetes para los datagramas recibidos a través de IPv6, pero no se puede proporcionar para los datagramas recibidos a través \_ de IPv4.

Tenga en cuenta que el archivo de encabezado *Ws2ipdef.h* se incluye automáticamente en *Ws2tcpip.h* y nunca se debe usar directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Ws2ipdef.h (incluya Ws2tcpip.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sockets de pila doble](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[**Opciones de socket \_ IPV6 de IPPROTO**](ipproto-ipv6-socket-options.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Zócalo**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
