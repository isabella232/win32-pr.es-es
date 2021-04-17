---
description: El \_ código de control COPYCHUNK de ioctl inicia una copia del lado servidor de un intervalo de datos, también denominado fragmento.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Código de control de IOCTL_COPYCHUNK
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666161"
---
# <a name="ioctl_copychunk-control-code"></a><span data-ttu-id="e753d-103">\_Código de control COPYCHUNK de ioctl</span><span class="sxs-lookup"><span data-stu-id="e753d-103">IOCTL\_COPYCHUNK control code</span></span>

<span data-ttu-id="e753d-104">El código de control **\_ COPYCHUNK de ioctl** inicia una copia del lado servidor de un intervalo de datos, también denominado fragmento.</span><span class="sxs-lookup"><span data-stu-id="e753d-104">The **IOCTL\_COPYCHUNK** control code initiates a server-side copy of a range of data, also called a chunk.</span></span>

<span data-ttu-id="e753d-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="e753d-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="e753d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e753d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e753d-107">*hDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e753d-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e753d-108">Identificador del archivo que es el destino de la operación de copia del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="e753d-108">A handle to the file that is the target of the server-side copy operation.</span></span> <span data-ttu-id="e753d-109">Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="e753d-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="e753d-110">*dwIoControlCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e753d-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e753d-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="e753d-111">The control code for the operation.</span></span> <span data-ttu-id="e753d-112">Use **ioctl \_ COPYCHUNK** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="e753d-112">Use **IOCTL\_COPYCHUNK** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="e753d-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="e753d-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="e753d-114">Un puntero al búfer de entrada, una estructura de **\_ \_ copia de COPYCHUNK SRV** .</span><span class="sxs-lookup"><span data-stu-id="e753d-114">A pointer to the input buffer, a **SRV\_COPYCHUNK\_COPY** structure.</span></span> <span data-ttu-id="e753d-115">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e753d-115">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="e753d-116">*nInBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e753d-116">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e753d-117">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e753d-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e753d-118">*lpOutBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e753d-118">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e753d-119">Un puntero al búfer de salida, una estructura de **\_ \_ respuesta COPYCHUNK SRV** .</span><span class="sxs-lookup"><span data-stu-id="e753d-119">A pointer to the output buffer, a **SRV\_COPYCHUNK\_RESPONSE** structure.</span></span> <span data-ttu-id="e753d-120">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e753d-120">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="e753d-121">*nOutBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e753d-121">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e753d-122">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e753d-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e753d-123">*lpBytesReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e753d-123">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e753d-124">Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e753d-124">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="e753d-125">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente** y *lpBytesReturned* es cero.</span><span class="sxs-lookup"><span data-stu-id="e753d-125">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="e753d-126">Si el parámetro *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="e753d-126">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="e753d-127">Incluso cuando una operación no devuelve datos de salida y el parámetro *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="e753d-127">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="e753d-128">Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="e753d-128">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="e753d-129">Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="e753d-129">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="e753d-130">Si *lpOverlapped* no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="e753d-130">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="e753d-131">Para recuperar el número de bytes devueltos, llame a la función [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="e753d-131">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="e753d-132">Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="e753d-132">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="e753d-133">*lpOverlapped* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e753d-133">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e753d-134">Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="e753d-134">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="e753d-135">Si el parámetro *hDevice* se ha abierto sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="e753d-135">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="e753d-136">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="e753d-136">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="e753d-137">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="e753d-137">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="e753d-138">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="e753d-138">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="e753d-139">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="e753d-139">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="e753d-140">De lo contrario, la función no devuelve ningún resultado hasta que la operación se haya completado o hasta que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="e753d-140">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e753d-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e753d-141">Return value</span></span>

<span data-ttu-id="e753d-142">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e753d-142">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="e753d-143">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e753d-143">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="e753d-144">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="e753d-144">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e753d-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e753d-145">Remarks</span></span>

<span data-ttu-id="e753d-146">Este código de control no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="e753d-146">This control code has no associated header file.</span></span> <span data-ttu-id="e753d-147">Debe definir el código de control y las estructuras de datos como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e753d-147">You must define the control code and data structures as follows.</span></span>

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

<span data-ttu-id="e753d-148">Estos miembros se pueden describir como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e753d-148">These members can be described as follows.</span></span>



