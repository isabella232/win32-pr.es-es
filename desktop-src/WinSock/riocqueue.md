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
# <a name="rio_cq"></a><span data-ttu-id="056be-103">Río \_ CQ</span><span class="sxs-lookup"><span data-stu-id="056be-103">RIO\_CQ</span></span>

<span data-ttu-id="056be-104">La definición de tipo **Rio \_ CQ** especifica un descriptor de cola de finalización que se usa para la notificación de finalización de e/s mediante solicitudes de envío y recepción con las extensiones de e/s registradas de Winsock.</span><span class="sxs-lookup"><span data-stu-id="056be-104">The **RIO\_CQ** typedef specifies a completion queue descriptor used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

<span data-ttu-id="056be-105">**Río \_ CQ**</span><span class="sxs-lookup"><span data-stu-id="056be-105">**RIO\_CQ**</span></span>
</dt> <dd>

<span data-ttu-id="056be-106">Un tipo de datos que especifica un descriptor de cola de finalización utilizado para la notificación de finalización de e/s mediante solicitudes de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="056be-106">A data type that specifies a completion queue descriptor used for I/O completion notification by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="056be-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="056be-107">Remarks</span></span>

<span data-ttu-id="056be-108">El objeto **Rio \_ CQ** se usa para la notificación de finalización de e/s de las solicitudes de red de envío y recepción de las extensiones de e/s registradas de Winsock.</span><span class="sxs-lookup"><span data-stu-id="056be-108">The **RIO\_CQ** object is used for I/O completion notification of send and receive networking requests by the Winsock registered I/O extensions.</span></span>

