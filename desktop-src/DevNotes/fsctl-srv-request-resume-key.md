---
description: El código de control de la \_ \_ clave de la solicitud del archivo FSCTL SRV \_ \_ se usa para recuperar una referencia de archivo opaca para su uso con el \_ código de control COPYCHUNK de ioctl.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Código de control de FSCTL_SRV_REQUEST_RESUME_KEY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906996"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a><span data-ttu-id="045b3-103">\_Código de \_ control de \_ clave de recuperación de solicitud \_ de FSCTL SRV</span><span class="sxs-lookup"><span data-stu-id="045b3-103">FSCTL\_SRV\_REQUEST\_RESUME\_KEY control code</span></span>

<span data-ttu-id="045b3-104">El código de control de la clave de la solicitud del archivo **FSCTL \_ SRV \_ \_ \_** se usa para recuperar una referencia de archivo opaca para su uso con el código de control [**\_ COPYCHUNK de ioctl**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="045b3-104">The **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** control code is used to retrieve an opaque file reference for use with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span>

<span data-ttu-id="045b3-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="045b3-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="045b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="045b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="045b3-107">*hDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="045b3-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="045b3-108">Identificador del archivo para el que se va a solicitar la clave del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="045b3-108">A handle to the file for which the source file key is to be requested.</span></span> <span data-ttu-id="045b3-109">Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="045b3-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="045b3-110">*dwIoControlCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="045b3-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="045b3-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="045b3-111">The control code for the operation.</span></span> <span data-ttu-id="045b3-112">Use **la \_ \_ \_ \_ clave de reanudación de solicitud de FSCTL SRV** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="045b3-112">Use **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="045b3-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="045b3-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="045b3-114">No se utiliza con esta operación; se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="045b3-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="045b3-115">*nInBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="045b3-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="045b3-116">No se utiliza con esta operación; se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="045b3-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="045b3-117">*lpOutBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="045b3-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="045b3-118">Un puntero al búfer de salida, una estructura de **\_ \_ \_ clave de reanudación de solicitud SRV** .</span><span class="sxs-lookup"><span data-stu-id="045b3-118">A pointer to the output buffer, a **SRV\_REQUEST\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="045b3-119">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="045b3-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="045b3-120">*nOutBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="045b3-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="045b3-121">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="045b3-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="045b3-122">*lpBytesReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="045b3-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="045b3-123">Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="045b3-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="045b3-124">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente** y *lpBytesReturned* es cero.</span><span class="sxs-lookup"><span data-stu-id="045b3-124">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="045b3-125">Si el parámetro *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="045b3-125">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="045b3-126">Incluso cuando una operación no devuelve datos de salida y el parámetro *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="045b3-126">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="045b3-127">Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="045b3-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="045b3-128">Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="045b3-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="045b3-129">Si *lpOverlapped* no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="045b3-129">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="045b3-130">Para recuperar el número de bytes devueltos, llame a la función [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="045b3-130">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="045b3-131">Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="045b3-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="045b3-132">*lpOverlapped* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="045b3-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="045b3-133">Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="045b3-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="045b3-134">Si el parámetro *hDevice* se ha abierto sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="045b3-134">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="045b3-135">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="045b3-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="045b3-136">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="045b3-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="045b3-137">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="045b3-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="045b3-138">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="045b3-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="045b3-139">De lo contrario, la función no devuelve ningún resultado hasta que la operación se haya completado o hasta que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="045b3-139">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="045b3-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="045b3-140">Return value</span></span>

<span data-ttu-id="045b3-141">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="045b3-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="045b3-142">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="045b3-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="045b3-143">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="045b3-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="045b3-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="045b3-144">Remarks</span></span>

<span data-ttu-id="045b3-145">Este código de control no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="045b3-145">This control code has no associated header file.</span></span> <span data-ttu-id="045b3-146">Debe definir el código de control y las estructuras de datos como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="045b3-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

<span data-ttu-id="045b3-147">Estos miembros se pueden describir como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="045b3-147">These members can be described as follows.</span></span>



| <span data-ttu-id="045b3-148">Miembro</span><span class="sxs-lookup"><span data-stu-id="045b3-148">Member</span></span>                                                                                                                       | <span data-ttu-id="045b3-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="045b3-149">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="045b3-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span><span class="sxs-lookup"><span data-stu-id="045b3-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span></span><br/>                 | <span data-ttu-id="045b3-151">Un valor opaco que identifica el archivo de origen en el servidor.</span><span class="sxs-lookup"><span data-stu-id="045b3-151">An opaque value that identifies the source file to the server.</span></span><br/>                                                                                                   |
| <span data-ttu-id="045b3-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="045b3-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span></span><br/>                 | <span data-ttu-id="045b3-153">Un valor opaco que identifica la hora en que se abrió el archivo.</span><span class="sxs-lookup"><span data-stu-id="045b3-153">An opaque value that identifies the time when the file was opened.</span></span><br/>                                                                                               |
| <span data-ttu-id="045b3-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**ID**</span><span class="sxs-lookup"><span data-stu-id="045b3-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span></span><br/>                                         | <span data-ttu-id="045b3-155">Un valor opaco que identifica el proceso que abrió el archivo.</span><span class="sxs-lookup"><span data-stu-id="045b3-155">An opaque value that identifies the process that opened the file.</span></span><br/>                                                                                                |
| <span data-ttu-id="045b3-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Clave**</span><span class="sxs-lookup"><span data-stu-id="045b3-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Key**</span></span><br/>                                         | <span data-ttu-id="045b3-157">Una estructura de **\_ \_ clave de reanudación de SRV** .</span><span class="sxs-lookup"><span data-stu-id="045b3-157">A **SRV\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="045b3-158">Para realizar una operación de copia en el lado servidor, use esta estructura con el código de control [**ioctl \_ COPYCHUNK**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="045b3-158">To perform a server-side copy operation, use this structure with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span><br/> |
| <span data-ttu-id="045b3-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span><span class="sxs-lookup"><span data-stu-id="045b3-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span></span><br/> | <span data-ttu-id="045b3-160">Este miembro está reservado para uso del sistema. No use.</span><span class="sxs-lookup"><span data-stu-id="045b3-160">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |
| <span data-ttu-id="045b3-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contexto**</span><span class="sxs-lookup"><span data-stu-id="045b3-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Context**</span></span><br/>                         | <span data-ttu-id="045b3-162">Este miembro está reservado para uso del sistema. No use.</span><span class="sxs-lookup"><span data-stu-id="045b3-162">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |



 

## <a name="see-also"></a><span data-ttu-id="045b3-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="045b3-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045b3-164">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="045b3-164">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="045b3-165">**IOCTL \_ COPYCHUNK**</span><span class="sxs-lookup"><span data-stu-id="045b3-165">**IOCTL\_COPYCHUNK**</span></span>](ioctl-copychunk.md)
</dt> </dl>

 

 
