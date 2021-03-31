---
description: El código de control habilita o deshabilita el valor por conexión de la opción Keep-Alive de TCP, que especifica el tiempo de espera y el intervalo de mantenimiento de conexiones TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Código de control de SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155865"
---
# <a name="sio_keepalive_vals-control-code"></a><span data-ttu-id="b8ea3-103">Código de control de SIO_KEEPALIVE_VALS</span><span class="sxs-lookup"><span data-stu-id="b8ea3-103">SIO_KEEPALIVE_VALS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="b8ea3-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8ea3-104">Description</span></span>

<span data-ttu-id="b8ea3-105">El código de control **SiO \_ KEEPALIVE \_ vals** habilita o deshabilita el valor por conexión de la opción Keep-Alive de TCP, que especifica el tiempo de espera y el intervalo de mantenimiento de conexiones TCP.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-105">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval.</span></span>

<span data-ttu-id="b8ea3-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="b8ea3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8ea3-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="b8ea3-108">s</span><span class="sxs-lookup"><span data-stu-id="b8ea3-108">s</span></span>

<span data-ttu-id="b8ea3-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="b8ea3-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="b8ea3-110">dwIoControlCode</span></span>

<span data-ttu-id="b8ea3-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-111">The control code for the operation.</span></span>
<span data-ttu-id="b8ea3-112">Use **SiO \_ KEEPALIVE \_ vals** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-112">Use **SIO\_KEEPALIVE\_VALS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="b8ea3-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="b8ea3-113">lpvInBuffer</span></span>

<span data-ttu-id="b8ea3-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="b8ea3-115">Este parámetro debe apuntar a una estructura **TCP \_ KeepAlive** .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-115">This parameter should point to a **tcp\_keepalive** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="b8ea3-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="b8ea3-116">cbInBuffer</span></span>

<span data-ttu-id="b8ea3-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="b8ea3-118">Este parámetro debe ser igual o mayor que el tamaño de la estructura **TCP \_ KeepAlive** señalada por el parámetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-118">This parameter should equal to or greater than the size of the **tcp\_keepalive** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="b8ea3-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b8ea3-119">lpvOutBuffer</span></span>

<span data-ttu-id="b8ea3-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="b8ea3-121">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="b8ea3-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b8ea3-122">cbOutBuffer</span></span>

<span data-ttu-id="b8ea3-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="b8ea3-124">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="b8ea3-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="b8ea3-125">lpcbBytesReturned</span></span>

<span data-ttu-id="b8ea3-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="b8ea3-127">Este parámetro devuelve un valor **DWORD** de cero para esta operación, ya que no hay ninguna salida.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="b8ea3-128">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="b8ea3-128">lpvOverlapped</span></span>

<span data-ttu-id="b8ea3-129">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b8ea3-130">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="b8ea3-131">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="b8ea3-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="b8ea3-132">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b8ea3-133">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="b8ea3-134">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="b8ea3-135">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="b8ea3-135">lpCompletionRoutine</span></span>

<span data-ttu-id="b8ea3-136">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="b8ea3-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="b8ea3-137">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="b8ea3-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="b8ea3-138">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="b8ea3-138">lpThreadId</span></span>

<span data-ttu-id="b8ea3-139">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="b8ea3-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="b8ea3-140">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="b8ea3-141">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="b8ea3-142">lpErrno</span><span class="sxs-lookup"><span data-stu-id="b8ea3-142">lpErrno</span></span>

<span data-ttu-id="b8ea3-143">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-143">A pointer to the error code.</span></span>

<span data-ttu-id="b8ea3-144">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8ea3-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8ea3-145">Return value</span></span>

