---
description: El \_ \_ código de control de LMR de ioctl deshabilitar el \_ \_ código de control de almacenamiento en búfer local deshabilita el almacenamiento en caché en memoria del cliente local al leer o escribir datos en un archivo remoto. Este es un código de control definido internamente que no está disponible en un encabezado público.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: Código de control de IOCTL_LMR_DISABLE_LOCAL_BUFFERING
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648159"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a><span data-ttu-id="a160b-104">IOCTL \_ LMR \_ deshabilitar el \_ \_ código de control de almacenamiento en búfer local</span><span class="sxs-lookup"><span data-stu-id="a160b-104">IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING control code</span></span>

<span data-ttu-id="a160b-105">El código de control de LMR de ioctl deshabilitar el código de control de **\_ almacenamiento en \_ \_ \_ búfer local** deshabilita el almacenamiento en caché en memoria del cliente local al leer o escribir datos en un archivo remoto.</span><span class="sxs-lookup"><span data-stu-id="a160b-105">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code disables local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="a160b-106">Este es un código de control definido internamente que no está disponible en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="a160b-106">This is an internally-defined control code not available in a public header.</span></span>

<span data-ttu-id="a160b-107">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="a160b-107">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="a160b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a160b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a160b-109">*hDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a160b-109">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a160b-110">Identificador del archivo remoto.</span><span class="sxs-lookup"><span data-stu-id="a160b-110">A handle to the remote file.</span></span> <span data-ttu-id="a160b-111">Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="a160b-111">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="a160b-112">*dwIoControlCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a160b-112">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a160b-113">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="a160b-113">The control code for the operation.</span></span> <span data-ttu-id="a160b-114">Use el valor 0x140390 para esta operación.</span><span class="sxs-lookup"><span data-stu-id="a160b-114">Use the value 0x140390 for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a160b-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="a160b-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a160b-116">No se utiliza, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a160b-116">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a160b-117">*nInBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a160b-117">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a160b-118">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a160b-118">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="a160b-119">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a160b-119">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a160b-120">*lpOutBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a160b-120">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a160b-121">No se utiliza, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a160b-121">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a160b-122">*nOutBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a160b-122">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a160b-123">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a160b-123">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="a160b-124">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a160b-124">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a160b-125">*lpBytesReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a160b-125">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a160b-126">Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a160b-126">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="a160b-127">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el **error \_ \_ búfer insuficiente** y *lpBytesReturned* es cero.</span><span class="sxs-lookup"><span data-stu-id="a160b-127">If the output buffer is too small, then the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="a160b-128">Si el parámetro *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a160b-128">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="a160b-129">Incluso cuando una operación no devuelve datos de salida y el parámetro *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="a160b-129">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="a160b-130">Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="a160b-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="a160b-131">Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a160b-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="a160b-132">Si *lpOverlapped* no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="a160b-132">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="a160b-133">Para recuperar el número de bytes devueltos, llame a la función [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="a160b-133">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="a160b-134">Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a160b-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="a160b-135">*lpOverlapped* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a160b-135">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a160b-136">Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a160b-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a160b-137">Si el parámetro *hDevice* se ha abierto sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="a160b-137">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="a160b-138">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="a160b-138">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="a160b-139">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="a160b-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="a160b-140">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="a160b-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="a160b-141">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="a160b-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="a160b-142">De lo contrario, la función no devuelve ningún resultado hasta que la operación se haya completado o hasta que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="a160b-142">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a160b-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a160b-143">Return value</span></span>

<span data-ttu-id="a160b-144">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a160b-144">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="a160b-145">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a160b-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="a160b-146">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a160b-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a160b-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a160b-147">Remarks</span></span>

<span data-ttu-id="a160b-148">El sistema define internamente el código de control de **\_ almacenamiento en \_ \_ \_ búfer local de ioctl LMR** como 0x140390 y no en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="a160b-148">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code is defined internally by the system as 0x140390 and not in a public header file.</span></span> <span data-ttu-id="a160b-149">Lo usan las aplicaciones de uso especial para deshabilitar el almacenamiento en caché local en memoria de los datos al leer o escribir datos en un archivo remoto.</span><span class="sxs-lookup"><span data-stu-id="a160b-149">It is used by special-purpose applications to disable local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="a160b-150">Una vez deshabilitado el almacenamiento en búfer local, el valor permanece en vigor hasta que se cierren todos los identificadores abiertos del archivo y el redirector Limpie sus estructuras de datos internas.</span><span class="sxs-lookup"><span data-stu-id="a160b-150">After local buffering is disabled, the setting remains in effect until all open handles to the file are closed and the redirector cleans up its internal data structures.</span></span>

<span data-ttu-id="a160b-151">Las aplicaciones de uso general no deben usar **ioctl \_ LMR \_ deshabilitar el almacenamiento en \_ \_ búfer local**, ya que esto puede provocar un tráfico excesivo de red y una pérdida de rendimiento asociada.</span><span class="sxs-lookup"><span data-stu-id="a160b-151">General-purpose applications should not use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING**, because it can result in excessive network traffic and associated loss of performance.</span></span> <span data-ttu-id="a160b-152">La LMR de ioctl deshabilitar el código de control de **\_ almacenamiento en \_ \_ \_ búfer local** solo debe usarse en aplicaciones especializadas que mueven grandes cantidades de datos a través de la red al intentar maximizar el uso del ancho de banda de red.</span><span class="sxs-lookup"><span data-stu-id="a160b-152">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code should be used only in specialized applications moving large amounts of data over the network while attempting to maximize use of network bandwidth.</span></span> <span data-ttu-id="a160b-153">Por ejemplo, las funciones [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) y [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) usan **ioctl \_ LMR \_ deshabilitar el \_ almacenamiento en \_ búfer local** para mejorar el rendimiento de la copia de archivos de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="a160b-153">For example, the [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) and [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) functions use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** to improve large file copy performance.</span></span>

<span data-ttu-id="a160b-154">**Ioctl \_ LMR \_ deshabilitar el \_ \_ almacenamiento en búfer local** no está implementado por sistemas de archivos locales y se producirá un error con la **\_ \_ función no válida**.</span><span class="sxs-lookup"><span data-stu-id="a160b-154">**IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** is not implemented by local file systems and will fail with the error **ERROR\_INVALID\_FUNCTION**.</span></span> <span data-ttu-id="a160b-155">Si se emite el código de control de **\_ almacenamiento en \_ \_ \_ búfer local de ioctl LMR** en los identificadores de directorio remoto, se producirá un **error que no se \_ \_ admite**.</span><span class="sxs-lookup"><span data-stu-id="a160b-155">Issuing the **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code on remote directory handles will fail with the error **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a160b-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="a160b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a160b-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="a160b-157">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
