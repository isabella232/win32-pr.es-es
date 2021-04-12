---
description: El código de control asocia un socket con una reserva persistente o en tiempo de ejecución para un bloque de TCP o UDP identificado por el token de reserva de puerto.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: Código de control de SIO_ASSOCIATE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278093"
---
# <a name="sio_associate_port_reservation-control-code"></a><span data-ttu-id="7d168-103">Código de control de SIO_ASSOCIATE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="7d168-103">SIO_ASSOCIATE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="7d168-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d168-104">Description</span></span>

<span data-ttu-id="7d168-105">El código de control de **\_ \_ \_ reserva de puerto asociado de SiO** asocia un socket con una reserva persistente o en tiempo de ejecución para un bloque de TCP o UDP identificado por el token de reserva de puerto.</span><span class="sxs-lookup"><span data-stu-id="7d168-105">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** control code associates a socket with a persistent or runtime reservation for a block of TCP or UDP identified by the port reservation token.</span></span>
<span data-ttu-id="7d168-106">Este IOCTL debe emitirse antes de enlazar el socket.</span><span class="sxs-lookup"><span data-stu-id="7d168-106">This IOCTL must be issued before the socket is bound.</span></span>
<span data-ttu-id="7d168-107">Si y cuando se enlaza el socket, el puerto asignado a él se seleccionará en la reserva de Puerto identificada por el token especificado.</span><span class="sxs-lookup"><span data-stu-id="7d168-107">If and when the socket is bound, the port assigned to it will be selected from the port reservation identified by the given token.</span></span>
<span data-ttu-id="7d168-108">Si no hay puertos disponibles en la reserva especificada, se producirá un error en la llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="7d168-108">If no ports are available from the specified reservation, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function call will fail.</span></span>

<span data-ttu-id="7d168-109">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d168-109">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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

## <a name="parameters"></a><span data-ttu-id="7d168-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d168-110">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="7d168-111">s</span><span class="sxs-lookup"><span data-stu-id="7d168-111">s</span></span>

<span data-ttu-id="7d168-112">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="7d168-112">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="7d168-113">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="7d168-113">dwIoControlCode</span></span>

<span data-ttu-id="7d168-114">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="7d168-114">The control code for the operation.</span></span>
<span data-ttu-id="7d168-115">Use **SiO \_ asociar el \_ Puerto de \_ reserva** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="7d168-115">Use **SIO\_ASSOCIATE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="7d168-116">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="7d168-116">lpvInBuffer</span></span>

<span data-ttu-id="7d168-117">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="7d168-117">A pointer to the input buffer.</span></span>
<span data-ttu-id="7d168-118">Este parámetro contiene un puntero a una estructura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) con el token para la reserva de puerto TCP o UDP que se va a asociar al socket.</span><span class="sxs-lookup"><span data-stu-id="7d168-118">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to associate with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="7d168-119">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="7d168-119">cbInBuffer</span></span>

