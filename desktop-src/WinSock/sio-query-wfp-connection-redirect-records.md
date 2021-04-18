---
description: El código de control recupera el registro de redireccionamiento para la conexión TCP/IP aceptada para su uso por parte de un servicio de redireccionamiento de la plataforma de filtrado de Windows.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: Código de control de SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720479"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="43fcf-103">Código de control de SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS</span><span class="sxs-lookup"><span data-stu-id="43fcf-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="43fcf-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="43fcf-104">Description</span></span>

<span data-ttu-id="43fcf-105">El código de control de la conexión de WFP de la **consulta SiO recupera el registro \_ \_ \_ \_ \_** de redireccionamiento para la conexión TCP/IP aceptada para su uso por parte de un servicio de redireccionamiento de la plataforma de filtrado de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="43fcf-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code retrieves the redirect record for the accepted TCP/IP connection for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="43fcf-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="43fcf-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="43fcf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43fcf-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="43fcf-108">s</span><span class="sxs-lookup"><span data-stu-id="43fcf-108">s</span></span>

<span data-ttu-id="43fcf-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="43fcf-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="43fcf-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="43fcf-110">dwIoControlCode</span></span>

<span data-ttu-id="43fcf-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="43fcf-111">The control code for the operation.</span></span>
<span data-ttu-id="43fcf-112">Use **SiO \_ query \_ WFP \_ \_ redirigir \_ registros** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="43fcf-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="43fcf-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="43fcf-113">lpvInBuffer</span></span>

<span data-ttu-id="43fcf-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="43fcf-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="43fcf-115">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="43fcf-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="43fcf-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="43fcf-116">cbInBuffer</span></span>

<span data-ttu-id="43fcf-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="43fcf-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="43fcf-118">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="43fcf-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="43fcf-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="43fcf-119">lpvOutBuffer</span></span>

<span data-ttu-id="43fcf-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="43fcf-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="43fcf-121">Este parámetro debe apuntar a un tipo de datos **ULong** si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**.</span><span class="sxs-lookup"><span data-stu-id="43fcf-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="43fcf-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="43fcf-122">cbOutBuffer</span></span>

<span data-ttu-id="43fcf-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="43fcf-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="43fcf-124">Este parámetro debe ser al menos el tamaño de un tipo de datos **ULong** .</span><span class="sxs-lookup"><span data-stu-id="43fcf-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="43fcf-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="43fcf-125">lpcbBytesReturned</span></span>

<span data-ttu-id="43fcf-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="43fcf-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="43fcf-127">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="43fcf-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="43fcf-128">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="43fcf-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="43fcf-129">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="43fcf-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="43fcf-130">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="43fcf-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="43fcf-131">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="43fcf-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="43fcf-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="43fcf-132">lpvOverlapped</span></span>

<span data-ttu-id="43fcf-133">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="43fcf-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="43fcf-134">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="43fcf-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="43fcf-135">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="43fcf-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="43fcf-136">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="43fcf-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="43fcf-137">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="43fcf-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="43fcf-138">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="43fcf-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="43fcf-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="43fcf-139">lpCompletionRoutine</span></span>

<span data-ttu-id="43fcf-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="43fcf-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="43fcf-141">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="43fcf-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="43fcf-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="43fcf-142">lpThreadId</span></span>

<span data-ttu-id="43fcf-143">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="43fcf-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="43fcf-144">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="43fcf-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="43fcf-145">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="43fcf-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="43fcf-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="43fcf-146">lpErrno</span></span>

<span data-ttu-id="43fcf-147">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="43fcf-147">A pointer to the error code.</span></span>

<span data-ttu-id="43fcf-148">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="43fcf-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="43fcf-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43fcf-149">Return value</span></span>

