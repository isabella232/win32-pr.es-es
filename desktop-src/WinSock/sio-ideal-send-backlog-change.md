---
description: El código de control notifica una aplicación cuando cambia el valor de trabajo pendiente de envío ideal para la conexión.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: Código de control de SIO_IDEAL_SEND_BACKLOG_CHANGE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812452"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a><span data-ttu-id="5318b-103">Código de control de SIO_IDEAL_SEND_BACKLOG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="5318b-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="5318b-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="5318b-104">Description</span></span>

<span data-ttu-id="5318b-105">El código de control de **\_ \_ \_ \_ cambio de trabajo pendiente de envío adecuado de SiO** notifica una aplicación cuando cambia el valor de trabajo pendiente de envío (ISB) ideal para la conexión.</span><span class="sxs-lookup"><span data-stu-id="5318b-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** control code notifies an application when the ideal send backlog (ISB) value changes for the connection.</span></span>

<span data-ttu-id="5318b-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="5318b-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="5318b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5318b-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="5318b-108">s</span><span class="sxs-lookup"><span data-stu-id="5318b-108">s</span></span>

<span data-ttu-id="5318b-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="5318b-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="5318b-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="5318b-110">dwIoControlCode</span></span>

<span data-ttu-id="5318b-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="5318b-111">The control code for the operation.</span></span>
<span data-ttu-id="5318b-112">Use **el \_ \_ cambio de \_ trabajo \_ acumulado de envío ideal** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5318b-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="5318b-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="5318b-113">lpvInBuffer</span></span>

<span data-ttu-id="5318b-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="5318b-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="5318b-115">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5318b-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="5318b-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="5318b-116">cbInBuffer</span></span>

<span data-ttu-id="5318b-117">Tamaño, en bytes, del búfer de entrada. Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5318b-117">The size, in bytes, of the input buffer.This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="5318b-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5318b-118">lpvOutBuffer</span></span>

<span data-ttu-id="5318b-119">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5318b-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="5318b-120">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5318b-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="5318b-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5318b-121">cbOutBuffer</span></span>

<span data-ttu-id="5318b-122">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5318b-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="5318b-123">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="5318b-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="5318b-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="5318b-124">lpcbBytesReturned</span></span>

<span data-ttu-id="5318b-125">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5318b-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="5318b-126">Este parámetro devuelve un valor **DWORD** de cero para esta operación, ya que no hay ninguna salida.</span><span class="sxs-lookup"><span data-stu-id="5318b-126">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="5318b-127">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="5318b-127">lpvOverlapped</span></span>

<span data-ttu-id="5318b-128">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="5318b-128">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5318b-129">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="5318b-129">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="5318b-130">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="5318b-130">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="5318b-131">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="5318b-131">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5318b-132">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="5318b-132">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="5318b-133">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="5318b-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="5318b-134">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="5318b-134">lpCompletionRoutine</span></span>

<span data-ttu-id="5318b-135">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="5318b-135">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="5318b-136">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="5318b-136">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="5318b-137">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="5318b-137">lpThreadId</span></span>

<span data-ttu-id="5318b-138">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="5318b-138">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="5318b-139">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="5318b-139">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="5318b-140">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5318b-140">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="5318b-141">lpErrno</span><span class="sxs-lookup"><span data-stu-id="5318b-141">lpErrno</span></span>

<span data-ttu-id="5318b-142">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="5318b-142">A pointer to the error code.</span></span>

<span data-ttu-id="5318b-143">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5318b-143">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="5318b-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5318b-144">Return value</span></span>

<span data-ttu-id="5318b-145">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5318b-145">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="5318b-146">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="5318b-146">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="5318b-147">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="5318b-147">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="5318b-148">Código de error</span><span class="sxs-lookup"><span data-stu-id="5318b-148">Error code</span></span> | <span data-ttu-id="5318b-149">Significado</span><span class="sxs-lookup"><span data-stu-id="5318b-149">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="5318b-150">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="5318b-150">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="5318b-151">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="5318b-151">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="5318b-152">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="5318b-152">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="5318b-153">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SiO \_ Flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="5318b-153">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="5318b-154">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="5318b-154">**WSAEFAULT**</span></span> | <span data-ttu-id="5318b-155">El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="5318b-155">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="5318b-156">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="5318b-156">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="5318b-157">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="5318b-157">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="5318b-158">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="5318b-158">**WSAEINTR**</span></span> | <span data-ttu-id="5318b-159">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="5318b-159">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="5318b-160">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="5318b-160">**WSAEINVAL**</span></span> | <span data-ttu-id="5318b-161">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="5318b-161">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="5318b-162">Se devuelve este error si el parámetro *cbOutBuffer* no es cero.</span><span class="sxs-lookup"><span data-stu-id="5318b-162">This error is returned if the *cbOutBuffer* parameter is not zero.</span></span> |
| <span data-ttu-id="5318b-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="5318b-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="5318b-164">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="5318b-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="5318b-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="5318b-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="5318b-166">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="5318b-166">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="5318b-167">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="5318b-167">**WSAENOTCONN**</span></span> | <span data-ttu-id="5318b-168">El socket *s* no está conectado.</span><span class="sxs-lookup"><span data-stu-id="5318b-168">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="5318b-169">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="5318b-169">**WSAENOTSOCK**</span></span> | <span data-ttu-id="5318b-170">El descriptor *s* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="5318b-170">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="5318b-171">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="5318b-171">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="5318b-172">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="5318b-172">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="5318b-173">Se devuelve este error si el proveedor de transporte no admite el **\_ cambio de \_ trabajo pendiente de envío de \_ \_ intercambio ideal** .</span><span class="sxs-lookup"><span data-stu-id="5318b-173">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="5318b-174">Este error también se devuelve cuando un intento de usar el **\_ cambio de \_ \_ trabajo pendiente \_ de envío de la opción SiO ideal** se realiza en un socket de datagrama.</span><span class="sxs-lookup"><span data-stu-id="5318b-174">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="5318b-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5318b-175">Remarks</span></span>

