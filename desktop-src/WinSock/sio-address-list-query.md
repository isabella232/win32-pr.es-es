---
description: El código de control obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Código de control de SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720651"
---
# <a name="sio_address_list_query-control-code"></a><span data-ttu-id="8dea1-103">Código de control de SIO_ADDRESS_LIST_QUERY</span><span class="sxs-lookup"><span data-stu-id="8dea1-103">SIO_ADDRESS_LIST_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="8dea1-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dea1-104">Description</span></span>

<span data-ttu-id="8dea1-105">El código de control de consulta de la lista de direcciones de SiO obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dea1-105">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="8dea1-106">La lista de direcciones varía en función de la familia de direcciones y algunas direcciones se excluyen de la lista.</span><span class="sxs-lookup"><span data-stu-id="8dea1-106">The list of addresses varies based on address family and some addresses are excluded from the list.</span></span>

<span data-ttu-id="8dea1-107">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="8dea1-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="8dea1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8dea1-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="8dea1-109">s</span><span class="sxs-lookup"><span data-stu-id="8dea1-109">s</span></span>

<span data-ttu-id="8dea1-110">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="8dea1-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="8dea1-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="8dea1-111">dwIoControlCode</span></span>

<span data-ttu-id="8dea1-112">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="8dea1-112">The control code for the operation.</span></span>
<span data-ttu-id="8dea1-113">Use **la \_ \_ \_ consulta** de la lista de direcciones de SiO para esta operación.</span><span class="sxs-lookup"><span data-stu-id="8dea1-113">Use **SIO\_ADDRESS\_LIST\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="8dea1-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="8dea1-114">lpvInBuffer</span></span>

<span data-ttu-id="8dea1-115">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="8dea1-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="8dea1-116">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="8dea1-116">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="8dea1-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="8dea1-117">cbInBuffer</span></span>

<span data-ttu-id="8dea1-118">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="8dea1-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="8dea1-119">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="8dea1-119">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="8dea1-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="8dea1-120">lpvOutBuffer</span></span>

<span data-ttu-id="8dea1-121">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8dea1-121">A pointer to the output buffer.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="8dea1-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="8dea1-122">cbOutBuffer</span></span>

<span data-ttu-id="8dea1-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8dea1-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="8dea1-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="8dea1-124">lpcbBytesReturned</span></span>

<span data-ttu-id="8dea1-125">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8dea1-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="8dea1-126">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="8dea1-126">lpvOverlapped</span></span>

<span data-ttu-id="8dea1-127">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="8dea1-127">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8dea1-128">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="8dea1-128">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="8dea1-129">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="8dea1-129">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="8dea1-130">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="8dea1-130">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8dea1-131">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="8dea1-131">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="8dea1-132">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="8dea1-132">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="8dea1-133">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="8dea1-133">lpCompletionRoutine</span></span>

<span data-ttu-id="8dea1-134">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="8dea1-134">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="8dea1-135">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="8dea1-135">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="8dea1-136">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="8dea1-136">lpThreadId</span></span>

<span data-ttu-id="8dea1-137">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="8dea1-137">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="8dea1-138">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="8dea1-138">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="8dea1-139">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="8dea1-139">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="8dea1-140">lpErrno</span><span class="sxs-lookup"><span data-stu-id="8dea1-140">lpErrno</span></span>

<span data-ttu-id="8dea1-141">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="8dea1-141">A pointer to the error code.</span></span>

<span data-ttu-id="8dea1-142">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="8dea1-142">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="8dea1-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8dea1-143">Return value</span></span>

