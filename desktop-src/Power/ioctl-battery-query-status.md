---
description: Recupera el estado actual de la batería.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: Código de control de IOCTL_BATTERY_QUERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667213"
---
# <a name="ioctl_battery_query_status-control-code"></a><span data-ttu-id="10032-103">\_Código de \_ control de estado de consulta de batería ioctl \_</span><span class="sxs-lookup"><span data-stu-id="10032-103">IOCTL\_BATTERY\_QUERY\_STATUS control code</span></span>

<span data-ttu-id="10032-104">Recupera el estado actual de la batería.</span><span class="sxs-lookup"><span data-stu-id="10032-104">Retrieves the current status of the battery.</span></span>

<span data-ttu-id="10032-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="10032-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="10032-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10032-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10032-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="10032-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-108">Identificador de la batería desde la que se va a devolver información.</span><span class="sxs-lookup"><span data-stu-id="10032-108">A handle to the battery from which information is to be returned.</span></span> <span data-ttu-id="10032-109">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="10032-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="10032-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="10032-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="10032-111">The control code for the operation.</span></span> <span data-ttu-id="10032-112">Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="10032-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="10032-113">Use **el \_ \_ \_ Estado** de la consulta de batería de ioctl para esta operación.</span><span class="sxs-lookup"><span data-stu-id="10032-113">Use **IOCTL\_BATTERY\_QUERY\_STATUS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="10032-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="10032-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-115">Puntero a una estructura [**de \_ \_ Estado de espera de batería**](battery-wait-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="10032-115">A pointer to a [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="10032-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="10032-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-117">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="10032-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="10032-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="10032-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-119">Puntero a una estructura [**de \_ Estado**](battery-status-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="10032-119">A pointer to a [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="10032-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="10032-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-121">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="10032-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="10032-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="10032-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-123">Puntero a una variable que recibe el tamaño de los datos devueltos en el búfer de *lpOutBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="10032-123">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="10032-124">Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código **\_ insuficiente \_ búfer** y el recuento de bytes devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="10032-124">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="10032-125">Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="10032-125">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="10032-126">Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="10032-126">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="10032-127">Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="10032-127">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="10032-128">Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="10032-128">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="10032-129">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="10032-129">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="10032-130">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="10032-130">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="10032-131">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="10032-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="10032-132">En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="10032-132">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="10032-133">Si el dispositivo se ha abierto con la marca de **indicador de archivo \_ \_ superpuesto** y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.</span><span class="sxs-lookup"><span data-stu-id="10032-133">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="10032-134">Si *hDevice* se ha abierto sin especificar la marca de la **marca de archivo \_ \_ superpuesta** , *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no vuelve hasta que se ha completado la operación o hasta que se produce un error.</span><span class="sxs-lookup"><span data-stu-id="10032-134">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10032-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10032-135">Return value</span></span>

<span data-ttu-id="10032-136">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="10032-136">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="10032-137">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="10032-137">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="10032-138">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="10032-138">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="10032-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10032-139">Remarks</span></span>

<span data-ttu-id="10032-140">Este IOCTL de la batería recupera el estado de la batería en el momento en que se devuelve la operación.</span><span class="sxs-lookup"><span data-stu-id="10032-140">This battery IOCTL retrieves the status of the battery at the time the operation returns.</span></span> <span data-ttu-id="10032-141">La estructura de parámetros de entrada, [**\_ \_ Estado de espera**](battery-wait-status-str.md)de la batería, indica cuándo se debe procesar y devolver el estado de la batería.</span><span class="sxs-lookup"><span data-stu-id="10032-141">The input parameter structure, [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md), indicates when the battery status is to be processed and returned.</span></span>

<span data-ttu-id="10032-142">Las solicitudes de estado de la batería pueden ser para la devolución inmediata o se pueden establecer para esperar una condición determinada antes de completarse.</span><span class="sxs-lookup"><span data-stu-id="10032-142">Requests for battery status can be for immediate return or can be set to wait for a particular condition before completing.</span></span> <span data-ttu-id="10032-143">Por ejemplo, se puede realizar una solicitud de información de batería que espere hasta que la capacidad de la batería alcance un punto especificado o cambie el estado de la batería.</span><span class="sxs-lookup"><span data-stu-id="10032-143">For example, a request for battery information can be made that waits until the battery capacity reaches a specified point or the battery state changes.</span></span>

<span data-ttu-id="10032-144">Todas las solicitudes de información de batería se completarán con el estado **\_ \_ no \_ se encontró el archivo de error** cuando el elemento **BatteryTag** de la solicitud no coincide con el de la etiqueta de la batería actual.</span><span class="sxs-lookup"><span data-stu-id="10032-144">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="10032-145">(Consulte [etiquetas de batería](battery-information.md) para obtener más información). Se utiliza para asegurarse de que la información de la batería devuelta coincide con la de la batería solicitada.</span><span class="sxs-lookup"><span data-stu-id="10032-145">(See [Battery Tags](battery-information.md) for more information.) This is used to ensure that the returned battery information matches that of the requested battery.</span></span>

<span data-ttu-id="10032-146">Para conocer las implicaciones de la e/s superpuesta en esta operación, consulte la sección Comentarios del tema [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="10032-146">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="10032-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="10032-147">Examples</span></span>

<span data-ttu-id="10032-148">Para obtener un ejemplo, consulte [enumeración de dispositivos de batería](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="10032-148">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10032-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10032-149">Requirements</span></span>



| <span data-ttu-id="10032-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="10032-150">Requirement</span></span> | <span data-ttu-id="10032-151">Value</span><span class="sxs-lookup"><span data-stu-id="10032-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10032-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10032-152">Minimum supported client</span></span><br/> | <span data-ttu-id="10032-153">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="10032-153">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="10032-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10032-154">Minimum supported server</span></span><br/> | <span data-ttu-id="10032-155">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="10032-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="10032-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10032-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="10032-157"><dt>Poclass. h; </dt> <dt>BatClass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="10032-157"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10032-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="10032-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10032-159">Información de la batería</span><span class="sxs-lookup"><span data-stu-id="10032-159">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="10032-160">Códigos de control de administración de energía</span><span class="sxs-lookup"><span data-stu-id="10032-160">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="10032-161">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="10032-161">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="10032-162">**Estado de la batería \_**</span><span class="sxs-lookup"><span data-stu-id="10032-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="10032-163">**\_Estado de espera de la batería \_**</span><span class="sxs-lookup"><span data-stu-id="10032-163">**BATTERY\_WAIT\_STATUS**</span></span>](battery-wait-status-str.md)
</dt> <dt>

[<span data-ttu-id="10032-164">**\_información de \_ consulta de batería ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="10032-164">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="10032-165">**\_etiqueta de \_ consulta ioctl Battery \_**</span><span class="sxs-lookup"><span data-stu-id="10032-165">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="10032-166">**\_información del \_ conjunto de baterías de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="10032-166">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

