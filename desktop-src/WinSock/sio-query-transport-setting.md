---
description: El código de control consulta la configuración de transporte en un socket.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: Código de control de SIO_QUERY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908568"
---
# <a name="sio_query_transport_setting-control-code"></a><span data-ttu-id="5f8bd-103">Código de control de SIO_QUERY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="5f8bd-103">SIO_QUERY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="5f8bd-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f8bd-104">Description</span></span>

<span data-ttu-id="5f8bd-105">El código de control de configuración de transporte de la **\_ consulta SiO \_ \_ consulta** la configuración de transporte en un socket.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-105">The **SIO\_QUERY\_TRANSPORT\_SETTING** control code queries the transport settings on a socket.</span></span>

<span data-ttu-id="5f8bd-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="5f8bd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f8bd-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="5f8bd-108">s</span><span class="sxs-lookup"><span data-stu-id="5f8bd-108">s</span></span>

<span data-ttu-id="5f8bd-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="5f8bd-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="5f8bd-110">dwIoControlCode</span></span>

<span data-ttu-id="5f8bd-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-111">The control code for the operation.</span></span>
<span data-ttu-id="5f8bd-112">Use **la \_ \_ \_ configuración de transporte de consulta SiO** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-112">Use **SIO\_QUERY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="5f8bd-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-113">lpvInBuffer</span></span>

<span data-ttu-id="5f8bd-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="5f8bd-115">Este parámetro contiene un puntero a una estructura en la que el primer miembro de la estructura es una estructura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) que determina qué configuración de transporte se está consultando.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being queried.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="5f8bd-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-116">cbInBuffer</span></span>

<span data-ttu-id="5f8bd-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="5f8bd-118">Este parámetro depende de la configuración de transporte que se consulta.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-118">This parameter depends on the transport setting being queried.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="5f8bd-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-119">lpvOutBuffer</span></span>

<span data-ttu-id="5f8bd-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="5f8bd-121">Este parámetro depende de la configuración de transporte que se consulta si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-121">This parameter depends on the transport setting being queried if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="5f8bd-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-122">cbOutBuffer</span></span>

<span data-ttu-id="5f8bd-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="5f8bd-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="5f8bd-124">lpcbBytesReturned</span></span>

<span data-ttu-id="5f8bd-125">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="5f8bd-126">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="5f8bd-127">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="5f8bd-128">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="5f8bd-129">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="5f8bd-130">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="5f8bd-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="5f8bd-131">lpvOverlapped</span></span>

<span data-ttu-id="5f8bd-132">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5f8bd-133">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="5f8bd-134">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="5f8bd-135">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5f8bd-136">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="5f8bd-137">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="5f8bd-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="5f8bd-138">lpCompletionRoutine</span></span>

<span data-ttu-id="5f8bd-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="5f8bd-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="5f8bd-140">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="5f8bd-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="5f8bd-141">lpThreadId</span></span>

<span data-ttu-id="5f8bd-142">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="5f8bd-143">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="5f8bd-144">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="5f8bd-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="5f8bd-145">lpErrno</span></span>

<span data-ttu-id="5f8bd-146">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-146">A pointer to the error code.</span></span>

<span data-ttu-id="5f8bd-147">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f8bd-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f8bd-148">Return value</span></span>

<span data-ttu-id="5f8bd-149">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="5f8bd-150">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="5f8bd-151">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="5f8bd-152">Código de error</span><span class="sxs-lookup"><span data-stu-id="5f8bd-152">Error code</span></span> | <span data-ttu-id="5f8bd-153">Significado</span><span class="sxs-lookup"><span data-stu-id="5f8bd-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="5f8bd-154">**ERROR \_ de \_ búfer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-154">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="5f8bd-155">El área de datos que se pasa a una llamada del sistema es demasiado pequeña.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-155">The data area passed to a system call is too small.</span></span> <span data-ttu-id="5f8bd-156">Se devuelve este error si el búfer señalado por el parámetro *lpvOutBuffer* con un tamaño de búfer pasado en el parámetro *cbOutBuffer* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-156">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="5f8bd-157">El tamaño de búfer necesario se devolverá en el parámetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-157">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="5f8bd-158">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="5f8bd-159">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-159">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="5f8bd-160">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-160">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="5f8bd-161">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SiO \_ Flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-161">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="5f8bd-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-162">**WSAEFAULT**</span></span> | <span data-ttu-id="5f8bd-163">Los parámetros *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no están totalmente contenidos en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-163">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="5f8bd-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="5f8bd-165">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-165">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="5f8bd-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-166">**WSAEINTR**</span></span> | <span data-ttu-id="5f8bd-167">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-167">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="5f8bd-168">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-168">**WSAEINVAL**</span></span> | <span data-ttu-id="5f8bd-169">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-169">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="5f8bd-170">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-170">**WSAENETDOWN**</span></span> | <span data-ttu-id="5f8bd-171">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-171">The network subsystem has failed.</span></span> |
| <span data-ttu-id="5f8bd-172">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-172">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="5f8bd-173">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-173">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="5f8bd-174">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-174">**WSAENOTCONN**</span></span> | <span data-ttu-id="5f8bd-175">El socket s no está conectado.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-175">The socket s is not connected.</span></span> |
| <span data-ttu-id="5f8bd-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="5f8bd-177">El descriptor s no es un socket.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-177">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="5f8bd-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="5f8bd-179">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-179">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="5f8bd-180">Este error se devuelve si el proveedor de transporte no admite la configuración de transporte de la **\_ consulta \_ \_ SiO** ioctl.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-180">This error is returned if the **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="5f8bd-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f8bd-181">Remarks</span></span>