<span data-ttu-id="b8ea3-146">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="b8ea3-147">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="b8ea3-148">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b8ea3-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="b8ea3-149">Código de error</span><span class="sxs-lookup"><span data-stu-id="b8ea3-149">Error code</span></span> | <span data-ttu-id="b8ea3-150">Significado</span><span class="sxs-lookup"><span data-stu-id="b8ea3-150">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="b8ea3-151">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="b8ea3-152">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="b8ea3-153">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="b8ea3-154">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH ioctl** .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="b8ea3-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-155">**WSAEFAULT**</span></span> | <span data-ttu-id="b8ea3-156">El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="b8ea3-157">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="b8ea3-158">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="b8ea3-159">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-159">**WSAEINTR**</span></span> | <span data-ttu-id="b8ea3-160">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="b8ea3-161">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-161">**WSAEINVAL**</span></span> | <span data-ttu-id="b8ea3-162">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="b8ea3-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="b8ea3-164">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="b8ea3-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="b8ea3-166">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-166">The socket option is not supported on the specified protocol.</span></span> <span data-ttu-id="b8ea3-167">Este error se devuelve para un socket de datagrama.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-167">This error is returned for a datagram socket.</span></span> |
| <span data-ttu-id="b8ea3-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="b8ea3-169">El descriptor s no es un socket.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-169">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="b8ea3-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="b8ea3-171">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="b8ea3-172">Este error se devuelve si el proveedor de transporte no admite el ioctl **SiO \_ KEEPALIVE \_ vals** .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-172">This error is returned if the **SIO\_KEEPALIVE\_VALS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b8ea3-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8ea3-173">Remarks</span></span>

