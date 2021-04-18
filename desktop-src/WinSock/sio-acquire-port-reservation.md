---
description: El código de control adquiere una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: Código de control de SIO_ACQUIRE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720498"
---
# <a name="sio_acquire_port_reservation-control-code"></a><span data-ttu-id="399d6-103">Código de control de SIO_ACQUIRE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="399d6-103">SIO_ACQUIRE_PORT_RESERVATION control code</span></span>

## <a name="description"></a><span data-ttu-id="399d6-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="399d6-104">Description</span></span>

<span data-ttu-id="399d6-105">El código de control de reserva de puerto de adquisición de SiO adquiere una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-105">The **SIO\_ACQUIRE\_PORT\_RESERVATION** control code acquires a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="399d6-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="399d6-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="399d6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="399d6-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="399d6-108">s</span><span class="sxs-lookup"><span data-stu-id="399d6-108">s</span></span>

<span data-ttu-id="399d6-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="399d6-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="399d6-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="399d6-110">dwIoControlCode</span></span>

<span data-ttu-id="399d6-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="399d6-111">The control code for the operation.</span></span>
<span data-ttu-id="399d6-112">Utilice **la \_ \_ \_ reserva de puerto de adquisición de SiO**  para esta operación.</span><span class="sxs-lookup"><span data-stu-id="399d6-112">Use **SIO\_ACQUIRE\_PORT\_RESERVATION**  for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="399d6-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="399d6-113">lpvInBuffer</span></span>

