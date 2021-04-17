---
description: Está diseñado para permitir que una aplicación habilite los paquetes Keep-Alive para una conexión de socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Opción de socket de SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706827"
---
# <a name="so_keepalive-socket-option"></a>\_Opción de socket KEEPALIVE

La opción de socket **so \_ KEEPALIVE** está diseñada para permitir que una aplicación habilite los paquetes Keep-Alive para una conexión de socket.

Para consultar el estado de esta opción de socket, llame a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Para establecer esta opción, llame a [**la función del método de llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.

## <a name="socket-option-value"></a>Valor de opción de socket

La constante que representa esta opción de socket es 0x0008.

## <a name="syntax"></a>Sintaxis


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
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

Nivel en el que se define la opción. Use **el \_ socket sol** para esta operación.

</dd> <dt>

*optname* \[ de\]
</dt> <dd>

Opción de socket para la que se va a establecer el valor. Úselo **para \_** esta operación.

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

Si la operación se completa [**correctamente, el valor de la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) función devuelve cero.

Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código de error                                                                                                                                              | Significado                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Error en el subsistema de red.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario. Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de un valor **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | El parámetro *LEVEL* es desconocido o no es válido. En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La opción es desconocida o no es compatible con la familia del protocolo indicada. Se devuelve este error si el descriptor de socket pasado en el parámetro *s* era para un socket de datagramas.<br/>                                                                   |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket **so \_ KEEPALIVE** permite que una aplicación recupere el estado actual de la opción keepalive, aunque esta característica no se utiliza normalmente. Si una aplicación necesita habilitar paquetes keepalive en un socket, simplemente llama a la función de la [**función de llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción.

La [**función que**](/windows/desktop/api/winsock/nf-winsock-setsockopt) se llama con la opción de socket **so \_ KEEPALIVE** permite que una aplicación habilite los paquetes Keep-Alive para una conexión de socket. De forma predeterminada, la opción de **\_ KEEPALIVE** para un socket está deshabilitada (establecida en **false**).

Cuando esta opción de socket está habilitada, la pila TCP envía paquetes Keep-Alive cuando no se ha recibido ningún paquete de datos o de confirmación para la conexión dentro de un intervalo. Para obtener más información acerca de la opción Keep-Alive, consulte la sección 4.2.3.6 sobre los *requisitos de los hosts de Internet: las capas de comunicación* especificadas en RFC 1122 están disponibles en el [sitio web de IETF](https://www.ietf.org/rfc/rfc1122.txt). (Este recurso solo está disponible en inglés).

La opción de socket **so \_ KEEPALIVE** solo es válida para los protocolos que admiten la noción de Keep-Alive (protocolos orientados a la conexión). Para TCP, el tiempo de espera de mantenimiento de conexión predeterminado es de 2 horas y el intervalo de mantenimiento de conexión es de 1 segundo. El número predeterminado de sondeos Keep-Alive varía en función de la versión de Windows.

El código de control [**SiO \_ KEEPALIVE \_ vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) se puede usar para habilitar o deshabilitar Keep-Alive, y ajustar el tiempo de espera y el intervalo para una única conexión. Si Keep-Alive está habilitado con la opción **\_ KeepAlive**, se usará la configuración predeterminada de TCP para el tiempo de espera y el intervalo de mantenimiento de conexión, a menos que estos valores se hayan cambiado mediante **SiO \_ KEEPALIVE \_ vals**.

El valor predeterminado para todo el sistema del tiempo de espera de mantenimiento de conexión se controla mediante la configuración del registro [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) , que toma un valor en milisegundos. El valor predeterminado para todo el sistema del intervalo Keep-Alive se controla a través de la configuración del registro [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que toma un valor en milisegundos.

En Windows Vista y versiones posteriores, el número de sondeos Keep-Alive (retransmisiones de datos) se establece en 10 y no se puede cambiar.

En Windows Server 2003, Windows XP y Windows 2000, la configuración predeterminada para el número de sondeos Keep-Alive es 5. El número de sondeos Keep-Alive se controla a través de la configuración del registro [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) y [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) . El número de sondeos Keep-Alive se establece en el mayor de los dos valores de clave del registro. Si este número es 0, no se enviarán sondeos Keep-Alive. Si este número es superior a 255, se ajusta a 255.

En Windows Vista y versiones posteriores, la opción de socket **so \_ KEEPALIVE** solo se puede establecer con la función de llamada a la función [**de la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) del socket en un estado conocido, no un estado de transición. Para TCP, la opción de socket **so \_ KEEPALIVE** debe establecerse antes de que se llame a la función Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)), o después de que se haya completado la solicitud de conexión. Si se llamó a la función de conexión de forma asincrónica, esto requiere esperar la finalización de la conexión antes de intentar establecer la opción de socket **so \_ KEEPALIVE** . Si una aplicación intenta establecer la opción de socket **so \_ KEEPALIVE** cuando una solicitud de conexión todavía está en curso, se producirá un error **en la función** MUTE y se devolverá [WSAEINVAL](windows-sockets-error-codes-2.md).

En Windows Server 2003, Windows XP y Windows 2000, la opción de socket **so \_ KEEPALIVE** se puede establecer con la [**función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) llamada a la función de-r cuando el socket es un estado de transición (una solicitud de conexión todavía está en curso) y un estado conocido.

Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Ws2def. h (incluir WinSock2. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))
</dt> <dt>

[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))
</dt> <dt>

[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**tomacorriente**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KEEPALIVE \_ vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
