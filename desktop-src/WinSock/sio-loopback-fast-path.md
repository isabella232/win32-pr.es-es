---
description: El código de control configura un socket TCP para una menor latencia y operaciones más rápidas en la interfaz de bucle invertido.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: Código de control de SIO_LOOPBACK_FAST_PATH
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720647"
---
# <a name="sio_loopback_fast_path-control-code"></a><span data-ttu-id="a0eaf-103">Código de control de SIO_LOOPBACK_FAST_PATH</span><span class="sxs-lookup"><span data-stu-id="a0eaf-103">SIO_LOOPBACK_FAST_PATH Control Code</span></span>

## <a name="description"></a><span data-ttu-id="a0eaf-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0eaf-104">Description</span></span>

<span data-ttu-id="a0eaf-105">El código de control de **\_ \_ \_ ruta rápida de bucle invertido de SiO** configura un socket TCP para una menor latencia y operaciones más rápidas en la interfaz de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-105">The **SIO\_LOOPBACK\_FAST\_PATH** control code configures a TCP socket for lower latency and faster operations on the loopback interface.</span></span>

<span data-ttu-id="a0eaf-106">**Importante**  La **\_ ruta de \_ \_ acceso rápido de bucle invertido de SiO** está en desuso y no se recomienda su uso en el código.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-106">**Important**  The **SIO\_LOOPBACK\_FAST\_PATH** is deprecated and is not recommended to be used in your code.</span></span>

<span data-ttu-id="a0eaf-107">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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

## <a name="parameters"></a><span data-ttu-id="a0eaf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0eaf-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="a0eaf-109">s</span><span class="sxs-lookup"><span data-stu-id="a0eaf-109">s</span></span>

<span data-ttu-id="a0eaf-110">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="a0eaf-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="a0eaf-111">dwIoControlCode</span></span>

<span data-ttu-id="a0eaf-112">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-112">The control code for the operation.</span></span>
<span data-ttu-id="a0eaf-113">Use **la \_ \_ ruta de \_ acceso rápido de bucle invertido de SiO** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-113">Use **SIO\_LOOPBACK\_FAST\_PATH** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="a0eaf-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="a0eaf-114">lpvInBuffer</span></span>

<span data-ttu-id="a0eaf-115">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="a0eaf-116">Este parámetro contiene un puntero a un valor booleano que indica si el socket se debe configurar para las operaciones de bucle invertido rápido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-116">This parameter contains a pointer to a Boolean value that indicates if the socket should be configured for fast loopback operations.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="a0eaf-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="a0eaf-117">cbInBuffer</span></span>

<span data-ttu-id="a0eaf-118">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-118">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="a0eaf-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a0eaf-119">lpvOutBuffer</span></span>

<span data-ttu-id="a0eaf-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="a0eaf-121">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="a0eaf-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a0eaf-122">cbOutBuffer</span></span>

<span data-ttu-id="a0eaf-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="a0eaf-124">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="a0eaf-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="a0eaf-125">lpcbBytesReturned</span></span>

<span data-ttu-id="a0eaf-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="a0eaf-127">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="a0eaf-128">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="a0eaf-129">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="a0eaf-130">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="a0eaf-131">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="a0eaf-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="a0eaf-132">lpvOverlapped</span></span>

<span data-ttu-id="a0eaf-133">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a0eaf-134">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="a0eaf-135">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="a0eaf-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="a0eaf-136">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a0eaf-137">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="a0eaf-138">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="a0eaf-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="a0eaf-139">lpCompletionRoutine</span></span>

<span data-ttu-id="a0eaf-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="a0eaf-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="a0eaf-141">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="a0eaf-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="a0eaf-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="a0eaf-142">lpThreadId</span></span>

<span data-ttu-id="a0eaf-143">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="a0eaf-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="a0eaf-144">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="a0eaf-145">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="a0eaf-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="a0eaf-146">lpErrno</span></span>

<span data-ttu-id="a0eaf-147">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-147">A pointer to the error code.</span></span>

<span data-ttu-id="a0eaf-148">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0eaf-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0eaf-149">Return value</span></span>

