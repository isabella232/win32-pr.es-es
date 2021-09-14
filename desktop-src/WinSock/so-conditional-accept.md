---
description: Está diseñado para permitir que una aplicación decida si acepta o no una conexión entrante en un socket de escucha.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: SO_CONDITIONAL_ACCEPT de socket (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359112"
---
# <a name="so_conditional_accept-socket-option"></a>Opción de socket SO \_ CONDITIONAL \_ ACCEPT

La opción de socket **SO \_ CONDITIONAL \_ ACCEPT** está diseñada para permitir que una aplicación decida si acepta o no una conexión entrante en un socket de escucha.

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

Descriptor que identifica el socket.

</dd> <dt>

*level* \[ En\]
</dt> <dd>

Nivel en el que se define la opción. Use **SOL \_ SOCKET para** esta operación.

</dd> <dt>

*optname* \[ En\]
</dt> <dd>

Opción de socket para la que se va a establecer el valor. Use **SO CONDITIONAL ACCEPT \_ \_ para** esta operación.

</dd> <dt>

*optval* \[ out\]
</dt> <dd>

Puntero al búfer que contiene el valor de la opción que se establece. Este parámetro debe apuntar a un búfer igual o mayor que el tamaño de un **valor DWORD.**

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
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno de los *parámetros optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario. Este error también se devuelve si el valor al que apunta el *parámetro optlen* es menor que el tamaño de un **valor DWORD.**<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Una llamada Windows sockets 1.1 está en curso o el proveedor de servicios sigue procesando una función de devolución de llamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | El *parámetro level* es desconocido o no es válido. Este error también se devuelve si el socket ya estaba en estado de escucha.<br/>                                                                                                                        |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | La familia de protocolos indicada desconoce o no admite la opción.<br/>                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | El descriptor no es un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

La [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) llamada con la opción de socket **SO CONDITIONAL \_ \_ ACCEPT** permite a una aplicación decidir si acepta o no una conexión entrante en un socket de escucha. La opción de aceptación condicional para un socket está deshabilitada (establecida en **FALSE)** de forma predeterminada.

Cuando esta opción de socket está habilitada, la pila TCP no acepta automáticamente las conexiones. Espera a que la aplicación indique que acepta la conexión a través de la devolución de llamada de aceptación condicional registrada con la [**función WSAAccept.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) Una vez recibida una solicitud de conexión, Winsock invoca la devolución de llamada de aceptación condicional registrada por la aplicación. Solo cuando la devolución de llamada de aceptación condicional devuelva **CF \_ ACCEPT,** Winsock notificará al transporte que acepte completamente la conexión.

Cuando la opción de socket **SO \_ CONDITIONAL \_ ACCEPT** está establecida en enabled (se establece en **TRUE),** esto tiene varios efectos secundarios en el socket:

-   Esto deshabilita las defensas de protección contra ataques SYN integradas de la pila TCP, ya que la aplicación ahora toma posesión de la aceptación de conexiones.
-   Esto deshabilita eficazmente el trabajo pendiente de escucha, ya que las conexiones no se aceptan en nombre de un socket de escucha. Una conexión nunca se acepta por completo hasta que la aplicación acepta completamente mediante el **mecanismo CF \_ ACCEPT.**
-   Esto también significa que la aplicación se encarga de estar siempre en un estado para controlar fácilmente las devoluciones de llamada de aceptación para aceptar la conexión. Si la aplicación está ocupada realizando otro procesamiento, el lado cliente puede tiempo de espera antes de que la aplicación acepte realmente la conexión. Esto conduce a una experiencia de cliente deficiente.

Por lo general, la razón principal por la que las aplicaciones usan la aceptación condicional es inspeccionar la dirección IP de origen o el puerto usado por el cliente que se conecta y, a continuación, decidir aceptar o rechazar la conexión. Sin embargo, es probable que las aplicaciones funcionen mejor si la opción SO CONDITIONAL ACCEPT no está habilitada y la aplicación permite que la pila TCP y el trabajo pendiente de escucha funcionen según \_ \_ lo previsto. A continuación, cuando la aplicación controla la conexión aceptada, si se trata de una dirección o puerto de origen IP incorrectos, la aplicación solo puede cerrar el socket. El inconveniente de seguridad de este comportamiento es que ahora el cliente tiene la confirmación de que la aplicación está escuchando en una dirección IP y un puerto, ya que cerró por la fuerza la conexión aceptada anteriormente. Sin embargo, los inconvenientes de habilitar **SO \_ CONDITIONAL \_ ACCEPT** suelen superar esta limitación.

La [**función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket **SO CONDITIONAL \_ \_ ACCEPT** permite a una aplicación recuperar el estado actual de la opción de aceptación condicional, aunque esta característica no se usa normalmente. Si una aplicación necesita habilitar la aceptación condicional en un socket, simplemente llama a la [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción.

Tenga en cuenta que el archivo de encabezado *Ws2def.h* se incluye automáticamente en *Winsock2.h* y nunca se debe usar directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Ws2def.h (incluye Winsock2.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