<span data-ttu-id="7d168-120">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="7d168-120">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="7d168-121">Este parámetro debe ser al menos el tamaño de la estructura [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="7d168-121">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="7d168-122">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="7d168-122">lpvOutBuffer</span></span>

<span data-ttu-id="7d168-123">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="7d168-123">A pointer to the output buffer.</span></span>
<span data-ttu-id="7d168-124">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="7d168-124">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="7d168-125">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="7d168-125">cbOutBuffer</span></span>

<span data-ttu-id="7d168-126">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="7d168-126">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="7d168-127">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="7d168-127">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="7d168-128">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="7d168-128">lpcbBytesReturned</span></span>

<span data-ttu-id="7d168-129">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="7d168-129">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="7d168-130">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="7d168-130">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="7d168-131">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="7d168-131">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="7d168-132">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="7d168-132">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="7d168-133">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="7d168-133">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="7d168-134">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="7d168-134">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="7d168-135">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="7d168-135">lpvOverlapped</span></span>

<span data-ttu-id="7d168-136">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="7d168-136">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7d168-137">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="7d168-137">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="7d168-138">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="7d168-138">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="7d168-139">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="7d168-139">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7d168-140">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="7d168-140">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="7d168-141">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="7d168-141">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="7d168-142">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="7d168-142">lpCompletionRoutine</span></span>

<span data-ttu-id="7d168-143">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="7d168-143">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="7d168-144">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="7d168-144">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="7d168-145">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="7d168-145">lpThreadId</span></span>

<span data-ttu-id="7d168-146">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="7d168-146">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="7d168-147">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="7d168-147">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="7d168-148">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="7d168-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="7d168-149">lpErrno</span><span class="sxs-lookup"><span data-stu-id="7d168-149">lpErrno</span></span>

<span data-ttu-id="7d168-150">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="7d168-150">A pointer to the error code.</span></span>

<span data-ttu-id="7d168-151">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="7d168-151">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d168-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d168-152">Return value</span></span>

<span data-ttu-id="7d168-153">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="7d168-153">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="7d168-154">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="7d168-154">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="7d168-155">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="7d168-155">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="7d168-156">Código de error</span><span class="sxs-lookup"><span data-stu-id="7d168-156">Error code</span></span> | <span data-ttu-id="7d168-157">Significado</span><span class="sxs-lookup"><span data-stu-id="7d168-157">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="7d168-158">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="7d168-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="7d168-159">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="7d168-159">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="7d168-160">Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="7d168-160">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="7d168-161">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="7d168-161">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="7d168-162">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7d168-162">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="7d168-163">Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de **\_ ioctl de volcado de SiO** .</span><span class="sxs-lookup"><span data-stu-id="7d168-163">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="7d168-164">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="7d168-164">**WSAEACCES**</span></span> | <span data-ttu-id="7d168-165">Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="7d168-165">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="7d168-166">Este error se devuelve en varias condiciones para las reservas de Puerto persistentes que incluyen lo siguiente: el usuario no dispone de los privilegios administrativos necesarios en el equipo local o la aplicación no se está ejecutando en un shell mejorado como administrador integrado ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="7d168-166">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="7d168-167">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7d168-167">**WSAEFAULT**</span></span> | <span data-ttu-id="7d168-168">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="7d168-168">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="7d168-169">Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="7d168-169">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="7d168-170">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="7d168-170">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="7d168-171">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="7d168-171">A blocking operation is currently executing.</span></span> <span data-ttu-id="7d168-172">Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="7d168-172">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="7d168-173">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="7d168-173">**WSAEINTR**</span></span> | <span data-ttu-id="7d168-174">Una operación de bloqueo fue interrumpida por una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="7d168-174">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="7d168-175">Se devuelve este error si se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7d168-175">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="7d168-176">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="7d168-176">**WSAEINVAL**</span></span> | <span data-ttu-id="7d168-177">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="7d168-177">An invalid argument was supplied.</span></span> <span data-ttu-id="7d168-178">Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="7d168-178">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="7d168-179">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="7d168-179">**WSAENETDOWN**</span></span> | <span data-ttu-id="7d168-180">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d168-180">A socket operation encountered a dead network.</span></span> <span data-ttu-id="7d168-181">Se devuelve este error si se ha producido un error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="7d168-181">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="7d168-182">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="7d168-182">**WSAENOTSOCK**</span></span> | <span data-ttu-id="7d168-183">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="7d168-183">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="7d168-184">Se devuelve este error si el *descriptor* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="7d168-184">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="7d168-185">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="7d168-185">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="7d168-186">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="7d168-186">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="7d168-187">Se devuelve este error si no se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="7d168-187">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="7d168-188">Este error también se devuelve si el proveedor de transporte no admite el ioctl de **reserva de puertos de Asociación de SiO \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="7d168-188">This error is also returned if the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="7d168-189">Este error también se devuelve cuando se realiza un intento de usar el ioctl de reserva de puerto del asociado de SiO en un socket distinto de UDP o TCP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d168-189">This error is also returned when an attempt to use the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="7d168-190">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d168-190">Remarks</span></span>

<span data-ttu-id="7d168-191">Se admite el ioctl de reserva de puertos de Asociación de SiO en Windows Vista y versiones posteriores del sistema operativo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d168-191">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="7d168-192">Las aplicaciones y los servicios que necesitan reservar puertos se dividen en dos categorías.</span><span class="sxs-lookup"><span data-stu-id="7d168-192">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="7d168-193">La primera categoría incluye componentes que necesitan un puerto determinado como parte de su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="7d168-193">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="7d168-194">Por lo general, estos componentes prefieren especificar su puerto necesario en el momento de la instalación (por ejemplo, en un manifiesto de aplicación).</span><span class="sxs-lookup"><span data-stu-id="7d168-194">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="7d168-195">La segunda categoría incluye componentes que necesitan cualquier puerto o bloque de puertos disponible en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7d168-195">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="7d168-196">Estas dos categorías corresponden a las solicitudes de reserva de puertos específicos y comodín.</span><span class="sxs-lookup"><span data-stu-id="7d168-196">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="7d168-197">Las solicitudes de reserva específicas pueden ser persistentes o en tiempo de ejecución, mientras que las solicitudes de reserva de Puerto comodín solo se admiten en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7d168-197">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="7d168-198">Se usa el ioctl de **reserva de puertos de Asociación de SiO \_ \_ \_** para asociar una reserva de puerto TCP o UDP con una reserva persistente o en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7d168-198">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used to associate a TCP or UDP port reservation with either a persistent or runtime reservation.</span></span>

<span data-ttu-id="7d168-199">La función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) proporciona la capacidad de una aplicación o servicio para reservar un bloque persistente de puertos TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="7d168-199">The [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function provides the ability for an application or service to reserve a persistent block of TCP or UDP ports.</span></span>
<span data-ttu-id="7d168-200">Las reservas de Puerto persistentes se registran en un almacén persistente para el módulo TCP o UDP en Windows.</span><span class="sxs-lookup"><span data-stu-id="7d168-200">Persistent port reservations are recorded in a persistent store for the TCP or UDP module in Windows.</span></span>
<span data-ttu-id="7d168-201">Tenga en cuenta que el token de una reserva de Puerto persistente determinada puede cambiar cada vez que se reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="7d168-201">Note that the token for a given persistent port reservation may change each time the system is restarted.</span></span>

<span data-ttu-id="7d168-202">Una vez obtenida una reserva de puerto TCP o UDP persistente, una aplicación puede solicitar asignaciones de puerto desde la reserva de Puerto abriendo un socket TCP o UDP y, a continuación, llamando a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando el ioctl de reserva de puertos de Asociación de SiO y pasando el token de reserva antes de emitir una llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) en el socket. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d168-202">Once a persistent TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="7d168-203">El [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl se puede usar para solicitar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="7d168-203">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="7d168-204">En el caso de las reservas de puerto en tiempo de ejecución, el grupo de puertos requiere que se consuman reservas del proceso en cuyo socket se concedió la reserva.</span><span class="sxs-lookup"><span data-stu-id="7d168-204">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="7d168-205">Las reservas de puerto en tiempo de ejecución solo duran el tiempo que dure el socket en el que se llamó a la [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl.</span><span class="sxs-lookup"><span data-stu-id="7d168-205">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="7d168-206">Por el contrario, cualquier proceso puede consumir reservas de Puerto persistentes creadas con la función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.</span><span class="sxs-lookup"><span data-stu-id="7d168-206">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="7d168-207">Una vez que se ha obtenido una reserva de puerto TCP o UDP en tiempo de ejecución, una aplicación puede solicitar asignaciones de puerto desde la reserva de puerto mediante la apertura de un socket TCP o UDP y, a continuación, una llamada a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) que especifica el ioctl de reserva de [](/windows/desktop/api/winsock/nf-winsock-bind) puertos de Asociación de SiO y el token de reserva antes de emitir una llamada a la función BIND en el socket **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d168-207">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="7d168-208">Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son NULL, el socket de esta función se tratará como un socket no superpuesto.</span><span class="sxs-lookup"><span data-stu-id="7d168-208">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="7d168-209">En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine* , salvo que la función puede bloquearse si socket *s* está en modo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7d168-209">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="7d168-210">Si socket *s* está en modo de no bloqueo, esta función seguirá bloqueando, ya que este ioctl determinado no admite el modo de no bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7d168-210">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="7d168-211">En el caso de los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="7d168-211">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="7d168-212">Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="7d168-212">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="7d168-213">Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.</span><span class="sxs-lookup"><span data-stu-id="7d168-213">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="7d168-214">Se puede producir un error en el ioctl de  **reserva de \_ \_ puertos \_ de asociación** de **WSA_OPERATION_ABORTED** WSAEINTR en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="7d168-214">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA_OPERATION_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="7d168-215">El administrador de e/s cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d168-215">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="7d168-216">El socket está cerrado.</span><span class="sxs-lookup"><span data-stu-id="7d168-216">The socket is closed.</span></span>