<span data-ttu-id="a0eaf-150">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="a0eaf-151">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="a0eaf-152">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="a0eaf-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="a0eaf-153">Código de error</span><span class="sxs-lookup"><span data-stu-id="a0eaf-153">Error code</span></span> | <span data-ttu-id="a0eaf-154">Significado</span><span class="sxs-lookup"><span data-stu-id="a0eaf-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="a0eaf-155">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="a0eaf-156">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="a0eaf-157">Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="a0eaf-158">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="a0eaf-159">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="a0eaf-160">Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de **\_ ioctl de volcado de SiO** .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="a0eaf-161">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-161">**WSAEACCES**</span></span> | <span data-ttu-id="a0eaf-162">Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-162">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="a0eaf-163">Este error se devuelve en varias condiciones para las reservas de Puerto persistentes que incluyen lo siguiente: el usuario no dispone de los privilegios administrativos necesarios en el equipo local o la aplicación no se está ejecutando en un shell mejorado como administrador integrado ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="a0eaf-163">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="a0eaf-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-164">**WSAEFAULT**</span></span> | <span data-ttu-id="a0eaf-165">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-165">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="a0eaf-166">Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-166">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="a0eaf-167">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-167">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="a0eaf-168">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-168">A blocking operation is currently executing.</span></span> <span data-ttu-id="a0eaf-169">Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-169">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="a0eaf-170">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-170">**WSAEINTR**</span></span> | <span data-ttu-id="a0eaf-171">Una operación de bloqueo fue interrumpida por una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="a0eaf-171">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="a0eaf-172">Se devuelve este error si se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-172">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="a0eaf-173">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-173">**WSAEINVAL**</span></span> | <span data-ttu-id="a0eaf-174">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-174">An invalid argument was supplied.</span></span> <span data-ttu-id="a0eaf-175">Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-175">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="a0eaf-176">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-176">**WSAENETDOWN**</span></span> | <span data-ttu-id="a0eaf-177">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-177">A socket operation encountered a dead network.</span></span> <span data-ttu-id="a0eaf-178">Se devuelve este error si se ha producido un error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-178">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="a0eaf-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="a0eaf-180">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-180">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="a0eaf-181">Se devuelve este error si el *descriptor* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-181">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="a0eaf-182">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-182">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="a0eaf-183">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-183">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="a0eaf-184">Se devuelve este error si no se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-184">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="a0eaf-185">Este error también se devuelve si el proveedor de transporte no admite el ioctl de **\_ ruta de bucle \_ rápido \_ de SiO** .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-185">This error is also returned if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a0eaf-186">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0eaf-186">Remarks</span></span>

<span data-ttu-id="a0eaf-187">Una aplicación puede usar la **\_ ruta de \_ \_ acceso rápido de bucle invertido de SiO** para reducir la latencia y mejorar el rendimiento de las operaciones de bucle invertido en un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-187">An application can use the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL to reduce the latency and improve the performance of loopback operations on a TCP socket.</span></span>
<span data-ttu-id="a0eaf-188">Este IOCTL solicita que la pila TCP/IP use una ruta de acceso rápida especial para las operaciones de bucle invertido en este socket.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-188">This IOCTL requests that the TCP/IP stack uses a special fast path for loopback operations on this socket.</span></span>
<span data-ttu-id="a0eaf-189">La **\_ ruta de \_ \_ acceso rápido de bucle invertido de SiO** solo se puede usar con Sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-189">The **SIO\_LOOPBACK\_FAST\_PATH** IOCTL can be used only with TCP sockets.</span></span>
<span data-ttu-id="a0eaf-190">Este IOCTL debe usarse en ambos lados de la sesión de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-190">This IOCTL must be used on both sides of the loopback session.</span></span>
<span data-ttu-id="a0eaf-191">La ruta de acceso rápido de bucle invertido TCP se admite mediante la interfaz de bucle invertido IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-191">The TCP loopback fast path is supported using either the IPv4 or IPv6 loopback interface.</span></span>

<span data-ttu-id="a0eaf-192">El socket que planea iniciar la solicitud de conexión debe aplicar este IOCTL antes de realizar la solicitud de conexión.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-192">The socket that plans to initiate the connection request must apply this IOCTL before making the connection request.</span></span>
<span data-ttu-id="a0eaf-193">Por lo tanto, el socket utilizado por las funciones [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) para iniciar la conexión debe aplicar este ioctl para usar la ruta de acceso rápida para las operaciones de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-193">So the socket used by the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) function to initiate the connection must apply this IOCTL to use the fast path for loopback operations.</span></span>

