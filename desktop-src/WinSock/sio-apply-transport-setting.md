---
description: El código de control aplica una o más configuraciones de transporte a un socket.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: Código de control de SIO_APPLY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720482"
---
# <a name="sio_apply_transport_setting-control-code"></a><span data-ttu-id="03350-103">Código de control de SIO_APPLY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="03350-103">SIO_APPLY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="03350-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="03350-104">Description</span></span>

<span data-ttu-id="03350-105">El código de control de **\_ \_ \_ configuración de transporte SiO** aplica una o más configuraciones de transporte a un socket.</span><span class="sxs-lookup"><span data-stu-id="03350-105">The **SIO\_APPLY\_TRANSPORT\_SETTING** control code applies one or more transport settings to a socket.</span></span>

<span data-ttu-id="03350-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="03350-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="03350-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03350-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="03350-108">s</span><span class="sxs-lookup"><span data-stu-id="03350-108">s</span></span>

<span data-ttu-id="03350-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="03350-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="03350-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="03350-110">dwIoControlCode</span></span>

<span data-ttu-id="03350-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="03350-111">The control code for the operation.</span></span>
<span data-ttu-id="03350-112">Use **la \_ \_ \_ opción de transporte SiO Apply** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="03350-112">Use **SIO\_APPLY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="03350-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="03350-113">lpvInBuffer</span></span>

<span data-ttu-id="03350-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="03350-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="03350-115">Este parámetro contiene un puntero a una estructura en la que el primer miembro de la estructura es una estructura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) que determina qué configuración de transporte se aplica.</span><span class="sxs-lookup"><span data-stu-id="03350-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being applied.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="03350-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="03350-116">cbInBuffer</span></span>

<span data-ttu-id="03350-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="03350-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="03350-118">Este parámetro depende de la configuración de transporte que se aplica.</span><span class="sxs-lookup"><span data-stu-id="03350-118">This parameter depends on the transport setting being applied.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="03350-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="03350-119">lpvOutBuffer</span></span>

<span data-ttu-id="03350-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="03350-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="03350-121">Este parámetro depende de la configuración de transporte que se aplica.</span><span class="sxs-lookup"><span data-stu-id="03350-121">This parameter depends on the transport setting being applied.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="03350-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="03350-122">cbOutBuffer</span></span>

<span data-ttu-id="03350-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="03350-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="03350-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="03350-124">lpcbBytesReturned</span></span>

<span data-ttu-id="03350-125">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="03350-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="03350-126">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="03350-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="03350-127">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="03350-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="03350-128">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="03350-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="03350-129">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="03350-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="03350-130">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="03350-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="03350-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="03350-131">lpvOverlapped</span></span>

<span data-ttu-id="03350-132">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="03350-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="03350-133">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="03350-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="03350-134">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="03350-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="03350-135">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="03350-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="03350-136">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="03350-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="03350-137">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="03350-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="03350-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="03350-138">lpCompletionRoutine</span></span>

<span data-ttu-id="03350-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="03350-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="03350-140">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="03350-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="03350-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="03350-141">lpThreadId</span></span>

<span data-ttu-id="03350-142">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="03350-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="03350-143">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="03350-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="03350-144">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="03350-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="03350-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="03350-145">lpErrno</span></span>

<span data-ttu-id="03350-146">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="03350-146">A pointer to the error code.</span></span>

<span data-ttu-id="03350-147">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="03350-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="03350-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03350-148">Return value</span></span>

<span data-ttu-id="03350-149">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="03350-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="03350-150">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="03350-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="03350-151">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="03350-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="03350-152">Código de error</span><span class="sxs-lookup"><span data-stu-id="03350-152">Error code</span></span> | <span data-ttu-id="03350-153">Significado</span><span class="sxs-lookup"><span data-stu-id="03350-153">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="03350-154">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="03350-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="03350-155">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="03350-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="03350-156">Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="03350-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="03350-157">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="03350-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="03350-158">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="03350-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="03350-159">Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de ioctl de **\_ volcado de SiO** .</span><span class="sxs-lookup"><span data-stu-id="03350-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="03350-160">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="03350-160">**WSAEFAULT**</span></span> | <span data-ttu-id="03350-161">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="03350-161">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="03350-162">Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="03350-162">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="03350-163">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="03350-163">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="03350-164">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="03350-164">A blocking operation is currently executing.</span></span> <span data-ttu-id="03350-165">Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="03350-165">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="03350-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="03350-166">**WSAEINTR**</span></span> | <span data-ttu-id="03350-167">Una operación de bloqueo fue interrumpida por una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="03350-167">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="03350-168">Se devuelve este error si se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="03350-168">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="03350-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="03350-169">**WSAEINVAL**</span></span> | <span data-ttu-id="03350-170">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="03350-170">An invalid argument was supplied.</span></span> <span data-ttu-id="03350-171">Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="03350-171">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="03350-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="03350-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="03350-173">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="03350-173">A socket operation encountered a dead network.</span></span> <span data-ttu-id="03350-174">Se devuelve este error si se ha producido un error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="03350-174">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="03350-175">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="03350-175">**WSAENOTSOCK**</span></span> | <span data-ttu-id="03350-176">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="03350-176">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="03350-177">Se devuelve este error si el *descriptor* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="03350-177">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="03350-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="03350-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="03350-179">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="03350-179">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="03350-180">Se devuelve este error si no se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="03350-180">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="03350-181">Este error también se devuelve si el proveedor de transporte no admite la configuración de transporte de la **\_ \_ \_ opción SiO Apply** .</span><span class="sxs-lookup"><span data-stu-id="03350-181">This error is also returned if the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="03350-182">Este error también se devuelve cuando se realiza un intento de usar la configuración de transporte de la **\_ \_ \_ opción SiO** en un socket distinto de UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="03350-182">This error is also returned when an attempt to use the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="03350-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03350-183">Remarks</span></span>

