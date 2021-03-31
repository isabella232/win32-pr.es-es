---
description: El código de control recupera el contexto de redirección para un registro de redireccionamiento usado por un servicio de redirección de la plataforma de filtrado de Windows.
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: Código de control de SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 1e5e5f6c56411ada1e87e8cdf240a89f9c293e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154251"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a><span data-ttu-id="098e1-103">Código de control de SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="098e1-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Control Code</span></span>

## <a name="description"></a><span data-ttu-id="098e1-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="098e1-104">Description</span></span>

<span data-ttu-id="098e1-105">El código de control de contexto de redirección de conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** recupera el contexto de redireccionamiento para un registro de redirección utilizado por un servicio de redirección de la plataforma de filtrado de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="098e1-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** control code retrieves the redirect context for a redirect record used by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="098e1-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="098e1-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure 
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="098e1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="098e1-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="098e1-108">s</span><span class="sxs-lookup"><span data-stu-id="098e1-108">s</span></span>

<span data-ttu-id="098e1-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="098e1-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="098e1-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="098e1-110">dwIoControlCode</span></span>

<span data-ttu-id="098e1-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="098e1-111">The control code for the operation.</span></span>
<span data-ttu-id="098e1-112">Utilice **la \_ consulta \_ SiO \_ \_ \_ contexto de redireccionamiento de conexión de WFP** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="098e1-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="098e1-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="098e1-113">lpvInBuffer</span></span>

<span data-ttu-id="098e1-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="098e1-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="098e1-115">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="098e1-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="098e1-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="098e1-116">cbInBuffer</span></span>

<span data-ttu-id="098e1-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="098e1-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="098e1-118">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="098e1-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="098e1-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="098e1-119">lpvOutBuffer</span></span>

<span data-ttu-id="098e1-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="098e1-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="098e1-121">Este parámetro debe apuntar a un tipo de datos **ULong** si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**.</span><span class="sxs-lookup"><span data-stu-id="098e1-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="098e1-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="098e1-122">cbOutBuffer</span></span>

<span data-ttu-id="098e1-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="098e1-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="098e1-124">Este parámetro debe ser al menos el tamaño de un tipo de datos **ULong** .</span><span class="sxs-lookup"><span data-stu-id="098e1-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="098e1-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="098e1-125">lpcbBytesReturned</span></span>

<span data-ttu-id="098e1-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="098e1-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="098e1-127">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="098e1-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="098e1-128">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="098e1-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="098e1-129">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="098e1-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="098e1-130">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="098e1-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="098e1-131">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="098e1-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="098e1-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="098e1-132">lpvOverlapped</span></span>

<span data-ttu-id="098e1-133">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="098e1-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="098e1-134">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="098e1-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="098e1-135">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="098e1-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="098e1-136">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="098e1-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="098e1-137">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="098e1-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="098e1-138">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="098e1-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="098e1-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="098e1-139">lpCompletionRoutine</span></span>

<span data-ttu-id="098e1-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="098e1-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="098e1-141">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="098e1-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="098e1-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="098e1-142">lpThreadId</span></span>

<span data-ttu-id="098e1-143">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="098e1-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="098e1-144">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="098e1-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="098e1-145">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="098e1-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="098e1-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="098e1-146">lpErrno</span></span>

<span data-ttu-id="098e1-147">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="098e1-147">A pointer to the error code.</span></span>

<span data-ttu-id="098e1-148">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="098e1-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="098e1-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="098e1-149">Return value</span></span>