<span data-ttu-id="8dea1-144">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="8dea1-144">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="8dea1-145">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="8dea1-145">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="8dea1-146">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="8dea1-146">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="8dea1-147">Código de error</span><span class="sxs-lookup"><span data-stu-id="8dea1-147">Error code</span></span> | <span data-ttu-id="8dea1-148">Significado</span><span class="sxs-lookup"><span data-stu-id="8dea1-148">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="8dea1-149">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="8dea1-149">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="8dea1-150">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="8dea1-150">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="8dea1-151">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="8dea1-151">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="8dea1-152">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SiO \_ Flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="8dea1-152">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="8dea1-153">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8dea1-153">**WSAEFAULT**</span></span> | <span data-ttu-id="8dea1-154">El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="8dea1-154">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="8dea1-155">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="8dea1-155">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="8dea1-156">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="8dea1-156">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="8dea1-157">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="8dea1-157">**WSAEINTR**</span></span> | <span data-ttu-id="8dea1-158">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="8dea1-158">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="8dea1-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="8dea1-159">**WSAEINVAL**</span></span> | <span data-ttu-id="8dea1-160">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="8dea1-160">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="8dea1-161">Se devuelve este error si el parámetro *cbInBuffer* no se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="8dea1-161">This error is returned if the *cbInBuffer* parameter is not set to **NULL**.</span></span> |
| <span data-ttu-id="8dea1-162">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="8dea1-162">**WSAENETDOWN**</span></span> | <span data-ttu-id="8dea1-163">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="8dea1-163">The network subsystem has failed.</span></span> |
| <span data-ttu-id="8dea1-164">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="8dea1-164">**WSAENOBUFS**</span></span> | <span data-ttu-id="8dea1-165">No hay espacio de búfer disponible.</span><span class="sxs-lookup"><span data-stu-id="8dea1-165">No buffer space available.</span></span> |
| <span data-ttu-id="8dea1-166">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="8dea1-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="8dea1-167">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="8dea1-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="8dea1-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="8dea1-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="8dea1-169">El descriptor *s* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="8dea1-169">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="8dea1-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="8dea1-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="8dea1-171">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="8dea1-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="8dea1-172">Se devuelve este error si el proveedor de transporte no admite el ioctl de consulta de la **\_ lista de direcciones de \_ \_ SiO** .</span><span class="sxs-lookup"><span data-stu-id="8dea1-172">This error is returned if the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="8dea1-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8dea1-173">Remarks</span></span>

<span data-ttu-id="8dea1-174">El ioctl de consulta de la lista de direcciones de SiO es compatible con Windows 2000 y versiones posteriores del sistema operativo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dea1-174">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="8dea1-175">El código de control de consulta de la lista de direcciones de SiO obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dea1-175">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="8dea1-176">La lista de direcciones varía en función de la familia de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8dea1-176">The list of addresses varies based on address family.</span></span>

