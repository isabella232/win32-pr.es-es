---
description: Código de control establece el registro de redirección en el nuevo socket TCP que se usa para conectar el servicio de redirección.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: Código de control SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720646"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="11c39-103">Código de control SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS</span><span class="sxs-lookup"><span data-stu-id="11c39-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="11c39-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="11c39-104">Description</span></span>

<span data-ttu-id="11c39-105">El código de control **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** establece el registro de redireccionamiento en el nuevo socket TCP usado para conectarse al destino final para que lo use un servicio de redirección de la plataforma de filtrado de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="11c39-105">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code sets the redirect record to the new TCP socket used for connecting to the final destination for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="11c39-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="11c39-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="11c39-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11c39-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="11c39-108">s</span><span class="sxs-lookup"><span data-stu-id="11c39-108">s</span></span>

<span data-ttu-id="11c39-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="11c39-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="11c39-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="11c39-110">dwIoControlCode</span></span>

<span data-ttu-id="11c39-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="11c39-111">The control code for the operation.</span></span>
<span data-ttu-id="11c39-112">Use **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="11c39-112">Use **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="11c39-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="11c39-113">lpvInBuffer</span></span>

<span data-ttu-id="11c39-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="11c39-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="11c39-115">Este parámetro contiene un puntero al registro de redirección de WFP asociado al socket.</span><span class="sxs-lookup"><span data-stu-id="11c39-115">This parameter contains a pointer to the WFP redirect record associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="11c39-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="11c39-116">cbInBuffer</span></span>

<span data-ttu-id="11c39-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="11c39-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="11c39-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="11c39-118">lpvOutBuffer</span></span>

<span data-ttu-id="11c39-119">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="11c39-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="11c39-120">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="11c39-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="11c39-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="11c39-121">cbOutBuffer</span></span>

<span data-ttu-id="11c39-122">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="11c39-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="11c39-123">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="11c39-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="11c39-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="11c39-124">lpcbBytesReturned</span></span>

<span data-ttu-id="11c39-125">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="11c39-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="11c39-126">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="11c39-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="11c39-127">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="11c39-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="11c39-128">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="11c39-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="11c39-129">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="11c39-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="11c39-130">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="11c39-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="11c39-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="11c39-131">lpvOverlapped</span></span>

<span data-ttu-id="11c39-132">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="11c39-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="11c39-133">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="11c39-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="11c39-134">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="11c39-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="11c39-135">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="11c39-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="11c39-136">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="11c39-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="11c39-137">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="11c39-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="11c39-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="11c39-138">lpCompletionRoutine</span></span>

<span data-ttu-id="11c39-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="11c39-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="11c39-140">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="11c39-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="11c39-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="11c39-141">lpThreadId</span></span>

<span data-ttu-id="11c39-142">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="11c39-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="11c39-143">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="11c39-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="11c39-144">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="11c39-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="11c39-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="11c39-145">lpErrno</span></span>

<span data-ttu-id="11c39-146">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="11c39-146">A pointer to the error code.</span></span>

<span data-ttu-id="11c39-147">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="11c39-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="11c39-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11c39-148">Return value</span></span>

<span data-ttu-id="11c39-149">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="11c39-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="11c39-150">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="11c39-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="11c39-151">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="11c39-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="11c39-152">Código de error</span><span class="sxs-lookup"><span data-stu-id="11c39-152">Error code</span></span> | <span data-ttu-id="11c39-153">Significado</span><span class="sxs-lookup"><span data-stu-id="11c39-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="11c39-154">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="11c39-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="11c39-155">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="11c39-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="11c39-156">Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="11c39-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="11c39-157">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="11c39-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="11c39-158">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="11c39-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="11c39-159">Se devuelve este error si se ha cancelado una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="11c39-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="11c39-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="11c39-160">**WSAEACCES**</span></span> | <span data-ttu-id="11c39-161">Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="11c39-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="11c39-162">Este error se devuelve en varias condiciones, entre las que se incluyen las siguientes: el usuario no dispone de los privilegios administrativos necesarios en el equipo local o la aplicación no se está ejecutando en un shell mejorado como administrador integrado ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="11c39-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="11c39-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="11c39-163">**WSAEFAULT**</span></span> | <span data-ttu-id="11c39-164">El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.</span><span class="sxs-lookup"><span data-stu-id="11c39-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="11c39-165">Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="11c39-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="11c39-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="11c39-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="11c39-167">Se está ejecutando una operación de bloqueo actualmente.</span><span class="sxs-lookup"><span data-stu-id="11c39-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="11c39-168">Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="11c39-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="11c39-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="11c39-169">**WSAEINTR**</span></span> | <span data-ttu-id="11c39-170">Una operación de bloqueo fue interrumpida por una llamada a **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="11c39-170">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="11c39-171">Se devuelve este error si se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="11c39-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="11c39-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="11c39-172">**WSAEINVAL**</span></span> | <span data-ttu-id="11c39-173">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="11c39-173">An invalid argument was supplied.</span></span> <span data-ttu-id="11c39-174">Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="11c39-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="11c39-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="11c39-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="11c39-176">Una operación de socket encontró una red inactiva.</span><span class="sxs-lookup"><span data-stu-id="11c39-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="11c39-177">Se devuelve este error si se ha producido un error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="11c39-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="11c39-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="11c39-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="11c39-179">Se intentó realizar una operación en algo que no es un socket.</span><span class="sxs-lookup"><span data-stu-id="11c39-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="11c39-180">Se devuelve este error si el *descriptor* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="11c39-180">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="11c39-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="11c39-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="11c39-182">La operación intentada no se admite para el tipo de objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="11c39-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="11c39-183">Se devuelve este error si no se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="11c39-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="11c39-184">Este error también se devuelve si el proveedor de transporte no admite el **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** .</span><span class="sxs-lookup"><span data-stu-id="11c39-184">This error is also returned if the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="11c39-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11c39-185">Remarks</span></span>

