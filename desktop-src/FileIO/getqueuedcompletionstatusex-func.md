---
description: Recupera simultáneamente varias entradas del puerto de finalización.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Función GetQueuedCompletionStatusEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669693"
---
# <a name="getqueuedcompletionstatusex-function"></a><span data-ttu-id="ab18d-103">GetQueuedCompletionStatusEx función)</span><span class="sxs-lookup"><span data-stu-id="ab18d-103">GetQueuedCompletionStatusEx function</span></span>

<span data-ttu-id="ab18d-104">Recupera simultáneamente varias entradas del puerto de finalización.</span><span class="sxs-lookup"><span data-stu-id="ab18d-104">Retrieves multiple completion port entries simultaneously.</span></span> <span data-ttu-id="ab18d-105">Espera a que se completen las operaciones de e/s pendientes asociadas al puerto de finalización especificado.</span><span class="sxs-lookup"><span data-stu-id="ab18d-105">It waits for pending I/O operations that are associated with the specified completion port to complete.</span></span>

<span data-ttu-id="ab18d-106">Para quitar de la cola los paquetes de finalización de e/s de uno en uno, use la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="ab18d-106">To dequeue I/O completion packets one at a time, use the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab18d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab18d-107">Syntax</span></span>


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a><span data-ttu-id="ab18d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab18d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab18d-109">*CompletionPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-109">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-110">Identificador del puerto de finalización.</span><span class="sxs-lookup"><span data-stu-id="ab18d-110">A handle to the completion port.</span></span> <span data-ttu-id="ab18d-111">Para crear un puerto de finalización, utilice la función [**CreateIoCompletionPort**](createiocompletionport.md) .</span><span class="sxs-lookup"><span data-stu-id="ab18d-111">To create a completion port, use the [**CreateIoCompletionPort**](createiocompletionport.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ab18d-112">*lpCompletionPortEntries* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-112">*lpCompletionPortEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-113">En la entrada, apunta a una matriz preasignada de estructuras de [**\_ entrada superpuestas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .</span><span class="sxs-lookup"><span data-stu-id="ab18d-113">On input, points to a pre-allocated array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures.</span></span>

<span data-ttu-id="ab18d-114">En la salida, recibe una matriz de estructuras de [**\_ entrada superpuestas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) que contienen las entradas.</span><span class="sxs-lookup"><span data-stu-id="ab18d-114">On output, receives an array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures that hold the entries.</span></span> <span data-ttu-id="ab18d-115">El número de elementos de matriz lo proporciona *ulNumEntriesRemoved*.</span><span class="sxs-lookup"><span data-stu-id="ab18d-115">The number of array elements is provided by *ulNumEntriesRemoved*.</span></span>

<span data-ttu-id="ab18d-116">Número de bytes transferidos durante cada operación de e/s, la clave de finalización que indica en qué archivo se produjo cada e/s y la dirección de la estructura superpuesta utilizada en cada e/s original se devuelve en la matriz *lpCompletionPortEntries* .</span><span class="sxs-lookup"><span data-stu-id="ab18d-116">The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O occurred, and the overlapped structure address used in each original I/O are all returned in the *lpCompletionPortEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="ab18d-117">*ulCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-117">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-118">Número máximo de entradas que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="ab18d-118">The maximum number of entries to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ab18d-119">*ulNumEntriesRemoved* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-119">*ulNumEntriesRemoved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-120">Puntero a una variable que recibe el número de entradas realmente quitadas.</span><span class="sxs-lookup"><span data-stu-id="ab18d-120">A pointer to a variable that receives the number of entries actually removed.</span></span>

</dd> <dt>

<span data-ttu-id="ab18d-121">*dwMilliseconds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-121">*dwMilliseconds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-122">Número de milisegundos que el llamador está dispuesto a esperar a que aparezca un paquete de finalización en el puerto de finalización.</span><span class="sxs-lookup"><span data-stu-id="ab18d-122">The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port.</span></span> <span data-ttu-id="ab18d-123">Si un paquete de finalización no aparece en el tiempo especificado, la función agota el tiempo de espera y devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="ab18d-123">If a completion packet does not appear within the specified time, the function times out and returns **FALSE**.</span></span>

<span data-ttu-id="ab18d-124">Si *dwMilliseconds* es **infinito** (0xFFFFFFFF), la función nunca agotará el tiempo de espera. Si *dwMilliseconds* es cero y no hay ninguna operación de e/s para quitar de la cola, se agotará el tiempo de espera de la función de inmediato.</span><span class="sxs-lookup"><span data-stu-id="ab18d-124">If *dwMilliseconds* is **INFINITE** (0xFFFFFFFF), the function will never time out. If *dwMilliseconds* is zero and there is no I/O operation to dequeue, the function will time out immediately.</span></span>

</dd> <dt>

<span data-ttu-id="ab18d-125">*fAlertable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-125">*fAlertable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18d-126">Si este parámetro es **false**, la función no devuelve ningún resultado hasta que haya transcurrido el período de tiempo de espera o se haya recuperado una entrada.</span><span class="sxs-lookup"><span data-stu-id="ab18d-126">If this parameter is **FALSE**, the function does not return until the time-out period has elapsed or an entry is retrieved.</span></span>

<span data-ttu-id="ab18d-127">Si el parámetro es **true** y no hay ninguna entrada disponible, la función realiza una espera de alerta.</span><span class="sxs-lookup"><span data-stu-id="ab18d-127">If the parameter is **TRUE** and there are no available entries, the function performs an alertable wait.</span></span> <span data-ttu-id="ab18d-128">El subproceso devuelve cuando el sistema pone en cola una rutina de finalización de e/s o APC en el subproceso y el subproceso ejecuta la función.</span><span class="sxs-lookup"><span data-stu-id="ab18d-128">The thread returns when the system queues an I/O completion routine or APC to the thread and the thread executes the function.</span></span>

<span data-ttu-id="ab18d-129">Una rutina de finalización se pone en cola cuando se ha completado la función [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) en la que se especificó, y el subproceso que realiza la llamada es el subproceso que inició la operación.</span><span class="sxs-lookup"><span data-stu-id="ab18d-129">A completion routine is queued when the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function in which it was specified has completed, and the calling thread is the thread that initiated the operation.</span></span> <span data-ttu-id="ab18d-130">Un APC se pone en cola cuando se llama a [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span><span class="sxs-lookup"><span data-stu-id="ab18d-130">An APC is queued when you call [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab18d-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab18d-131">Return value</span></span>

<span data-ttu-id="ab18d-132">Devuelve un valor distinto de cero (**true**) si es correcto o cero (**false**) en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ab18d-132">Returns nonzero (**TRUE**) if successful or zero (**FALSE**) otherwise.</span></span>

<span data-ttu-id="ab18d-133">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ab18d-133">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab18d-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab18d-134">Remarks</span></span>

<span data-ttu-id="ab18d-135">Esta función asocia un subproceso al puerto de finalización especificado.</span><span class="sxs-lookup"><span data-stu-id="ab18d-135">This function associates a thread with the specified completion port.</span></span> <span data-ttu-id="ab18d-136">Un subproceso se puede asociar a un puerto de finalización como máximo.</span><span class="sxs-lookup"><span data-stu-id="ab18d-136">A thread can be associated with at most one completion port.</span></span>

<span data-ttu-id="ab18d-137">Esta función devuelve **true** cuando se ha completado al menos una e/s pendiente, pero es posible que se haya producido un error en una o varias operaciones de e/s.</span><span class="sxs-lookup"><span data-stu-id="ab18d-137">This function returns **TRUE** when at least one pending I/O is completed, but it is possible that one or more I/O operations failed.</span></span> <span data-ttu-id="ab18d-138">Tenga en cuenta que el usuario de esta función puede comprobar la lista de entradas devueltas en el parámetro *lpCompletionPortEntries* para determinar cuáles se corresponden con las posibles operaciones de e/s con errores examinando el estado contenido en el miembro **lpOverlapped** de cada [**\_ entrada superpuesta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span><span class="sxs-lookup"><span data-stu-id="ab18d-138">Note that it is up to the user of this function to check the list of returned entries in the *lpCompletionPortEntries* parameter to determine which of them correspond to any possible failed I/O operations by looking at the status contained in the **lpOverlapped** member in each [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span></span>

<span data-ttu-id="ab18d-139">Esta función devuelve **false** cuando no se quitó la cola de ninguna operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="ab18d-139">This function returns **FALSE** when no I/O operation was dequeued.</span></span> <span data-ttu-id="ab18d-140">Esto suele significar que se ha producido un error al procesar los parámetros de esta llamada o que el identificador *CompletionPort* se cerró o no es válido.</span><span class="sxs-lookup"><span data-stu-id="ab18d-140">This typically means that an error occurred while processing the parameters to this call, or that the *CompletionPort* handle was closed or is otherwise invalid.</span></span> <span data-ttu-id="ab18d-141">La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) proporciona información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="ab18d-141">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function provides extended error information.</span></span>

<span data-ttu-id="ab18d-142">Si se produce un error en una llamada a [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) porque el identificador asociado a él está cerrado, la función devuelve **false** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el error que se ha **\_ abandonado \_ Wait \_ 0**.</span><span class="sxs-lookup"><span data-stu-id="ab18d-142">If a call to [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) fails because the handle associated with it is closed, the function returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return **ERROR\_ABANDONED\_WAIT\_0**.</span></span>

<span data-ttu-id="ab18d-143">Las aplicaciones de servidor pueden tener varios subprocesos que llaman a la función **GetQueuedCompletionStatusEx** para el mismo puerto de finalización.</span><span class="sxs-lookup"><span data-stu-id="ab18d-143">Server applications may have several threads calling the **GetQueuedCompletionStatusEx** function for the same completion port.</span></span> <span data-ttu-id="ab18d-144">A medida que se completan las operaciones de e/s, se ponen en cola en este puerto en el orden de los primeros en salir.</span><span class="sxs-lookup"><span data-stu-id="ab18d-144">As I/O operations complete, they are queued to this port in first-in-first-out order.</span></span> <span data-ttu-id="ab18d-145">Si un subproceso está esperando activamente en esta llamada, una o varias solicitudes en cola completan la llamada solo para ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="ab18d-145">If a thread is actively waiting on this call, one or more queued requests complete the call for that thread only.</span></span>

<span data-ttu-id="ab18d-146">Para obtener más información sobre la teoría del puerto de finalización de e/s, el uso y las funciones asociadas, consulte [puertos de finalización de e/s](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="ab18d-146">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="ab18d-147">En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.</span><span class="sxs-lookup"><span data-stu-id="ab18d-147">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="ab18d-148">Technology</span><span class="sxs-lookup"><span data-stu-id="ab18d-148">Technology</span></span>                                           | <span data-ttu-id="ab18d-149">Compatible</span><span class="sxs-lookup"><span data-stu-id="ab18d-149">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="ab18d-150">Protocolo bloque de mensajes del servidor (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="ab18d-150">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="ab18d-151">Sí</span><span class="sxs-lookup"><span data-stu-id="ab18d-151">Yes</span></span><br/> |
| <span data-ttu-id="ab18d-152">Conmutación por error transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="ab18d-152">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="ab18d-153">Sí</span><span class="sxs-lookup"><span data-stu-id="ab18d-153">Yes</span></span><br/> |
| <span data-ttu-id="ab18d-154">SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)</span><span class="sxs-lookup"><span data-stu-id="ab18d-154">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="ab18d-155">Sí</span><span class="sxs-lookup"><span data-stu-id="ab18d-155">Yes</span></span><br/> |
| <span data-ttu-id="ab18d-156">Sistema de archivos Volumen compartido de clúster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="ab18d-156">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="ab18d-157">Sí</span><span class="sxs-lookup"><span data-stu-id="ab18d-157">Yes</span></span><br/> |
| <span data-ttu-id="ab18d-158">Sistema de archivos resistente a errores (ReFS)</span><span class="sxs-lookup"><span data-stu-id="ab18d-158">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="ab18d-159">Sí</span><span class="sxs-lookup"><span data-stu-id="ab18d-159">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ab18d-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab18d-160">Requirements</span></span>



| <span data-ttu-id="ab18d-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab18d-161">Requirement</span></span> | <span data-ttu-id="ab18d-162">Value</span><span class="sxs-lookup"><span data-stu-id="ab18d-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab18d-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab18d-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ab18d-164">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-164">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="ab18d-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab18d-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ab18d-166">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ab18d-166">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="ab18d-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab18d-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab18d-168"><dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista (incluido Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab18d-168"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ab18d-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab18d-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab18d-170"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab18d-170"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="ab18d-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab18d-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab18d-172"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab18d-172"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="ab18d-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab18d-173">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab18d-174">**Temas de información general**</span><span class="sxs-lookup"><span data-stu-id="ab18d-174">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="ab18d-175">Funciones de administración de archivos</span><span class="sxs-lookup"><span data-stu-id="ab18d-175">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="ab18d-176">Puertos de finalización de e/s</span><span class="sxs-lookup"><span data-stu-id="ab18d-176">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="ab18d-177">Usar los encabezados de Windows</span><span class="sxs-lookup"><span data-stu-id="ab18d-177">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

<span data-ttu-id="ab18d-178">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="ab18d-178">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="ab18d-179">**ConnectNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="ab18d-179">**ConnectNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[<span data-ttu-id="ab18d-180">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="ab18d-180">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="ab18d-181">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="ab18d-181">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="ab18d-182">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="ab18d-182">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="ab18d-183">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="ab18d-183">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="ab18d-184">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="ab18d-184">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="ab18d-185">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="ab18d-185">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="ab18d-186">**TransactNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="ab18d-186">**TransactNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[<span data-ttu-id="ab18d-187">**WaitCommEvent**</span><span class="sxs-lookup"><span data-stu-id="ab18d-187">**WaitCommEvent**</span></span>](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[<span data-ttu-id="ab18d-188">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="ab18d-188">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