<span data-ttu-id="8dea1-177">En el caso de la \_ familia de direcciones AF inet6, se devuelven todas las direcciones excepto las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8dea1-177">For the AF\_INET6 address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="8dea1-178">Cualquier dirección IP en la que el estado de detección de direcciones duplicadas (DAD) no es IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="8dea1-178">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="8dea1-179">Cualquier dirección IP con un nivel de ámbito inferior a ScopeLevelSubnet en una interfaz en la que el tipo de interfaz es **si el \_ tipo es \_ \_ bucle invertido**.</span><span class="sxs-lookup"><span data-stu-id="8dea1-179">Any IP address with a scope level lower than ScopeLevelSubnet on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK**.</span></span>
<span data-ttu-id="8dea1-180">Esto significa que las direcciones locales de vínculo (fe80: \*) y de bucle invertido (:: 1) en las interfaces de si se excluye el tipo de **\_ \_ \_ bucle invertido de software** , pero no si estas direcciones se encuentran en una interfaz con un tipo diferente.</span><span class="sxs-lookup"><span data-stu-id="8dea1-180">This means link-local (fe80:\*) and loopback (::1) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="8dea1-181">En el caso de la familia de direcciones de **AF \_ inet** , se devuelven todas las direcciones excepto las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8dea1-181">For the **AF\_INET** address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="8dea1-182">Cualquier dirección IP en la que el estado de detección de direcciones duplicadas (DAD) no es IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="8dea1-182">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="8dea1-183">Cualquier dirección IP de una interfaz en la que el tipo de interfaz sea **si el \_ tipo de \_ \_ bucle invertido** y el vínculo es local.</span><span class="sxs-lookup"><span data-stu-id="8dea1-183">Any IP address on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK** and link is local.</span></span>
<span data-ttu-id="8dea1-184">Esto significa que las direcciones locales de vínculo (169,254 *) y bucle invertido (127.*) en las interfaces de si se excluye el tipo de **\_ \_ \_ bucle invertido de software** , pero no si estas direcciones se encuentran en una interfaz con un tipo diferente.</span><span class="sxs-lookup"><span data-stu-id="8dea1-184">This means link-local (169.254.*) and loopback (127.*) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="8dea1-185">Para obtener más información sobre el estado del padre, consulte la documentación de la aplicación auxiliar de IP en la estructura de [**\_ \_ Estado**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) de los direcciones IP de los adaptadores de IP y la [**\_ \_ \_ dirección de unidifusión**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) y la documentación de MIB en la estructura de [**\_ \_ filas MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .</span><span class="sxs-lookup"><span data-stu-id="8dea1-185">For more information on DAD state, see the IP Helper documentation on the [**IP\_DAD\_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) enumeration and [**IP\_ADAPTER\_UNICAST\_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) structure and the MIB documentation on the [**MIB\_UNICASTIPADDRESS\_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) structure.</span></span>
<span data-ttu-id="8dea1-186">Para obtener más información sobre el tipo de interfaz, consulte la documentación de la aplicación auxiliar de IP en la estructura de [**direcciones del \_ adaptador \_ de IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) y la función [**GETADAPTERSADDRESSES**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) y la documentación de MIB en [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) estructura.</span><span class="sxs-lookup"><span data-stu-id="8dea1-186">For more information on interface type, see the IP Helper documentation on the [**IP\_ADAPTER\_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the MIB documentation on [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span></span>
<span data-ttu-id="8dea1-187">Para obtener más información sobre el nivel de ámbito, consulte la documentación de la aplicación auxiliar de IP en la estructura de [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) y la enumeración de [**\_ nivel de ámbito**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .</span><span class="sxs-lookup"><span data-stu-id="8dea1-187">For more information on the scope level, see the IP Helper documentation on the [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**SCOPE\_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) enumeration.</span></span>

<span data-ttu-id="8dea1-188">La lista devuelta en el búfer de salida al que apunta el parámetro *lpvOutBuffer* tiene el formato de una estructura de [**lista de \_ direcciones \_ de socket**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .</span><span class="sxs-lookup"><span data-stu-id="8dea1-188">The list returned in the output buffer pointed to by the *lpvOutBuffer* parameter is in the form of a [**SOCKET\_ADDRESS\_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) structure.</span></span>

<span data-ttu-id="8dea1-189">Si el búfer de salida especificado en el parámetro *lpvOutBuffer* no es lo suficientemente grande como para contener la lista de direcciones, el **\_ error de socket** se devuelve como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="8dea1-189">If the output buffer specified in the *lpvOutBuffer* parameter is not large enough to contain the address list, **SOCKET\_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [WSAEFAULT](windows-sockets-error-codes-2.md).</span></span>
<span data-ttu-id="8dea1-190">En este caso, se devuelve el tamaño necesario, en bytes, para el búfer de salida en el parámetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="8dea1-190">The required size, in bytes, for the output buffer is returned in the *lpcbBytesReturned* parameter in this case.</span></span>
<span data-ttu-id="8dea1-191">Nota: el código de error [WSAEFAULT](windows-sockets-error-codes-2.md) también se devuelve si el parámetro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* no está completamente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="8dea1-191">Note the [WSAEFAULT](windows-sockets-error-codes-2.md) error code is also returned if the *lpvInBuffer*, *lpvOutBuffer*, or *lpcbBytesReturned* parameter is not completely contained in a valid part of the user address space.</span></span>

<span data-ttu-id="8dea1-192">Normalmente, la consulta de la lista de direcciones de SiO ioctl se llama sincrónicamente con el parámetro *lpvOverlapped* establecido en **null**, ya que la lista de direcciones se devuelve inmediatamente. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dea1-192">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is normally called synchronously with the *lpvOverlapped* parameter set to **NULL**, since the list of addresses is returned immediately.</span></span>

<span data-ttu-id="8dea1-193">**Nota:**  En los entornos de plug-n-Play de Windows, las direcciones se pueden agregar y quitar de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="8dea1-193">**Note**  In Windows Plug-n-Play environments, addresses can be added and removed dynamically.</span></span>
<span data-ttu-id="8dea1-194">Por lo tanto, las aplicaciones no pueden basarse en la información devuelta por la consulta de lista de direcciones de SiO para ser persistentes. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dea1-194">Therefore, applications cannot rely on the information returned by **SIO\_ADDRESS\_LIST\_QUERY** to be persistent.</span></span>
<span data-ttu-id="8dea1-195">Las aplicaciones pueden registrarse para recibir notificaciones de cambio de dirección a través del cambio de la lista de direcciones de SiO que proporciona la notificación a través de un evento de **cambio de \_ \_ lista \_ de direcciones** de e/s o FD superpuesto. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dea1-195">Applications may register for address change notifications through the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL which provides for notification through either overlapped I/O or **FD\_ADDRESS\_LIST\_CHANGE** event.</span></span>
<span data-ttu-id="8dea1-196">Se puede usar la siguiente secuencia de acciones para garantizar que la aplicación tenga siempre información de lista de direcciones actual:</span><span class="sxs-lookup"><span data-stu-id="8dea1-196">The following sequence of actions can be used to guarantee that the application always has current address list information:</span></span>

* <span data-ttu-id="8dea1-197">Emitir el **cambio de la lista de direcciones de SiO \_ \_ \_** ioctl</span><span class="sxs-lookup"><span data-stu-id="8dea1-197">Issue the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL</span></span>
* <span data-ttu-id="8dea1-198">Emitir la **consulta de la lista de direcciones de SiO \_ \_ \_** ioctl</span><span class="sxs-lookup"><span data-stu-id="8dea1-198">Issue the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL</span></span>
* <span data-ttu-id="8dea1-199">Siempre que el cambio de la **lista de direcciones de SiO \_ \_ \_ cambie** la llamada de ioctl notifica a la aplicación de un cambio en la lista de direcciones (ya sea a través de e/s superpuesta o por evento de cambio de **\_ \_ lista \_ de direcciones FD** ), se debe repetir la secuencia de acciones completa.</span><span class="sxs-lookup"><span data-stu-id="8dea1-199">Whenever the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL call notifies the application of an address list change (either through overlapped I/O or by signaling **FD\_ADDRESS\_LIST\_CHANGE** event), the whole sequence of actions should be repeated.</span></span>

<span data-ttu-id="8dea1-200">En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el código de control de consulta de la lista de direcciones de SiO se define en el archivo de encabezado *Ws2def. h* . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dea1-200">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the **SIO\_ADDRESS\_LIST\_QUERY** control code is defined in the *Ws2def.h* header file.</span></span>
<span data-ttu-id="8dea1-201">Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.</span><span class="sxs-lookup"><span data-stu-id="8dea1-201">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="8dea1-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dea1-202">See also</span></span>

[<span data-ttu-id="8dea1-203">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="8dea1-203">**GetAdaptersAddresses**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[<span data-ttu-id="8dea1-204">**IP_ADAPTER_ADDRESSES**</span><span class="sxs-lookup"><span data-stu-id="8dea1-204">**IP_ADAPTER_ADDRESSES**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[<span data-ttu-id="8dea1-205">**IP_ADAPTER_UNICAST_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="8dea1-205">**IP_ADAPTER_UNICAST_ADDRESS**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[<span data-ttu-id="8dea1-206">**IP_DAD_STATE**</span><span class="sxs-lookup"><span data-stu-id="8dea1-206">**IP_DAD_STATE**</span></span>](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[<span data-ttu-id="8dea1-207">**MIB_IF_ROW2**</span><span class="sxs-lookup"><span data-stu-id="8dea1-207">**MIB_IF_ROW2**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[<span data-ttu-id="8dea1-208">**MIB_UNICASTIPADDRESS_ROW**</span><span class="sxs-lookup"><span data-stu-id="8dea1-208">**MIB_UNICASTIPADDRESS_ROW**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[<span data-ttu-id="8dea1-209">**SCOPE_LEVEL**</span><span class="sxs-lookup"><span data-stu-id="8dea1-209">**SCOPE_LEVEL**</span></span>](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[<span data-ttu-id="8dea1-210">**SOCKET_ADDRESS_LIST**</span><span class="sxs-lookup"><span data-stu-id="8dea1-210">**SOCKET_ADDRESS_LIST**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[<span data-ttu-id="8dea1-211">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="8dea1-211">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="8dea1-212">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="8dea1-212">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="8dea1-213">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="8dea1-213">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="8dea1-214">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="8dea1-214">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="8dea1-215">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="8dea1-215">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="8dea1-216">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="8dea1-216">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="8dea1-217">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="8dea1-217">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
