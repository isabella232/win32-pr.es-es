---
title: Código de control FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: El código de control de FSCTL_DFS_GET_PKT_ENTRY_STATE puede obtener la misma información que la función NetDfsGetClientInfo, pero puede proporcionar un mejor rendimiento en algunas configuraciones con latencias altas a los servidores DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539177"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a><span data-ttu-id="6997c-103">Código de control de FSCTL_DFS_GET_PKT_ENTRY_STATE</span><span class="sxs-lookup"><span data-stu-id="6997c-103">FSCTL_DFS_GET_PKT_ENTRY_STATE control code</span></span>

<span data-ttu-id="6997c-104">El código de control de **FSCTL_DFS_GET_PKT_ENTRY_STATE** puede obtener la misma información que la función [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , pero puede proporcionar un mejor rendimiento en algunas configuraciones con latencias altas a los servidores DFS.</span><span class="sxs-lookup"><span data-stu-id="6997c-104">The **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="6997c-105">No se recomienda usar el código de control de **FSCTL_DFS_GET_PKT_ENTRY_STATE** a menos que haya problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6997c-105">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="6997c-106">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="6997c-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a><span data-ttu-id="6997c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6997c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6997c-108">*hDevice* [in]</span><span class="sxs-lookup"><span data-stu-id="6997c-108">*hDevice* [in]</span></span>
</dt> <dd>

<span data-ttu-id="6997c-109">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6997c-109">A handle to the device.</span></span> <span data-ttu-id="6997c-110">Para obtener un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="6997c-110">To obtain a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="6997c-111">*dwIoControlCode* [in]</span><span class="sxs-lookup"><span data-stu-id="6997c-111">*dwIoControlCode* [in]</span></span>
</dt> <dd>

<span data-ttu-id="6997c-112">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="6997c-112">The control code for the operation.</span></span> <span data-ttu-id="6997c-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="6997c-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="6997c-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="6997c-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="6997c-115">Dirección de una estructura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) y las cadenas unicode 1-3 siguientes.</span><span class="sxs-lookup"><span data-stu-id="6997c-115">Address of a [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure and the 1-3 Unicode strings that follow.</span></span>

</dd> <dt>

<span data-ttu-id="6997c-116">*nInBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="6997c-116">*nInBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="6997c-117">Tamaño, en bytes, del búfer al que apunta el parámetro *lpInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="6997c-117">Size, in bytes, of the buffer pointed to by the *lpInBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6997c-118">*lpOutBuffer* [out]</span><span class="sxs-lookup"><span data-stu-id="6997c-118">*lpOutBuffer* [out]</span></span>
</dt> <dd>

<span data-ttu-id="6997c-119">Dirección de una estructura de **DFS_INFO_ \#** y de las cadenas y estructuras a las que apunta la estructura de **DFS_INFO_ \#** .</span><span class="sxs-lookup"><span data-stu-id="6997c-119">Address of a **DFS_INFO_\#** structure and any strings and structures pointed to by the **DFS_INFO_\#** structure.</span></span> <span data-ttu-id="6997c-120">La estructura específica devuelta depende del miembro de **nivel** de la estructura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) pasada en el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="6997c-120">The specific structure returned depends on the **Level** member in the [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure passed in the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6997c-121">*nOutBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="6997c-121">*nOutBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="6997c-122">Tamaño, en bytes, del búfer al que apunta el parámetro *lpOutBuffer* .</span><span class="sxs-lookup"><span data-stu-id="6997c-122">Size, in bytes, of the buffer pointed to by the *lpOutBuffer* parameter.</span></span> <span data-ttu-id="6997c-123">Debido a las cadenas y estructuras a las que hace referencia la estructura de **DFS_INFO_ \#** devuelta que también están en el búfer de salida, este búfer debe ser mayor que la estructura de **DFS_INFO_ \#** especificada.</span><span class="sxs-lookup"><span data-stu-id="6997c-123">Due to the strings and structures referenced by the returned **DFS_INFO_\#** structure that are also in the output buffer, this buffer should be larger than the **DFS_INFO_\#** structure specified.</span></span>

</dd> <dt>

<span data-ttu-id="6997c-124">*lpBytesReturned* [out]</span><span class="sxs-lookup"><span data-stu-id="6997c-124">*lpBytesReturned* [out]</span></span>
</dt> <dd>

<span data-ttu-id="6997c-125">Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6997c-125">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="6997c-126">Si el búfer de salida es demasiado pequeño, pero al menos lo suficientemente grande como para contener un **valor DWORD**, se produce un error en la llamada, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR_MORE_DATA**, y el primer **valor DWORD** del búfer de salida contiene el tamaño que se habría requerido.</span><span class="sxs-lookup"><span data-stu-id="6997c-126">If the output buffer is too small, but at least large enough to hold a **DWORD**, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the first **DWORD** of the output buffer contains the size that would have been required.</span></span> <span data-ttu-id="6997c-127">Si el búfer de salida no puede contener un **valor DWORD** , se produce un error en la llamada con **ERROR_INSUFFICIENT_BUFFER** y el valor de *lpBytesReturned* es cero.</span><span class="sxs-lookup"><span data-stu-id="6997c-127">If the output buffer cannot hold a **DWORD** then the call fails with **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="6997c-128">Si *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6997c-128">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="6997c-129">Incluso cuando una operación no devuelve datos de salida y *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="6997c-129">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="6997c-130">Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="6997c-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="6997c-131">Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6997c-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="6997c-132">Si este parámetro no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="6997c-132">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="6997c-133">Para recuperar el número de bytes devueltos, llame a [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="6997c-133">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="6997c-134">Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="6997c-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="6997c-135">*lpOverlapped* [in]</span><span class="sxs-lookup"><span data-stu-id="6997c-135">*lpOverlapped* [in]</span></span>
</dt> <dd>

<span data-ttu-id="6997c-136">Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="6997c-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="6997c-137">Si se abrió *hDevice* sin especificar **FILE_FLAG_OVERLAPPED**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="6997c-137">If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="6997c-138">Si *hDevice* se abrió con la marca **FILE_FLAG_OVERLAPPED** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="6997c-138">If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="6997c-139">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="6997c-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="6997c-140">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="6997c-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="6997c-141">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="6997c-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="6997c-142">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="6997c-142">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6997c-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6997c-143">Return value</span></span>

<span data-ttu-id="6997c-144">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6997c-144">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="6997c-145">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6997c-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="6997c-146">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="6997c-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="6997c-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6997c-147">Requirements</span></span>

| <span data-ttu-id="6997c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6997c-148">Requirement</span></span> | <span data-ttu-id="6997c-149">Value</span><span class="sxs-lookup"><span data-stu-id="6997c-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6997c-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6997c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6997c-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6997c-151">Windows Vista</span></span><br/>                                                                             |
| <span data-ttu-id="6997c-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6997c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6997c-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6997c-153">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="6997c-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6997c-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6997c-155"><dt>LmDfs. h (incluye LmDfs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6997c-155"><dt>LmDfs.h (include LmDfs.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="6997c-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="6997c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6997c-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="6997c-157">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="6997c-158">**NetDfsGetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="6997c-158">**NetDfsGetClientInfo**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
