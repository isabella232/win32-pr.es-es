---
description: El código de control permite a un socket recibir todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: Código de control de SIO_RCVALL
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720363"
---
# <a name="sio_rcvall-control-code"></a><span data-ttu-id="cd1a4-103">Código de control de SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="cd1a4-103">SIO_RCVALL Control Code</span></span>

## <a name="description"></a><span data-ttu-id="cd1a4-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd1a4-104">Description</span></span>
<span data-ttu-id="cd1a4-105">El código de control **SiO \_ RCVALL** permite a un socket recibir todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-105">The **SIO\_RCVALL** control code enables a socket to receive all IPv4 or IPv6 packets passing through a network interface.</span></span>

<span data-ttu-id="cd1a4-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="cd1a4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd1a4-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="cd1a4-108">s</span><span class="sxs-lookup"><span data-stu-id="cd1a4-108">s</span></span>

<span data-ttu-id="cd1a4-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="cd1a4-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="cd1a4-110">dwIoControlCode</span></span>

<span data-ttu-id="cd1a4-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-111">The control code for the operation.</span></span>
<span data-ttu-id="cd1a4-112">Use **SiO \_ RCVALL** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-112">Use **SIO\_RCVALL** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="cd1a4-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="cd1a4-113">lpvInBuffer</span></span>

<span data-ttu-id="cd1a4-114">Puntero al búfer de entrada que debe contener el valor de la opción.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-114">A pointer to the input buffer that should contain the option value.</span></span>
<span data-ttu-id="cd1a4-115">Los valores posibles para la opción de ioctl **SiO \_ RCVALL** se especifican en la enumeración **RCVALL_VALUE** definida en el archivo de encabezado *Mstcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-115">The possible values for the **SIO\_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the *Mstcpip.h* header file.</span></span>

<span data-ttu-id="cd1a4-116">Los valores posibles para **SiO \_ RCVALL** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd1a4-116">The possible values for **SIO\_RCVALL** are as follows:</span></span>

| <span data-ttu-id="cd1a4-117">Value</span><span class="sxs-lookup"><span data-stu-id="cd1a4-117">Value</span></span> | <span data-ttu-id="cd1a4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cd1a4-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="cd1a4-119">**RCVALL \_ desactivado**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-119">**RCVALL\_OFF**</span></span> | <span data-ttu-id="cd1a4-120">Deshabilite esta opción para que un socket no reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-120">Disable this option so a socket does not receive all IPv4 or IPv6 packets passing through a network interface.</span></span> |
| <span data-ttu-id="cd1a4-121">**RCVALL \_**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-121">**RCVALL\_ON**</span></span> | <span data-ttu-id="cd1a4-122">Habilite esta opción para que un socket reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-122">Enable this option so a socket receives all IPv4 or IPv6 packets passing through a network interface.</span></span> <span data-ttu-id="cd1a4-123">Esta opción habilita el modo promiscuo en la tarjeta de interfaz de red (NIC), si la NIC es compatible con el modo promiscuo.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-123">This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode.</span></span> <span data-ttu-id="cd1a4-124">En un segmento LAN con un concentrador de red, una NIC que admita el modo promiscuo capturará todo el tráfico de IPv4 o IPv6 en la LAN, incluido el tráfico entre otros equipos del mismo segmento de LAN.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-124">On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment.</span></span> <span data-ttu-id="cd1a4-125">Todos los paquetes capturados (IPv4 o IPv6, según el socket) se entregarán al socket sin formato.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-125">All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket.</span></span> <span data-ttu-id="cd1a4-126">Esta opción no capturará otros paquetes (por ejemplo, paquetes ARP, IPX y NetBEUI) en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-126">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span> <span data-ttu-id="cd1a4-127">Netmon usa el mismo modo para la interfaz de red, pero no usa esta opción para capturar el tráfico.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-127">Netmon uses the same mode for the network interface, but does not use this option to capture traffic.</span></span> |
| <span data-ttu-id="cd1a4-128">**RCVALL \_ SOCKETLEVELONLY**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-128">**RCVALL\_SOCKETLEVELONLY**</span></span> | <span data-ttu-id="cd1a4-129">Esta característica no está implementada actualmente, por lo que establecer esta opción no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-129">This feature is not currently implemented, so setting this option does not have any affect.</span></span> |
| <span data-ttu-id="cd1a4-130">**RCVALL \_ IPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-130">**RCVALL\_IPLEVEL**</span></span> | <span data-ttu-id="cd1a4-131">Habilite esta opción para que un socket IPv4 o IPv6 reciba todos los paquetes en el nivel de IP que pasan a través de una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-131">Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level passing through a network interface.</span></span> <span data-ttu-id="cd1a4-132">Esta opción no habilita el modo promiscuo en la tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-132">This option does not enable promiscuous mode on the network interface card.</span></span> <span data-ttu-id="cd1a4-133">Esta opción solo afecta al procesamiento de paquetes en el nivel de IP.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-133">This option only affects packet processing at the IP level.</span></span> <span data-ttu-id="cd1a4-134">La NIC sigue recibiendo solo los paquetes dirigidos a sus direcciones de unidifusión y multidifusión configuradas.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-134">The NIC still receives only packets directed to its configured unicast and multicast addresses.</span></span> <span data-ttu-id="cd1a4-135">Sin embargo, un socket con esta opción habilitada no solo recibirá paquetes dirigidos a direcciones IP específicas, sino que recibirá todos los paquetes IPv4 o IPv6 que reciba la NIC.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-135">However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.</span></span> <span data-ttu-id="cd1a4-136">Esta opción no capturará otros paquetes (por ejemplo, los paquetes ARP, IPX y NetBEUI) recibidos en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-136">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.</span></span> |

