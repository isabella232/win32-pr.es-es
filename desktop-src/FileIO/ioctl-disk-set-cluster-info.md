---
description: Establece la información del clúster en un disco.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: Código de control de IOCTL_DISK_SET_CLUSTER_INFO (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669686"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a><span data-ttu-id="249eb-103">\_Código de \_ control de información de \_ clúster de conjunto de discos ioctl \_</span><span class="sxs-lookup"><span data-stu-id="249eb-103">IOCTL\_DISK\_SET\_CLUSTER\_INFO control code</span></span>

<span data-ttu-id="249eb-104">Establece la información del clúster en un disco.</span><span class="sxs-lookup"><span data-stu-id="249eb-104">Sets the cluster information on a disk.</span></span>

<span data-ttu-id="249eb-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="249eb-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="249eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="249eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="249eb-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="249eb-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-108">Identificador del disco.</span><span class="sxs-lookup"><span data-stu-id="249eb-108">A handle to the disk.</span></span>

<span data-ttu-id="249eb-109">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="249eb-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="249eb-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="249eb-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="249eb-111">The control code for the operation.</span></span>

<span data-ttu-id="249eb-112">Use **ioctl \_ Disk \_ set \_ cluster \_ info** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="249eb-112">Use **IOCTL\_DISK\_SET\_CLUSTER\_INFO** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="249eb-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="249eb-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-114">Un puntero a una estructura de datos de [**\_ \_ información del clúster de disco**](disk-cluster-info.md) que contiene información del clúster para el disco.</span><span class="sxs-lookup"><span data-stu-id="249eb-114">A pointer to a [**DISK\_CLUSTER\_INFO**](disk-cluster-info.md) data structure that contains cluster information for the disk.</span></span>

</dd> <dt>

<span data-ttu-id="249eb-115">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="249eb-115">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-116">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="249eb-116">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="249eb-117">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="249eb-117">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-118">No se usa con esta operación.</span><span class="sxs-lookup"><span data-stu-id="249eb-118">Not used with this operation.</span></span> <span data-ttu-id="249eb-119">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="249eb-119">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="249eb-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="249eb-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-121">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="249eb-121">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="249eb-122">Se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="249eb-122">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="249eb-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="249eb-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-124">No se usa con esta operación.</span><span class="sxs-lookup"><span data-stu-id="249eb-124">Not used with this operation.</span></span> <span data-ttu-id="249eb-125">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="249eb-125">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="249eb-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="249eb-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-127">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="249eb-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="249eb-128">Si se abrió *hDevice* sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="249eb-128">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="249eb-129">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="249eb-129">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="249eb-130">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="249eb-130">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="249eb-131">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="249eb-131">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="249eb-132">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="249eb-132">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="249eb-133">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="249eb-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="249eb-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="249eb-134">Return value</span></span>

<span data-ttu-id="249eb-135">Si la operación se completa correctamente, lo que indica que todos los volúmenes del disco están listos para su uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="249eb-135">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="249eb-136">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="249eb-136">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="249eb-137">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="249eb-137">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="249eb-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="249eb-138">Requirements</span></span>



| <span data-ttu-id="249eb-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="249eb-139">Requirement</span></span> | <span data-ttu-id="249eb-140">Value</span><span class="sxs-lookup"><span data-stu-id="249eb-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="249eb-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="249eb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="249eb-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="249eb-142">None supported</span></span><br/>                                                             |
| <span data-ttu-id="249eb-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="249eb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="249eb-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="249eb-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="249eb-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="249eb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="249eb-146"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="249eb-146"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="249eb-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="249eb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249eb-148">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="249eb-148">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="249eb-149">Códigos de control de administración de discos</span><span class="sxs-lookup"><span data-stu-id="249eb-149">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="249eb-150">**\_información del clúster de disco \_**</span><span class="sxs-lookup"><span data-stu-id="249eb-150">**DISK\_CLUSTER\_INFO**</span></span>](disk-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="249eb-151">**\_información de \_ clúster de obtención de disco de ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249eb-151">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