<span data-ttu-id="7d168-217">El ioctl de reserva de puerto de Asociación de la **\_ Asociación \_ \_** IOCTL que se pasa a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** para una reserva de Puerto persistente solo se puede usar en una aplicación cuando el usuario ha iniciado sesión como miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="7d168-217">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function for a persistent port reservation can only be used in an application when the user is logged on as a member of the Administrators group.</span></span>
<span data-ttu-id="7d168-218">Si se usa **SiO \_ Associate de \_ \_ reserva de Puerto** ioctl en una aplicación cuando el usuario no es miembro del grupo de administradores, se producirá un error en la llamada a la función y se devolverá **WSAEACCES** .</span><span class="sxs-lookup"><span data-stu-id="7d168-218">If **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used in an application when the user is not a member of the Administrators group, the function call will fail and **WSAEACCES** is returned.</span></span>
<span data-ttu-id="7d168-219">También se puede producir un error en el uso del ioctl de reserva de puertos de Asociación de SiO en Windows Vista y versiones posteriores. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d168-219">The use of the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can also fail because of user account control (UAC) on Windows Vista and later.</span></span>
<span data-ttu-id="7d168-220">Si una aplicación que usa este IOCTL con una reserva de Puerto persistente es ejecutada por un usuario que ha iniciado sesión como miembro del grupo de administradores distinto del administrador integrado, esta llamada producirá un error a menos que la aplicación se haya marcado en el archivo de manifiesto con una **requestedExecutionLevel** establecida en *requireAdministrator*.</span><span class="sxs-lookup"><span data-stu-id="7d168-220">If an application that uses this IOCTL with a persistent port reservation is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to *requireAdministrator*.</span></span>
<span data-ttu-id="7d168-221">Si la aplicación no tiene este archivo de manifiesto, un usuario que haya iniciado sesión como miembro del grupo administradores que no sea el administrador integrado deberá ejecutar la aplicación en un shell mejorado como administrador integrado ( `RunAs administrator` ) para que esta función se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d168-221">If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (`RunAs administrator`) for this function to succeed.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d168-222">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d168-222">See also</span></span>

[<span data-ttu-id="7d168-223">**volver**</span><span class="sxs-lookup"><span data-stu-id="7d168-223">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="7d168-224">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7d168-224">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="7d168-225">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7d168-225">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="7d168-226">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7d168-226">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="7d168-227">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7d168-227">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="7d168-228">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="7d168-228">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="7d168-229">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7d168-229">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="7d168-230">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="7d168-230">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="7d168-231">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="7d168-231">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="7d168-232">**SIO_RELEASE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="7d168-232">**SIO_RELEASE_PORT_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="7d168-233">tomacorriente</span><span class="sxs-lookup"><span data-stu-id="7d168-233">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="7d168-234">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="7d168-234">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="7d168-235">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="7d168-235">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="7d168-236">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="7d168-236">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="7d168-237">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="7d168-237">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="7d168-238">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="7d168-238">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="7d168-239">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="7d168-239">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
