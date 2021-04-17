---
description: Marca las operaciones de e/s pendientes para el identificador de archivo especificado. La función solo cancela las operaciones de e/s en el proceso actual, independientemente del subproceso que haya creado la operación de e/s.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Función CancelIoEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687405"
---
# <a name="cancelioex-function"></a><span data-ttu-id="3c4ee-104">CancelIoEx función)</span><span class="sxs-lookup"><span data-stu-id="3c4ee-104">CancelIoEx function</span></span>

<span data-ttu-id="3c4ee-105">Marca las operaciones de e/s pendientes para el identificador de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-105">Marks any outstanding I/O operations for the specified file handle.</span></span> <span data-ttu-id="3c4ee-106">La función solo cancela las operaciones de e/s en el proceso actual, independientemente del subproceso que haya creado la operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-106">The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4ee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c4ee-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="3c4ee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c4ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c4ee-109">*hFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c4ee-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ee-110">Identificador del archivo.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-110">A handle to the file.</span></span>

</dd> <dt>

<span data-ttu-id="3c4ee-111">*lpOverlapped* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3c4ee-111">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ee-112">Puntero a una estructura de datos [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que contiene los datos usados para la e/s asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-112">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) data structure that contains the data used for asynchronous I/O.</span></span>

<span data-ttu-id="3c4ee-113">Si este parámetro es **null**, se cancelan todas las solicitudes de e/s para el parámetro *hFile* .</span><span class="sxs-lookup"><span data-stu-id="3c4ee-113">If this parameter is **NULL**, all I/O requests for the *hFile* parameter are canceled.</span></span>

<span data-ttu-id="3c4ee-114">Si este parámetro no es **null**, solo las solicitudes de e/s específicas emitidas para el archivo con la estructura superpuesta *lpOverlapped* especificada se marcan como canceladas, lo que significa que puede cancelar una o más solicitudes, mientras que la función [**CancelIo**](cancelio.md) cancela todas las solicitudes pendientes en un identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-114">If this parameter is not **NULL**, only those specific I/O requests that were issued for the file with the specified *lpOverlapped* overlapped structure are marked as canceled, meaning that you can cancel one or more requests, while the [**CancelIo**](cancelio.md) function cancels all outstanding requests on a file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c4ee-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c4ee-115">Return value</span></span>

<span data-ttu-id="3c4ee-116">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-116">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="3c4ee-117">La operación de cancelación para todas las operaciones de e/s pendientes emitidas por el proceso de llamada para el identificador de archivo especificado se solicitó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-117">The cancel operation for all pending I/O operations issued by the calling process for the specified file handle was successfully requested.</span></span> <span data-ttu-id="3c4ee-118">La aplicación no debe liberar o reutilizar la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada a las operaciones de e/s canceladas hasta que se hayan completado.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-118">The application must not free or reuse the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the canceled I/O operations until they have completed.</span></span> <span data-ttu-id="3c4ee-119">El subproceso puede usar la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar cuándo se han completado las operaciones de e/s.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-119">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="3c4ee-120">Si se produce un error en la función, el valor devuelto es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="3c4ee-120">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="3c4ee-121">Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="3c4ee-121">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="3c4ee-122">Si esta función no encuentra una solicitud para cancelar, el valor devuelto es 0 (cero) y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **error \_ no \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-122">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c4ee-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c4ee-123">Remarks</span></span>

<span data-ttu-id="3c4ee-124">La función **CancelIoEx** permite cancelar solicitudes en subprocesos distintos del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-124">The **CancelIoEx** function allows you to cancel requests in threads other than the calling thread.</span></span> <span data-ttu-id="3c4ee-125">La función [**CancelIo**](cancelio.md) solo cancela las solicitudes en el mismo subproceso que llamó a la función **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="3c4ee-125">The [**CancelIo**](cancelio.md) function only cancels requests in the same thread that called the **CancelIo** function.</span></span> <span data-ttu-id="3c4ee-126">**CancelIoEx** cancela solo e/s pendientes en el identificador, no cambia el estado del identificador. Esto significa que no se puede confiar en el estado del identificador porque no se puede saber si la operación se completó correctamente o se canceló.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-126">**CancelIoEx** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="3c4ee-127">Si hay alguna operación de e/s pendiente en curso para el identificador de archivo especificado, la función **CancelIoEx** las marca para su cancelación.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-127">If there are any pending I/O operations in progress for the specified file handle, the **CancelIoEx** function marks them for cancellation.</span></span> <span data-ttu-id="3c4ee-128">La mayoría de los tipos de operaciones se pueden cancelar inmediatamente; otras operaciones pueden continuar hasta su finalización antes de que se cancelen realmente y se notifique al llamador.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-128">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="3c4ee-129">La función **CancelIoEx** no espera a que se completen todas las operaciones canceladas.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-129">The **CancelIoEx** function does not wait for all canceled operations to complete.</span></span>

<span data-ttu-id="3c4ee-130">Si el identificador de archivo está asociado a un puerto de finalización, un paquete de finalización de e/s no se pone en cola en el puerto si se cancela correctamente una operación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-130">If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if a synchronous operation is successfully canceled.</span></span> <span data-ttu-id="3c4ee-131">En el caso de las operaciones asincrónicas aún pendientes, la operación de cancelación pondrá en cola un paquete de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-131">For asynchronous operations still pending, the cancel operation will queue an I/O completion packet.</span></span>

<span data-ttu-id="3c4ee-132">La operación que se está cancelando se completa con uno de los tres Estados siguientes: debe comprobar el estado de finalización para determinar el estado de finalización.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-132">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="3c4ee-133">Los tres Estados son:</span><span class="sxs-lookup"><span data-stu-id="3c4ee-133">The three statuses are:</span></span>

-   <span data-ttu-id="3c4ee-134">La operación se completó con normalidad.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-134">The operation completed normally.</span></span> <span data-ttu-id="3c4ee-135">Esto puede ocurrir incluso si se canceló la operación, porque es posible que no se haya enviado la solicitud de cancelación en el tiempo para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-135">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="3c4ee-136">Operación cancelada.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-136">The operation was canceled.</span></span> <span data-ttu-id="3c4ee-137">La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve la **operación de error \_ \_ anulada**.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-137">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="3c4ee-138">No se pudo realizar la operación debido a otro error.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-138">The operation failed with another error.</span></span> <span data-ttu-id="3c4ee-139">La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error pertinente.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-139">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="3c4ee-140">En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.</span><span class="sxs-lookup"><span data-stu-id="3c4ee-140">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="3c4ee-141">Technology</span><span class="sxs-lookup"><span data-stu-id="3c4ee-141">Technology</span></span>                                           | <span data-ttu-id="3c4ee-142">Compatible</span><span class="sxs-lookup"><span data-stu-id="3c4ee-142">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="3c4ee-143">Protocolo bloque de mensajes del servidor (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="3c4ee-143">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="3c4ee-144">Sí</span><span class="sxs-lookup"><span data-stu-id="3c4ee-144">Yes</span></span><br/> |
| <span data-ttu-id="3c4ee-145">Conmutación por error transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="3c4ee-145">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="3c4ee-146">Sí</span><span class="sxs-lookup"><span data-stu-id="3c4ee-146">Yes</span></span><br/> |
| <span data-ttu-id="3c4ee-147">SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)</span><span class="sxs-lookup"><span data-stu-id="3c4ee-147">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="3c4ee-148">Sí</span><span class="sxs-lookup"><span data-stu-id="3c4ee-148">Yes</span></span><br/> |
| <span data-ttu-id="3c4ee-149">Sistema de archivos Volumen compartido de clúster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="3c4ee-149">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="3c4ee-150">Sí</span><span class="sxs-lookup"><span data-stu-id="3c4ee-150">Yes</span></span><br/> |
| <span data-ttu-id="3c4ee-151">Sistema de archivos resistente a errores (ReFS)</span><span class="sxs-lookup"><span data-stu-id="3c4ee-151">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="3c4ee-152">Sí</span><span class="sxs-lookup"><span data-stu-id="3c4ee-152">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3c4ee-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c4ee-153">Requirements</span></span>



| <span data-ttu-id="3c4ee-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c4ee-154">Requirement</span></span> | <span data-ttu-id="3c4ee-155">Value</span><span class="sxs-lookup"><span data-stu-id="3c4ee-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4ee-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c4ee-156">Minimum supported client</span></span><br/> | <span data-ttu-id="3c4ee-157">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="3c4ee-157">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="3c4ee-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c4ee-158">Minimum supported server</span></span><br/> | <span data-ttu-id="3c4ee-159">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="3c4ee-159">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="3c4ee-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c4ee-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c4ee-161"><dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista (incluido Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ee-161"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3c4ee-162">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c4ee-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c4ee-163"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ee-163"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="3c4ee-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c4ee-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c4ee-165"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ee-165"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="3c4ee-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c4ee-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c4ee-167">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="3c4ee-167">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="3c4ee-168">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="3c4ee-168">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="3c4ee-169">Cancelar operaciones de e/s pendientes</span><span class="sxs-lookup"><span data-stu-id="3c4ee-169">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)
</dt> <dt>

[<span data-ttu-id="3c4ee-170">Funciones de administración de archivos</span><span class="sxs-lookup"><span data-stu-id="3c4ee-170">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="3c4ee-171">E/s sincrónica y asincrónica</span><span class="sxs-lookup"><span data-stu-id="3c4ee-171">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