<span data-ttu-id="a0eaf-194">El socket que está escuchando la solicitud de conexión debe aplicar este IOCTL antes de aceptar la conexión.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-194">The socket that is listening for the connection request must apply this IOCTL before accepting the connection.</span></span>
<span data-ttu-id="a0eaf-195">Por lo tanto, el socket utilizado por la función Listen debe aplicar este IOCTL, de modo que los sockets que se acepten usarán la ruta de acceso rápida para el bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-195">So the socket used by the listen function must apply this IOCTL so any sockets that are accepted will use the fast path for loopback.</span></span>
<span data-ttu-id="a0eaf-196">Los sockets devueltos por la función Listen y que se pasan a la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)o [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) se marcarán para utilizar la ruta de acceso rápida especial para las operaciones de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-196">Any sockets returned by the listen function and passed to the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex), or [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) function will be marked to use the special fast path for loopback operations.</span></span>

<span data-ttu-id="a0eaf-197">Una vez que una aplicación establece la conexión en una interfaz de bucle invertido mediante la ruta de acceso rápida, todos los paquetes de la duración de la conexión deben usar la ruta de acceso rápida.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-197">Once an application establishes the connection on a loopback interface using the fast path, all packets for the lifetime of the connection must use the fast path.</span></span>

<span data-ttu-id="a0eaf-198">Aplicar **la \_ \_ ruta de \_ acceso rápido de bucle invertido de SiO** a un socket que se conectará a una ruta de acceso que no es de bucle invertido no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-198">Applying **SIO\_LOOPBACK\_FAST\_PATH** to a socket which will be connected to a non-loopback path will have no effect.</span></span>

<span data-ttu-id="a0eaf-199">Esta optimización de bucle invertido TCP produce paquetes que fluyen a través de la capa de transporte (TL) en lugar del bucle invertido tradicional a través de la capa de red.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-199">This TCP loopback optimization results in packets that flow through the Transport Layer (TL) instead of the traditional loopback through the Network Layer.</span></span>
<span data-ttu-id="a0eaf-200">Esta optimización mejora la latencia de los paquetes de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-200">This optimization improves the latency for loopback packets.</span></span>
<span data-ttu-id="a0eaf-201">Una vez que una aplicación opte por una configuración de nivel de conexión para usar la ruta de acceso rápido de bucle invertido, todos los paquetes seguirán la ruta de acceso de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-201">Once an application opts in for a connection level setting to use the loopback fast path, all packets will follow the loopback path.</span></span>
<span data-ttu-id="a0eaf-202">En el caso de las comunicaciones de bucle invertido, no se espera la congestión y la eliminación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-202">For loopback communications, congestion and packet drop are not expected.</span></span>
<span data-ttu-id="a0eaf-203">La noción de control de congestión y entrega confiable en TCP no será necesaria.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-203">The notion of congestion control and reliable delivery in TCP will be unnecessary.</span></span>
<span data-ttu-id="a0eaf-204">Sin embargo, esto no es cierto para el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-204">This, however, is not true for flow control.</span></span>
<span data-ttu-id="a0eaf-205">Sin control de flujo, el remitente puede sobrecargar el búfer de recepción, lo que provoca un comportamiento de bucle invertido TCP erróneo.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-205">Without flow control, the sender can overwhelm the receive buffer, leading to erroneous TCP loopback behavior.</span></span>
<span data-ttu-id="a0eaf-206">El control de flujo de la ruta de acceso de bucle invertido con TCP optimizado se mantiene colocando las solicitudes de envío en una cola.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-206">The flow control in the TCP optimized loopback path is maintained by placing send requests in a queue.</span></span>
<span data-ttu-id="a0eaf-207">Cuando el búfer de recepción está lleno, la pila TCP/IP garantiza que los envíos no se completarán hasta que se realice el mantenimiento de la cola manteniendo el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-207">When receive buffer is full, the TCP/IP stack guarantees that the sends won't complete until the queue is serviced maintaining flow control.</span></span>

