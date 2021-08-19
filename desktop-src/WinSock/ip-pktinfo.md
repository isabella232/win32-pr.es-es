---
description: Permite que una aplicación habilite o deshabilite la devolución de información de paquetes mediante la función WSARecvMsg en un socket IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: IP_PKTINFO de socket (Ws2ipdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ba653b4ece11086706493b920e1ed650b66eecdd6e788a5edfe259cf9eb9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097795"
---
# <a name="ip_pktinfo-socket-option"></a>Opción \_ de socket PKTINFO de IP

La opción de socket IP PKTINFO permite que una aplicación habilite o deshabilite la devolución de información de paquetes mediante la función \_ [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) en un socket IPv4.

Para consultar el estado de esta opción de socket, llame a [**la función getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Para establecer esta opción, llame a la [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.

## <a name="socket-option-value"></a>Valor de opción de socket

La constante que representa esta opción de socket es 19.

## <a name="syntax"></a>Sintaxis


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
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

Nivel en el que se define la opción. Use **IP DE \_ IPPROTO** para esta operación.

</dd> <dt>

*optname* \[ En\]
</dt> <dd>

Opción de socket para la que se va a obtener o establecer el valor. Use IP \_ PKTINFO para esta operación.

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
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Una llamada Windows sockets 1.1 está en curso o el proveedor de servicios sigue procesando una función de devolución de llamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Se proporcionó un argumento no válido. Este error se devuelve si el *parámetro de* nivel es desconocido o no es válido. En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La familia de protocolos indicada desconoce o no admite la opción. Este error se devuelve si el parámetro *de tipo* para el descriptor de socket pasado en el parámetro *s* no era **SOCK \_ DGRAM** o **SOCK \_ RAW.** <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket IP PKTINFO permite a una aplicación determinar si la función \_ [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)va a devolver información de paquetes para un socket IPv4.

La [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) llamada con la opción de socket IP PKTINFO permite que una aplicación habilite o deshabilite la devolución de información de paquetes mediante la función \_ LPFN_WSARECVMSG [**(WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) La opción \_ IP PKTINFO para un socket está deshabilitada (se establece en **FALSE)** de forma predeterminada.

Cuando esta opción de socket está habilitada en un socket IPv4 de tipo **SOCK \_ DGRAM** o **SOCK \_ RAW,** la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelve información de paquetes en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a la que apunta el *parámetro lpMsg.* Uno de los objetos de datos de control de la estructura **WSAMSG** devuelta contendrá una estructura [**\_ en pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) que se usa para almacenar la información de la dirección de paquete recibida.

Para los datagramas recibidos por la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sobre IPv4, el miembro **Control** de la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recibida contendrá una estructura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contiene una estructura **WSACMSGHDR.** El miembro de nivel **\_ cmsg** de esta estructura **WSACMSGHDR** contendrá **IP \_ IP de IPPROTO,** el miembro de tipo **cmsg \_** de esta estructura contendrá **IP \_ PKTINFO** y el miembro de datos **cmsg \_** contendrá una estructura [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) que se usa para almacenar la información de la dirección de paquete IPv4 recibida. La dirección IPv4 de la **estructura \_ in pktinfo** es la dirección IPv4 desde la que se recibió el paquete.

Para un socket de datagrama de doble pila, si una aplicación requiere que la función [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelva información de paquetes en una estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para los datagramas recibidos a través de IPv4, la opción de socket PKTINFO de IP debe establecerse en true en el \_ socket. Si solo la opción [ \_ PKTINFO de IPV6](ipv6-pktinfo.md) se establece en true en el socket, se proporciona información de paquetes para los datagramas recibidos a través de IPv6, pero no se puede proporcionar para los datagramas recibidos a través de IPv4.

Si una aplicación intenta establecer la opción de socket IP PKTINFO en un socket de datagrama de doble pila e IPv4 está deshabilitado en el sistema, se producirá un error en la función \_ [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devolverá un error de [WSAEINVAL.](windows-sockets-error-codes-2.md) La función **setsockopt** también devuelve este mismo error como resultado de otros errores. Si una aplicación intenta establecer una opción de socket de nivel IPPROTO en un socket de pila doble y se produce un error con \_ [WSAEINVAL,](windows-sockets-error-codes-2.md)la aplicación debe determinar si IPv4 está deshabilitado en el equipo local. Un método que se puede usar para detectar si IPv4 está habilitado o deshabilitado es llamar a la función [**de socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con el parámetro *af* establecido en AF INET para intentar crear un \_ socket IPv4. Si se **produce un** error en la función de socket y **WSAGetLastError** devuelve un error [de WSAEAFNOSUPPORT,](windows-sockets-error-codes-2.md)significa que IPv4 no está habilitado. En este caso, la aplicación puede omitir un error de función **setsockopt** al intentar establecer la opción de \_ socket IP PKTINFO. De lo contrario, un error al intentar establecer la opción de \_ socket IP PKTINFO debe tratarse como un error inesperado.

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

[**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**Opciones de socket \_ IPPROTO**](ipproto-ip-socket-options.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Zócalo**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
