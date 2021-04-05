---
description: Establece los niveles de retroiluminación de AC y DC actuales.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: Código de control de IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001956"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a><span data-ttu-id="cacc7-103">Juego de vídeo de IOCTL \_ \_ \_ Mostrar \_ código de control de brillo</span><span class="sxs-lookup"><span data-stu-id="cacc7-103">IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="cacc7-104">Establece los niveles de retroiluminación de AC y DC actuales.</span><span class="sxs-lookup"><span data-stu-id="cacc7-104">Sets the current AC and DC backlight levels.</span></span>

<span data-ttu-id="cacc7-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="cacc7-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="cacc7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cacc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cacc7-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="cacc7-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-108">Identificador de \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="cacc7-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="cacc7-109">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="cacc7-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="cacc7-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="cacc7-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="cacc7-111">The control code for the operation.</span></span> <span data-ttu-id="cacc7-112">Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="cacc7-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="cacc7-113">Use el brillo de la pantalla del conjunto de vídeos de ioctl para esta operación. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cacc7-113">Use **IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="cacc7-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="cacc7-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-115">Puntero a una estructura [**de \_ brillo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cacc7-115">A pointer to a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cacc7-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="cacc7-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-117">Tamaño del búfer al que apunta *lpOutBuffer*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cacc7-117">The size of the buffer pointed to by *lpOutBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cacc7-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="cacc7-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-119">No se utiliza con esta operación; se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="cacc7-119">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cacc7-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="cacc7-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-121">No se utiliza con esta operación; se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="cacc7-121">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cacc7-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="cacc7-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-123">Puntero a una variable que recibe el recuento real de bytes devueltos por la función en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="cacc7-123">A pointer to a variable that receives the actual count of bytes returned by the function in the output buffer.</span></span>

<span data-ttu-id="cacc7-124">Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* se usa internamente y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cacc7-124">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* is used internally and cannot be **NULL**.</span></span>

<span data-ttu-id="cacc7-125">Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cacc7-125">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cacc7-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="cacc7-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="cacc7-127">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="cacc7-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="cacc7-128">Si *hDevice* se abrió con la marca de indicador de archivo \_ \_ superpuesto, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="cacc7-128">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="cacc7-129">En este caso, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="cacc7-129">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="cacc7-130">Si el dispositivo se ha abierto con la \_ marca de indicador de archivo \_ superpuesto y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.</span><span class="sxs-lookup"><span data-stu-id="cacc7-130">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="cacc7-131">Si se abrió *hDevice* sin especificar la marca de la marca de archivo \_ \_ superpuesta, se omite *lpOverlapped* y [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no devuelve ningún resultado hasta que se haya completado la operación o hasta que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="cacc7-131">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cacc7-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cacc7-132">Return value</span></span>

<span data-ttu-id="cacc7-133">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cacc7-133">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="cacc7-134">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cacc7-134">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="cacc7-135">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cacc7-135">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="cacc7-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cacc7-136">Remarks</span></span>

<span data-ttu-id="cacc7-137">Los valores especificados en los miembros **ucACBrightness** y **ucDCBrightness** de la estructura de [**\_ brillo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de la pantalla deben haber sido devueltos previamente por el [**\_ \_ \_ \_ brillo compatible con la consulta de vídeo ioctl**](ioctl-video-query-supported-brightness.md).</span><span class="sxs-lookup"><span data-stu-id="cacc7-137">The values specified in the **ucACBrightness** and **ucDCBrightness** members of the [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure must have been previously returned by [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md).</span></span> <span data-ttu-id="cacc7-138">Por ejemplo, si los valores admitidos son 10, 20, 30, 40, 50, 60, 70, 80, 90 y 100, el uso de un valor de 33 sería un error.</span><span class="sxs-lookup"><span data-stu-id="cacc7-138">For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.</span></span>

<span data-ttu-id="cacc7-139">El archivo de encabezado utilizado para compilar aplicaciones que incluyen esta funcionalidad, Ntddvdeo. h, se incluye en el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cacc7-139">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="cacc7-140">Para obtener información sobre cómo obtener el DDK, vea [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="cacc7-140">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="cacc7-141">Como alternativa, puede definir este código de control como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cacc7-141">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="cacc7-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cacc7-142">Requirements</span></span>



| <span data-ttu-id="cacc7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="cacc7-143">Requirement</span></span> | <span data-ttu-id="cacc7-144">Value</span><span class="sxs-lookup"><span data-stu-id="cacc7-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cacc7-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cacc7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="cacc7-146">Windows Vista, Windows XP con SP1 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="cacc7-146">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="cacc7-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cacc7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="cacc7-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cacc7-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cacc7-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cacc7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="cacc7-150"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="cacc7-150"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cacc7-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="cacc7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cacc7-152">Interfaz de control de retroiluminación</span><span class="sxs-lookup"><span data-stu-id="cacc7-152">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="cacc7-153">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="cacc7-153">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="cacc7-154">[**brillo de la pantalla \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cacc7-154">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cacc7-155">**\_brillo de \_ visualización de consulta de vídeo ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cacc7-155">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)
</dt> <dt>

[<span data-ttu-id="cacc7-156">**\_ \_ \_ brillo compatible con consulta de vídeo ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="cacc7-156">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

