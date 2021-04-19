---
description: Recupera la etiqueta actual de la batería.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: Código de control de IOCTL_BATTERY_QUERY_TAG (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677902"
---
# <a name="ioctl_battery_query_tag-control-code"></a><span data-ttu-id="768be-103">\_Código de \_ control de etiqueta de consulta de pila ioctl \_</span><span class="sxs-lookup"><span data-stu-id="768be-103">IOCTL\_BATTERY\_QUERY\_TAG control code</span></span>

<span data-ttu-id="768be-104">Recupera la etiqueta actual de la batería.</span><span class="sxs-lookup"><span data-stu-id="768be-104">Retrieves the battery's current tag.</span></span>

<span data-ttu-id="768be-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="768be-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="768be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="768be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="768be-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="768be-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-108">Identificador de la batería de la que se va a recuperar la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="768be-108">A handle to the battery from which the tag is to be retrieved.</span></span> <span data-ttu-id="768be-109">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="768be-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="768be-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="768be-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="768be-111">The control code for the operation.</span></span> <span data-ttu-id="768be-112">Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="768be-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="768be-113">Use **la \_ \_ \_ etiqueta de consulta ioctl Battery** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="768be-113">Use **IOCTL\_BATTERY\_QUERY\_TAG** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="768be-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="768be-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-115">Puntero a un búfer de entrada **ULong** .</span><span class="sxs-lookup"><span data-stu-id="768be-115">A pointer to a **ULONG** input buffer.</span></span> <span data-ttu-id="768be-116">El valor indica el número de milisegundos que se esperará si no hay ninguna batería.</span><span class="sxs-lookup"><span data-stu-id="768be-116">The value indicates the number of milliseconds to wait if there is no battery.</span></span> <span data-ttu-id="768be-117">Un valor de-1 indica que la solicitud esperará indefinidamente (o hasta que se cancele por algún otro evento).</span><span class="sxs-lookup"><span data-stu-id="768be-117">A value of -1 indicates the request will wait indefinitely (or until canceled by some other event).</span></span>

</dd> <dt>

<span data-ttu-id="768be-118">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="768be-118">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-119">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="768be-119">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="768be-120">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="768be-120">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-121">Puntero a un búfer de salida **ULong** .</span><span class="sxs-lookup"><span data-stu-id="768be-121">A pointer to a **ULONG** output buffer.</span></span> <span data-ttu-id="768be-122">Si se realiza correctamente, este búfer contiene la etiqueta de la batería actual, que puede ser cualquier valor excepto la etiqueta de batería \_ \_ no válida.</span><span class="sxs-lookup"><span data-stu-id="768be-122">On success this buffer contains the current battery tag, which can be any value except BATTERY\_TAG\_INVALID.</span></span> <span data-ttu-id="768be-123">En caso de error, si [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el archivo de error del código de error **\_ \_ no \_ encontrado**, este búfer contiene la etiqueta de la batería del valor no **\_ \_ válida**.</span><span class="sxs-lookup"><span data-stu-id="768be-123">On failure, if [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_FILE\_NOT\_FOUND**, this buffer contains the value **BATTERY\_TAG\_INVALID**.</span></span>

</dd> <dt>

<span data-ttu-id="768be-124">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="768be-124">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-125">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="768be-125">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="768be-126">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="768be-126">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-127">Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de *lpOutBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="768be-127">A pointer to a variable that receives the size of the data stored in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="768be-128">Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código **\_ insuficiente \_ búfer** y el recuento de bytes devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="768be-128">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="768be-129">Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="768be-129">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="768be-130">Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="768be-130">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="768be-131">Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="768be-131">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="768be-132">Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="768be-132">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="768be-133">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="768be-133">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="768be-134">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="768be-134">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="768be-135">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="768be-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="768be-136">En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="768be-136">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="768be-137">Si el dispositivo se ha abierto con la marca de **indicador de archivo \_ \_ superpuesto** y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.</span><span class="sxs-lookup"><span data-stu-id="768be-137">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="768be-138">Si *hDevice* se ha abierto sin especificar la marca de la **marca de archivo \_ \_ superpuesta** , *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no vuelve hasta que se ha completado la operación o hasta que se produce un error.</span><span class="sxs-lookup"><span data-stu-id="768be-138">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="768be-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="768be-139">Return value</span></span>

<span data-ttu-id="768be-140">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="768be-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="768be-141">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="768be-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="768be-142">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="768be-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="768be-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="768be-143">Remarks</span></span>

<span data-ttu-id="768be-144">Este IOCTL de la batería recupera la etiqueta actual de la batería.</span><span class="sxs-lookup"><span data-stu-id="768be-144">This battery IOCTL retrieves the battery's current tag.</span></span> <span data-ttu-id="768be-145">La etiqueta de la batería es un valor único distinto de cero que cambia cuando la batería física se vuelve a insertar, reemplazar o se somete a cualquier cambio de característica.</span><span class="sxs-lookup"><span data-stu-id="768be-145">The battery tag is a unique nonzero value that changes when the physical battery is reinserted, replaced, or undergoes any characteristic changes.</span></span> <span data-ttu-id="768be-146">Consulte la sección etiquetas de la batería en el tema información general de la [batería](battery-information.md) para obtener más detalles sobre cuándo cambia una etiqueta de la batería, cómo detectar el cambio y cómo debe continuar una aplicación después de un cambio de etiqueta de la batería.</span><span class="sxs-lookup"><span data-stu-id="768be-146">See the Battery Tags section in the [Battery Information](battery-information.md) overview topic for more detail on when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag change.</span></span> <span data-ttu-id="768be-147">Cuando no haya ninguna batería, esta solicitud esperará la hora indicada y, si aún no existe ninguna, se devolverá un archivo de **error \_ \_ no \_ encontrado** y la etiqueta de la batería en la etiqueta de batería no será **\_ \_ válida**.</span><span class="sxs-lookup"><span data-stu-id="768be-147">When a battery is not present, this request will wait the indicated time, and if there is still no battery present, then it will return **ERROR\_FILE\_NOT\_FOUND** and set the battery tag to **BATTERY\_TAG\_INVALID**.</span></span> <span data-ttu-id="768be-148">(Consulte la información de la batería para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="768be-148">(See Battery Information for more information.)</span></span>

<span data-ttu-id="768be-149">Todas las solicitudes de información de la batería requieren que el autor de la llamada proporcione la etiqueta de la batería correspondiente.</span><span class="sxs-lookup"><span data-stu-id="768be-149">All requests for other battery information require the caller to supply the matching battery tag.</span></span> <span data-ttu-id="768be-150">Esto garantiza que el autor de la llamada recibe información de la misma batería para cada solicitud y garantiza que el autor de la llamada tenga en cuenta los cambios de la batería sin sondeos constantes.</span><span class="sxs-lookup"><span data-stu-id="768be-150">This ensures that the caller is receiving information for the same battery for every request and ensures that the caller is aware of battery changes without constant polling.</span></span>

<span data-ttu-id="768be-151">Para conocer las implicaciones de la e/s superpuesta en esta operación, consulte la sección Comentarios del tema [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="768be-151">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="768be-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="768be-152">Examples</span></span>

<span data-ttu-id="768be-153">Para obtener un ejemplo, consulte [enumeración de dispositivos de batería](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="768be-153">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="768be-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="768be-154">Requirements</span></span>



| <span data-ttu-id="768be-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="768be-155">Requirement</span></span> | <span data-ttu-id="768be-156">Value</span><span class="sxs-lookup"><span data-stu-id="768be-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="768be-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="768be-157">Minimum supported client</span></span><br/> | <span data-ttu-id="768be-158">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="768be-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="768be-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="768be-159">Minimum supported server</span></span><br/> | <span data-ttu-id="768be-160">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="768be-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="768be-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="768be-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="768be-162"><dt>Poclass. h; </dt> <dt>BatClass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="768be-162"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="768be-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="768be-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="768be-164">Información de la batería</span><span class="sxs-lookup"><span data-stu-id="768be-164">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="768be-165">Códigos de control de administración de energía</span><span class="sxs-lookup"><span data-stu-id="768be-165">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="768be-166">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="768be-166">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="768be-167">**\_información de \_ consulta de batería ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="768be-167">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="768be-168">**Estado de la \_ consulta de batería ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="768be-168">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="768be-169">**\_información del \_ conjunto de baterías de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="768be-169">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

