---
description: Código de control que configura los parámetros de tiempo de espera de retransmisión (RTO) inicial en un socket.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: Código de control de SIO_TCP_INITIAL_RTO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "104488471"
---
# <a name="sio_tcp_initial_rto-control-code"></a><span data-ttu-id="f3fc3-103">Código de control de SIO_TCP_INITIAL_RTO</span><span class="sxs-lookup"><span data-stu-id="f3fc3-103">SIO_TCP_INITIAL_RTO control code</span></span>

## <a name="description"></a><span data-ttu-id="f3fc3-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3fc3-104">Description</span></span>

<span data-ttu-id="f3fc3-105">El código de control de **SIO_TCP_INITIAL_RTO** configura los parámetros de tiempo de espera de retransmisión inicial (RTO) en un socket.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-105">The **SIO_TCP_INITIAL_RTO** control code configures initial retransmission timeout (RTO) parameters on a socket.</span></span>

<span data-ttu-id="f3fc3-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="f3fc3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3fc3-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="f3fc3-108">s</span><span class="sxs-lookup"><span data-stu-id="f3fc3-108">s</span></span>

<span data-ttu-id="f3fc3-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="f3fc3-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="f3fc3-110">dwIoControlCode</span></span>

<span data-ttu-id="f3fc3-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-111">The control code for the operation.</span></span>
<span data-ttu-id="f3fc3-112">Use **SIO_TCP_INITIAL_RTO** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-112">Use **SIO_TCP_INITIAL_RTO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="f3fc3-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="f3fc3-113">lpvInBuffer</span></span>

