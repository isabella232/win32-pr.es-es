---
description: El código de control recupera el valor de trabajo pendiente de envío ideal para la conexión subyacente.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: Código de control de SIO_IDEAL_SEND_BACKLOG_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720648"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a><span data-ttu-id="a5e1d-103">Código de control de SIO_IDEAL_SEND_BACKLOG_QUERY</span><span class="sxs-lookup"><span data-stu-id="a5e1d-103">SIO_IDEAL_SEND_BACKLOG_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="a5e1d-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5e1d-104">Description</span></span>

<span data-ttu-id="a5e1d-105">El código de control de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** recupera el valor de trabajo pendiente de envío (ISB) ideal para la conexión subyacente.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** control code retrieves the ideal send backlog (ISB) value for the underlying connection.</span></span>

<span data-ttu-id="a5e1d-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="a5e1d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5e1d-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="a5e1d-108">s</span><span class="sxs-lookup"><span data-stu-id="a5e1d-108">s</span></span>

<span data-ttu-id="a5e1d-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="a5e1d-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="a5e1d-110">dwIoControlCode</span></span>

<span data-ttu-id="a5e1d-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-111">The control code for the operation.</span></span>
<span data-ttu-id="a5e1d-112">Use **la \_ \_ consulta de \_ trabajo \_ pendiente de envío de SiO ideal** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="a5e1d-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="a5e1d-113">lpvInBuffer</span></span>

<span data-ttu-id="a5e1d-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="a5e1d-115">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="a5e1d-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="a5e1d-116">cbInBuffer</span></span>

<span data-ttu-id="a5e1d-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="a5e1d-118">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="a5e1d-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a5e1d-119">lpvOutBuffer</span></span>

<span data-ttu-id="a5e1d-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="a5e1d-121">Este parámetro debe apuntar a un tipo de datos **ULong** si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="a5e1d-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a5e1d-122">cbOutBuffer</span></span>

<span data-ttu-id="a5e1d-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="a5e1d-124">Este parámetro debe ser al menos el tamaño de un tipo de datos **ULong** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="a5e1d-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="a5e1d-125">lpcbBytesReturned</span></span>

<span data-ttu-id="a5e1d-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="a5e1d-127">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="a5e1d-128">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="a5e1d-129">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="a5e1d-130">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="a5e1d-131">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="a5e1d-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="a5e1d-132">lpvOverlapped</span></span>

<span data-ttu-id="a5e1d-133">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a5e1d-134">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="a5e1d-135">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="a5e1d-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="a5e1d-136">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a5e1d-137">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="a5e1d-138">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="a5e1d-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="a5e1d-139">lpCompletionRoutine</span></span>

<span data-ttu-id="a5e1d-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="a5e1d-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="a5e1d-141">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="a5e1d-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="a5e1d-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="a5e1d-142">lpThreadId</span></span>

<span data-ttu-id="a5e1d-143">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="a5e1d-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="a5e1d-144">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="a5e1d-145">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="a5e1d-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="a5e1d-146">lpErrno</span></span>

<span data-ttu-id="a5e1d-147">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-147">A pointer to the error code.</span></span>

<span data-ttu-id="a5e1d-148">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5e1d-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5e1d-149">Return value</span></span>