<span data-ttu-id="a0eaf-208">Las conexiones de bucle invertido de Fast Path de TCP en presencia de una llamada de plataforma de filtrado de Windows (WFP) para los datos de conexión deben tener la ruta de acceso lenta no optimizada para bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-208">TCP fast path loopback connections in the presence of a Windows Filtering Platform (WFP) callout for connection data must take the un-optimized slow path for loopback.</span></span>
<span data-ttu-id="a0eaf-209">Por lo tanto, los filtros de WFP impedirán que se use esta nueva ruta de acceso rápido de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-209">So WFP filters will prevent this new loopback fast path from being used.</span></span>
<span data-ttu-id="a0eaf-210">Cuando se habilita un filtro WFP, el sistema utilizará la ruta de acceso lenta incluso si se ha establecido la **\_ ruta de \_ \_ acceso rápido de bucle invertido de SiO** .</span><span class="sxs-lookup"><span data-stu-id="a0eaf-210">When a WFP filter is enabled, the system we will use the slow path even if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL was set.</span></span>
<span data-ttu-id="a0eaf-211">Esto garantiza que las aplicaciones de modo usuario tienen la capacidad de seguridad completa de WFP.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-211">This ensures that user-mode applications have the full WFP security capability.</span></span>

<span data-ttu-id="a0eaf-212">De forma predeterminada, el valor de la **\_ ruta de \_ \_ acceso rápido de los bucles de SiO** es</span><span class="sxs-lookup"><span data-stu-id="a0eaf-212">By default, **SIO\_LOOPBACK\_FAST\_PATH** is disabled.</span></span>

<span data-ttu-id="a0eaf-213">Solo se admite un subconjunto de las opciones de socket TCP/IP cuando se usa la **\_ ruta de \_ \_ acceso rápido de bucle de retroceso de SiO** para habilitar la ruta de acceso rápida de bucle invertido en un socket.</span><span class="sxs-lookup"><span data-stu-id="a0eaf-213">Only a subset of the TCP/IP socket options are supported when the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is used to enable the loopback fast path on a socket.</span></span>
<span data-ttu-id="a0eaf-214">La lista de opciones admitidas incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a0eaf-214">The list of supported options includes the following:</span></span>

* <span data-ttu-id="a0eaf-215">**TTL de IP \_**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-215">**IP\_TTL**</span></span>
* <span data-ttu-id="a0eaf-216">**\_UNIDIFUSIÓN IP \_ si**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-216">**IP\_UNICAST\_IF**</span></span>
* <span data-ttu-id="a0eaf-217">**\_Saltos de UNIDIFUSIÓN IPv6 \_**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-217">**IPV6\_UNICAST\_HOPS**</span></span>
* <span data-ttu-id="a0eaf-218">**\_UNIDIFUSIÓN IPv6 \_ si**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-218">**IPV6\_UNICAST\_IF**</span></span>
* <span data-ttu-id="a0eaf-219">**\_V6ONLY IPv6**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-219">**IPV6\_V6ONLY**</span></span>
* <span data-ttu-id="a0eaf-220">**\_aceptación condicional \_**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-220">**SO\_CONDITIONAL\_ACCEPT**</span></span>
* <span data-ttu-id="a0eaf-221">**\_EXCLUSIVEADDRUSE**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-221">**SO\_EXCLUSIVEADDRUSE**</span></span>
* <span data-ttu-id="a0eaf-222">**\_ \_ escalabilidad de puertos**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-222">**SO\_PORT\_SCALABILITY**</span></span>
* <span data-ttu-id="a0eaf-223">**\_RCVBUF**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-223">**SO\_RCVBUF**</span></span>
* <span data-ttu-id="a0eaf-224">**\_REUSEADDR**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-224">**SO\_REUSEADDR**</span></span>
* <span data-ttu-id="a0eaf-225">**\_BSDURGENT TCP**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-225">**TCP\_BSDURGENT**</span></span>

## <a name="see-also"></a><span data-ttu-id="a0eaf-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0eaf-226">See also</span></span>

[<span data-ttu-id="a0eaf-227">**Opciones de IPPROTO_IP socket**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-227">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="a0eaf-228">**Opciones de IPPROTO_IPV6 socket**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-228">**IPPROTO_IPV6 Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[<span data-ttu-id="a0eaf-229">**Opciones de IPPROTO_TCP socket**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-229">**IPPROTO_TCP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-tcp-socket-options)

[<span data-ttu-id="a0eaf-230">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-230">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="a0eaf-231">**Opciones de SOL_SOCKET socket**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-231">**SOL_SOCKET Socket Options**</span></span>](/windows/desktop/winsock/sol-socket-socket-options)

[<span data-ttu-id="a0eaf-232">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-232">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="a0eaf-233">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-233">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="a0eaf-234">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-234">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="a0eaf-235">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-235">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="a0eaf-236">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-236">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="a0eaf-237">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="a0eaf-237">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