### <a name="cbinbuffer"></a><span data-ttu-id="cd1a4-137">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="cd1a4-137">cbInBuffer</span></span>

<span data-ttu-id="cd1a4-138">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-138">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="cd1a4-139">Este parámetro debe ser igual o mayor que el tamaño del valor de enumeración **RCVALL_VALUE** al que apunta el parámetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-139">This parameter should be equal to or greater than the size of the **RCVALL_VALUE** enumeration value pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="cd1a4-140">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="cd1a4-140">lpvOutBuffer</span></span>

<span data-ttu-id="cd1a4-141">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-141">A pointer to the output buffer.</span></span>
<span data-ttu-id="cd1a4-142">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-142">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="cd1a4-143">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="cd1a4-143">cbOutBuffer</span></span>

<span data-ttu-id="cd1a4-144">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-144">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="cd1a4-145">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-145">This parameter is unused for this operation.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="cd1a4-146">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="cd1a4-146">lpcbBytesReturned</span></span>

<span data-ttu-id="cd1a4-147">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-147">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="cd1a4-148">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-148">This parameter is unused for this operation.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="cd1a4-149">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="cd1a4-149">lpvOverlapped</span></span>

<span data-ttu-id="cd1a4-150">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-150">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="cd1a4-151">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-151">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="cd1a4-152">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="cd1a4-152">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="cd1a4-153">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-153">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="cd1a4-154">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-154">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="cd1a4-155">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-155">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="cd1a4-156">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="cd1a4-156">lpCompletionRoutine</span></span>

<span data-ttu-id="cd1a4-157">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="cd1a4-157">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="cd1a4-158">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="cd1a4-158">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="cd1a4-159">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="cd1a4-159">lpThreadId</span></span>

<span data-ttu-id="cd1a4-160">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="cd1a4-160">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="cd1a4-161">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-161">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="cd1a4-162">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-162">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="cd1a4-163">lpErrno</span><span class="sxs-lookup"><span data-stu-id="cd1a4-163">lpErrno</span></span>

<span data-ttu-id="cd1a4-164">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-164">A pointer to the error code.</span></span>

<span data-ttu-id="cd1a4-165">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-165">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd1a4-166">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd1a4-166">Return value</span></span>