<span data-ttu-id="399d6-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="399d6-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="399d6-115">Este parámetro contiene un puntero a una estructura de [**\_ \_ intervalo de puertos inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) que especifica el número de punto inicial y el número de puertos que se van a reservar.</span><span class="sxs-lookup"><span data-stu-id="399d6-115">This parameter contains a pointer to an [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure that specifies the starting point number and the number of ports to reserve.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="399d6-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="399d6-116">cbInBuffer</span></span>

<span data-ttu-id="399d6-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="399d6-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="399d6-118">Este parámetro debe ser el tamaño de la estructura de [**\_ \_ intervalo de puertos inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) .</span><span class="sxs-lookup"><span data-stu-id="399d6-118">This parameter should be the size of the [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="399d6-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="399d6-119">lpvOutBuffer</span></span>

<span data-ttu-id="399d6-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="399d6-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="399d6-121">Si el resultado es correcto, este parámetro contiene un puntero a una estructura de [**\_ instancia de \_ reserva \_ de Puerto inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="399d6-121">On successful output, this parameter contains a pointer to an [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="399d6-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="399d6-122">cbOutBuffer</span></span>

<span data-ttu-id="399d6-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="399d6-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="399d6-124">Este parámetro debe ser al menos el tamaño de la estructura de la [**\_ instancia de \_ reserva \_ de Puerto inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="399d6-124">This parameter must be at least the size of the [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="399d6-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="399d6-125">lpcbBytesReturned</span></span>

<span data-ttu-id="399d6-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="399d6-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="399d6-127">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="399d6-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="399d6-128">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="399d6-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="399d6-129">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="399d6-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="399d6-130">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="399d6-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="399d6-131">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="399d6-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="399d6-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="399d6-132">lpvOverlapped</span></span>

<span data-ttu-id="399d6-133">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="399d6-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="399d6-134">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="399d6-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="399d6-135">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="399d6-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="399d6-136">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="399d6-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="399d6-137">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="399d6-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="399d6-138">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="399d6-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="399d6-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="399d6-139">lpCompletionRoutine</span></span>

<span data-ttu-id="399d6-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="399d6-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="399d6-141">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="399d6-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="399d6-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="399d6-142">lpThreadId</span></span>

<span data-ttu-id="399d6-143">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a **WPUQueueApc**.</span><span class="sxs-lookup"><span data-stu-id="399d6-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to **WPUQueueApc**.</span></span>
<span data-ttu-id="399d6-144">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función **WPUQueueApc** .</span><span class="sxs-lookup"><span data-stu-id="399d6-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the **WPUQueueApc** function returns.</span></span>

<span data-ttu-id="399d6-145">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="399d6-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="399d6-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="399d6-146">lpErrno</span></span>

<span data-ttu-id="399d6-147">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="399d6-147">A pointer to the error code.</span></span>

<span data-ttu-id="399d6-148">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="399d6-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="399d6-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="399d6-149">Return value</span></span>

<span data-ttu-id="399d6-150">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="399d6-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="399d6-151">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="399d6-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="399d6-152">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="399d6-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="399d6-153">Código de error</span><span class="sxs-lookup"><span data-stu-id="399d6-153">Error code</span></span> | <span data-ttu-id="399d6-154">Significado</span><span class="sxs-lookup"><span data-stu-id="399d6-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="399d6-155">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="399d6-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="399d6-156">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="399d6-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="399d6-157">Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="399d6-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="399d6-158">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="399d6-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="399d6-159">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="399d6-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="399d6-160">Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de ioctl de **\_ volcado de SiO** .</span><span class="sxs-lookup"><span data-stu-id="399d6-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="399d6-161">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="399d6-161">**WSAEFAULT**</span></span> | <span data-ttu-id="399d6-162">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="399d6-162">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="399d6-163">Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="399d6-163">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="399d6-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="399d6-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="399d6-165">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="399d6-165">A blocking operation is currently executing.</span></span> <span data-ttu-id="399d6-166">Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="399d6-166">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="399d6-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="399d6-167">**WSAEINTR**</span></span> | <span data-ttu-id="399d6-168">Una operación de bloqueo fue interrumpida por una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="399d6-168">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="399d6-169">Se devuelve este error si se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="399d6-169">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="399d6-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="399d6-170">**WSAEINVAL**</span></span> | <span data-ttu-id="399d6-171">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="399d6-171">An invalid argument was supplied.</span></span> <span data-ttu-id="399d6-172">Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="399d6-172">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="399d6-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="399d6-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="399d6-174">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="399d6-174">A socket operation encountered a dead network.</span></span> <span data-ttu-id="399d6-175">Se devuelve este error si se ha producido un error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="399d6-175">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="399d6-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="399d6-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="399d6-177">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="399d6-177">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="399d6-178">Se devuelve este error si el *descriptor* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="399d6-178">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="399d6-179">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="399d6-179">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="399d6-180">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="399d6-180">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="399d6-181">Se devuelve este error si no se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="399d6-181">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="399d6-182">Este error también se devuelve si el proveedor de transporte no admite el ioctl de **reserva de puertos de adquisición de SiO \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="399d6-182">This error is also returned if the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="399d6-183">Este error también se devuelve cuando un intento de usar el ioctl de reserva de puerto de adquisición de SiO se realiza en un socket distinto de UDP o TCP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-183">This error is also returned when an attempt to use the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="399d6-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="399d6-184">Remarks</span></span>

<span data-ttu-id="399d6-185">El ioctl de reserva de puertos de adquisición de SiO es compatible con Windows Vista y versiones posteriores del sistema operativo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-185">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="399d6-186">Las aplicaciones y los servicios que necesitan reservar puertos se dividen en dos categorías.</span><span class="sxs-lookup"><span data-stu-id="399d6-186">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="399d6-187">La primera categoría incluye componentes que necesitan un puerto determinado como parte de su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="399d6-187">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="399d6-188">Por lo general, estos componentes prefieren especificar su puerto necesario en el momento de la instalación (por ejemplo, en un manifiesto de aplicación).</span><span class="sxs-lookup"><span data-stu-id="399d6-188">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="399d6-189">La segunda categoría incluye componentes que necesitan cualquier puerto o bloque de puertos disponible en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="399d6-189">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="399d6-190">Estas dos categorías corresponden a las solicitudes de reserva de puertos específicos y comodín.</span><span class="sxs-lookup"><span data-stu-id="399d6-190">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="399d6-191">Las solicitudes de reserva específicas pueden ser persistentes o en tiempo de ejecución, mientras que las solicitudes de reserva de Puerto comodín solo se admiten en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="399d6-191">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="399d6-192">El ioctl de reserva de puertos de adquisición de SiO se usa para solicitar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-192">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="399d6-193">En el caso de las reservas de puerto en tiempo de ejecución, el grupo de puertos requiere que se consuman reservas del proceso en cuyo socket se concedió la reserva.</span><span class="sxs-lookup"><span data-stu-id="399d6-193">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="399d6-194">Las reservas de puerto en tiempo de ejecución solo duran el tiempo que dure el socket en el que se llamó al método de **adquisición de puerto de adquisición de SiO \_ \_ \_**  .</span><span class="sxs-lookup"><span data-stu-id="399d6-194">Runtime port reservations last only as long as the lifetime of the socket on which the **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL was called.</span></span>
<span data-ttu-id="399d6-195">Por el contrario, cualquier proceso puede consumir reservas de Puerto persistentes creadas con la función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.</span><span class="sxs-lookup"><span data-stu-id="399d6-195">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="399d6-196">Una vez que se ha obtenido una reserva de puerto TCP o UDP en tiempo de ejecución, una aplicación puede solicitar asignaciones de puerto desde la reserva de puerto mediante la apertura de un socket TCP o UDP y, a continuación, una llamada a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) que especifica el ioctl de reserva de puertos de Asociación de SiO y el token de reserva antes de emitir una llamada a la función BIND en el socket [**\_ \_ \_**](sio-associate-port-reservation.md)</span><span class="sxs-lookup"><span data-stu-id="399d6-196">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the [**SIO\_ASSOCIATE\_PORT\_RESERVATION**](sio-associate-port-reservation.md) IOCTL and passing the reservation token before issuing a call to the bind function on the socket.</span></span>

<span data-ttu-id="399d6-197">Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**, el socket de esta función se tratará como un socket no superpuesto.</span><span class="sxs-lookup"><span data-stu-id="399d6-197">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="399d6-198">En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine* , salvo que la función puede bloquearse si socket *s* está en modo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="399d6-198">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="399d6-199">Si socket *s* está en modo de no bloqueo, esta función seguirá bloqueando, ya que este ioctl determinado no admite el modo de no bloqueo.</span><span class="sxs-lookup"><span data-stu-id="399d6-199">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="399d6-200">En el caso de los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="399d6-200">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="399d6-201">Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="399d6-201">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="399d6-202">Si la aplicación no puede tolerar el bloqueo en una llamada de función WSAIoctl o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.</span><span class="sxs-lookup"><span data-stu-id="399d6-202">If the application cannot tolerate blocking in a WSAIoctl or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="399d6-203">Se puede producir un error en la operación de  adquisición de **Puerto de \_ adquisición \_ \_ SiO** ioctl con WSAEINTR o **WSA \_ \_ anulada** en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="399d6-203">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="399d6-204">El administrador de e/s cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="399d6-204">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="399d6-205">El socket está cerrado.</span><span class="sxs-lookup"><span data-stu-id="399d6-205">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="399d6-206">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="399d6-206">Examples</span></span>

<span data-ttu-id="399d6-207">En el ejemplo siguiente se adquiere una reserva de puerto en tiempo de ejecución, se crea un socket y se asigna un puerto a partir de la reserva de puerto en tiempo de ejecución para el socket y, a continuación, se cierra el socket y se libera la reserva de puertos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="399d6-207">The following example acquires a runtime port reservation, then creates a socket and allocates a port from the runtime port reservation for the socket, and then closes the socket and the releases the runtime port reservation.</span></span>

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

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

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

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
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

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
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

## <a name="see-also"></a><span data-ttu-id="399d6-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="399d6-208">See also</span></span>

[<span data-ttu-id="399d6-209">**acept**</span><span class="sxs-lookup"><span data-stu-id="399d6-209">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)

[<span data-ttu-id="399d6-210">**volver**</span><span class="sxs-lookup"><span data-stu-id="399d6-210">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="399d6-211">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="399d6-211">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="399d6-212">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="399d6-212">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="399d6-213">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="399d6-213">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="399d6-214">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="399d6-214">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="399d6-215">**\_intervalo de puertos inet \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-215">**INET\_PORT\_RANGE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[<span data-ttu-id="399d6-216">**\_instancia de \_ reserva de Puerto inet \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-216">**INET\_PORT\_RESERVATION\_INSTANCE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[<span data-ttu-id="399d6-217">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="399d6-217">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="399d6-218">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="399d6-218">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="399d6-219">**SIO \_ asociar \_ reserva de puerto \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-219">**SIO\_ASSOCIATE\_PORT\_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="399d6-220">**versión de la reserva del puerto de lanzamiento de SIO \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="399d6-220">**SIO\_RELEASE\_PORT\_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="399d6-221">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="399d6-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="399d6-222">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="399d6-222">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="399d6-223">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="399d6-223">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="399d6-224">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="399d6-224">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="399d6-225">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="399d6-225">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="399d6-226">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="399d6-226">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="399d6-227">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="399d6-227">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
