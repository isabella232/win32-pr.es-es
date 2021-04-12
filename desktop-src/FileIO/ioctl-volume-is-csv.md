---
description: Determina si un volumen es un volumen CSV.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: Código de control de IOCTL_VOLUME_IS_CSV (Ntddvol. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361307"
---
# <a name="ioctl_volume_is_csv-control-code"></a><span data-ttu-id="44892-103">El \_ volumen ioctl \_ es \_ código de control CSV</span><span class="sxs-lookup"><span data-stu-id="44892-103">IOCTL\_VOLUME\_IS\_CSV control code</span></span>

<span data-ttu-id="44892-104">Determina si un volumen es un volumen CSV.</span><span class="sxs-lookup"><span data-stu-id="44892-104">Determines whether a volume is a CSV volume.</span></span>

<span data-ttu-id="44892-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="44892-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="44892-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44892-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44892-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="44892-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-108">Identificador del volumen.</span><span class="sxs-lookup"><span data-stu-id="44892-108">A handle to the volume.</span></span> <span data-ttu-id="44892-109">Para recuperar un identificador de volumen, llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="44892-109">To retrieve a volume handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="44892-110">Solo los administradores pueden abrir identificadores de volumen.</span><span class="sxs-lookup"><span data-stu-id="44892-110">Only administrators can open volume handles.</span></span>

</dd> <dt>

<span data-ttu-id="44892-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="44892-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-112">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="44892-112">The control code for the operation.</span></span> <span data-ttu-id="44892-113">Use **el \_ volumen ioctl \_ es \_ CSV** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="44892-113">Use **IOCTL\_VOLUME\_IS\_CSV** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="44892-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="44892-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-115">No se utiliza con esta operación; se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="44892-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44892-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="44892-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-117">No se utiliza con esta operación; se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="44892-117">Not used with this operation; set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="44892-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="44892-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-119">Un puntero a **true** si el volumen es un volumen CSV; de lo contrario, se produce un error en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="44892-119">A pointer to **TRUE** if the volume is a CSV volume; otherwise, the function call fails.</span></span>

</dd> <dt>

<span data-ttu-id="44892-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="44892-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-121">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="44892-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="44892-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="44892-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-123">Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="44892-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="44892-124">Si *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="44892-124">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="44892-125">Incluso cuando una operación no devuelve datos de salida y *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="44892-125">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="44892-126">Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="44892-126">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="44892-127">Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="44892-127">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="44892-128">Si este parámetro no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="44892-128">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="44892-129">Para recuperar el número de bytes devueltos, llame a [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="44892-129">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="44892-130">Si *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="44892-130">If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="44892-131">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="44892-131">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="44892-132">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="44892-132">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="44892-133">Si se abrió *hDevice* sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="44892-133">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="44892-134">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="44892-134">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="44892-135">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="44892-135">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="44892-136">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="44892-136">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="44892-137">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="44892-137">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="44892-138">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="44892-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44892-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44892-139">Return value</span></span>

<span data-ttu-id="44892-140">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="44892-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="44892-141">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="44892-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero (0).</span></span> <span data-ttu-id="44892-142">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="44892-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="44892-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44892-143">Requirements</span></span>



| <span data-ttu-id="44892-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="44892-144">Requirement</span></span> | <span data-ttu-id="44892-145">Value</span><span class="sxs-lookup"><span data-stu-id="44892-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44892-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44892-146">Minimum supported client</span></span><br/> | <span data-ttu-id="44892-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44892-147">None supported</span></span><br/>                                                            |
| <span data-ttu-id="44892-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44892-148">Minimum supported server</span></span><br/> | <span data-ttu-id="44892-149">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="44892-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44892-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44892-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="44892-151"><dt>Ntddvol. h</dt></span><span class="sxs-lookup"><span data-stu-id="44892-151"><dt>Ntddvol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44892-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="44892-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44892-153">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="44892-153">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="44892-154">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="44892-154">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="44892-155">Códigos de control de administración del volumen</span><span class="sxs-lookup"><span data-stu-id="44892-155">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