<span data-ttu-id="5318b-176">El ioctl de **\_ \_ \_ \_ intercambio de trabajo pendiente de la opción SiO** es compatible con Windows Server 2008, Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5318b-176">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="5318b-177">Al enviar datos a través de una conexión TCP mediante Windows Sockets, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no confirmados todavía) en TCP para lograr el máximo rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5318b-177">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="5318b-178">El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina el tamaño de trabajo pendiente de envío (ISB) ideal.</span><span class="sxs-lookup"><span data-stu-id="5318b-178">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="5318b-179">El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y, en parte, de la cantidad de congestión de la red).</span><span class="sxs-lookup"><span data-stu-id="5318b-179">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="5318b-180">El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5318b-180">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="5318b-181">Una aplicación puede usar el ioctl de **\_ \_ \_ \_ cambio de trabajo pendiente de envío ideal de SiO** para recibir una notificación cuando el valor de ISB Cambie dinámicamente para una conexión.</span><span class="sxs-lookup"><span data-stu-id="5318b-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="5318b-182">En Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo, se admiten los ioctl de **\_ \_ \_ \_ cambio de trabajo acumulado de envío** y [**SiO \_ idóneos \_ \_ \_**](sio-ideal-send-backlog-query.md) en los sockets orientados a flujos que se encuentran en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="5318b-182">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="5318b-183">En teoría, el intervalo para el valor de ISB para una conexión TCP puede variar de 0 a un máximo de 16 megabytes.</span><span class="sxs-lookup"><span data-stu-id="5318b-183">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="5318b-184">Consulte la página de referencia de ioctl de la consulta de registro de carga de [**\_ \_ \_ trabajo \_ ideal**](sio-ideal-send-backlog-query.md) para el uso típico del mecanismo de ISB con el fin de lograr un mejor rendimiento de las conexiones de productos con retraso de ancho de banda alto.</span><span class="sxs-lookup"><span data-stu-id="5318b-184">See the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL reference page for typical usage of the ISB mechanism for achieving better throughput over high bandwidth-delay product connections.</span></span>

<span data-ttu-id="5318b-185">El **\_ \_ \_ \_ intercambio de trabajo acumulado de envío ideal de SiO** solo se permite en un socket de secuencia que está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="5318b-185">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="5318b-186">De lo contrario, se producirá un error en la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="5318b-186">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="5318b-187">El **\_ intercambio de \_ \_ trabajo pendiente \_ de envío ideal de SiO** no usa ningún búfer de entrada ni de salida, pends ni se bloquea hasta que se produce un cambio de ISB en la conexión subyacente.</span><span class="sxs-lookup"><span data-stu-id="5318b-187">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL uses no input or output buffers and pends or blocks until an ISB change occurs on the underlying connection.</span></span>
<span data-ttu-id="5318b-188">Cuando se completa este IOCTL, una aplicación Winsock puede usar la [**\_ consulta de \_ \_ trabajo pendiente \_ de envío de la opción SiO ideal**](sio-ideal-send-backlog-query.md) para recuperar el nuevo valor de ISB en la conexión.</span><span class="sxs-lookup"><span data-stu-id="5318b-188">When this IOCTL is completed, a Winsock application can use the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL to retrieve the new ISB value on the connection.</span></span>

<span data-ttu-id="5318b-189">El **\_ intercambio de \_ \_ trabajo pendiente \_ de envío ideal de SiO** no admite el modo de no bloqueo.</span><span class="sxs-lookup"><span data-stu-id="5318b-189">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL does not support non-blocking mode.</span></span>
<span data-ttu-id="5318b-190">Una aplicación puede emitir este IOCTL en un socket que no sea de bloqueo, pero el IOCTL simplemente se bloqueará o permanecerá hasta que cambie el valor de ISB.</span><span class="sxs-lookup"><span data-stu-id="5318b-190">An application is allowed to issue this IOCTL on a non-blocking socket, but the IOCTL will simply block or pend until the ISB value changes.</span></span>