| <span data-ttu-id="e753d-149">Miembro</span><span class="sxs-lookup"><span data-stu-id="e753d-149">Member</span></span>                                                                                                                                       | <span data-ttu-id="e753d-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="e753d-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e753d-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span><span class="sxs-lookup"><span data-stu-id="e753d-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span></span><br/>                     | <span data-ttu-id="e753d-152">Desplazamiento, en bytes, desde el principio del archivo de código fuente hasta el fragmento que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="e753d-152">The offset, in bytes, from the beginning of the source file to the chunk to be copied.</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e753d-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span><span class="sxs-lookup"><span data-stu-id="e753d-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span></span><br/> | <span data-ttu-id="e753d-154">Desplazamiento, en bytes, desde el principio del archivo de destino hasta la ubicación donde se va a copiar el fragmento.</span><span class="sxs-lookup"><span data-stu-id="e753d-154">The offset, in bytes, from the beginning of the target file to the location where the chunk is to be copied.</span></span><br/>                                                                                                                                                                                                                                               |
| <span data-ttu-id="e753d-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Longitud**</span><span class="sxs-lookup"><span data-stu-id="e753d-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Length**</span></span><br/>                                             | <span data-ttu-id="e753d-156">El número de bytes de datos en el fragmento que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="e753d-156">The number of bytes of data in the chunk to be copied.</span></span> <span data-ttu-id="e753d-157">Debe ser mayor que cero y menor o igual que 1 MB.</span><span class="sxs-lookup"><span data-stu-id="e753d-157">Must be greater than zero and less than or equal to 1 MB.</span></span> <span data-ttu-id="e753d-158">**Longitud** \* **ChunkCount** debe ser menor o igual que 16 MB.</span><span class="sxs-lookup"><span data-stu-id="e753d-158">**Length** \* **ChunkCount** must be less than or equal to 16 MB.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="e753d-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="e753d-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span></span><br/>                             | <span data-ttu-id="e753d-160">Clave que representa el archivo de código fuente con los datos que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="e753d-160">A key that represents the source file with the data to be copied.</span></span> <span data-ttu-id="e753d-161">Esta clave se obtiene a través de la [**\_ \_ \_ \_ clave de reanudación de solicitud de FSCTL SRV**](fsctl-srv-request-resume-key.md).</span><span class="sxs-lookup"><span data-stu-id="e753d-161">This key is obtained through [**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**](fsctl-srv-request-resume-key.md).</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="e753d-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span><span class="sxs-lookup"><span data-stu-id="e753d-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span></span><br/>                             | <span data-ttu-id="e753d-163">El número de fragmentos que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="e753d-163">The number of chunks to be copied.</span></span> <span data-ttu-id="e753d-164">Debe ser mayor que cero y menor o igual que 256.</span><span class="sxs-lookup"><span data-stu-id="e753d-164">Must be greater than zero and less than or equal to 256.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="e753d-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Sector**</span><span class="sxs-lookup"><span data-stu-id="e753d-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved**</span></span><br/>                                     | <span data-ttu-id="e753d-166">Este miembro está reservado para uso del sistema. No use.</span><span class="sxs-lookup"><span data-stu-id="e753d-166">This member is reserved for system use; do not use.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e753d-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Paquete**</span><span class="sxs-lookup"><span data-stu-id="e753d-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Chunk**</span></span><br/>                                                 | <span data-ttu-id="e753d-168">Una matriz de estructuras **ChunkCount** **SRV \_ COPYCHUNK** , una para cada fragmento que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="e753d-168">An array of **ChunkCount** **SRV\_COPYCHUNK** structures, one for each chunk to be copied.</span></span> <span data-ttu-id="e753d-169">La longitud, en bytes, de esta matriz debe ser **ChunkCount** \* sizeof (**SRV \_ COPYCHUNK**).</span><span class="sxs-lookup"><span data-stu-id="e753d-169">The length, in bytes, of this array must be **ChunkCount** \* sizeof(**SRV\_COPYCHUNK**).</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="e753d-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span><span class="sxs-lookup"><span data-stu-id="e753d-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span></span><br/>                 | <span data-ttu-id="e753d-171">Si se produjo un error en la operación con un **\_ \_ parámetro no válido**, este valor indica el número máximo de fragmentos que el servidor aceptará en una única solicitud, que es 256.</span><span class="sxs-lookup"><span data-stu-id="e753d-171">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of chunks the server will accept in a single request, which is 256.</span></span> <span data-ttu-id="e753d-172">De lo contrario, este valor indica el número de fragmentos que se escribieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="e753d-172">Otherwise, this value indicates the number of chunks that were successfully written.</span></span><br/>                                                                                               |
| <span data-ttu-id="e753d-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="e753d-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span></span><br/> | <span data-ttu-id="e753d-174">Si se produjo un error en la operación con un **\_ \_ parámetro no válido**, este valor indica el número máximo de bytes que el servidor permitirá escribir en un único fragmento, que es 1 MB.</span><span class="sxs-lookup"><span data-stu-id="e753d-174">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will allow to be written in a single chunk, which is 1 MB.</span></span> <span data-ttu-id="e753d-175">De lo contrario, este valor indica el número de bytes que se escribieron correctamente en el último fragmento que no se procesó correctamente (si se produjo una escritura parcial).</span><span class="sxs-lookup"><span data-stu-id="e753d-175">Otherwise, this value indicates the number of bytes that were successfully written in the last chunk that was not successfully processed (if a partial write occurred).</span></span><br/> |
| <span data-ttu-id="e753d-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="e753d-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span></span><br/> | <span data-ttu-id="e753d-177">Si se produjo un error en la operación con un **\_ \_ parámetro no válido**, este valor indica el número máximo de bytes que el servidor copiará en una única solicitud, que es de 16 MB.</span><span class="sxs-lookup"><span data-stu-id="e753d-177">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will copy in a single request, which is 16 MB.</span></span> <span data-ttu-id="e753d-178">De lo contrario, este valor indica el número de bytes que se escribieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="e753d-178">Otherwise, this value indicates the number of bytes that were successfully written.</span></span><br/>                                                                                                 |



 

## <a name="see-also"></a><span data-ttu-id="e753d-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="e753d-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e753d-180">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="e753d-180">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="e753d-181">**\_clave de \_ \_ reanudación de solicitud \_ de FSCTL SRV**</span><span class="sxs-lookup"><span data-stu-id="e753d-181">**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**</span></span>](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