<span data-ttu-id="cd1a4-167">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-167">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="cd1a4-168">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-168">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="cd1a4-169">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="cd1a4-169">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="cd1a4-170">Código de error</span><span class="sxs-lookup"><span data-stu-id="cd1a4-170">Error code</span></span> | <span data-ttu-id="cd1a4-171">Significado</span><span class="sxs-lookup"><span data-stu-id="cd1a4-171">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="cd1a4-172">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-172">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="cd1a4-173">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-173">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="cd1a4-174">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-174">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="cd1a4-175">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-175">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="cd1a4-176">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-176">**WSAEFAULT**</span></span> | <span data-ttu-id="cd1a4-177">El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-177">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="cd1a4-178">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-178">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="cd1a4-179">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-179">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="cd1a4-180">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-180">**WSAEINTR**</span></span> | <span data-ttu-id="cd1a4-181">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-181">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="cd1a4-182">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-182">**WSAEINVAL**</span></span> | <span data-ttu-id="cd1a4-183">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-183">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="cd1a4-184">Este error también se devuelve si el parámetro *cbInBuffer* es menor que `sizeof(UCHAR)` o el parámetro *lpvInBuffer* apunta a un valor que no es un valor de enumeración de **RCVALL_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-184">This error is also returned if the *cbInBuffer* parameter is less than the `sizeof(UCHAR)` or the *lpvInBuffer* parameter points to value that is not a **RCVALL_VALUE** enumeration value.</span></span> <span data-ttu-id="cd1a4-185">Este error también se puede devolver si no se encuentra la interfaz de red asociada al socket.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-185">This error can also be returned if the network interface associated with the socket cannot be found.</span></span> <span data-ttu-id="cd1a4-186">Esto puede ocurrir si se elimina o se quita la interfaz de red asociada con el socket (por ejemplo, se quita un dispositivo de red PCMCIA o USB).</span><span class="sxs-lookup"><span data-stu-id="cd1a4-186">This could occur if the network interface associated with the socket is deleted or removed (a remove PCMCIA or USB network device, for example).</span></span> |
| <span data-ttu-id="cd1a4-187">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-187">**WSAENETDOWN**</span></span> | <span data-ttu-id="cd1a4-188">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-188">The network subsystem has failed.</span></span> |
| <span data-ttu-id="cd1a4-189">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-189">**WSAENOBUFS**</span></span> | <span data-ttu-id="cd1a4-190">No hay espacio de búfer disponible.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-190">No buffer space available.</span></span> |
| <span data-ttu-id="cd1a4-191">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-191">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="cd1a4-192">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-192">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="cd1a4-193">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-193">**WSAENOTSOCK**</span></span> | <span data-ttu-id="cd1a4-194">El descriptor *s* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-194">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="cd1a4-195">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-195">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="cd1a4-196">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-196">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="cd1a4-197">Se devuelve este error si el proveedor de transporte no admite el ioctl **SiO \_ RCVALL** .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-197">This error is returned if the **SIO\_RCVALL** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="cd1a4-198">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd1a4-198">Remarks</span></span>

<span data-ttu-id="cd1a4-199">El **ioctl \_ RCVALL de SiO** es compatible con Windows 2000 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-199">The **SIO\_RCVALL** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="cd1a4-200">El ioctl **SiO \_ RCVALL** permite a un socket recibir todos los paquetes IPv4 o IPv6 en una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-200">The **SIO\_RCVALL** IOCTL enables a socket to receive all IPv4 or IPv6 packets on a network interface.</span></span>
<span data-ttu-id="cd1a4-201">El identificador de socket que se pasa a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd1a4-201">The socket handle passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function must be one of the following:</span></span>

* <span data-ttu-id="cd1a4-202">Un socket IPv4 creado con la familia de direcciones establecida en AF_INET, el tipo de socket establecido en SOCK_RAW y el protocolo establecido en IPPROTO_IP.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-202">An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.</span></span>
* <span data-ttu-id="cd1a4-203">Un socket IPv6 que se creó con la familia de direcciones establecida en AF_INET6, el tipo de socket establecido en SOCK_RAW y el protocolo establecido en IPPROTO_IPV6.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-203">An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.</span></span>

