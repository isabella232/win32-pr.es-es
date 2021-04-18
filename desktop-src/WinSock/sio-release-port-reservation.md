---
description: El código de control libera una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: Código de control de SIO_RELEASE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57f96d0396d661eba12f9e64238c492f38e97b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720478"
---
# <a name="sio_release_port_reservation-control-code"></a><span data-ttu-id="44da1-103">Código de control de SIO_RELEASE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="44da1-103">SIO_RELEASE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="44da1-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="44da1-104">Description</span></span>

<span data-ttu-id="44da1-105">El código de control de **\_ reserva de \_ Puerto \_ de versión SiO** libera una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="44da1-105">The **SIO\_RELEASE\_PORT\_RESERVATION** control code releases a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="44da1-106">La reserva en tiempo de ejecución que se va a liberar debe haberse obtenido del proceso de emisión mediante el [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl.</span><span class="sxs-lookup"><span data-stu-id="44da1-106">The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span></span>

<span data-ttu-id="44da1-107">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="44da1-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="44da1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44da1-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="44da1-109">s</span><span class="sxs-lookup"><span data-stu-id="44da1-109">s</span></span>

<span data-ttu-id="44da1-110">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="44da1-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="44da1-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="44da1-111">dwIoControlCode</span></span>

<span data-ttu-id="44da1-112">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="44da1-112">The control code for the operation.</span></span>
<span data-ttu-id="44da1-113">Use **la \_ \_ \_ reserva de puertos de versión SiO** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="44da1-113">Use **SIO\_RELEASE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="44da1-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="44da1-114">lpvInBuffer</span></span>

<span data-ttu-id="44da1-115">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="44da1-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="44da1-116">Este parámetro contiene un puntero a una estructura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) con el token de la reserva de puerto TCP o UDP que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="44da1-116">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to release.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="44da1-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="44da1-117">cbInBuffer</span></span>

<span data-ttu-id="44da1-118">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="44da1-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="44da1-119">Este parámetro debe ser al menos el tamaño de la estructura [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="44da1-119">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="44da1-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="44da1-120">lpvOutBuffer</span></span>

<span data-ttu-id="44da1-121">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="44da1-121">A pointer to the output buffer.</span></span>
<span data-ttu-id="44da1-122">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="44da1-122">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="44da1-123">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="44da1-123">cbOutBuffer</span></span>

<span data-ttu-id="44da1-124">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="44da1-124">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="44da1-125">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="44da1-125">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="44da1-126">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="44da1-126">lpcbBytesReturned</span></span>

<span data-ttu-id="44da1-127">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="44da1-127">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="44da1-128">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="44da1-128">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="44da1-129">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="44da1-129">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="44da1-130">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="44da1-130">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="44da1-131">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="44da1-131">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="44da1-132">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="44da1-132">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="44da1-133">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="44da1-133">lpvOverlapped</span></span>

<span data-ttu-id="44da1-134">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="44da1-134">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="44da1-135">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="44da1-135">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="44da1-136">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="44da1-136">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="44da1-137">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="44da1-137">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="44da1-138">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="44da1-138">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="44da1-139">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="44da1-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="44da1-140">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="44da1-140">lpCompletionRoutine</span></span>

<span data-ttu-id="44da1-141">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="44da1-141">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="44da1-142">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="44da1-142">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="44da1-143">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="44da1-143">lpThreadId</span></span>

<span data-ttu-id="44da1-144">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="44da1-144">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="44da1-145">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="44da1-145">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="44da1-146">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="44da1-146">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="44da1-147">lpErrno</span><span class="sxs-lookup"><span data-stu-id="44da1-147">lpErrno</span></span>

<span data-ttu-id="44da1-148">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="44da1-148">A pointer to the error code.</span></span>

<span data-ttu-id="44da1-149">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="44da1-149">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="44da1-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44da1-150">Return value</span></span>

<span data-ttu-id="44da1-151">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="44da1-151">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="44da1-152">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="44da1-152">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="44da1-153">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="44da1-153">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="44da1-154">Código de error</span><span class="sxs-lookup"><span data-stu-id="44da1-154">Error code</span></span> | <span data-ttu-id="44da1-155">Significado</span><span class="sxs-lookup"><span data-stu-id="44da1-155">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="44da1-156">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="44da1-156">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="44da1-157">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="44da1-157">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="44da1-158">Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="44da1-158">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="44da1-159">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="44da1-159">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="44da1-160">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="44da1-160">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="44da1-161">Se devuelve este error si se ha cancelado una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="44da1-161">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="44da1-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="44da1-162">**WSAEFAULT**</span></span> | <span data-ttu-id="44da1-163">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="44da1-163">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="44da1-164">Este error se devuelve cuando el parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="44da1-164">This error is returned of the *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="44da1-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="44da1-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="44da1-166">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="44da1-166">A blocking operation is currently executing.</span></span> <span data-ttu-id="44da1-167">Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="44da1-167">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="44da1-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="44da1-168">**WSAEINTR**</span></span> | <span data-ttu-id="44da1-169">Una operación de bloqueo fue interrumpida por una llamada a **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="44da1-169">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="44da1-170">Se devuelve este error si se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="44da1-170">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="44da1-171">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="44da1-171">**WSAEINVAL**</span></span> | <span data-ttu-id="44da1-172">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="44da1-172">An invalid argument was supplied.</span></span> <span data-ttu-id="44da1-173">Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="44da1-173">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="44da1-174">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="44da1-174">**WSAENETDOWN**</span></span> | <span data-ttu-id="44da1-175">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="44da1-175">A socket operation encountered a dead network.</span></span> <span data-ttu-id="44da1-176">Se devuelve este error si se ha producido un error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="44da1-176">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="44da1-177">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="44da1-177">**WSAENOTSOCK**</span></span> | <span data-ttu-id="44da1-178">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="44da1-178">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="44da1-179">Se devuelve este error si el *descriptor* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="44da1-179">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="44da1-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="44da1-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="44da1-181">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="44da1-181">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="44da1-182">Se devuelve este error si no se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="44da1-182">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="44da1-183">Este error también se devuelve si el proveedor de transporte no admite el ioctl de reserva de puertos de la **\_ versión \_ \_ SiO** .</span><span class="sxs-lookup"><span data-stu-id="44da1-183">This error is also returned if the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="44da1-184">Este error también se devuelve cuando se realiza un intento de usar el ioctl de **\_ reserva de \_ puertos \_ de versión SiO** en un socket distinto de UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="44da1-184">This error is also returned when an attempt to use the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="44da1-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44da1-185">Remarks</span></span>

<span data-ttu-id="44da1-186">El ioctl de **\_ reserva de \_ puertos \_ de versión SiO** es compatible con Windows Vista y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="44da1-186">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="44da1-187">Las aplicaciones y los servicios que necesitan reservar puertos se dividen en dos categorías.</span><span class="sxs-lookup"><span data-stu-id="44da1-187">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="44da1-188">La primera categoría incluye componentes que necesitan un puerto determinado como parte de su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="44da1-188">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="44da1-189">Por lo general, estos componentes prefieren especificar su puerto necesario en el momento de la instalación (por ejemplo, en un manifiesto de aplicación).</span><span class="sxs-lookup"><span data-stu-id="44da1-189">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="44da1-190">La segunda categoría incluye componentes que necesitan cualquier puerto o bloque de puertos disponible en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="44da1-190">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="44da1-191">Estas dos categorías corresponden a las solicitudes de reserva de puertos específicos y comodín.</span><span class="sxs-lookup"><span data-stu-id="44da1-191">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="44da1-192">Las solicitudes de reserva específicas pueden ser persistentes o en tiempo de ejecución, mientras que las solicitudes de reserva de Puerto comodín solo se admiten en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="44da1-192">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="44da1-193">El [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl se usa para solicitar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="44da1-193">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="44da1-194">En el caso de las reservas de puerto en tiempo de ejecución, el grupo de puertos requiere que se consuman reservas del proceso en cuyo socket se concedió la reserva.</span><span class="sxs-lookup"><span data-stu-id="44da1-194">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="44da1-195">Las reservas de puerto en tiempo de ejecución solo duran el tiempo que dure el socket en el que se llamó a la [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl.</span><span class="sxs-lookup"><span data-stu-id="44da1-195">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="44da1-196">Por el contrario, cualquier proceso puede consumir reservas de Puerto persistentes creadas con la función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.</span><span class="sxs-lookup"><span data-stu-id="44da1-196">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="44da1-197">El ioctl de **\_ reserva de \_ puertos \_ de versión SiO** se usa para liberar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="44da1-197">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is used to release a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="44da1-198">Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**, el socket de esta función se tratará como un socket no superpuesto.</span><span class="sxs-lookup"><span data-stu-id="44da1-198">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="44da1-199">En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine* , salvo que la función puede bloquearse si socket *s* está en modo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="44da1-199">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="44da1-200">Si socket *s* está en modo de no bloqueo, esta función seguirá bloqueando, ya que este ioctl determinado no admite el modo de no bloqueo.</span><span class="sxs-lookup"><span data-stu-id="44da1-200">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="44da1-201">En el caso de los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="44da1-201">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="44da1-202">Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="44da1-202">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="44da1-203">Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.</span><span class="sxs-lookup"><span data-stu-id="44da1-203">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="44da1-204">Se puede producir un error en la operación de **WSAEINTR** o **WSA \_ \_** de la **\_ reserva de \_ puertos \_ de versión SiO** en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="44da1-204">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="44da1-205">El administrador de e/s cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44da1-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="44da1-206">El socket está cerrado.</span><span class="sxs-lookup"><span data-stu-id="44da1-206">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="44da1-207">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="44da1-207">Examples</span></span>

<span data-ttu-id="44da1-208">En el ejemplo siguiente se adquiere una reserva de puerto en tiempo de ejecución y después se libera la reserva de puerto en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="44da1-208">The following example acquires a runtime port reservation and then releases the runtime port reservation.</span></span>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a><span data-ttu-id="44da1-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="44da1-209">See also</span></span>

[<span data-ttu-id="44da1-210">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="44da1-210">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="44da1-211">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="44da1-211">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="44da1-212">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="44da1-212">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="44da1-213">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="44da1-213">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="44da1-214">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="44da1-214">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="44da1-215">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="44da1-215">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="44da1-216">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="44da1-216">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="44da1-217">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="44da1-217">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="44da1-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="44da1-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="44da1-219">tomacorriente</span><span class="sxs-lookup"><span data-stu-id="44da1-219">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="44da1-220">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="44da1-220">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="44da1-221">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="44da1-221">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="44da1-222">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="44da1-222">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="44da1-223">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="44da1-223">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="44da1-224">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="44da1-224">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="44da1-225">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="44da1-225">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