<span data-ttu-id="098e1-150">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="098e1-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="098e1-151">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="098e1-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="098e1-152">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="098e1-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="098e1-153">Código de error</span><span class="sxs-lookup"><span data-stu-id="098e1-153">Error code</span></span> | <span data-ttu-id="098e1-154">Significado</span><span class="sxs-lookup"><span data-stu-id="098e1-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="098e1-155">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="098e1-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="098e1-156">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="098e1-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="098e1-157">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="098e1-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="098e1-158">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando SIO_FLUSH IOCTL.</span><span class="sxs-lookup"><span data-stu-id="098e1-158">An overlapped operation was canceled due to the closure of the socket or the execution of the SIO_FLUSH IOCTL command.</span></span> |
| <span data-ttu-id="098e1-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="098e1-159">**WSAEFAULT**</span></span> | <span data-ttu-id="098e1-160">Los parámetros *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no están totalmente contenidos en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="098e1-160">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="098e1-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="098e1-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="098e1-162">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="098e1-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="098e1-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="098e1-163">**WSAEINTR**</span></span> | <span data-ttu-id="098e1-164">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="098e1-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="098e1-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="098e1-165">**WSAEINVAL**</span></span> | <span data-ttu-id="098e1-166">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="098e1-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="098e1-167">Se devuelve este error si el parámetro *cbOutBuffer* es menor que el tamaño de un tipo de datos **ULong** .</span><span class="sxs-lookup"><span data-stu-id="098e1-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="098e1-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="098e1-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="098e1-169">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="098e1-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="098e1-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="098e1-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="098e1-171">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="098e1-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="098e1-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="098e1-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="098e1-173">El socket *s* no está conectado.</span><span class="sxs-lookup"><span data-stu-id="098e1-173">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="098e1-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="098e1-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="098e1-175">El descriptor *s* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="098e1-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="098e1-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="098e1-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="098e1-177">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="098e1-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="098e1-178">Este error se devuelve si el proveedor de transporte no admite el **\_ \_ \_ \_ \_ contexto de redirección de conexión de WFP de la consulta SiO** .</span><span class="sxs-lookup"><span data-stu-id="098e1-178">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="098e1-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="098e1-179">Remarks</span></span>