<span data-ttu-id="cd1a4-204">Para obtener más información sobre los sockets sin formato, consulte [**Sockets sin formato de TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span><span class="sxs-lookup"><span data-stu-id="cd1a4-204">For more information on raw sockets, see [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span></span>

<span data-ttu-id="cd1a4-205">El socket también debe estar enlazado a una interfaz IPv4 o IPv6 local explícita, lo que significa que no se puede enlazar a **inaddress \_ any** o **in6addr \_ any**.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-205">The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR\_ANY** or **in6addr\_any**.</span></span>

<span data-ttu-id="cd1a4-206">Una vez que se enlaza el socket y el IOCTL se completa correctamente, las llamadas a las funciones [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) o [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven datagramas IPv4 que pasan a través de la interfaz IPv4 dada o devuelven datagramas IPv6 que pasan a través de la interfaz IPv6 dada.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-206">Once the socket is bound and the IOCTL completes successfully, calls to the [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) or [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions return IPv4 datagrams passing through the given IPv4 interface or return IPv6 datagrams passing through the given IPv6 interface.</span></span>
<span data-ttu-id="cd1a4-207">Tenga en cuenta que debe proporcionar un búfer suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-207">Note that you must supply a sufficiently large buffer.</span></span>
<span data-ttu-id="cd1a4-208">Al establecer este IOCTL solo se capturarán los paquetes IPv4 o IPv6 en una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-208">Setting this IOCTL will only capture IPv4 or IPv6 packets on a given interface.</span></span>
<span data-ttu-id="cd1a4-209">Este IOCTL no capturará otros paquetes (por ejemplo, paquetes ARP, IPX y NetBEUI) en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-209">This IOCTL will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span>

<span data-ttu-id="cd1a4-210">Un socket enlazado a una interfaz local específica con el ioctl **SiO \_ RCVALL** solo recibirá los paquetes que pasan a través de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-210">A socket bound to a specific local interface with the **SIO\_RCVALL** IOCTL will receive only packets passing through that interface.</span></span>
<span data-ttu-id="cd1a4-211">No recibirá los paquetes recibidos en otra interfaz y se reenviarán en otra interfaz diferente a la del socket enlazado con **SiO \_ RCVALL** ioctl.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-211">It will not receive packets received on another interface and getting forwarded out on another interface different from the socket bound with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="cd1a4-212">En Windows Server 2008 y versiones anteriores, el valor de ioctl de **SiO \_ RCVALL** no capturar los paquetes locales enviados fuera de una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-212">On Windows Server 2008 and earlier, the **SIO\_RCVALL** IOCTL setting would not capture local packets sent out of a network interface.</span></span>
<span data-ttu-id="cd1a4-213">Esto incluye los paquetes recibidos en otra interfaz y reenviados fuera de la interfaz de red especificada para el ioctl **SiO \_ RCVALL** .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-213">This included packets received on another interface and forwarded out the network interface specified for the **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="cd1a4-214">En Windows 7 y Windows Server 2008 R2, se ha cambiado para que los paquetes locales enviados fuera de una interfaz de red también se capturen.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-214">On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured.</span></span>
<span data-ttu-id="cd1a4-215">Esto incluye los paquetes recibidos en otra interfaz y, a continuación, reenviar la interfaz de red enlazada al socket con el ioctl **SiO \_ RCVALL** .</span><span class="sxs-lookup"><span data-stu-id="cd1a4-215">This includes packets received on another interface and then forwarded out the network interface bound to the socket with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="cd1a4-216">La configuración de este IOCTL requiere privilegios de administrador en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-216">Setting this IOCTL requires Administrator privilege on the local computer.</span></span>

<span data-ttu-id="cd1a4-217">Esta característica se denomina a veces modo promiscuo.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-217">This feature is sometimes referred to as promiscuous mode.</span></span>
<span data-ttu-id="cd1a4-218">No se admite cualquier cambio directo de aplicar esta opción en una interfaz y, a continuación, a otra interfaz con una única llamada mediante este IOCTL.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-218">Any direct change from applying this option on one interface and then to another interface with a single call using this IOCTL is not supported.</span></span>
<span data-ttu-id="cd1a4-219">Una aplicación debe usar primero este IOCTL para desactivar el comportamiento en la primera interfaz y, a continuación, utilizar este IOCTL para habilitar el comportamiento en una nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="cd1a4-219">An application must first use this IOCTL to turn off the behavior on the first interface, and then use this IOCTL to enable the behavior on a new interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd1a4-220">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd1a4-220">See also</span></span>

[<span data-ttu-id="cd1a4-221">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="cd1a4-222">**Sockets sin formato de TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-222">**TCP/IP Raw Sockets**</span></span>](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[<span data-ttu-id="cd1a4-223">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-223">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="cd1a4-224">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-224">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="cd1a4-225">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-225">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="cd1a4-226">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-226">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="cd1a4-227">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-227">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="cd1a4-228">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="cd1a4-228">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