<span data-ttu-id="b8ea3-174">El ioctl de **\_ \_ vals KEEPALIVE** es compatible con Windows 2000 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-174">The **SIO\_KEEPALIVE\_VALS** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="b8ea3-175">El código de control **SiO \_ KEEPALIVE \_ vals** habilita o deshabilita el valor por conexión de la opción Keep-Alive de TCP, que especifica el tiempo de espera de mantenimiento de conexión TCP y el intervalo utilizado para los paquetes Keep-Alive de TCP.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-175">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval used for TCP keep-alive packets.</span></span>
<span data-ttu-id="b8ea3-176">Para obtener más información acerca de la opción Keep-Alive, consulte la sección 4.2.3.6 sobre los requisitos de los hosts de Internet: las capas de comunicación especificadas en RFC 1122 están disponibles en el [sitio web de IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="b8ea3-176">For more information on the keep-alive option, see section 4.2.3.6 on the Requirements for Internet Hosts—Communication Layers specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="b8ea3-177">(Este recurso solo está disponible en inglés).</span><span class="sxs-lookup"><span data-stu-id="b8ea3-177">(This resource may only be available in English.)</span></span>

<span data-ttu-id="b8ea3-178">El parámetro *lpvInBuffer* debe apuntar a una estructura **TCP \_ KeepAlive** definida en el archivo de encabezado *Mstcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-178">The *lpvInBuffer* parameter should point to a **tcp\_keepalive** structure defined in the *Mstcpip.h* header file.</span></span>
<span data-ttu-id="b8ea3-179">Esta estructura se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b8ea3-179">This structure is defined as follows:</span></span>

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

<span data-ttu-id="b8ea3-180">El valor especificado en el miembro **OnOff** determina si TCP Keep-Alive está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-180">The value specified in the **onoff** member determines if TCP keep-alive is enabled or disabled.</span></span>
<span data-ttu-id="b8ea3-181">Si el miembro **OnOff** se establece en un valor distinto de cero, se habilita TCP Keep-Alive y se usan los demás miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-181">If the **onoff** member is set to a nonzero value, TCP keep-alive is enabled and the other members in the structure are used.</span></span>
<span data-ttu-id="b8ea3-182">El miembro **KeepAliveTime** especifica el tiempo de espera, en milisegundos, sin actividad hasta que se envía el primer paquete Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-182">The **keepalivetime** member specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent.</span></span>
<span data-ttu-id="b8ea3-183">El miembro **KeepAliveInterval** especifica el intervalo, en milisegundos, entre el momento en que se envían los paquetes Keep-Alive sucesivos Si no se recibe ninguna confirmación.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-183">The **keepaliveinterval** member specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgement is received.</span></span>

<span data-ttu-id="b8ea3-184">La opción [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , que es una de las [**Opciones de socket de SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), también puede usarse para habilitar o deshabilitar TCP Keep-Alive en una conexión, así como para consultar el estado actual de esta opción.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-184">The [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option, which is one of the [**SOL_SOCKET Socket Options**](/windows/desktop/winsock/sol-socket-socket-options), can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option.</span></span>
<span data-ttu-id="b8ea3-185">Para consultar si TCP Keep-Alive está habilitado en un socket, se puede llamar a la función getsockopt con la opción [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-185">To query whether TCP keep-alive is enabled on a socket, the getsockopt function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="b8ea3-186">Para habilitar o deshabilitar TCP Keep-Alive, se puede llamar a **la función del método de llamada** con la opción [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-186">To enable or disable TCP keep-alive, the **setsockopt** function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="b8ea3-187">Si TCP Keep-Alive está habilitado con [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), se usará la configuración predeterminada de TCP para el tiempo de espera de mantenimiento de conexión y el intervalo, a menos que estos valores se hayan cambiado mediante **SiO \_ KEEPALIVE \_ vals**.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-187">If TCP keep-alive is enabled with [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="b8ea3-188">El valor predeterminado para todo el sistema del tiempo de espera de mantenimiento de conexión se controla mediante la configuración del registro [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) , que toma un valor en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-188">The default system-wide value of the keep-alive timeout is controllable through the [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="b8ea3-189">Si no se establece la clave, el tiempo de espera de mantenimiento de conexión predeterminado es de 2 horas.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-189">If the key is not set, the default keep-alive timeout is 2 hours.</span></span>
<span data-ttu-id="b8ea3-190">El valor predeterminado para todo el sistema del intervalo Keep-Alive se controla a través de la configuración del registro [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que toma un valor en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-190">The default system-wide value of the keep-alive interval is controllable through the [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="b8ea3-191">Si no se establece la clave, el intervalo de mantenimiento de conexión predeterminado es de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-191">If the key is not set, the default keep-alive interval is 1 second.</span></span>

<span data-ttu-id="b8ea3-192">En Windows Vista y versiones posteriores, el número de sondeos Keep-Alive (retransmisiones de datos) se establece en 10 y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-192">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="b8ea3-193">En Windows Server 2003, Windows XP y Windows 2000, la configuración predeterminada para el número de sondeos Keep-Alive es 5.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-193">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span>
<span data-ttu-id="b8ea3-194">El número de sondeos Keep-Alive se controla a través de la configuración del registro **TcpMaxDataRetransmissions** y [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-194">The number of keep-alive probes is controllable through the **TcpMaxDataRetransmissions** and [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span>
<span data-ttu-id="b8ea3-195">El número de sondeos Keep-Alive se establece en el mayor de los dos valores de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-195">The number of keep-alive probes is set to the larger of the two registry key values.</span></span>
<span data-ttu-id="b8ea3-196">Si este número es 0, no se enviarán sondeos Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-196">If this number is 0, then keep-alive probes will not be sent.</span></span>
<span data-ttu-id="b8ea3-197">Si este número es superior a 255, se ajusta a 255.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-197">If this number is above 255, then it is adjusted to 255.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8ea3-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8ea3-198">See also</span></span>

<span data-ttu-id="b8ea3-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b8ea3-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>

<span data-ttu-id="b8ea3-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b8ea3-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>

<span data-ttu-id="b8ea3-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b8ea3-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>

[<span data-ttu-id="b8ea3-202">tomacorriente</span><span class="sxs-lookup"><span data-stu-id="b8ea3-202">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="b8ea3-203">**SO_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-203">**SO_KEEPALIVE**</span></span>](/windows/desktop/winsock/so-keepalive)

[<span data-ttu-id="b8ea3-204">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-204">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="b8ea3-205">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-205">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="b8ea3-206">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-206">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="b8ea3-207">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-207">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="b8ea3-208">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-208">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="b8ea3-209">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="b8ea3-209">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
