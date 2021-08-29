---
description: Especifica un descriptor de cola de finalización que se usa para la notificación de finalización de E/S mediante el envío y recepción de solicitudes con las extensiones de E/S registradas de Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86aac301dbf9bc9432b3f6a686e69e521be017d0ab775ba9f7deb3bc1a4b29a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121225"
---
# <a name="rio_cq"></a>RIO \_ CQ

La definición de **\_ tipo CQ** de RIO especifica un descriptor de cola de finalización que se usa para la notificación de finalización de E/S mediante el envío y recepción de solicitudes con las extensiones de E/S registradas en Winsock.


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

**RIO \_ CQ**
</dt> <dd>

Tipo de datos que especifica un descriptor de cola de finalización utilizado para la notificación de finalización de E/S mediante solicitudes de envío y recepción.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **objeto RIO \_ CQ** se usa para la notificación de finalización de E/S de envío y recepción de solicitudes de red por parte de las extensiones de E/S registradas de Winsock.

Una aplicación puede usar la [**función RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) para solicitar una notificación cuando una cola de finalización **\_ CQ** de RIO no está vacía. Una aplicación también puede sondear el estado en cualquier momento de una cola de finalización **\_ CQ de RIO** de forma sin bloqueo mediante la [**función RIODequeueCompletion.**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)

El **objeto \_ CQ de RIO** se crea mediante la función [**RIOCreateCompletionQueue.**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) En el momento de la creación, la aplicación debe especificar el tamaño de la cola, que determina cuántas entradas de finalización puede contener. Cuando una aplicación llama a la [**función RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) para obtener un identificador [**\_ RQ de RIO,**](riorqueue.md) la aplicación debe especificar un identificador **\_ CQ** de RIO para las finalizaciones de envío y un identificador **\_ CQ** de RIO para las finalizaciones de recepción. Estos identificadores pueden ser idénticos cuando se debe usar la misma cola para la finalización de envío y recepción. La **función RIOCreateRequestQueue** también requiere un número máximo de operaciones de envío y recepción pendientes, que se cobran en función de la capacidad de las colas o colas de finalización asociadas. Si las colas no tienen capacidad suficiente restante, se producirá un error en la llamada **a RIOCreateRequestQueue** con [WSAENOBUFS](windows-sockets-error-codes-2.md).

El comportamiento de notificación de una cola de finalización se establece cuando se crea **el \_ CQ de RIO.**

Para una cola de finalización que usa un evento , el miembro **Type** de la [**estructura DE FINALIZACIÓN DE NOTIFICACIÓN \_ \_ DE RIO**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) se establece en FINALIZACIÓN DE EVENTOS DE **\_ \_ RIO**. El **miembro Event.EventHandle** debe contener el identificador de un evento creado por la [**función WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) [**o CreateEvent.**](/windows/win32/api/synchapi/nf-synchapi-createeventa) Para recibir la [**finalización de RIONotify,**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) la aplicación debe esperar en el identificador de evento especificado mediante [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o una rutina de espera similar. Si la aplicación planea restablecer y reutilizar el evento, la aplicación puede reducir la sobrecarga estableciendo el **miembro Event.NotifyReset** en un valor distinto de cero. Esto hace que la función **RIONotify** restablezca automáticamente el evento cuando se produzca la notificación. Esto mitiga la necesidad de llamar a la función [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) para restablecer el evento entre llamadas a la **función RIONotify.**

En el caso de una cola de finalización que usa un puerto de finalización de E/S, el miembro **Type** de la estructura DE FINALIZACIÓN DE NOTIFICACIÓN [**\_ \_ DE RIO**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) se establece en **RIO \_ IOCP \_ COMPLETION**. El **miembro Iocp.IocpHandle** debe contener el identificador de un puerto de finalización de E/S creado por la [**función CreateIoCompletionPort.**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) Para recibir la [**finalización de RIONotify,**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) la aplicación debe llamar a las funciones [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) La aplicación debe proporcionar un objeto [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dedicado para la cola de finalización y también puede usar el miembro **Iocp.CompletionKey** para distinguir las solicitudes **DE RIONotify** en la cola de finalización de otras finalizaciones de E/S, incluidas las finalizaciones **de RIONotify** para otras colas de finalización.

> [!Note]  
> Por motivos de eficiencia, el acceso a las colas de finalización (estructuras **\_ CQ** de RIO) y las colas de solicitud (estructuras [**\_ RQ**](riorqueue.md) de RIO) no están protegidas por primitivos de sincronización. Si necesita acceder a una cola de finalización o solicitud desde varios subprocesos, el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritura de lector más fino o un mecanismo similar. Este bloqueo no es necesario para el acceso de un único subproceso. Los distintos subprocesos pueden acceder a solicitudes o colas de finalización independientes sin bloqueos. La necesidad de sincronización solo se produce cuando varios subprocesos intentan acceder a la misma cola. También es necesaria la sincronización si varios subprocesos emiten envíos y recepción en el mismo socket porque las operaciones de envío y recepción usan la cola de solicitudes del socket.

 

Si varios subprocesos intentan tener acceso a la misma **\_ CQ de RIO** mediante [**RIODequeueCompletion,**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritor de lectores finos o un mecanismo de exclusión mutua similar. Si no se comparten las colas de finalización, no se requiere la exclusión mutua.

Cuando ya no se necesita una cola de finalización, una aplicación puede cerrarla mediante la [**función RIOCloseCompletionQueue.**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))

La **\_ definición** de tipo CQ de RIO se define en el archivo de encabezado *Mswsockdef.h* que se incluye automáticamente en el archivo de encabezado *Mswsock.h.* El *archivo de encabezado Mswsockdef.h* nunca debe usarse directamente.

## <a name="thread-safety"></a>Seguridad para subprocesos

Si varios subprocesos intentan tener acceso a la misma **\_ CQ de RIO** mediante [**RIODequeueCompletion,**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritor de lectores finos o un mecanismo de exclusión mutua similar. Si no se comparten las colas de finalización, no se requiere la exclusión mutua.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mswsockdef.h (incluya Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[**Comprometidos**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[**FINALIZACIÓN \_ DE NOTIFICACIONES DE \_ RIO**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[**TIPO \_ DE FINALIZACIÓN DE NOTIFICACIÓN DE \_ \_ RIO**](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[**RIO \_ RQ**](riorqueue.md)
</dt> <dt>

[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))
</dt> <dt>

[**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