<span data-ttu-id="a5e1d-150">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="a5e1d-151">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="a5e1d-152">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="a5e1d-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="a5e1d-153">Código de error</span><span class="sxs-lookup"><span data-stu-id="a5e1d-153">Error code</span></span> | <span data-ttu-id="a5e1d-154">Significado</span><span class="sxs-lookup"><span data-stu-id="a5e1d-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="a5e1d-155">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="a5e1d-156">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="a5e1d-157">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="a5e1d-158">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SiO \_ Flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-158">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="a5e1d-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-159">**WSAEFAULT**</span></span> | <span data-ttu-id="a5e1d-160">Los parámetros *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no están totalmente contenidos en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-160">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="a5e1d-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="a5e1d-162">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="a5e1d-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-163">**WSAEINTR**</span></span> | <span data-ttu-id="a5e1d-164">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="a5e1d-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-165">**WSAEINVAL**</span></span> | <span data-ttu-id="a5e1d-166">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="a5e1d-167">Se devuelve este error si el parámetro *cbOutBuffer* es menor que el tamaño de un tipo de datos **ULong** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span>
| <span data-ttu-id="a5e1d-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="a5e1d-169">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="a5e1d-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="a5e1d-171">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="a5e1d-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="a5e1d-173">El socket s no está conectado.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-173">The socket s is not connected.</span></span> |
| <span data-ttu-id="a5e1d-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="a5e1d-175">El descriptor *s* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="a5e1d-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="a5e1d-177">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="a5e1d-178">Este error se devuelve si el proveedor de transporte no admite el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-178">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="a5e1d-179">Este error también se devuelve cuando se realiza un intento de usar el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío de SiO ideal** en un socket de datagramas.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-179">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a5e1d-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5e1d-180">Remarks</span></span>

<span data-ttu-id="a5e1d-181">El ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** es compatible con Windows Server 2008, Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="a5e1d-182">Al enviar datos a través de una conexión TCP mediante Windows Sockets, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no confirmados todavía) en TCP para lograr el máximo rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-182">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="a5e1d-183">El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina el tamaño de trabajo pendiente de envío (ISB) ideal.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-183">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="a5e1d-184">El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y, en parte, de la cantidad de congestión de la red).</span><span class="sxs-lookup"><span data-stu-id="a5e1d-184">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="a5e1d-185">El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-185">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="a5e1d-186">Una aplicación puede usar el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** para recibir una notificación cuando el valor de ISB Cambie dinámicamente para una conexión.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-186">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="a5e1d-187">En Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo, se admiten los ioctl de [**\_ \_ \_ \_ cambio de trabajo acumulado de envío**](sio-ideal-send-backlog-change.md) y **SiO \_ idóneos \_ \_ \_** en los sockets orientados a flujos que se encuentran en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-187">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="a5e1d-188">En teoría, el intervalo para el valor de ISB para una conexión TCP puede variar de 0 a un máximo de 16 megabytes.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-188">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="a5e1d-189">El uso típico de la opción de búsqueda de trabajo pendiente de envío ideal y SiO de la **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal** se basa en el método de envío que usan las aplicaciones. [**\_ \_ \_ \_**](sio-ideal-send-backlog-change.md)</span><span class="sxs-lookup"><span data-stu-id="a5e1d-189">The typical usage of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs is based on the send method used by the applications.</span></span>
<span data-ttu-id="a5e1d-190">Se describen dos casos comunes.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-190">Two common cases are discussed.</span></span>

<span data-ttu-id="a5e1d-191">Las aplicaciones que realizan una solicitud de envío o de bloqueo sin bloqueo a la vez suelen basarse en el almacenamiento en búfer interno de Winsock para lograr un rendimiento aceptable.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-191">Applications that perform one blocking or non-blocking send request at a time typically rely on internal send buffering by Winsock to achieve decent throughput.</span></span>
<span data-ttu-id="a5e1d-192">El límite del búfer de envío para una conexión determinada se controla mediante la opción de socket **so \_ SNDBUF** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-192">The send buffer limit for a given connection is controlled by the **SO\_SNDBUF** socket option.</span></span>
<span data-ttu-id="a5e1d-193">En el caso del método de envío y bloqueo sin bloqueo, el límite del búfer de envío determina la cantidad de datos que se mantienen pendientes en TCP.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-193">For the blocking and non-blocking send method, the send buffer limit determines how much data is kept outstanding in TCP.</span></span>
<span data-ttu-id="a5e1d-194">Si el valor de ISB para la conexión es mayor que el límite del búfer de envío, el rendimiento conseguido en la conexión no será óptimo.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-194">If the ISB value for the connection is larger than the send buffer limit, then the throughput achieved on the connection will not be optimal.</span></span>
<span data-ttu-id="a5e1d-195">Con el fin de lograr un mejor rendimiento, las aplicaciones pueden establecer el límite del búfer de envío según el resultado de la consulta de ISB a medida que se producen notificaciones de cambios de ISB en la conexión.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-195">In order to achieve better throughput, the applications can set the send buffer limit based on the result of the ISB query as ISB change notifications occur on the connection.</span></span>