<span data-ttu-id="5f8bd-182">La **\_ configuración de \_ transporte \_ de la consulta SiO** ioctl es compatible con windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-182">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="5f8bd-183">La **\_ configuración de \_ transporte \_ de la consulta SiO** ioctl es un ioctl genérico que se utiliza para consultar la configuración de transporte en un socket.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-183">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to query the transport settings on a socket.</span></span>
<span data-ttu-id="5f8bd-184">La configuración de transporte que se consulta se basa en el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el parámetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-184">The transport setting being queried is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="5f8bd-185">La única configuración de transporte que define actualmente es para la funcionalidad de **\_ notificación en tiempo \_ \_ real** en un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-185">The only transport setting currently defines is for the **REAL\_TIME\_NOTIFICATION\_CAPABILITY** capability on a TCP socket.</span></span>

<span data-ttu-id="5f8bd-186">Si el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el parámetro *lpvInBuffer* tiene el miembro GUID establecido en **\_ \_ \_ funcionalidad de notificación en tiempo real**, se trata de una solicitud para consultar la configuración de notificación en tiempo real para el socket TCP que se usa con la [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-186">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to query the real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="5f8bd-187">El parámetro *lpvInBuffer* debe apuntar a una estructura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-187">The *lpvInBuffer* parameter should point to a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure.</span></span>
<span data-ttu-id="5f8bd-188">El parámetro *lpvOutBuffer* debe apuntar a una estructura de salida de **configuración de \_ \_ notificación en \_ \_ tiempo real** .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-188">The *lpvOutBuffer* parameter should point to a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure.</span></span>
<span data-ttu-id="5f8bd-189">Esta configuración de transporte solo se aplica a los Sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-189">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="5f8bd-190">Esta configuración de transporte proporciona una manera para que WinInet o servicios de red similares consulten un socket TCP determinado para determinar el estado de la [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .</span><span class="sxs-lookup"><span data-stu-id="5f8bd-190">This transport setting provides a way for WinInet or similar network services to query a given TCP socket to determine the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) status.</span></span>
<span data-ttu-id="5f8bd-191">Una aplicación de la tienda Windows no llamará a este IOCTL directamente.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-191">A Windows Store app will not call this IOCTL directly.</span></span>
<span data-ttu-id="5f8bd-192">Si la llamada a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** es correcta, este ioctl devuelve una estructura de **salida de configuración de \_ notificación en tiempo \_ \_ \_ real** con el estado actual.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-192">If the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** call is successful, this IOCTL returns a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure with the current status.</span></span>

<span data-ttu-id="5f8bd-193">La **\_ configuración de \_ transporte \_ de la consulta SiO** ioctl proporciona una manera para que WinInet o los servicios de red similares consulten el estado de configuración de transporte de un socket TCP determinado para determinar si [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) está habilitado en el socket.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-193">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL provides a way for WinInet or similar network services to query for the transport setting status for a given TCP socket to determine if [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) is enabled on the socket.</span></span>
<span data-ttu-id="5f8bd-194">Una aplicación de la tienda Windows no llamará a este IOCTL directamente.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-194">A Windows Store app will not call this IOCTL directly.</span></span>

<span data-ttu-id="5f8bd-195">Este IOCTL solo se aplica a los Sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-195">This IOCTL applies only to TCP sockets.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f8bd-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f8bd-196">See also</span></span>

[<span data-ttu-id="5f8bd-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span></span>](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[<span data-ttu-id="5f8bd-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="5f8bd-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[<span data-ttu-id="5f8bd-200">**SIO_APPLY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-200">**SIO_APPLY_TRANSPORT_SETTING**</span></span>](sio-apply-transport-setting.md)

[<span data-ttu-id="5f8bd-201">tomacorriente</span><span class="sxs-lookup"><span data-stu-id="5f8bd-201">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="5f8bd-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="5f8bd-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="5f8bd-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="5f8bd-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="5f8bd-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="5f8bd-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="5f8bd-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