<span data-ttu-id="098e1-180">El **\_ contexto de \_ \_ \_ redireccionamiento \_ de la conexión WFP de la consulta SiO** es compatible con Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="098e1-180">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="098e1-181">WFP permite el acceso a la ruta de procesamiento de paquetes TCP/IP, en la que se pueden examinar o cambiar los paquetes salientes y entrantes antes de permitir que se procesen más.</span><span class="sxs-lookup"><span data-stu-id="098e1-181">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="098e1-182">Al puntear en la ruta de acceso de procesamiento de TCP/IP, los fabricantes de software independientes (ISV) pueden crear más fácilmente firewalls, software antivirus, software de diagnóstico y otros tipos de aplicaciones y servicios.</span><span class="sxs-lookup"><span data-stu-id="098e1-182">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="098e1-183">WFP proporciona componentes en modo de usuario y de modo kernel para que los ISV de terceros puedan participar en las decisiones de filtrado que tienen lugar en varias capas de la pila de protocolos TCP/IP y en todo el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="098e1-183">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="098e1-184">La característica de redirección de conexión de WFP permite a un controlador de kernel de llamada de WFP redirigir una conexión localmente a un proceso de modo de usuario, realizar la inspección de contenido en modo de usuario y reenviar el contenido inspeccionado mediante una conexión diferente al destino original.</span><span class="sxs-lookup"><span data-stu-id="098e1-184">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="098e1-185">El **\_ contexto de \_ \_ \_ redirección \_ de conexión WFP de la consulta SiO** y otros ioctl relacionados son componentes de modo de usuario que se usan para permitir que varias aplicaciones proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de forma cooperativa.</span><span class="sxs-lookup"><span data-stu-id="098e1-185">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="098e1-186">Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha inspeccionado otro agente de inspección.</span><span class="sxs-lookup"><span data-stu-id="098e1-186">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="098e1-187">Con la presencia de varios servidores proxy (desarrollados por fabricantes de software independientes, por ejemplo), la conexión utilizada por un proxy para comunicarse con el destino final podría redirigirse a su vez por un segundo proxy, y esa nueva conexión podría redirigirse de nuevo mediante el proxy original.</span><span class="sxs-lookup"><span data-stu-id="098e1-187">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="098e1-188">Sin el seguimiento de la conexión, la conexión original podría no llegar nunca a su destino final, ya que se bloquea en un bucle proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="098e1-188">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="098e1-189">El **\_ contexto de \_ \_ \_ redireccionamiento de \_ conexión de WFP de la consulta SiO** se usa para permitir que varias aplicaciones de proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de una manera cooperativa.</span><span class="sxs-lookup"><span data-stu-id="098e1-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="098e1-190">Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha inspeccionado otro agente de inspección.</span><span class="sxs-lookup"><span data-stu-id="098e1-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="098e1-191">Con la presencia de varios servidores proxy (desarrollados por fabricantes de software independientes, por ejemplo), la conexión utilizada por un proxy para comunicarse con el destino final podría redirigirse a su vez por un segundo proxy, y esa nueva conexión podría redirigirse de nuevo mediante el proxy original.</span><span class="sxs-lookup"><span data-stu-id="098e1-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="098e1-192">Sin el seguimiento de la conexión, la conexión original podría no llegar nunca a su destino final, ya que se bloquea en un bucle proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="098e1-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>
<span data-ttu-id="098e1-193">El **\_ contexto de \_ \_ \_ redirección \_ de conexión WFP de la consulta SiO** se usa para proporcionar un seguimiento de la conexión de proxy en las conexiones de socket redirigido.</span><span class="sxs-lookup"><span data-stu-id="098e1-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="098e1-194">Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.</span><span class="sxs-lookup"><span data-stu-id="098e1-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="098e1-195">El servicio de redireccionamiento basado en WFP usa el servicio de redirección basada en WFP para recuperar el registro de redireccionamiento de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo), se le redirigió mediante su llamada de modo kernel conectada en las capas de **\_ \_ redireccionamiento de Ale** en un controlador de modo kernel **\_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098e1-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="098e1-196">El servicio de redirección basada en WFP usa el  contexto de redireccionamiento de conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** para recuperar el contexto de redirección de un registro de redirección de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo) redirigido a él mediante su llamada complementaria registrada en ALE_CONNECT_REDIRECT capas.</span><span class="sxs-lookup"><span data-stu-id="098e1-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE_CONNECT_REDIRECT** layers.</span></span>
<span data-ttu-id="098e1-197">El contexto de redireccionamiento es opcional y se usa si el estado de redirección actual de una conexión es que la conexión se redirigió mediante el servicio de redireccionamiento de llamada o que el servicio de redirección de llamada redirigió la conexión anteriormente, pero posteriormente se redirigió de nuevo mediante otro servicio de redirección.</span><span class="sxs-lookup"><span data-stu-id="098e1-197">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="098e1-198">El servicio de redireccionamiento transfiere el registro de redireccionamiento recuperado al socket TCP que usa para crear el proxy del contenido original mediante el protocolo **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** .</span><span class="sxs-lookup"><span data-stu-id="098e1-198">The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="098e1-199">Dado que el contexto de redireccionamiento de WFP es un BLOB de datos de longitud variable establecido por el servicio de redirección, el autor de la llamada puede proporcionar un búfer de salida grande (un búfer de 1 k al que apunta el parámetro *lpvOutBuffer* , por ejemplo) o puede pasar como un tamaño de búfer de salida en el parámetro *cbOutBuffer* de 0 para consultar el tamaño de búfer necesario</span><span class="sxs-lookup"><span data-stu-id="098e1-199">Since the WFP redirect context is a variable length data blob set by the redirect service, the caller can either supply a large output buffer (a 1K buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass as an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="098e1-200">Si el tamaño del búfer de salida no es suficiente para almacenar los datos, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devolverán un **error de \_ \_ búfer insuficiente** y se devolverá el tamaño de búfer necesario en el valor al que apunta el parámetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="098e1-200">If the output buffer size is not sufficient the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="098e1-201">La aplicación que llama a **SiO \_ query \_ WF \ P_CONNECTION \_ redirigir \_ registros** ioctl no necesita comprender el BLOB que contiene los registros de redireccionamiento recuperados.</span><span class="sxs-lookup"><span data-stu-id="098e1-201">The application calling the **SIO\_QUERY\_WF\P_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect records retrieved.</span></span>
<span data-ttu-id="098e1-202">Se trata de un BLOB opaco de datos que la aplicación necesita recuperar y devolver al nuevo socket.</span><span class="sxs-lookup"><span data-stu-id="098e1-202">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="098e1-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="098e1-203">See also</span></span>

[<span data-ttu-id="098e1-204">**Opciones de IPPROTO_IP socket**</span><span class="sxs-lookup"><span data-stu-id="098e1-204">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="098e1-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="098e1-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="098e1-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="098e1-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-set-wfp-connection-redirect-records.md)

[<span data-ttu-id="098e1-207">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="098e1-207">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="098e1-208">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="098e1-208">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="098e1-209">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="098e1-209">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="098e1-210">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="098e1-210">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="098e1-211">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="098e1-211">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="098e1-212">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="098e1-212">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="098e1-213">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="098e1-213">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