<span data-ttu-id="f3fc3-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="f3fc3-115">Este parámetro contiene un puntero al [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) asociado al socket.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-115">This parameter contains a pointer to the [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="f3fc3-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="f3fc3-116">cbInBuffer</span></span>

<span data-ttu-id="f3fc3-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="f3fc3-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="f3fc3-118">lpvOutBuffer</span></span>

<span data-ttu-id="f3fc3-119">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="f3fc3-120">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="f3fc3-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="f3fc3-121">cbOutBuffer</span></span>

<span data-ttu-id="f3fc3-122">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="f3fc3-123">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="f3fc3-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="f3fc3-124">lpcbBytesReturned</span></span>

<span data-ttu-id="f3fc3-125">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="f3fc3-126">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="f3fc3-127">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="f3fc3-128">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="f3fc3-129">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="f3fc3-130">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="f3fc3-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="f3fc3-131">lpvOverlapped</span></span>

<span data-ttu-id="f3fc3-132">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="f3fc3-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="f3fc3-133">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="f3fc3-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="f3fc3-134">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="f3fc3-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="f3fc3-135">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="f3fc3-136">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="f3fc3-137">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="f3fc3-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="f3fc3-138">lpCompletionRoutine</span></span>

<span data-ttu-id="f3fc3-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="f3fc3-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="f3fc3-140">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="f3fc3-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="f3fc3-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="f3fc3-141">lpThreadId</span></span>

<span data-ttu-id="f3fc3-142">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="f3fc3-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="f3fc3-143">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="f3fc3-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="f3fc3-144">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="f3fc3-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="f3fc3-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="f3fc3-145">lpErrno</span></span>

<span data-ttu-id="f3fc3-146">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-146">A pointer to the error code.</span></span>

<span data-ttu-id="f3fc3-147">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="f3fc3-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3fc3-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3fc3-148">Return value</span></span>

<span data-ttu-id="f3fc3-149">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="f3fc3-150">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="f3fc3-151">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="f3fc3-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="f3fc3-152">Código de error</span><span class="sxs-lookup"><span data-stu-id="f3fc3-152">Error code</span></span> | <span data-ttu-id="f3fc3-153">Significado</span><span class="sxs-lookup"><span data-stu-id="f3fc3-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="f3fc3-154">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="f3fc3-155">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="f3fc3-156">Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="f3fc3-157">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="f3fc3-158">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="f3fc3-159">Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de ioctl de **\_ volcado de SiO** .</span><span class="sxs-lookup"><span data-stu-id="f3fc3-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="f3fc3-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-160">**WSAEACCES**</span></span> | <span data-ttu-id="f3fc3-161">Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="f3fc3-162">Este error se devuelve en varias condiciones, entre las que se incluyen las siguientes: el usuario no dispone de los privilegios administrativos necesarios en el equipo local o la aplicación no se está ejecutando en un shell mejorado como administrador integrado ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="f3fc3-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="f3fc3-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-163">**WSAEFAULT**</span></span> | <span data-ttu-id="f3fc3-164">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="f3fc3-165">Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="f3fc3-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="f3fc3-167">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="f3fc3-168">Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="f3fc3-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-169">**WSAEINTR**</span></span> | <span data-ttu-id="f3fc3-170">Una operación de bloqueo fue interrumpida por una llamada a *WSACancelBlockingCall*.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-170">A blocking operation was interrupted by a call to *WSACancelBlockingCall*.</span></span> <span data-ttu-id="f3fc3-171">Se devuelve este error si se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="f3fc3-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-172">**WSAEINVAL**</span></span> | <span data-ttu-id="f3fc3-173">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-173">An invalid argument was supplied.</span></span> <span data-ttu-id="f3fc3-174">Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="f3fc3-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="f3fc3-176">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="f3fc3-177">Se devuelve este error si se ha producido un error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="f3fc3-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="f3fc3-179">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="f3fc3-180">Se devuelve este error si el descriptor no es un socket.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-180">This error is returned if the descriptor s is not a socket.</span></span> |
| <span data-ttu-id="f3fc3-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="f3fc3-182">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="f3fc3-183">Se devuelve este error si no se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="f3fc3-184">Este error también se devuelve si el proveedor de transporte no admite el ioctl **SIO_TCP_INITIAL_RTO** .</span><span class="sxs-lookup"><span data-stu-id="f3fc3-184">This error is also returned if the **SIO_TCP_INITIAL_RTO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f3fc3-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3fc3-185">Remarks</span></span>

<span data-ttu-id="f3fc3-186">Una aplicación puede usar el **SIO_TCP_INITIAL_RTO** ioctl para controlar las características de retransmisión iniciales (SYN/SYN + ACK) de un socket TCP, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-186">An application can use the **SIO_TCP_INITIAL_RTO** IOCTL to control the initial (SYN / SYN+ACK) retransmission characteristics of a TCP socket if required.</span></span>
<span data-ttu-id="f3fc3-187">Una aplicación, si se usa esta opción, debe proporcionar los valores adecuados antes de iniciar un intento de conexión TCP en el socket.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-187">An application, if using this option, must supply suitable values before starting a TCP connection attempt on the socket.</span></span>

<span data-ttu-id="f3fc3-188">El [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) ioctl permite que una aplicación configure el tiempo de espera de retransmisión (RTO) inicial (SYN) que usa el socket.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-188">The [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL allows an application to configure the initial (SYN) retransmission timeout (RTO) used by the socket.</span></span>

<span data-ttu-id="f3fc3-189">Un puntero a una estructura de [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) pasada en el parámetro *lpvInBuffer* permite que una aplicación configure el tiempo de ida y vuelta (RTT) inicial que se usa para calcular el tiempo de espera de la retransmisión.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-189">A pointer to a [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) structure passed in the *lpvInBuffer* parameter allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout.</span></span>
<span data-ttu-id="f3fc3-190">La aplicación también puede configurar el número de retransmisiones que se intentarán antes de que se produzca un error en el intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="f3fc3-190">The application can also configure the number of retransmissions that will be attempted before the connection attempt fails.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3fc3-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3fc3-191">See also</span></span>

[<span data-ttu-id="f3fc3-192">tomacorriente</span><span class="sxs-lookup"><span data-stu-id="f3fc3-192">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="f3fc3-193">**TCP_INITIAL_RTO_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-193">**TCP_INITIAL_RTO_PARAMETERS**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[<span data-ttu-id="f3fc3-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="f3fc3-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="f3fc3-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="f3fc3-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="f3fc3-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="f3fc3-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="f3fc3-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
