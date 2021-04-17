---
description: Espera a que todos los volúmenes del disco especificado estén listos para su uso.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: Código de control de IOCTL_DISK_ARE_VOLUMES_READY (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688460"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a><span data-ttu-id="d8bae-103">El \_ disco \_ ioctl \_ está \_ preparado para el código de control</span><span class="sxs-lookup"><span data-stu-id="d8bae-103">IOCTL\_DISK\_ARE\_VOLUMES\_READY control code</span></span>

<span data-ttu-id="d8bae-104">Espera a que todos los volúmenes del disco especificado estén listos para su uso.</span><span class="sxs-lookup"><span data-stu-id="d8bae-104">Waits for all volumes on the specified disk to be ready for use.</span></span>

<span data-ttu-id="d8bae-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8bae-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="d8bae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8bae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8bae-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="d8bae-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-108">Identificador del disco.</span><span class="sxs-lookup"><span data-stu-id="d8bae-108">A handle to the disk.</span></span>

<span data-ttu-id="d8bae-109">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="d8bae-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="d8bae-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="d8bae-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="d8bae-111">The control code for the operation.</span></span>

<span data-ttu-id="d8bae-112">Usar **el \_ disco ioctl \_ son \_ volúmenes \_ preparados** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="d8bae-112">Use **IOCTL\_DISK\_ARE\_VOLUMES\_READY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="d8bae-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="d8bae-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-114">No se usa con esta operación.</span><span class="sxs-lookup"><span data-stu-id="d8bae-114">Not used with this operation.</span></span> <span data-ttu-id="d8bae-115">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="d8bae-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d8bae-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="d8bae-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-117">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d8bae-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="d8bae-118">Se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d8bae-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d8bae-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="d8bae-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-120">No se usa con esta operación.</span><span class="sxs-lookup"><span data-stu-id="d8bae-120">Not used with this operation.</span></span> <span data-ttu-id="d8bae-121">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="d8bae-121">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d8bae-122">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="d8bae-122">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-123">No se usa con esta operación.</span><span class="sxs-lookup"><span data-stu-id="d8bae-123">Not used with this operation.</span></span> <span data-ttu-id="d8bae-124">Se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d8bae-124">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d8bae-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="d8bae-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-126">No se usa con esta operación.</span><span class="sxs-lookup"><span data-stu-id="d8bae-126">Not used with this operation.</span></span> <span data-ttu-id="d8bae-127">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="d8bae-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d8bae-128">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="d8bae-128">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="d8bae-129">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="d8bae-129">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="d8bae-130">Si se abrió *hDevice* sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="d8bae-130">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="d8bae-131">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="d8bae-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="d8bae-132">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="d8bae-132">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="d8bae-133">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="d8bae-133">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="d8bae-134">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="d8bae-134">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="d8bae-135">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="d8bae-135">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8bae-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8bae-136">Return value</span></span>

<span data-ttu-id="d8bae-137">Si la operación se completa correctamente, lo que indica que todos los volúmenes del disco están listos para su uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d8bae-137">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="d8bae-138">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d8bae-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="d8bae-139">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d8bae-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8bae-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8bae-140">Requirements</span></span>



| <span data-ttu-id="d8bae-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8bae-141">Requirement</span></span> | <span data-ttu-id="d8bae-142">Value</span><span class="sxs-lookup"><span data-stu-id="d8bae-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8bae-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8bae-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d8bae-144">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8bae-144">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d8bae-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8bae-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d8bae-146">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8bae-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8bae-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8bae-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8bae-148"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8bae-148"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8bae-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8bae-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8bae-150">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="d8bae-150">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="d8bae-151">Códigos de control de administración de discos</span><span class="sxs-lookup"><span data-stu-id="d8bae-151">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> </dl>

 

