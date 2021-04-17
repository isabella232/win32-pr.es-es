---
description: Permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función WSARecvMsg en un socket IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: Opción de socket de IP_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2134b31ead9efeb032b4ed72fcaedcd4cc9f67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360297"
---
# <a name="ip_pktinfo-socket-option"></a>IP \_ PKTINFO socket, opción

La \_ opción de socket PKTINFO de IP permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) en un socket IPv4.

Para consultar el estado de esta opción de socket, llame a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Para establecer esta opción, llame a [**la función del método de llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.

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

Un descriptor que identifica el socket.

</dd> <dt>

*nivel* \[ de de\]
</dt> <dd>

Nivel en el que se define la opción. Use **la \_ dirección IP de IPPROTO** para esta operación.

</dd> <dt>

*optname* \[ de\]
</dt> <dd>

Opción de socket para la que se va a obtener o establecer el valor. Use \_ la PKTINFO IP para esta operación.

</dd> <dt>

*optval* \[ enuncia\]
</dt> <dd>

Puntero al búfer que contiene el valor de la opción que se va a establecer. Este parámetro debe apuntar al búfer igual o mayor que el tamaño de un valor **DWORD** .

Este valor se trata como un valor booleano con 0 que se usa para indicar **false** (deshabilitado) y un valor distinto de cero para indicar **true** (habilitado).

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Puntero al tamaño, en bytes, del búfer *optval* . Este tamaño debe ser igual o mayor que el tamaño de un valor **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o el [**valor de My**](/windows/desktop/api/winsock/nf-winsock-setsockopt) devuelve cero.

Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código de error                                                                                                                                              | Significado                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Error en el subsistema de red.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario. Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de un valor **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Se proporcionó un argumento no válido. Este error se devuelve si el parámetro *LEVEL* es desconocido o no es válido. En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La opción es desconocida o no es compatible con la familia del protocolo indicada. Se devuelve este error si el parámetro de *tipo* para el descriptor de socket pasado en el parámetro *s* no era **sock \_ DGRAM** o **sock \_ raw**. <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) a la que se llama con la \_ opción IP PKTINFO socket permite que una aplicación determine si la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)devolverá información de paquetes para un socket IPv4.

La [**función de la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la llamada con la \_ opción de socket PKTINFO de IP permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . De \_ forma predeterminada, la opción PKTINFO de IP para un socket está deshabilitada (establecida en **false**).

Cuando esta opción de socket está habilitada en un socket IPv4 de tipo **sock \_ DGRAM** o **sock \_ raw**, la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelve información de paquetes en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) señalada por el parámetro *lpMsg* . Uno de los objetos de datos de control de la estructura **WSAMSG** devuelta contendrá una estructura [**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) que se usa para almacenar la información de dirección de paquetes recibida.

En el caso de los datagramas recibidos por la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) a través de IPv4, el miembro de **control** de la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recibida contendrá una estructura [**WSABUF utilizadas**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contiene una estructura **WSACMSGHDR** . El miembro de **\_ nivel cmsg** de esta estructura **WSACMSGHDR** contendría **IPPROTO \_ IP**, el miembro de **\_ tipo cmsg** de esta estructura contendría **\_ PKTINFO IP** y el miembro de **\_ datos Cmsg** contendría una estructura [**in \_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) utilizada para almacenar la información de dirección de paquetes IPv4 recibida. La dirección IPv4 en la estructura **de \_ pktinfo** es la dirección IPv4 desde la que se recibió el paquete.

En el caso de un socket de datagrama de pila doble, si una aplicación requiere la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) para devolver información de paquetes en una estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para los datagramas recibidos a través de IPv4, \_ la opción de socket de IP PKTINFO debe establecerse en true en el socket. Si solo la [opción \_ PKTINFO de IPv6](ipv6-pktinfo.md) está establecida en true en el socket, se proporcionará información de paquetes para los datagramas recibidos a través de IPv6, pero es posible que no se proporcionen para los datagramas recibidos a través de IPv4.

Si una aplicación intenta establecer la \_ opción de socket PKTINFO de IP en un socket de datagrama de pila doble e IPv4 está deshabilitado en el [](/windows/desktop/api/winsock/nf-winsock-setsockopt) sistema, se producirá un error en la función MUTE y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devolverá un error de [WSAEINVAL](windows-sockets-error-codes-2.md). Este mismo error **también lo devuelve la función** My como resultado de otros errores. Si una aplicación intenta establecer una \_ opción de socket de nivel IP de IPPROTO en un socket de doble pila y se produce un error con [WSAEINVAL](windows-sockets-error-codes-2.md), la aplicación debe determinar si IPv4 está deshabilitado en el equipo local. Un método que se puede usar para detectar si IPv4 está habilitado o deshabilitado es llamar a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con el parámetro *AF* establecido en AF \_ inet para probar y crear un socket IPv4. Si se produce un error en la función de **socket** y **WSAGetLastError** devuelve un error de [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), significa que IPv4 no está habilitado. En este caso, la aplicación puede pasar por alto **un error de la** función de r al intentar establecer la \_ opción de socket PKTINFO de IP. De lo contrario, un error al intentar establecer la \_ opción de socket PKTINFO de IP debe tratarse como un error inesperado.

Tenga en cuenta que el archivo de encabezado *Ws2ipdef. h* se incluye automáticamente en *Ws2tcpip. h* y nunca se debe usar directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Ws2ipdef. h (incluye Ws2tcpip. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sockets de doble pila](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**\_Opciones de socket IP IPPROTO**](ipproto-ip-socket-options.md)
</dt> <dt>

[\_PKTINFO IPv6](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**tomacorriente**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
