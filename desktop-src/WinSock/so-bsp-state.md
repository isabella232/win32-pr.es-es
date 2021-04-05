---
description: Devuelve la dirección local, el puerto local, la dirección remota, el puerto remoto, el tipo de socket y el protocolo utilizado por un socket.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Opción de socket de SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812445"
---
# <a name="so_bsp_state-socket-option"></a>\_Opción de \_ socket de estado BSP

La opción de socket de **\_ \_ Estado de BSP** devuelve la dirección local, el puerto local, la dirección remota, el puerto remoto, el tipo de socket y el protocolo que usa un socket.

Para realizar esta operación, llame a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con los parámetros siguientes.

## <a name="socket-option-value"></a>Valor de opción de socket

La constante que representa esta opción de socket es 0x1009.

## <a name="syntax"></a>Sintaxis


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
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

Nivel en el que se define la opción. Use **el \_ socket sol** para esta operación.

</dd> <dt>

*optname* \[ de\]
</dt> <dd>

Opción de socket para la que se va a recuperar el valor. Use **el \_ \_ Estado de BSP** para esta operación.

</dd> <dt>

*optval* \[ enuncia\]
</dt> <dd>

Puntero al búfer en el que se va a devolver el valor de la opción solicitada. Este parámetro debe apuntar al búfer igual o mayor que el tamaño de una estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Puntero al tamaño, en bytes, del búfer *optval* . Este tamaño debe ser igual o mayor que el tamaño de una estructura [**de \_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) devuelve cero.

Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código de error                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Error en el subsistema de red.<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario. Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de una estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.<br/>                                                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | El parámetro *LEVEL* es desconocido o no es válido.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La opción es desconocida o no es compatible con la familia del protocolo indicada.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket de **\_ \_ Estado de BSP** recupera la dirección local, el puerto local, la dirección remota, el puerto remoto, el tipo de socket y el protocolo que usa un socket. La opción de socket de **\_ \_ Estado de BSP** funciona con sockets IPv6 o IPv4 (las familias de direcciones **AF \_ inet6** y **AF \_ inet** ).

Si la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) se ejecuta correctamente, la información se devuelve en una estructura [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) en el búfer al que apunta el parámetro *optval* . El entero al que apunta *optlen* debe contener originalmente el tamaño de este búfer; en la devolución, se establecerá en la longitud, en bytes, del valor devuelto en el parámetro *optval* .

Los miembros **iSocketType** y **iProtocol** de la estructura [**de \_ información CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) devuelta se rellenan para el descriptor de socket en el parámetro *s* .

Si el socket está en estado conectado o enlazado, el miembro **LocalAddr** de la estructura devuelta [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) se establecerá en una estructura [SOCKADDR](sockaddr-2.md) que represente la dirección local y el puerto. Si el socket está en estado conectado, el miembro **RemoteAddr** de la estructura de **\_ información de CSADDR** devuelta se establecerá en una estructura SOCKADDR que represente la dirección remota y el puerto.

Si el socket no está en estado conectado o enlazado, se devuelve el miembro **LocalAddr** de la estructura de [**\_ información CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) devuelta con un puntero **nulo** en el miembro **lpSockaddr** y el miembro **iSockaddrLength** establecido en cero. Si el socket no está en un estado enlazado, se devuelve el miembro **RemoteAddr** de la estructura de **\_ información CSADDR** devuelta con un puntero **nulo** en el miembro **lpSockaddr** y el miembro **iSockaddrLength** establecido en cero.

Si se produce un error en la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , los parámetros *optval* y *optlen* se dejan sin cambios y el parámetro *optval* no apunta a una estructura de [**\_ información CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) devuelta.

Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Ws2def. h (incluir WinSock2. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**información de CSADDR \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 
