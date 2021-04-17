---
description: Cancela todas las operaciones de entrada y salida (e/s) pendientes emitidas por el subproceso que realiza la llamada para el archivo especificado.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Función CancelIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666966"
---
# <a name="cancelio-function"></a><span data-ttu-id="6a611-103">CancelIo función)</span><span class="sxs-lookup"><span data-stu-id="6a611-103">CancelIo function</span></span>

<span data-ttu-id="6a611-104">Cancela todas las operaciones de entrada y salida (e/s) pendientes emitidas por el subproceso que realiza la llamada para el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6a611-104">Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.</span></span> <span data-ttu-id="6a611-105">La función no cancela las operaciones de e/s que otros subprocesos emiten para un identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="6a611-105">The function does not cancel I/O operations that other threads issue for a file handle.</span></span>

<span data-ttu-id="6a611-106">Para cancelar las operaciones de e/s de otro subproceso, utilice la función [**CancelIoEx**](cancelioex-func.md) .</span><span class="sxs-lookup"><span data-stu-id="6a611-106">To cancel I/O operations from another thread, use the [**CancelIoEx**](cancelioex-func.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a611-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a611-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="6a611-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a611-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a611-109">*hFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a611-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a611-110">Identificador del archivo.</span><span class="sxs-lookup"><span data-stu-id="6a611-110">A handle to the file.</span></span>

<span data-ttu-id="6a611-111">La función cancela todas las operaciones de e/s pendientes para este identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="6a611-111">The function cancels all pending I/O operations for this file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a611-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a611-112">Return value</span></span>

<span data-ttu-id="6a611-113">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6a611-113">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="6a611-114">La operación de cancelación para todas las operaciones de e/s pendientes emitidas por el subproceso que realiza la llamada para el identificador de archivo especificado se solicitó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6a611-114">The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested.</span></span> <span data-ttu-id="6a611-115">El subproceso puede usar la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar cuándo se han completado las operaciones de e/s.</span><span class="sxs-lookup"><span data-stu-id="6a611-115">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="6a611-116">Si se produce un error en la función, el valor devuelto es cero (0).</span><span class="sxs-lookup"><span data-stu-id="6a611-116">If the function fails, the return value is zero (0).</span></span> <span data-ttu-id="6a611-117">Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="6a611-117">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a611-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a611-118">Remarks</span></span>

<span data-ttu-id="6a611-119">Si hay alguna operación de e/s pendiente en curso para el identificador de archivo especificado y la emite el subproceso que realiza la llamada, la función **CancelIo** las cancela.</span><span class="sxs-lookup"><span data-stu-id="6a611-119">If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the **CancelIo** function cancels them.</span></span> <span data-ttu-id="6a611-120">**CancelIo** cancela solo e/s pendientes en el identificador, no cambia el estado del identificador. Esto significa que no se puede confiar en el estado del identificador porque no se puede saber si la operación se completó correctamente o se canceló.</span><span class="sxs-lookup"><span data-stu-id="6a611-120">**CancelIo** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="6a611-121">Las operaciones de e/s deben emitirse como e/s superpuestas.</span><span class="sxs-lookup"><span data-stu-id="6a611-121">The I/O operations must be issued as overlapped I/O.</span></span> <span data-ttu-id="6a611-122">Si no es así, las operaciones de e/s no vuelven a permitir que el subproceso llame a la función **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="6a611-122">If they are not, the I/O operations do not return to allow the thread to call the **CancelIo** function.</span></span> <span data-ttu-id="6a611-123">La llamada a la función **CancelIo** con un identificador de archivo que no está abierto con la **marca de archivo \_ \_ superpuesto** no hace nada.</span><span class="sxs-lookup"><span data-stu-id="6a611-123">Calling the **CancelIo** function with a file handle that is not opened with **FILE\_FLAG\_OVERLAPPED** does nothing.</span></span>

<span data-ttu-id="6a611-124">Todas las operaciones de e/s que se han cancelado se **han \_ anulado con la operación error \_ cancelada** y todas las notificaciones de finalización de las operaciones de e/s se producen con normalidad.</span><span class="sxs-lookup"><span data-stu-id="6a611-124">All I/O operations that are canceled complete with the error **ERROR\_OPERATION\_ABORTED**, and all completion notifications for the I/O operations occur normally.</span></span>

<span data-ttu-id="6a611-125">En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.</span><span class="sxs-lookup"><span data-stu-id="6a611-125">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="6a611-126">Technology</span><span class="sxs-lookup"><span data-stu-id="6a611-126">Technology</span></span>                                           | <span data-ttu-id="6a611-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="6a611-127">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="6a611-128">Protocolo bloque de mensajes del servidor (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="6a611-128">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="6a611-129">Sí</span><span class="sxs-lookup"><span data-stu-id="6a611-129">Yes</span></span><br/> |
| <span data-ttu-id="6a611-130">Conmutación por error transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="6a611-130">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="6a611-131">Sí</span><span class="sxs-lookup"><span data-stu-id="6a611-131">Yes</span></span><br/> |
| <span data-ttu-id="6a611-132">SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)</span><span class="sxs-lookup"><span data-stu-id="6a611-132">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="6a611-133">Sí</span><span class="sxs-lookup"><span data-stu-id="6a611-133">Yes</span></span><br/> |
| <span data-ttu-id="6a611-134">Sistema de archivos Volumen compartido de clúster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="6a611-134">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="6a611-135">Sí</span><span class="sxs-lookup"><span data-stu-id="6a611-135">Yes</span></span><br/> |
| <span data-ttu-id="6a611-136">Sistema de archivos resistente a errores (ReFS)</span><span class="sxs-lookup"><span data-stu-id="6a611-136">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="6a611-137">Sí</span><span class="sxs-lookup"><span data-stu-id="6a611-137">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6a611-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a611-138">Requirements</span></span>



| <span data-ttu-id="6a611-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a611-139">Requirement</span></span> | <span data-ttu-id="6a611-140">Value</span><span class="sxs-lookup"><span data-stu-id="6a611-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a611-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a611-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6a611-142">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="6a611-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="6a611-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a611-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6a611-144">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="6a611-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="6a611-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a611-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a611-146"><dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP (incluido Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a611-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6a611-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a611-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a611-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a611-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="6a611-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a611-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a611-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a611-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="6a611-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a611-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a611-152">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="6a611-152">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="6a611-153">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="6a611-153">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="6a611-154">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="6a611-154">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="6a611-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="6a611-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="6a611-156">Funciones de administración de archivos</span><span class="sxs-lookup"><span data-stu-id="6a611-156">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="6a611-157">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="6a611-157">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="6a611-158">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="6a611-158">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[<span data-ttu-id="6a611-159">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="6a611-159">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="6a611-160">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="6a611-160">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="6a611-161">E/s sincrónica y asincrónica</span><span class="sxs-lookup"><span data-stu-id="6a611-161">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[<span data-ttu-id="6a611-162">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="6a611-162">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="6a611-163">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="6a611-163">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