<span data-ttu-id="a5e1d-196">En el caso de las aplicaciones que usan el método de envío superpuesto con varias solicitudes de envío pendientes, la cantidad de datos que se mantienen pendientes en TCP viene determinada por el límite de búfer de envío en Winsock y la cantidad total de datos contenidos en las solicitudes de envío superpuestas pendientes.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-196">For applications that use the overlapped send method with multiple send requests outstanding, the amount of data kept outstanding in TCP is determined by the send buffer limit in Winsock and the total amount of data contained in the outstanding overlapped send requests.</span></span>
<span data-ttu-id="a5e1d-197">En este caso, las aplicaciones deben usar el valor de ISB para determinar cuántas solicitudes de envío pendientes deben conservar y cuál debe ser el tamaño de los datos para cada solicitud de envío.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-197">In this case, applications should use the ISB value to determine how many outstanding send requests they should keep and what the data size for each send request should be.</span></span>
<span data-ttu-id="a5e1d-198">Idealmente, la aplicación debe intentar mantener la siguiente ecuación satisfactoria:</span><span class="sxs-lookup"><span data-stu-id="a5e1d-198">Ideally, the application should try to keep the following equation satisfied:</span></span>

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

<span data-ttu-id="a5e1d-199">Tenga en cuenta que el uso de los ioctl de ISB a través de Sockets TCP en el modo anterior puede provocar un aumento del uso de memoria en Exchange para aumentar el rendimiento en las conexiones con un producto de retraso de ancho de banda alto.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-199">Note that using the ISB IOCTLs over TCP sockets in the above fashion can lead to increased memory usage in exchange for increased throughput on connections with a high bandwidth-delay product.</span></span>
<span data-ttu-id="a5e1d-200">La implementación de TCP en Windows limitará los valores de ISB según sea necesario en función del uso global de la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-200">The TCP implementation in Windows will throttle ISB values as necessary based on overall system memory usage.</span></span>

<span data-ttu-id="a5e1d-201">El ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** solo se permite en un socket de secuencia que se encuentra en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-201">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="a5e1d-202">De lo contrario, se producirá un error en la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-202">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="a5e1d-203">Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-203">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="a5e1d-204">Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-204">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="a5e1d-205">No es probable que el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío perfecto** no se bloquee, por lo que normalmente se llama sincrónicamente con los parámetros *lpOverlapped* y *lpCompletionRoutine* establecidos en **null**.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-205">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not likely to block so it is normally called synchronously with the *lpOverlapped* and *lpCompletionRoutine* parameters set to **NULL**.</span></span>

<span data-ttu-id="a5e1d-206">Se puede producir un error en el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío de SiO ideal** con la operación **WSAEINTR** o **WSA \_ \_ anulada** en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="a5e1d-206">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

<span data-ttu-id="a5e1d-207">La conexión TCP está correctamente desconectada en la dirección de envío.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-207">The TCP connection is gracefully disconnected in the send direction.</span></span>
<span data-ttu-id="a5e1d-208">Esto puede ocurrir como resultado de una llamada a la función Shutdown con el parámetro how establecido en **SD \_ send**, una llamada a la función **DisconnectEx** o una llamada a la función **TransmitFile** o **TransmitPackets** con el parámetro *dwFlags* establecido en **TF \_ Disconnect** o **TF \_ reuse**.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-208">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
<span data-ttu-id="a5e1d-209">La conexión TCP se ha restablecido o anulado.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-209">The TCP connection has been reset or aborted.</span></span>
<span data-ttu-id="a5e1d-210">El administrador de e/s cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-210">The request is canceled by the I/O Manager.</span></span>

<span data-ttu-id="a5e1d-211">Dos funciones de contenedor en línea para estos ioctl se definen en el archivo de encabezado *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-211">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="a5e1d-212">Se recomienda usar estas funciones insertadas en lugar de usar el [**\_ \_ \_ \_ cambio de trabajo pendiente de envío**](sio-ideal-send-backlog-change.md) y **SiO ideales para la \_ \_ \_ \_ consulta de trabajo pendiente de envío ideal** directamente.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-212">It is recommended that these inline functions be used instead of using the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs directly.</span></span>

