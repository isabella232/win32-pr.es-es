---
description: Recupera los niveles de retroiluminación admitidos.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: Código de control de IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667212"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a><span data-ttu-id="c4364-103">\_Código de \_ control de \_ brillo compatible con consulta de vídeo ioctl \_</span><span class="sxs-lookup"><span data-stu-id="c4364-103">IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS control code</span></span>

<span data-ttu-id="c4364-104">Recupera los niveles de retroiluminación admitidos.</span><span class="sxs-lookup"><span data-stu-id="c4364-104">Retrieves the supported backlight levels.</span></span>

<span data-ttu-id="c4364-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="c4364-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="c4364-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4364-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4364-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="c4364-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-108">Identificador de \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="c4364-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="c4364-109">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="c4364-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="c4364-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="c4364-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="c4364-111">The control code for the operation.</span></span> <span data-ttu-id="c4364-112">Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="c4364-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="c4364-113">Use **el \_ \_ \_ \_ brillo compatible con la consulta de vídeo ioctl** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="c4364-113">Use **IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c4364-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="c4364-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-115">No se utiliza con esta operación; se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c4364-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4364-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c4364-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-117">No se utiliza con esta operación; se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="c4364-117">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4364-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="c4364-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-119">Un puntero a un búfer que recibe una matriz de los niveles de energía disponibles.</span><span class="sxs-lookup"><span data-stu-id="c4364-119">A pointer to a buffer that receives an array of the available power levels.</span></span> <span data-ttu-id="c4364-120">Este búfer debe tener una longitud de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="c4364-120">This buffer should be 256 bytes long.</span></span>

</dd> <dt>

<span data-ttu-id="c4364-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c4364-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-122">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c4364-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c4364-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="c4364-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-124">Puntero a una variable que recibe el tamaño, en bytes, de los datos de salida devueltos.</span><span class="sxs-lookup"><span data-stu-id="c4364-124">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="c4364-125">Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código \_ insuficiente \_ búfer y el recuento de bytes devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="c4364-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="c4364-126">Si el búfer de salida es demasiado pequeño para contener todos los datos, pero puede contener algunas entradas, el sistema operativo devuelve tanto como cabe en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error del código de error \_ más \_ datos y *lpBytesReturned* indica la cantidad de datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="c4364-126">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="c4364-127">La aplicación debe volver a llamar a [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la misma operación, especificando un nuevo punto de partida.</span><span class="sxs-lookup"><span data-stu-id="c4364-127">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="c4364-128">Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c4364-128">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="c4364-129">Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c4364-129">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="c4364-130">Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="c4364-130">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="c4364-131">Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="c4364-131">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="c4364-132">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="c4364-132">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="c4364-133">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="c4364-133">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="c4364-134">Si *hDevice* se abrió con la marca de indicador de archivo \_ \_ superpuesto, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="c4364-134">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="c4364-135">En este caso, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="c4364-135">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="c4364-136">Si el dispositivo se ha abierto con la \_ marca de indicador de archivo \_ superpuesto y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.</span><span class="sxs-lookup"><span data-stu-id="c4364-136">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="c4364-137">Si se abrió *hDevice* sin especificar la marca de la marca de archivo \_ \_ superpuesta, se omite *lpOverlapped* y [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no devuelve ningún resultado hasta que se haya completado la operación o hasta que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="c4364-137">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4364-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4364-138">Return value</span></span>

<span data-ttu-id="c4364-139">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c4364-139">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="c4364-140">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c4364-140">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="c4364-141">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c4364-141">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4364-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4364-142">Remarks</span></span>

<span data-ttu-id="c4364-143">Cada elemento de la matriz *lpOutBuffer* tiene un byte de longitud.</span><span class="sxs-lookup"><span data-stu-id="c4364-143">Each element in the *lpOutBuffer* array is one byte in length.</span></span> <span data-ttu-id="c4364-144">Por lo tanto, en el momento de la devolución, el parámetro *lpBytesReturned* indica el número de niveles admitidos.</span><span class="sxs-lookup"><span data-stu-id="c4364-144">Therefore, upon return, the *lpBytesReturned* parameter indicates the number of supported levels.</span></span> <span data-ttu-id="c4364-145">Cada nivel es un valor comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="c4364-145">Each level is a value from 0 to 100.</span></span> <span data-ttu-id="c4364-146">Cuanto mayor sea el valor, más brillante será la retroiluminación.</span><span class="sxs-lookup"><span data-stu-id="c4364-146">The larger the value, the brighter the backlight.</span></span> <span data-ttu-id="c4364-147">Se admiten todos los niveles si la fuente de alimentación es AC o DC.</span><span class="sxs-lookup"><span data-stu-id="c4364-147">All levels are supported whether the power source is AC or DC.</span></span>

<span data-ttu-id="c4364-148">El archivo de encabezado utilizado para compilar aplicaciones que incluyen esta funcionalidad, Ntddvdeo. h, se incluye en el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c4364-148">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="c4364-149">Para obtener información sobre cómo obtener el DDK, vea [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="c4364-149">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="c4364-150">Como alternativa, puede definir este código de control como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="c4364-150">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="c4364-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4364-151">Requirements</span></span>



| <span data-ttu-id="c4364-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4364-152">Requirement</span></span> | <span data-ttu-id="c4364-153">Value</span><span class="sxs-lookup"><span data-stu-id="c4364-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4364-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4364-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c4364-155">Windows Vista, Windows XP con SP1 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="c4364-155">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="c4364-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4364-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c4364-157">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4364-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4364-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4364-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4364-159"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4364-159"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4364-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4364-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4364-161">Interfaz de control de retroiluminación</span><span class="sxs-lookup"><span data-stu-id="c4364-161">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="c4364-162">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="c4364-162">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

