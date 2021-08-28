---
description: Está diseñado para permitir que una aplicación habilite paquetes de conexión continua para una conexión de socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: SO_KEEPALIVE de socket (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3590b8813f584aad16896a5b990baa2e3ad5607b76a13bd987d87961ee5f6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097475"
---
# <a name="so_keepalive-socket-option"></a>So \_ KEEPALIVE socket option

La **opción de socket SO \_ KEEPALIVE** está diseñada para permitir que una aplicación habilite paquetes keep-alive para una conexión de socket.

Para consultar el estado de esta opción de socket, llame a [**la función getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Para establecer esta opción, llame a la [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.

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

Descriptor que identifica el socket.

</dd> <dt>

*level* \[ En\]
</dt> <dd>

Nivel en el que se define la opción. Use **SOL \_ SOCKET para** esta operación.

</dd> <dt>

*optname* \[ En\]
</dt> <dd>

Opción de socket para la que se va a establecer el valor. Use **SO \_ KEEPALIVE** para esta operación.

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

Si la operación se completa correctamente, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) devuelve cero.

Si se produce un error en la operación, se devuelve un valor de SOCKET ERROR y se puede recuperar un código de error específico llamando \_ a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código de error                                                                                                                                              | Significado                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Debe [**producirse una llamada correcta a WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) antes de usar esta función.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Error en el subsistema de red.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno de los *parámetros optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario. Este error también se devuelve si el valor al que apunta el *parámetro optlen* es menor que el tamaño de **un valor DWORD.**<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Una llamada Windows sockets 1.1 está en curso o el proveedor de servicios sigue procesando una función de devolución de llamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | El *parámetro level* es desconocido o no es válido. En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La familia de protocolos indicada desconoce o no admite la opción. Este error se devuelve si el descriptor de socket pasado en el *parámetro s* era para un socket de datagrama.<br/>                                                                   |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

La [**función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket **SO \_ KEEPALIVE** permite a una aplicación recuperar el estado actual de la opción keepalive, aunque esta característica no se usa normalmente. Si una aplicación necesita habilitar paquetes keepalive en un socket, simplemente llama a la [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción.

La [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) llamada con la opción de socket **SO \_ KEEPALIVE** permite a una aplicación habilitar paquetes keep-alive para una conexión de socket. La **opción SO \_ KEEPALIVE** para un socket está deshabilitada (se establece en **FALSE)** de forma predeterminada.

Cuando esta opción de socket está habilitada, la pila TCP envía paquetes keep-alive cuando no se han recibido paquetes de confirmación o datos para la conexión dentro de un intervalo. Para obtener más información sobre la opción keep-alive, vea la sección 4.2.3.6 sobre los requisitos de los hosts de *Internet:* capas de comunicación especificadas en RFC 1122 disponible en el sitio web de [IETF](https://www.ietf.org/rfc/rfc1122.txt). (Este recurso solo puede estar disponible en inglés).

La opción de socket **\_ SO KEEPALIVE** solo es válida para los protocolos que admiten la noción de keep-alive (protocolos orientados a la conexión). Para TCP, el tiempo de espera de conexión continua predeterminado es de 2 horas y el intervalo de conexión continua es de 1 segundo. El número predeterminado de sondeos keep-alive varía en función de la versión de Windows.

El código de control [**\_ SIO KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) se puede usar para habilitar o deshabilitar la conexión continua, y ajustar el tiempo de espera y el intervalo para una sola conexión. Si keep-alive está habilitado con **SO \_ KEEPALIVE,** la configuración de TCP predeterminada se usa para el tiempo de espera y el intervalo de conexión continua, a menos que estos valores se hayan cambiado **mediante SIO \_ KEEPALIVE \_ VALS**.

El valor predeterminado para todo el sistema del tiempo de espera de conexión continua se puede controlar mediante la configuración del Registro [KeepAliveTime,](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) que toma un valor en milisegundos. El valor predeterminado para todo el sistema del intervalo de conexión continua se puede controlar mediante la configuración del Registro [KeepAliveInterval,](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) que toma un valor en milisegundos.

En Windows Vista y versiones posteriores, el número de sondeos de conexión continua (retransmisiones de datos) se establece en 10 y no se puede cambiar.

En Windows Server 2003, Windows XP y Windows 2000, la configuración predeterminada para el número de sondeos de conexión continua es 5. El número de sondeos keep-alive se puede controlar a través de la configuración del Registro [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) y [PPTPTcpMaxDataRetransmissions.](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) El número de sondeos de conexión continua se establece en el mayor de los dos valores de clave del Registro. Si este número es 0, los sondeos keep-alive no se enviarán. Si este número es superior a 255, se ajusta a 255.

En Windows Vista y versiones posteriores, la opción de socket **SO \_ KEEPALIVE** solo se puede establecer mediante la función [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) cuando el socket está en un estado conocido, no en un estado de transición. Para TCP, se debe establecer la opción de socket **SO \_ KEEPALIVE** antes de que se llame a la función connect [**(connect,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) [**ConnectEx,**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) [**WSAConnect,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName)**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)o después de que la solicitud de conexión se haya completado realmente. Si se llamó a la función connect de forma asincrónica, esto requiere esperar a la finalización de la conexión antes de intentar establecer la opción de socket **SO \_ KEEPALIVE.** Si una aplicación intenta establecer la opción de socket **SO \_ KEEPALIVE** cuando una solicitud de conexión todavía está en proceso, la función **setsockopt** producirá un error y devolverá [WSAEINVAL](windows-sockets-error-codes-2.md).

En Windows Server 2003, Windows XP y Windows 2000, la opción de socket **SO \_ KEEPALIVE** se puede establecer mediante la función [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) cuando el socket es un estado de transición (una solicitud de conexión todavía está en curso), así como un estado conocido.

Tenga en cuenta que el archivo de encabezado *Ws2def.h* se incluye automáticamente en *Winsock2.h* y nunca se debe usar directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Ws2def.h (incluye Winsock2.h)</dt> </dl> |



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

[**Zócalo**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