<span data-ttu-id="11c39-186">El **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** es compatible con Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="11c39-186">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="11c39-187">WFP permite el acceso a la ruta de procesamiento de paquetes TCP/IP, en la que se pueden examinar o cambiar los paquetes salientes y entrantes antes de permitir que se procesen más.</span><span class="sxs-lookup"><span data-stu-id="11c39-187">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="11c39-188">Al puntear en la ruta de acceso de procesamiento de TCP/IP, los fabricantes de software independientes (ISV) pueden crear más fácilmente firewalls, software antivirus, software de diagnóstico y otros tipos de aplicaciones y servicios.</span><span class="sxs-lookup"><span data-stu-id="11c39-188">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="11c39-189">WFP proporciona componentes en modo de usuario y de modo kernel para que los ISV de terceros puedan participar en las decisiones de filtrado que tienen lugar en varias capas de la pila de protocolos TCP/IP y en todo el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="11c39-189">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="11c39-190">La característica de redirección de conexión de WFP permite a un controlador de kernel de llamada de WFP redirigir una conexión localmente a un proceso de modo de usuario, realizar la inspección de contenido en modo de usuario y reenviar el contenido inspeccionado mediante una conexión diferente al destino original.</span><span class="sxs-lookup"><span data-stu-id="11c39-190">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="11c39-191">El **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ registra** ioctl y otros ioctl relacionados son componentes de modo usuario que se usan para permitir que varias aplicaciones proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de forma cooperativa.</span><span class="sxs-lookup"><span data-stu-id="11c39-191">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="11c39-192">Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha inspeccionado otro agente de inspección.</span><span class="sxs-lookup"><span data-stu-id="11c39-192">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="11c39-193">Con la presencia de varios servidores proxy (desarrollados por fabricantes de software independientes, por ejemplo), la conexión utilizada por un proxy para comunicarse con el destino final podría redirigirse a su vez por un segundo proxy, y esa nueva conexión podría redirigirse de nuevo mediante el proxy original.</span><span class="sxs-lookup"><span data-stu-id="11c39-193">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="11c39-194">Sin el seguimiento de la conexión, la conexión original podría no llegar nunca a su destino final, ya que se bloquea en un bucle proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="11c39-194">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="11c39-195">El **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** se usa para proporcionar un seguimiento de la conexión de proxy en las conexiones de socket redirigido.</span><span class="sxs-lookup"><span data-stu-id="11c39-195">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="11c39-196">Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.</span><span class="sxs-lookup"><span data-stu-id="11c39-196">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="11c39-197">El [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) ioctl se usa en un servicio de redireccionamiento basado en WFP para recuperar el registro de redireccionamiento de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo) redireccionado a él mediante su llamada de modo kernel de la guía registrada en las capas de  **\_ \_ redirección de conexión Ale** en un controlador de modo kernel</span><span class="sxs-lookup"><span data-stu-id="11c39-197">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at  **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="11c39-198">El [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) ioctl recupera el contexto de redireccionamiento de un registro de redirección, que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="11c39-198">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL retrieves the redirect context for a redirect record, which is used.</span></span>
<span data-ttu-id="11c39-199">El contexto de redireccionamiento es opcional y se usa si el estado de redirección actual de una conexión es que la conexión se redirigió mediante el servicio de redireccionamiento de llamada o que el servicio de redirección de llamada redirigió la conexión anteriormente, pero posteriormente se redirigió de nuevo mediante otro servicio de redirección. El servicio de redireccionamiento transfiere el registro de redireccionamiento recuperado al socket TCP que usa para crear el proxy del contenido original mediante el protocolo **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** .</span><span class="sxs-lookup"><span data-stu-id="11c39-199">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="11c39-200">La aplicación que llama a la interfaz **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** no necesita comprender el BLOB que contiene el registro de redireccionamiento que se establece.</span><span class="sxs-lookup"><span data-stu-id="11c39-200">The application calling the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect record being set.</span></span>
<span data-ttu-id="11c39-201">Se trata de un BLOB opaco de datos que la aplicación necesita devolver al nuevo socket.</span><span class="sxs-lookup"><span data-stu-id="11c39-201">This is an opaque blob of data that the application needs to pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="11c39-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="11c39-202">See also</span></span>

[<span data-ttu-id="11c39-203">**Opciones de IPPROTO_IP socket**</span><span class="sxs-lookup"><span data-stu-id="11c39-203">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="11c39-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="11c39-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="11c39-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="11c39-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="11c39-206">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="11c39-206">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="11c39-207">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="11c39-207">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="11c39-208">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="11c39-208">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="11c39-209">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="11c39-209">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="11c39-210">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="11c39-210">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="11c39-211">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="11c39-211">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="11c39-212">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="11c39-212">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
