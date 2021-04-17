---
description: Está diseñado para permitir que una aplicación decida si aceptar o no una conexión entrante en un socket de escucha.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Opción de socket de SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706828"
---
# <a name="so_conditional_accept-socket-option"></a>\_Opción de \_ socket de aceptación condicional

La opción de socket de **\_ \_ aceptación condicional** está diseñada para permitir que una aplicación decida si acepta o no una conexión entrante en un socket de escucha.

## <a name="socket-option-value"></a>Valor de opción de socket

La constante que representa esta opción de socket es 0x3002.

## <a name="syntax"></a>Sintaxis


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
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

Opción de socket para la que se va a establecer el valor. Use **la \_ \_ aceptación condicional** para esta operación.

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
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | El parámetro *LEVEL* es desconocido o no es válido. Este error también se devuelve si el socket ya estaba en un estado de escucha.<br/>                                                                                                                        |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La opción es desconocida o no es compatible con la familia del protocolo indicada.<br/>                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

La [**función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la función de la llamada con la opción de socket de **\_ \_ aceptación condicional** permite a una aplicación decidir si aceptar o no una conexión entrante en un socket de escucha. De forma predeterminada, la opción de aceptación condicional de un socket está deshabilitada (establecida en **false**).

Cuando se habilita esta opción de socket, la pila TCP no acepta conexiones automáticamente. Espera a que la aplicación indique que acepta la conexión a través de la devolución de llamada de aceptación condicional registrada con la función [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) . Una vez que se recibe una solicitud de conexión, Winsock invoca la devolución de llamada de aceptación condicional registrada por la aplicación. Solo si la devolución de llamada de aceptación condicional devuelve **CF \_ Accept** , Winsock notificará al transporte que acepte la conexión por completo.

Cuando la opción de socket de **\_ \_ aceptación condicional** está establecida en habilitado (establecido en **true**), esto tiene varios efectos secundarios en el socket:

-   Esto deshabilita las defensas integradas de protección contra ataques SYN de la pila TCP, ya que la aplicación ahora toma la propiedad de aceptar conexiones.
-   De este modo, se deshabilita el trabajo pendiente de escucha, ya que no se aceptan conexiones en nombre de un socket de escucha. Una conexión nunca se acepta por completo hasta que la aplicación acepta por completo el uso del mecanismo de **\_ aceptación de CF** .
-   Esto también significa que la aplicación se encarga de estar siempre en un estado para controlar fácilmente las devoluciones de llamada de aceptación para aceptar la conexión. Si la aplicación está ocupada en otro procesamiento, el cliente puede agotar el tiempo de espera antes de que la aplicación acepte realmente la conexión. Esto conduce a una experiencia de cliente deficiente.

Por lo general, el motivo principal por el que las aplicaciones usan la aceptación condicional es inspeccionar la dirección IP de origen o el puerto utilizado por el cliente que se conecta y, a continuación, decidir si aceptar o rechazar la conexión. Sin embargo, es probable que las aplicaciones funcionen mejor si la \_ \_ opción de aceptación condicional no está habilitada y la aplicación permite que la pila TCP y el trabajo pendiente de escucha funcionen según lo previsto. Después, cuando la aplicación controla la conexión aceptada, si se trata de un puerto o una dirección de origen IP incorrectos, la aplicación solo puede cerrar el socket. El inconveniente de seguridad de este comportamiento es que ahora el cliente ha confirmado que la aplicación está escuchando en una dirección IP y un puerto, ya que ha cerrado forzosamente la conexión previamente aceptada. Sin embargo, las desventajas de habilitar la **\_ \_ aceptación condicional** generalmente superan esta limitación.

La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket de **\_ \_ aceptación condicional** permite a una aplicación recuperar el estado actual de la opción de aceptación condicional, aunque esta característica no se utiliza normalmente. Si una aplicación necesita habilitar la aceptación condicional en un socket, simplemente llama a [**la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la función de llamada para habilitar la opción.

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

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




