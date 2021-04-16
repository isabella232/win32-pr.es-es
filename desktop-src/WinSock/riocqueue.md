---
description: Especifica un descriptor de cola de finalización que se usa para la notificación de finalización de e/s mediante solicitudes de envío y recepción con las extensiones de e/s registradas de Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706187"
---
# <a name="rio_cq"></a>Río \_ CQ

La definición de tipo **Rio \_ CQ** especifica un descriptor de cola de finalización que se usa para la notificación de finalización de e/s mediante solicitudes de envío y recepción con las extensiones de e/s registradas de Winsock.


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

**Río \_ CQ**
</dt> <dd>

Un tipo de datos que especifica un descriptor de cola de finalización utilizado para la notificación de finalización de e/s mediante solicitudes de envío y recepción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto **Rio \_ CQ** se usa para la notificación de finalización de e/s de las solicitudes de red de envío y recepción de las extensiones de e/s registradas de Winsock.

Una aplicación puede usar la función [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) para solicitar una notificación cuando una cola de finalización de **Rio \_ CQ** no esté vacía. Una aplicación también puede sondear el estado en cualquier momento de una cola de finalización de **Rio \_ CQ** sin bloqueo mediante la función [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .

El objeto **Rio \_ CQ** se crea mediante la función [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) . En el momento de la creación, la aplicación debe especificar el tamaño de la cola, que determina el número de entradas de finalización que puede contener. Cuando una aplicación llama a la función [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) para obtener un identificador de [**Rio \_ PET**](riorqueue.md) , la aplicación debe especificar un identificador de **río \_ CQ** para las finalizaciones de envío y un identificador de **Rio \_ CQ** para las finalizaciones de recepción. Estos identificadores pueden ser idénticos cuando se debe utilizar la misma cola para la finalización de envío y recepción. La función **RIOCreateRequestQueue** también requiere un número máximo de operaciones de envío y recepción pendientes, que se cobran por la capacidad de la cola o colas de finalización asociadas. Si las colas no tienen suficiente capacidad restante, se producirá un error en la llamada **RIOCreateRequestQueue** con [WSAENOBUFS](windows-sockets-error-codes-2.md).

El comportamiento de notificación de una cola de finalización se establece cuando se crea el **río \_ CQ** .

En el caso de una cola de finalización que utiliza un evento, el miembro de **tipo** de la estructura de [**\_ \_ finalización de notificaciones del río**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) se establece en la **\_ \_ finalización del evento** de Rio. El miembro **Event. EventHandle** debe contener el identificador de un evento creado por la función [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) o [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) . Para recibir la finalización de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , la aplicación debe esperar en el identificador de eventos especificado mediante [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o una rutina de espera similar. Si la aplicación planea restablecer y reutilizar el evento, la aplicación puede reducir la sobrecarga estableciendo el miembro **Event. NotifyReset** en un valor distinto de cero. Esto hace que la función **RIONotify** restablezca automáticamente el evento cuando se produce la notificación. Esto reduce la necesidad de llamar a la función [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) para restablecer el evento entre las llamadas a la función **RIONotify** .

En el caso de una cola de finalización que usa un puerto de finalización de e/s, el miembro de **tipo** de la estructura de [**\_ \_ finalización de notificaciones del río**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) se establece en **río \_ IOCP \_ finalización**. El miembro **IOCP. IocpHandle** debe contener el identificador de un puerto de finalización de e/s creado por la función [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) . Para recibir la finalización de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , la aplicación debe llamar a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) . La aplicación debe proporcionar un objeto [**SUPERpuesto**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dedicado para la cola de finalización y también puede usar el miembro **IOCP. CompletionKey** para distinguir las solicitudes **RIONotify** en la cola de finalización de otras finalizaciones de e/s, incluidas las finalizaciones de **RIONotify** para otras colas de finalización.

> [!Note]  
> Por motivos de eficacia, el acceso a las colas de finalización (estructuras **\_ CQ de Rio** ) y a las colas de solicitudes (Structs [**\_ PET**](riorqueue.md) ) no están protegidos por primitivas de sincronización. Si necesita tener acceso a una cola de finalización o solicitud desde varios subprocesos, el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritura de lector fino o un mecanismo similar. Este bloqueo no es necesario para el acceso a un único subproceso. Distintos subprocesos pueden tener acceso a solicitudes o colas de finalización independientes sin bloqueos. La necesidad de sincronización solo se produce cuando varios subprocesos intentan obtener acceso a la misma cola. La sincronización también es necesaria si varios subprocesos emiten y reciben en el mismo socket porque las operaciones de envío y recepción utilizan la cola de solicitudes del socket.

 

Si varios subprocesos intentan acceder al mismo **río \_ CQ** mediante [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritor de lector fino o un mecanismo de exclusión mutua similar. Si las colas de finalización no están compartidas, no se requiere la exclusión mutua.

Cuando ya no se necesita una cola de finalización, una aplicación puede cerrarla con la función [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .

La definición de tipo de **Rio \_ CQ** se define en el archivo de encabezado *Mswsockdef. h* que se incluye automáticamente en el archivo de encabezado *mswsock. h* . El archivo de encabezado *Mswsockdef. h* nunca debe usarse directamente.

## <a name="thread-safety"></a>Seguridad para subprocesos

Si varios subprocesos intentan acceder al mismo **río \_ CQ** mediante [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritor de lector fino o un mecanismo de exclusión mutua similar. Si las colas de finalización no están compartidas, no se requiere la exclusión mutua.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Mswsockdef. h (incluye mswsock. h)</dt> </dl> |



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

[**SUPERPUESTA**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[**finalización de la notificación de RIO \_ \_**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[**\_tipo de \_ finalización de notificación de Rio \_**](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[**Río \_ PET**](riorqueue.md)
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

 

 