<span data-ttu-id="056be-109">Una aplicación puede usar la función [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) para solicitar una notificación cuando una cola de finalización de **Rio \_ CQ** no esté vacía.</span><span class="sxs-lookup"><span data-stu-id="056be-109">An application can use the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function to request notification when a **RIO\_CQ** completion queue is not empty.</span></span> <span data-ttu-id="056be-110">Una aplicación también puede sondear el estado en cualquier momento de una cola de finalización de **Rio \_ CQ** sin bloqueo mediante la función [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="056be-110">An application can also poll the status at any time of a **RIO\_CQ** completion queue in a non-blocking way using the [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span>

<span data-ttu-id="056be-111">El objeto **Rio \_ CQ** se crea mediante la función [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="056be-111">The **RIO\_CQ** object is created using the [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span> <span data-ttu-id="056be-112">En el momento de la creación, la aplicación debe especificar el tamaño de la cola, que determina el número de entradas de finalización que puede contener.</span><span class="sxs-lookup"><span data-stu-id="056be-112">At creation time, the application must specify the size of the queue, which determines how many completion entries it can hold.</span></span> <span data-ttu-id="056be-113">Cuando una aplicación llama a la función [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) para obtener un identificador de [**Rio \_ PET**](riorqueue.md) , la aplicación debe especificar un identificador de **río \_ CQ** para las finalizaciones de envío y un identificador de **Rio \_ CQ** para las finalizaciones de recepción.</span><span class="sxs-lookup"><span data-stu-id="056be-113">When an application calls the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function to obtain a [**RIO\_RQ**](riorqueue.md) handle, the application must specify a **RIO\_CQ** handle for send completions and a **RIO\_CQ** handle for receive completions.</span></span> <span data-ttu-id="056be-114">Estos identificadores pueden ser idénticos cuando se debe utilizar la misma cola para la finalización de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="056be-114">These handles may be identical when the same queue should be used for send and receive completion.</span></span> <span data-ttu-id="056be-115">La función **RIOCreateRequestQueue** también requiere un número máximo de operaciones de envío y recepción pendientes, que se cobran por la capacidad de la cola o colas de finalización asociadas.</span><span class="sxs-lookup"><span data-stu-id="056be-115">The **RIOCreateRequestQueue** function also requires a maximum number of outstanding send and receive operations, which are charged against the capacity of the associated completion queue or queues.</span></span> <span data-ttu-id="056be-116">Si las colas no tienen suficiente capacidad restante, se producirá un error en la llamada **RIOCreateRequestQueue** con [WSAENOBUFS](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="056be-116">If the queues do not have sufficient capacity remaining, the **RIOCreateRequestQueue** call will fail with [WSAENOBUFS](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="056be-117">El comportamiento de notificación de una cola de finalización se establece cuando se crea el **río \_ CQ** .</span><span class="sxs-lookup"><span data-stu-id="056be-117">The notification behavior for a completion queue is set when the **RIO\_CQ** is created.</span></span>

<span data-ttu-id="056be-118">En el caso de una cola de finalización que utiliza un evento, el miembro de **tipo** de la estructura de [**\_ \_ finalización de notificaciones del río**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) se establece en la **\_ \_ finalización del evento** de Rio.</span><span class="sxs-lookup"><span data-stu-id="056be-118">For a completion queue that uses an event, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_EVENT\_COMPLETION**.</span></span> <span data-ttu-id="056be-119">El miembro **Event. EventHandle** debe contener el identificador de un evento creado por la función [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) o [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .</span><span class="sxs-lookup"><span data-stu-id="056be-119">The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) or [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function.</span></span> <span data-ttu-id="056be-120">Para recibir la finalización de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , la aplicación debe esperar en el identificador de eventos especificado mediante [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o una rutina de espera similar.</span><span class="sxs-lookup"><span data-stu-id="056be-120">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or a similar wait routine.</span></span> <span data-ttu-id="056be-121">Si la aplicación planea restablecer y reutilizar el evento, la aplicación puede reducir la sobrecarga estableciendo el miembro **Event. NotifyReset** en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="056be-121">If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value.</span></span> <span data-ttu-id="056be-122">Esto hace que la función **RIONotify** restablezca automáticamente el evento cuando se produce la notificación.</span><span class="sxs-lookup"><span data-stu-id="056be-122">This causes the event to be automatically reset by the **RIONotify** function when the notification occurs.</span></span> <span data-ttu-id="056be-123">Esto reduce la necesidad de llamar a la función [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) para restablecer el evento entre las llamadas a la función **RIONotify** .</span><span class="sxs-lookup"><span data-stu-id="056be-123">This mitigates the need to call the [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) function to reset the event between calls to the **RIONotify** function.</span></span>

<span data-ttu-id="056be-124">En el caso de una cola de finalización que usa un puerto de finalización de e/s, el miembro de **tipo** de la estructura de [**\_ \_ finalización de notificaciones del río**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) se establece en **río \_ IOCP \_ finalización**.</span><span class="sxs-lookup"><span data-stu-id="056be-124">For a completion queue that uses an I/O completion port, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_IOCP\_COMPLETION**.</span></span> <span data-ttu-id="056be-125">El miembro **IOCP. IocpHandle** debe contener el identificador de un puerto de finalización de e/s creado por la función [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) .</span><span class="sxs-lookup"><span data-stu-id="056be-125">The **Iocp.IocpHandle** member should contain the handle for an I/O completion port created by the [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) function.</span></span> <span data-ttu-id="056be-126">Para recibir la finalización de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , la aplicación debe llamar a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) .</span><span class="sxs-lookup"><span data-stu-id="056be-126">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should call the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) function.</span></span> <span data-ttu-id="056be-127">La aplicación debe proporcionar un objeto [**SUPERpuesto**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dedicado para la cola de finalización y también puede usar el miembro **IOCP. CompletionKey** para distinguir las solicitudes **RIONotify** en la cola de finalización de otras finalizaciones de e/s, incluidas las finalizaciones de **RIONotify** para otras colas de finalización.</span><span class="sxs-lookup"><span data-stu-id="056be-127">The application should provide a dedicated [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) object for the completion queue, and it may also use the **Iocp.CompletionKey** member to distinguish **RIONotify** requests on the completion queue from other I/O completions including **RIONotify** completions for other completion queues.</span></span>

> [!Note]  
> <span data-ttu-id="056be-128">Por motivos de eficacia, el acceso a las colas de finalización (estructuras **\_ CQ de Rio** ) y a las colas de solicitudes (Structs [**\_ PET**](riorqueue.md) ) no están protegidos por primitivas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="056be-128">For purposes of efficiency, access to the completion queues (**RIO\_CQ** structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="056be-129">Si necesita tener acceso a una cola de finalización o solicitud desde varios subprocesos, el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritura de lector fino o un mecanismo similar.</span><span class="sxs-lookup"><span data-stu-id="056be-129">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="056be-130">Este bloqueo no es necesario para el acceso a un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="056be-130">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="056be-131">Distintos subprocesos pueden tener acceso a solicitudes o colas de finalización independientes sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="056be-131">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="056be-132">La necesidad de sincronización solo se produce cuando varios subprocesos intentan obtener acceso a la misma cola.</span><span class="sxs-lookup"><span data-stu-id="056be-132">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="056be-133">La sincronización también es necesaria si varios subprocesos emiten y reciben en el mismo socket porque las operaciones de envío y recepción utilizan la cola de solicitudes del socket.</span><span class="sxs-lookup"><span data-stu-id="056be-133">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="056be-134">Si varios subprocesos intentan acceder al mismo **río \_ CQ** mediante [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritor de lector fino o un mecanismo de exclusión mutua similar.</span><span class="sxs-lookup"><span data-stu-id="056be-134">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="056be-135">Si las colas de finalización no están compartidas, no se requiere la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="056be-135">If the completion queues are not shared, mutual exclusion is not required.</span></span>

<span data-ttu-id="056be-136">Cuando ya no se necesita una cola de finalización, una aplicación puede cerrarla con la función [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="056be-136">When a completion queue is no longer needed, an application can close it using the [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) function.</span></span>

<span data-ttu-id="056be-137">La definición de tipo de **Rio \_ CQ** se define en el archivo de encabezado *Mswsockdef. h* que se incluye automáticamente en el archivo de encabezado *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="056be-137">The **RIO\_CQ** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="056be-138">El archivo de encabezado *Mswsockdef. h* nunca debe usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="056be-138">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="056be-139">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="056be-139">Thread Safety</span></span>

<span data-ttu-id="056be-140">Si varios subprocesos intentan acceder al mismo **río \_ CQ** mediante [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritor de lector fino o un mecanismo de exclusión mutua similar.</span><span class="sxs-lookup"><span data-stu-id="056be-140">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="056be-141">Si las colas de finalización no están compartidas, no se requiere la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="056be-141">If the completion queues are not shared, mutual exclusion is not required.</span></span>

## <a name="requirements"></a><span data-ttu-id="056be-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="056be-142">Requirements</span></span>



| <span data-ttu-id="056be-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="056be-143">Requirement</span></span> | <span data-ttu-id="056be-144">Value</span><span class="sxs-lookup"><span data-stu-id="056be-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="056be-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="056be-145">Minimum supported client</span></span><br/> | <span data-ttu-id="056be-146">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="056be-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="056be-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="056be-147">Minimum supported server</span></span><br/> | <span data-ttu-id="056be-148">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="056be-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="056be-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="056be-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="056be-150"><dt>Mswsockdef. h (incluye mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="056be-150"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="056be-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="056be-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056be-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="056be-152">**CreateIoCompletionPort**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[<span data-ttu-id="056be-153">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="056be-153">**CreateEvent**</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="056be-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="056be-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="056be-155">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="056be-155">**GetQueuedCompletionStatusEx**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[<span data-ttu-id="056be-156">**SUPERPUESTA**</span><span class="sxs-lookup"><span data-stu-id="056be-156">**OVERLAPPED**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[<span data-ttu-id="056be-157">**finalización de la notificación de RIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="056be-157">**RIO\_NOTIFICATION\_COMPLETION**</span></span>](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[<span data-ttu-id="056be-158">**\_tipo de \_ finalización de notificación de Rio \_**</span><span class="sxs-lookup"><span data-stu-id="056be-158">**RIO\_NOTIFICATION\_COMPLETION\_TYPE**</span></span>](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[<span data-ttu-id="056be-159">**Río \_ PET**</span><span class="sxs-lookup"><span data-stu-id="056be-159">**RIO\_RQ**</span></span>](riorqueue.md)
</dt> <dt>

<span data-ttu-id="056be-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="056be-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="056be-161">**RIOCreateCompletionQueue**</span><span class="sxs-lookup"><span data-stu-id="056be-161">**RIOCreateCompletionQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="056be-162">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="056be-162">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="056be-163">**RIODequeueCompletion**</span><span class="sxs-lookup"><span data-stu-id="056be-163">**RIODequeueCompletion**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="056be-164">**RIONotify**</span><span class="sxs-lookup"><span data-stu-id="056be-164">**RIONotify**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[<span data-ttu-id="056be-165">**WSACreateEvent**</span><span class="sxs-lookup"><span data-stu-id="056be-165">**WSACreateEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[<span data-ttu-id="056be-166">**WSAResetEvent**</span><span class="sxs-lookup"><span data-stu-id="056be-166">**WSAResetEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[<span data-ttu-id="056be-167">**WSAWaitForMultipleEvents**</span><span class="sxs-lookup"><span data-stu-id="056be-167">**WSAWaitForMultipleEvents**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