<span data-ttu-id="43fcf-150">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="43fcf-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="43fcf-151">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="43fcf-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="43fcf-152">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="43fcf-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="43fcf-153">Código de error</span><span class="sxs-lookup"><span data-stu-id="43fcf-153">Error code</span></span> | <span data-ttu-id="43fcf-154">Significado</span><span class="sxs-lookup"><span data-stu-id="43fcf-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="43fcf-155">**ERROR \_ de \_ búfer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="43fcf-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="43fcf-156">El área de datos que se pasa a una llamada del sistema es demasiado pequeña.</span><span class="sxs-lookup"><span data-stu-id="43fcf-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="43fcf-157">Se devuelve este error si el búfer señalado por el parámetro *lpvOutBuffer* con un tamaño de búfer pasado en el parámetro *cbOutBuffer* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="43fcf-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="43fcf-158">El tamaño de búfer necesario se devolverá en el parámetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="43fcf-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="43fcf-159">**WSA_IO_PENDING**</span><span class="sxs-lookup"><span data-stu-id="43fcf-159">**WSA_IO_PENDING**</span></span> | <span data-ttu-id="43fcf-160">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="43fcf-160">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="43fcf-161">**WSA_OPERATION_ABORTED**</span><span class="sxs-lookup"><span data-stu-id="43fcf-161">**WSA_OPERATION_ABORTED**</span></span> | <span data-ttu-id="43fcf-162">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="43fcf-162">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="43fcf-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="43fcf-163">**WSAEFAULT**</span></span> | <span data-ttu-id="43fcf-164">Los parámetros *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no están totalmente contenidos en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="43fcf-164">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="43fcf-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="43fcf-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="43fcf-166">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="43fcf-166">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="43fcf-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="43fcf-167">**WSAEINTR**</span></span> | <span data-ttu-id="43fcf-168">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="43fcf-168">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="43fcf-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="43fcf-169">**WSAEINVAL**</span></span> | <span data-ttu-id="43fcf-170">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="43fcf-170">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="43fcf-171">Se devuelve este error si el parámetro *cbOutBuffer* es menor que el tamaño de un tipo de datos **ULong** .</span><span class="sxs-lookup"><span data-stu-id="43fcf-171">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="43fcf-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="43fcf-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="43fcf-173">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="43fcf-173">The network subsystem has failed.</span></span> |
| <span data-ttu-id="43fcf-174">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="43fcf-174">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="43fcf-175">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="43fcf-175">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="43fcf-176">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="43fcf-176">**WSAENOTCONN**</span></span> | <span data-ttu-id="43fcf-177">El socket *s* no está conectado.</span><span class="sxs-lookup"><span data-stu-id="43fcf-177">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="43fcf-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="43fcf-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="43fcf-179">El descriptor *s* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="43fcf-179">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="43fcf-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="43fcf-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="43fcf-181">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="43fcf-181">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="43fcf-182">Este error se devuelve si el proveedor de transporte no admite los registros de la conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** .</span><span class="sxs-lookup"><span data-stu-id="43fcf-182">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="43fcf-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43fcf-183">Remarks</span></span>

<span data-ttu-id="43fcf-184">Los registros de la conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** se admiten en Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="43fcf-184">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="43fcf-185">WFP permite el acceso a la ruta de procesamiento de paquetes TCP/IP, en la que se pueden examinar o cambiar los paquetes salientes y entrantes antes de permitir que se procesen más.</span><span class="sxs-lookup"><span data-stu-id="43fcf-185">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="43fcf-186">Al puntear en la ruta de acceso de procesamiento de TCP/IP, los fabricantes de software independientes (ISV) pueden crear más fácilmente firewalls, software antivirus, software de diagnóstico y otros tipos de aplicaciones y servicios.</span><span class="sxs-lookup"><span data-stu-id="43fcf-186">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="43fcf-187">WFP proporciona componentes en modo de usuario y de modo kernel para que los ISV de terceros puedan participar en las decisiones de filtrado que tienen lugar en varias capas de la pila de protocolos TCP/IP y en todo el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="43fcf-187">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="43fcf-188">La característica de redirección de conexión de WFP permite a un controlador de kernel de llamada de WFP redirigir una conexión localmente a un proceso de modo de usuario, realizar la inspección de contenido en modo de usuario y reenviar el contenido inspeccionado mediante una conexión diferente al destino original.</span><span class="sxs-lookup"><span data-stu-id="43fcf-188">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="43fcf-189">La opción **SiO Query de la \_ \_ \_ conexión WFP \_ \_ registra los registros** ioctl y otros ioctl relacionados son componentes de modo usuario que se usan para permitir que varias aplicaciones proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de forma cooperativa.</span><span class="sxs-lookup"><span data-stu-id="43fcf-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="43fcf-190">Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha inspeccionado otro agente de inspección.</span><span class="sxs-lookup"><span data-stu-id="43fcf-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="43fcf-191">Con la presencia de varios servidores proxy (desarrollados por fabricantes de software independientes, por ejemplo), la conexión utilizada por un proxy para comunicarse con el destino final podría redirigirse a su vez por un segundo proxy, y esa nueva conexión podría redirigirse de nuevo mediante el proxy original.</span><span class="sxs-lookup"><span data-stu-id="43fcf-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="43fcf-192">Sin el seguimiento de la conexión, la conexión original podría no llegar nunca a su destino final, ya que se bloquea en un bucle proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="43fcf-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="43fcf-193">Los registros de la conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** se usan para proporcionar el seguimiento de la conexión de proxy en las conexiones de socket redirigido.</span><span class="sxs-lookup"><span data-stu-id="43fcf-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="43fcf-194">Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.</span><span class="sxs-lookup"><span data-stu-id="43fcf-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="43fcf-195">El servicio de redireccionamiento basado en WFP usa el servicio de redirección basada en WFP para recuperar el registro de redireccionamiento de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo), se le redirigió mediante su llamada de modo kernel asociada a **ALE_CONNECT_REDIRECT** capas en un controlador de modo kernel. **\_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="43fcf-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE_CONNECT_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="43fcf-196">El servicio de redirección basada en WFP usa el contexto de redireccionamiento de **\_ \_ \_ conexión \_ \_ WFP de la consulta SiO** para recuperar el contexto de redireccionamiento de un registro de redirección de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo) redirigido a él mediante su llamada complementaria registrada en las capas de **\_ \_ redirección de Ale** .</span><span class="sxs-lookup"><span data-stu-id="43fcf-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE\_CONNECT\_REDIRECT** layers.</span></span>
<span data-ttu-id="43fcf-197">El contexto de redireccionamiento es un contexto opcional asignado por el controlador que se usa si el estado de redirección actual de una conexión es que la conexión se redirigió mediante el servicio de redireccionamiento de llamada o la conexión se redirigió previamente mediante el servicio de redireccionamiento de llamada, pero posteriormente se redirigió de nuevo mediante otro servicio de redirección.</span><span class="sxs-lookup"><span data-stu-id="43fcf-197">The redirect context is an optional driver-allocated context used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="43fcf-198">En el caso de una conexión de proxy TCP, el servicio de redirección transfiere el registro de redirección recuperado al socket TCP que usa para crear el proxy del contenido original mediante el protocolo **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** .</span><span class="sxs-lookup"><span data-stu-id="43fcf-198">For a TCP proxy connection, the redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="43fcf-199">Cuando el servicio de redirección está redirigiendo a un socket que no es TCP (por ejemplo, UDP), los registros de redireccionamiento devueltos por la conexión de la conexión de WFP de la **consulta SiO indican a este servicio el \_ \_ \_ \_ \_** servicio de redireccionamiento mediante la estructura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) utilizada con la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="43fcf-199">When the redirect service is redirecting a non-TCP socket (UDP, for example), the redirect records returned by the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL indicate this to the redirect service using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure used with the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>
<span data-ttu-id="43fcf-200">El miembro de control de la estructura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) tendría un cmsg_type en la estructura **WSACMSGHDR** establecida en **\_ \_ \_ registro de redirección de conexión IP**.</span><span class="sxs-lookup"><span data-stu-id="43fcf-200">The Control member of the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure would have a cmsg_type in the **WSACMSGHDR** structure set to **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="43fcf-201">El servicio de redirección debe proporcionar el parámetro [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) al aceptar redirecciones que no son TCP.</span><span class="sxs-lookup"><span data-stu-id="43fcf-201">The [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) parameter must be supplied by the redirect service when accepting non-TCP redirects.</span></span>

