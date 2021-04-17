---
description: Recupera los niveles actuales de luz de corte de CA y DC y el estado de energía actual.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: Código de control de IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677900"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a><span data-ttu-id="012ac-103">\_Consulta de vídeo ioctl \_ \_ Mostrar código de control de \_ brillo</span><span class="sxs-lookup"><span data-stu-id="012ac-103">IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="012ac-104">\[Este código de control está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="012ac-104">\[This control code is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="012ac-105">La compatibilidad con este código de control se ha quitado en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="012ac-105">Support for this control code was removed in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="012ac-106">En su lugar, use la clase [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) .\]</span><span class="sxs-lookup"><span data-stu-id="012ac-106">Use the [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) class instead.\]</span></span>

<span data-ttu-id="012ac-107">Recupera los niveles actuales de luz de corte de CA y DC y el estado de energía actual.</span><span class="sxs-lookup"><span data-stu-id="012ac-107">Retrieves the current AC and DC backlight levels and the current power state.</span></span>

<span data-ttu-id="012ac-108">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="012ac-108">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="012ac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="012ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="012ac-110">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="012ac-110">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-111">Identificador de \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="012ac-111">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="012ac-112">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="012ac-112">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="012ac-113">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="012ac-113">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-114">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="012ac-114">The control code for the operation.</span></span> <span data-ttu-id="012ac-115">Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="012ac-115">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="012ac-116">Use **ioctl \_ video \_ query \_ Display \_ Brightness** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="012ac-116">Use **IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="012ac-117">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="012ac-117">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-118">No se utiliza con esta operación; se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="012ac-118">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="012ac-119">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="012ac-119">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-120">No se utiliza con esta operación; se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="012ac-120">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="012ac-121">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="012ac-121">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-122">Un puntero a un búfer que recibirá una estructura de [**\_ brillo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="012ac-122">A pointer to a buffer that will receive a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="012ac-123">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="012ac-123">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-124">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="012ac-124">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="012ac-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="012ac-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos de salida devueltos.</span><span class="sxs-lookup"><span data-stu-id="012ac-126">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="012ac-127">Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código \_ insuficiente \_ búfer y el recuento de bytes devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="012ac-127">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="012ac-128">Si el búfer de salida es demasiado pequeño para contener todos los datos, pero puede contener algunas entradas, el sistema operativo devuelve tanto como cabe en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error del código de error \_ más \_ datos y *lpBytesReturned* indica la cantidad de datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="012ac-128">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="012ac-129">La aplicación debe volver a llamar a [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la misma operación, especificando un nuevo punto de partida.</span><span class="sxs-lookup"><span data-stu-id="012ac-129">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="012ac-130">Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="012ac-130">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="012ac-131">Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="012ac-131">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="012ac-132">Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="012ac-132">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="012ac-133">Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="012ac-133">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="012ac-134">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="012ac-134">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="012ac-135">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="012ac-135">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="012ac-136">Si *hDevice* se abrió con la marca de indicador de archivo \_ \_ superpuesto, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="012ac-136">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="012ac-137">En este caso, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="012ac-137">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="012ac-138">Si el dispositivo se ha abierto con la \_ marca de indicador de archivo \_ superpuesto y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.</span><span class="sxs-lookup"><span data-stu-id="012ac-138">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="012ac-139">Si se abrió *hDevice* sin especificar la marca de la marca de archivo \_ \_ superpuesta, se omite *lpOverlapped* y [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no devuelve ningún resultado hasta que se haya completado la operación o hasta que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="012ac-139">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="012ac-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="012ac-140">Return value</span></span>

<span data-ttu-id="012ac-141">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="012ac-141">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="012ac-142">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="012ac-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="012ac-143">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="012ac-143">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="012ac-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="012ac-144">Remarks</span></span>

<span data-ttu-id="012ac-145">El archivo de encabezado utilizado para compilar aplicaciones que incluyen esta funcionalidad, Ntddvdeo. h, se incluye en el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="012ac-145">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="012ac-146">Para obtener información sobre cómo obtener el DDK, vea [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="012ac-146">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="012ac-147">Como alternativa, puede definir este código de control como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="012ac-147">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="012ac-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="012ac-148">Requirements</span></span>



| <span data-ttu-id="012ac-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="012ac-149">Requirement</span></span> | <span data-ttu-id="012ac-150">Value</span><span class="sxs-lookup"><span data-stu-id="012ac-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="012ac-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="012ac-151">Minimum supported client</span></span><br/> | <span data-ttu-id="012ac-152">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="012ac-152">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="012ac-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="012ac-153">Minimum supported server</span></span><br/> | <span data-ttu-id="012ac-154">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="012ac-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="012ac-155">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="012ac-155">End of client support</span></span><br/>    | <span data-ttu-id="012ac-156">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="012ac-156">Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="012ac-157">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="012ac-157">End of server support</span></span><br/>    | <span data-ttu-id="012ac-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="012ac-158">Windows Server 2003 R2</span></span><br/>                                                     |
| <span data-ttu-id="012ac-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="012ac-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="012ac-160"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="012ac-160"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="012ac-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="012ac-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="012ac-162">Interfaz de control de retroiluminación</span><span class="sxs-lookup"><span data-stu-id="012ac-162">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="012ac-163">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="012ac-163">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="012ac-164">[**brillo de la pantalla \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="012ac-164">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="012ac-165">**brillo de la pantalla del conjunto de \_ vídeos de ioctl \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="012ac-165">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