<span data-ttu-id="a5e1d-213">La función de contenedor en línea para [**el \_ \_ cambio de \_ trabajo \_ pendiente de envío de SiO ideal**](sio-ideal-send-backlog-change.md) es la función **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-213">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="a5e1d-214">La función de contenedor en línea para **la \_ opción \_ de \_ \_ búsqueda de trabajo pendiente de envío ideal de SiO** es la función **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="a5e1d-214">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is the **idealsendbacklogquery** function.</span></span>

<span data-ttu-id="a5e1d-215">El almacenamiento en búfer de envío dinámico para TCP se agregó en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-215">Dynamic send buffering for TCP was added on Windows 7 and Windows Server 2008 R2.</span></span>
<span data-ttu-id="a5e1d-216">De forma predeterminada, el almacenamiento en búfer de envío dinámico para TCP está habilitado a menos que una aplicación establezca la opción de socket for **\_ SNDBUF** en el socket de flujo.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-216">By default, dynamic send buffering for TCP is enabled unless an application sets the **SO\_SNDBUF** socket option on the stream socket.</span></span>

<span data-ttu-id="a5e1d-217">El uso de Netsh es el método recomendado para consultar o establecer el almacenamiento en búfer de envío dinámico para TCP.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-217">Using netsh is the recommended method to query or set dynamic send buffering for TCP.</span></span>

<span data-ttu-id="a5e1d-218">El valor actual del almacenamiento en búfer de envío dinámico para TCP se puede recuperar con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a5e1d-218">The current value for dynamic send buffering for TCP can be retrieved using the following command:</span></span>

`netsh winsock show autotuning`

<span data-ttu-id="a5e1d-219">El almacenamiento en búfer de envío dinámico para TCP se puede deshabilitar con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a5e1d-219">Dynamic send buffering for TCP can be disabled using the following command:</span></span>

`netsh winsock set autotuning off`

<span data-ttu-id="a5e1d-220">El almacenamiento en búfer de envío dinámico para TCP se puede habilitar con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a5e1d-220">Dynamic send buffering for TCP can be enabled using the following command:</span></span>

`netsh winsock set autotuning on`

<span data-ttu-id="a5e1d-221">Aunque no se recomienda, el almacenamiento en búfer de envío dinámico se puede deshabilitar en una aplicación si se establece el valor del Registro siguiente en cero:</span><span class="sxs-lookup"><span data-stu-id="a5e1d-221">While it is discouraged, dynamic send buffering can be disabled from an application by setting the following registry value to zero:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

<span data-ttu-id="a5e1d-222">Al cambiar el valor del almacenamiento en búfer de envío dinámico mediante NetSh.exe o cambiar el valor del registro, el equipo debe reiniciarse para que el cambio surta efecto.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-222">When changing the value for dynamic send buffering using NetSh.exe or changing the registry value, the computer must be restarted for the change to take effect.</span></span>

<span data-ttu-id="a5e1d-223">Con el almacenamiento en búfer dinámico de envíos en Windows 7 y Windows Server 2008 R2, el uso de los ioctl de **\_ \_ \_ \_ solicitud** de envío de [**\_ \_ \_ trabajo \_**](sio-ideal-send-backlog-change.md) en el trabajo de envío y SiO ideal solo es necesario en circunstancias especiales.</span><span class="sxs-lookup"><span data-stu-id="a5e1d-223">With dynamic send buffering on Windows 7 and Windows Server 2008 R2, the use of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are needed only in special circumstances.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5e1d-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5e1d-224">See also</span></span>

[<span data-ttu-id="a5e1d-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span></span>](sio-ideal-send-backlog-change.md)

[<span data-ttu-id="a5e1d-226">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-226">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="a5e1d-227">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-227">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="a5e1d-228">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-228">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="a5e1d-229">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-229">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="a5e1d-230">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-230">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="a5e1d-231">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-231">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="a5e1d-232">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="a5e1d-232">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
