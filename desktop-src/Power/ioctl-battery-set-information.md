---
description: Establece diversa información de la batería.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: Código de control de IOCTL_BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909698"
---
# <a name="ioctl_battery_set_information-control-code"></a><span data-ttu-id="dcfd1-103">\_Código de \_ control de información de conjunto de batería de ioctl \_</span><span class="sxs-lookup"><span data-stu-id="dcfd1-103">IOCTL\_BATTERY\_SET\_INFORMATION control code</span></span>

<span data-ttu-id="dcfd1-104">Establece diversa información de la batería.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-104">Sets various battery information.</span></span> <span data-ttu-id="dcfd1-105">La estructura del parámetro de entrada, [**\_ \_ información del conjunto**](battery-set-information-str.md)de la batería, indica qué información de estado de la batería se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-105">The input parameter structure, [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md), indicates which battery status information is to be set.</span></span>

<span data-ttu-id="dcfd1-106">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="dcfd1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcfd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcfd1-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-109">Identificador de la batería en la que se va a establecer la información.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-109">A handle to the battery on which the information is to be set.</span></span> <span data-ttu-id="dcfd1-110">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="dcfd1-110">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd1-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-112">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-112">The control code for the operation.</span></span> <span data-ttu-id="dcfd1-113">Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-113">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="dcfd1-114">Use **la \_ \_ \_ información del conjunto de baterías de ioctl** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-114">Use **IOCTL\_BATTERY\_SET\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd1-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-116">Puntero a una estructura [**de \_ \_ información de conjunto de batería**](battery-set-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="dcfd1-116">A pointer to a [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd1-117">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-117">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-118">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-118">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd1-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-120">No se utiliza con esta operación; se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-120">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd1-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-122">No se utiliza con esta operación; se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-122">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd1-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-124">Puntero a una variable que recibe el tamaño de los datos devueltos en el búfer de *lpOutBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-124">A pointer to a variable that receives the size of data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="dcfd1-125">Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código \_ insuficiente \_ búfer y el recuento de bytes devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="dcfd1-126">Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**, aunque *lpOutBuffer* sea **null**.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-126">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**, even if *lpOutBuffer* is **NULL**.</span></span>

<span data-ttu-id="dcfd1-127">Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-127">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="dcfd1-128">Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="dcfd1-128">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="dcfd1-129">Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="dcfd1-129">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="dcfd1-130">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="dcfd1-130">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfd1-131">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="dcfd1-131">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="dcfd1-132">Si *hDevice* se abrió con la marca de indicador de archivo \_ \_ superpuesto, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-132">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="dcfd1-133">En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="dcfd1-133">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="dcfd1-134">Si el dispositivo se ha abierto con la \_ marca de indicador de archivo \_ superpuesto y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-134">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="dcfd1-135">Si *hDevice* se ha abierto sin especificar la marca de la marca de archivo \_ \_ superpuesta, *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no vuelve hasta que se ha completado la operación o hasta que se produce un error.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-135">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcfd1-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcfd1-136">Return value</span></span>

<span data-ttu-id="dcfd1-137">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-137">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="dcfd1-138">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="dcfd1-139">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="dcfd1-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="dcfd1-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dcfd1-140">Remarks</span></span>

<span data-ttu-id="dcfd1-141">Todas las solicitudes para establecer la información de la batería se completarán con el estado archivo de ERROR \_ \_ no \_ encontrado si la etiqueta de la batería de la solicitud no coincide con la de la etiqueta de la batería actual.</span><span class="sxs-lookup"><span data-stu-id="dcfd1-141">All requests to set battery information will complete with the status of ERROR\_FILE\_NOT\_FOUND if the battery tag of the request does not match that of the current battery tag.</span></span>

<span data-ttu-id="dcfd1-142">Para conocer las implicaciones de la e/s superpuesta en esta operación, consulte la sección Comentarios del tema [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="dcfd1-142">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfd1-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcfd1-143">Requirements</span></span>



| <span data-ttu-id="dcfd1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcfd1-144">Requirement</span></span> | <span data-ttu-id="dcfd1-145">Value</span><span class="sxs-lookup"><span data-stu-id="dcfd1-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfd1-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcfd1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="dcfd1-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dcfd1-147">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="dcfd1-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcfd1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="dcfd1-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcfd1-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="dcfd1-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcfd1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcfd1-151"><dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="dcfd1-151"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfd1-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcfd1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfd1-153">Información de la batería</span><span class="sxs-lookup"><span data-stu-id="dcfd1-153">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="dcfd1-154">Códigos de control de administración de energía</span><span class="sxs-lookup"><span data-stu-id="dcfd1-154">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="dcfd1-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="dcfd1-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="dcfd1-156">**\_información del conjunto de batería \_**</span><span class="sxs-lookup"><span data-stu-id="dcfd1-156">**BATTERY\_SET\_INFORMATION**</span></span>](battery-set-information-str.md)
</dt> <dt>

[<span data-ttu-id="dcfd1-157">**\_información de \_ consulta de batería ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="dcfd1-157">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="dcfd1-158">**Estado de la \_ consulta de batería ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dcfd1-158">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="dcfd1-159">**\_etiqueta de \_ consulta ioctl Battery \_**</span><span class="sxs-lookup"><span data-stu-id="dcfd1-159">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