<span data-ttu-id="43fcf-202">Para el tráfico que no es TCP, el registro de redireccionamiento se reenvía mediante la estructura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) con la función [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="43fcf-202">For non-TCP traffic, the redirect record is forwarded using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure with the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) function.</span></span>

<span data-ttu-id="43fcf-203">Tenga en cuenta que para el tráfico que no es TCP, solo el paquete de creación de flujo llevará el **\_ \_ \_ registro de redirección de la conexión IP**.</span><span class="sxs-lookup"><span data-stu-id="43fcf-203">Note that for non-TCP traffic, only the flow-creating packet will carry the **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="43fcf-204">Como resultado, solo el primer paquete de proxy debe incluir esta información mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="43fcf-204">As a result, only the first proxied packet needs to include this information using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>

<span data-ttu-id="43fcf-205">Dado que el registro de redirección de WFP es un BLOB de datos de longitud variable, el autor de la llamada puede proporcionar un búfer de salida de gran tamaño (por ejemplo, un búfer de 1.024 bytes al que apunta el parámetro *lpvOutBuffer* ) o puede pasar un tamaño de búfer de salida en el parámetro *cbOutBuffer* de 0 para consultar el tamaño de búfer necesario para contener el BLOB devuelto.</span><span class="sxs-lookup"><span data-stu-id="43fcf-205">Since the WFP redirect record is a variable length data blob, the caller can either supply a large output buffer (a 1,024 byte buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="43fcf-206">Si el tamaño del búfer de salida no es suficiente para almacenar los datos, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devolverán un **error de \_ \_ búfer insuficiente** y se devolverá el tamaño de búfer necesario en el valor al que apunta el parámetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="43fcf-206">If the output buffer size is not sufficient to the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="43fcf-207">La aplicación que llama a la [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) no necesita comprender el BLOB que contiene el contexto de redireccionamiento recuperado.</span><span class="sxs-lookup"><span data-stu-id="43fcf-207">The application calling the [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) does not need to understand the blob containing the redirect context retrieved.</span></span>
<span data-ttu-id="43fcf-208">Se trata de un BLOB opaco de datos que la aplicación necesita recuperar y devolver al nuevo socket.</span><span class="sxs-lookup"><span data-stu-id="43fcf-208">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="43fcf-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="43fcf-209">See also</span></span>

[<span data-ttu-id="43fcf-210">**Opciones de IPPROTO_IP socket**</span><span class="sxs-lookup"><span data-stu-id="43fcf-210">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="43fcf-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="43fcf-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="43fcf-212">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="43fcf-212">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="43fcf-213">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="43fcf-213">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="43fcf-214">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="43fcf-214">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="43fcf-215">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="43fcf-215">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="43fcf-216">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="43fcf-216">**WSAMSG**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[<span data-ttu-id="43fcf-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="43fcf-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="43fcf-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="43fcf-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[<span data-ttu-id="43fcf-219">**WSASendMsg**</span><span class="sxs-lookup"><span data-stu-id="43fcf-219">**WSASendMsg**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[<span data-ttu-id="43fcf-220">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="43fcf-220">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="43fcf-221">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="43fcf-221">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
