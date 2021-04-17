---
description: Marca las operaciones de e/s sincrónicas pendientes que emite el subproceso especificado como cancelada.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Función CancelSynchronousIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546699"
---
# <a name="cancelsynchronousio-function"></a><span data-ttu-id="b4be4-103">CancelSynchronousIo función)</span><span class="sxs-lookup"><span data-stu-id="b4be4-103">CancelSynchronousIo function</span></span>

<span data-ttu-id="b4be4-104">Marca las operaciones de e/s sincrónicas pendientes que emite el subproceso especificado como cancelada.</span><span class="sxs-lookup"><span data-stu-id="b4be4-104">Marks pending synchronous I/O operations that are issued by the specified thread as canceled.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4be4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4be4-105">Syntax</span></span>


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a><span data-ttu-id="b4be4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4be4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4be4-107">*hThread* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4be4-107">*hThread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4be4-108">Identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="b4be4-108">A handle to the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4be4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4be4-109">Return value</span></span>

<span data-ttu-id="b4be4-110">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b4be4-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="b4be4-111">Si se produce un error en la función, el valor devuelto es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="b4be4-111">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="b4be4-112">Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="b4be4-112">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="b4be4-113">Si esta función no encuentra una solicitud para cancelar, el valor devuelto es 0 (cero) y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **error \_ no \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="b4be4-113">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4be4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4be4-114">Remarks</span></span>

<span data-ttu-id="b4be4-115">El autor de la llamada debe tener el [subproceso \_ terminar](/windows/desktop/ProcThread/thread-security-and-access-rights) el acceso.</span><span class="sxs-lookup"><span data-stu-id="b4be4-115">The caller must have the [THREAD\_TERMINATE](/windows/desktop/ProcThread/thread-security-and-access-rights) access right.</span></span>

<span data-ttu-id="b4be4-116">Si hay alguna operación de e/s pendiente en curso para el subproceso especificado, la función **CancelSynchronousIo** las marca para su cancelación.</span><span class="sxs-lookup"><span data-stu-id="b4be4-116">If there are any pending I/O operations in progress for the specified thread, the **CancelSynchronousIo** function marks them for cancellation.</span></span> <span data-ttu-id="b4be4-117">La mayoría de los tipos de operaciones se pueden cancelar inmediatamente; otras operaciones pueden continuar hasta su finalización antes de que se cancelen realmente y se notifique al llamador.</span><span class="sxs-lookup"><span data-stu-id="b4be4-117">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="b4be4-118">La función **CancelSynchronousIo** no espera a que se completen todas las operaciones canceladas.</span><span class="sxs-lookup"><span data-stu-id="b4be4-118">The **CancelSynchronousIo** function does not wait for all canceled operations to complete.</span></span> <span data-ttu-id="b4be4-119">Para obtener más información, vea [instrucciones de finalización/cancelación de e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="b4be4-119">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

<span data-ttu-id="b4be4-120">La operación que se está cancelando se completa con uno de los tres Estados siguientes: debe comprobar el estado de finalización para determinar el estado de finalización.</span><span class="sxs-lookup"><span data-stu-id="b4be4-120">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="b4be4-121">Los tres Estados son:</span><span class="sxs-lookup"><span data-stu-id="b4be4-121">The three statuses are:</span></span>

-   <span data-ttu-id="b4be4-122">**La operación se completó con normalidad.**</span><span class="sxs-lookup"><span data-stu-id="b4be4-122">**The operation completed normally.**</span></span> <span data-ttu-id="b4be4-123">Esto puede ocurrir incluso si se canceló la operación, porque es posible que no se haya enviado la solicitud de cancelación en el tiempo para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="b4be4-123">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="b4be4-124">**Operación cancelada.**</span><span class="sxs-lookup"><span data-stu-id="b4be4-124">**The operation was canceled.**</span></span> <span data-ttu-id="b4be4-125">La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve la **operación de error \_ \_ anulada**.</span><span class="sxs-lookup"><span data-stu-id="b4be4-125">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="b4be4-126">**No se pudo realizar la operación debido a otro error.**</span><span class="sxs-lookup"><span data-stu-id="b4be4-126">**The operation failed with another error.**</span></span> <span data-ttu-id="b4be4-127">La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error pertinente.</span><span class="sxs-lookup"><span data-stu-id="b4be4-127">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="b4be4-128">En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.</span><span class="sxs-lookup"><span data-stu-id="b4be4-128">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="b4be4-129">Technology</span><span class="sxs-lookup"><span data-stu-id="b4be4-129">Technology</span></span>                                           | <span data-ttu-id="b4be4-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="b4be4-130">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="b4be4-131">Protocolo bloque de mensajes del servidor (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="b4be4-131">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="b4be4-132">Sí</span><span class="sxs-lookup"><span data-stu-id="b4be4-132">Yes</span></span><br/> |
| <span data-ttu-id="b4be4-133">Conmutación por error transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="b4be4-133">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="b4be4-134">Sí</span><span class="sxs-lookup"><span data-stu-id="b4be4-134">Yes</span></span><br/> |
| <span data-ttu-id="b4be4-135">SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)</span><span class="sxs-lookup"><span data-stu-id="b4be4-135">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="b4be4-136">Sí</span><span class="sxs-lookup"><span data-stu-id="b4be4-136">Yes</span></span><br/> |
| <span data-ttu-id="b4be4-137">Sistema de archivos Volumen compartido de clúster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="b4be4-137">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="b4be4-138">Sí</span><span class="sxs-lookup"><span data-stu-id="b4be4-138">Yes</span></span><br/> |
| <span data-ttu-id="b4be4-139">Sistema de archivos resistente a errores (ReFS)</span><span class="sxs-lookup"><span data-stu-id="b4be4-139">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="b4be4-140">Sí</span><span class="sxs-lookup"><span data-stu-id="b4be4-140">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b4be4-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4be4-141">Requirements</span></span>



| <span data-ttu-id="b4be4-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4be4-142">Requirement</span></span> | <span data-ttu-id="b4be4-143">Value</span><span class="sxs-lookup"><span data-stu-id="b4be4-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4be4-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4be4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b4be4-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b4be4-145">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="b4be4-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4be4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b4be4-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4be4-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="b4be4-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4be4-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4be4-149"><dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista (incluido Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4be4-149"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b4be4-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4be4-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4be4-151"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4be4-151"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="b4be4-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4be4-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4be4-153"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4be4-153"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="b4be4-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4be4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4be4-155">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="b4be4-155">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="b4be4-156">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="b4be4-156">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="b4be4-157">Funciones de administración de archivos</span><span class="sxs-lookup"><span data-stu-id="b4be4-157">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="b4be4-158">E/s sincrónica y asincrónica</span><span class="sxs-lookup"><span data-stu-id="b4be4-158">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