<span data-ttu-id="5318b-191">Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son NULL, el socket de esta función se tratará como un socket no superpuesto.</span><span class="sxs-lookup"><span data-stu-id="5318b-191">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="5318b-192">En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine* , salvo que la función puede bloquearse si socket *s* está en modo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="5318b-192">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="5318b-193">Si socket *s* está en modo de no bloqueo, esta función seguirá bloqueando, ya que este ioctl determinado no admite el modo de no bloqueo.</span><span class="sxs-lookup"><span data-stu-id="5318b-193">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="5318b-194">En el caso de los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="5318b-194">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="5318b-195">Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="5318b-195">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="5318b-196">Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.</span><span class="sxs-lookup"><span data-stu-id="5318b-196">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="5318b-197">El **\_ intercambio de \_ \_ trabajo pendiente \_ de envío ideal de SiO** proporciona una notificación y se espera que se bloquee o quede pendiente hasta que cambie el valor de ISB.</span><span class="sxs-lookup"><span data-stu-id="5318b-197">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL provides a notification and is expected to block or pend until the ISB value changes.</span></span>
<span data-ttu-id="5318b-198">Por lo tanto, normalmente se llamaría de forma asincrónica con el parámetro *lpOverlapped* establecido en una estructura WSAOVERLAPPED válida.</span><span class="sxs-lookup"><span data-stu-id="5318b-198">So it would commonly be called asynchronously with the *lpOverlapped* parameter set to a valid WSAOVERLAPPED structure.</span></span>

<span data-ttu-id="5318b-199">Se puede producir un **error en la** **\_ operación \_** de **\_ \_ \_ \_ intercambio de trabajo pendiente de envío de la opción SiO** en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5318b-199">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="5318b-200">La conexión TCP está correctamente desconectada en la dirección de envío.</span><span class="sxs-lookup"><span data-stu-id="5318b-200">The TCP connection is gracefully disconnected in the send direction.</span></span> <span data-ttu-id="5318b-201">Esto puede ocurrir como resultado de una llamada a la función Shutdown con el parámetro how establecido en **SD \_ send**, una llamada a la función **DisconnectEx** o una llamada a la función **TransmitFile** o **TransmitPackets** con el parámetro *dwFlags* establecido en **TF \_ Disconnect** o **TF \_ reuse**.</span><span class="sxs-lookup"><span data-stu-id="5318b-201">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
* <span data-ttu-id="5318b-202">La conexión TCP se ha restablecido o anulado.</span><span class="sxs-lookup"><span data-stu-id="5318b-202">The TCP connection has been reset or aborted.</span></span>
* <span data-ttu-id="5318b-203">La aplicación emite un **\_ intercambio de \_ \_ trabajo pendiente \_ de envío de SiO ideal** cuando ya hay una solicitud de notificación pendiente.</span><span class="sxs-lookup"><span data-stu-id="5318b-203">The application issues a **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL when there is already a pended notification request.</span></span> <span data-ttu-id="5318b-204">Solo se permite la solicitud de **\_ \_ \_ \_ cambio de trabajo pendiente de envío** en una sola vez 1 1 a la vez.</span><span class="sxs-lookup"><span data-stu-id="5318b-204">Only one one pended **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** request is allowed at a time.</span></span>
* <span data-ttu-id="5318b-205">El administrador de e/s cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5318b-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="5318b-206">El socket está cerrado.</span><span class="sxs-lookup"><span data-stu-id="5318b-206">The socket is closed.</span></span>

<span data-ttu-id="5318b-207">Dos funciones de contenedor en línea para estos ioctl se definen en el archivo de encabezado *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="5318b-207">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="5318b-208">Se recomienda usar estas funciones insertadas en lugar de usar el **\_ \_ \_ \_ cambio de trabajo pendiente de envío** y [**SiO ideales para la \_ \_ \_ \_ consulta de trabajo pendiente de envío ideal**](sio-ideal-send-backlog-query.md) directamente.</span><span class="sxs-lookup"><span data-stu-id="5318b-208">It is recommended that these inline functions be used instead of using the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs directly.</span></span>

<span data-ttu-id="5318b-209">La función de contenedor en línea para **el \_ \_ cambio de \_ trabajo \_ pendiente de envío de SiO ideal** es la función **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="5318b-209">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="5318b-210">La función de contenedor en línea para [**la \_ opción \_ de \_ \_ búsqueda de trabajo pendiente de envío ideal de SiO**](sio-ideal-send-backlog-query.md) es la función **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="5318b-210">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL is the **idealsendbacklogquery** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="5318b-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="5318b-211">See also</span></span>

[<span data-ttu-id="5318b-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span><span class="sxs-lookup"><span data-stu-id="5318b-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span></span>](sio-ideal-send-backlog-query.md)

[<span data-ttu-id="5318b-213">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="5318b-213">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="5318b-214">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="5318b-214">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="5318b-215">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="5318b-215">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="5318b-216">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="5318b-216">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="5318b-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="5318b-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="5318b-218">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="5318b-218">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="5318b-219">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="5318b-219">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