<span data-ttu-id="03350-184">El ioctl de **\_ \_ \_ configuración de transporte SiO** es compatible con windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="03350-184">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="03350-185">La **\_ configuración de \_ transporte \_ de SiO aplicar** es un ioctl genérico que se usa para aplicar la configuración de transporte al socket.</span><span class="sxs-lookup"><span data-stu-id="03350-185">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to apply transport setting to socket.</span></span>
<span data-ttu-id="03350-186">La configuración de transporte que se está aplicando se basa en el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el parámetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="03350-186">The transport setting being applied is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="03350-187">A partir de Windows 8 y Windows Server 2012, el sistema define la capacidad de **REAL_TIME_NOTIFICATION_CAPABILITY** en un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="03350-187">Starting with Windows 8 and Windows Server 2012, the system defines the **REAL_TIME_NOTIFICATION_CAPABILITY** capability on a TCP socket.</span></span>
<span data-ttu-id="03350-188">A partir de Windows 10 y Windows Server 2016, también se define el **\_ \_ contexto Associate NAMERES** .</span><span class="sxs-lookup"><span data-stu-id="03350-188">Starting with Windows 10 and Windows Server 2016, **ASSOCIATE\_NAMERES\_CONTEXT** is also defined.</span></span>
<span data-ttu-id="03350-189">Para obtener más información, vea [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) y [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span><span class="sxs-lookup"><span data-stu-id="03350-189">For more information, see [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span></span>

<span data-ttu-id="03350-190">Si el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el parámetro lpvInBuffer tiene el miembro GUID establecido en **\_ funcionalidad de \_ notificación \_ en tiempo real**, se trata de una solicitud para aplicar la configuración de notificación en tiempo real para el socket TCP que se usa con la [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="03350-190">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the lpvInBuffer parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to apply real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="03350-191">El parámetro *lpvInBuffer* debe apuntar a una estructura **REAL_TIME_NOTIFICATION_SETTING_INPUT** .</span><span class="sxs-lookup"><span data-stu-id="03350-191">The *lpvInBuffer* parameter should point to a **REAL_TIME_NOTIFICATION_SETTING_INPUT** structure.</span></span>
<span data-ttu-id="03350-192">El parámetro *lpvOutBuffer* no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="03350-192">The *lpvOutBuffer* parameter is unused for this operation.</span></span>
<span data-ttu-id="03350-193">Esta configuración de transporte solo se aplica a los Sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="03350-193">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="03350-194">Esta configuración de transporte proporciona una manera para que WinInet o servicios de red similares marquen un socket TCP determinado como [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) habilitado.</span><span class="sxs-lookup"><span data-stu-id="03350-194">This transport setting provides a way for WinInet or similar network services to mark a given TCP socket as [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) enabled.</span></span>
<span data-ttu-id="03350-195">Windows marcará el socket TCP correspondiente y configurará la configuración de hardware y software adecuada cuando se llame a esta opción.</span><span class="sxs-lookup"><span data-stu-id="03350-195">Windows will mark the corresponding TCP socket and configure appropriate hardware and software settings when this option is called.</span></span>
<span data-ttu-id="03350-196">Una aplicación de la tienda Windows no llamará a este IOCTL directamente.</span><span class="sxs-lookup"><span data-stu-id="03350-196">A Windows Store app will not call this IOCTL directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="03350-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="03350-197">See also</span></span>

[<span data-ttu-id="03350-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="03350-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="03350-199">tomacorriente</span><span class="sxs-lookup"><span data-stu-id="03350-199">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="03350-200">**SIO_QUERY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="03350-200">**SIO_QUERY_TRANSPORT_SETTING**</span></span>](sio-query-transport-setting.md)

[<span data-ttu-id="03350-201">**TRANSPORT_SETTING_ID**</span><span class="sxs-lookup"><span data-stu-id="03350-201">**TRANSPORT_SETTING_ID**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[<span data-ttu-id="03350-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="03350-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="03350-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="03350-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="03350-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="03350-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="03350-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="03350-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="03350-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="03350-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="03350-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="03350-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
