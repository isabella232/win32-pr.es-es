---
description: El código de control recupera las estadísticas del Protocolo de control de transmisión (TCP) para un socket especificado.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f6076440f117ed287ad544c308e574454f33e2b7
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587793"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="dd6c1-103">SIO_TCP_INFO código de control</span><span class="sxs-lookup"><span data-stu-id="dd6c1-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="dd6c1-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd6c1-104">Description</span></span>

<span data-ttu-id="dd6c1-105">El código de control **\_ \_ SIO TCP INFO** recupera las estadísticas del Protocolo de control de transmisión (TCP) para un socket especificado.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="dd6c1-106">Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="dd6c1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd6c1-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="dd6c1-108">s</span><span class="sxs-lookup"><span data-stu-id="dd6c1-108">s</span></span>

<span data-ttu-id="dd6c1-109">Descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="dd6c1-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="dd6c1-110">dwIoControlCode</span></span>

<span data-ttu-id="dd6c1-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-111">The control code for the operation.</span></span>
<span data-ttu-id="dd6c1-112">Use **SIO \_ TCP INFO \_ para** esta operación.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="dd6c1-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="dd6c1-113">lpvInBuffer</span></span>

<span data-ttu-id="dd6c1-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="dd6c1-115">Este parámetro contiene un puntero a **un DWORD** que especifica la versión del código de control **TCP INFO \_ \_ de SIO** que está usando.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="dd6c1-116">Especifique 0 para usar [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span><span class="sxs-lookup"><span data-stu-id="dd6c1-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="dd6c1-117">Especifique 1 para usar [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), que proporciona más campos.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which provides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="dd6c1-118">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="dd6c1-118">cbInBuffer</span></span>

<span data-ttu-id="dd6c1-119">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="dd6c1-120">Este parámetro debe ser el tamaño del **tipo de datos DWORD.**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="dd6c1-121">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dd6c1-121">lpvOutBuffer</span></span>

<span data-ttu-id="dd6c1-122">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="dd6c1-123">Si la salida es correcta, este parámetro contiene un puntero a una [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) estructura que contiene las estadísticas TCP para el socket especificado.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="dd6c1-124">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dd6c1-124">cbOutBuffer</span></span>

<span data-ttu-id="dd6c1-125">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="dd6c1-126">Este parámetro debe ser al menos el tamaño de la [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) estructura.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="dd6c1-127">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="dd6c1-127">lpcbBytesReturned</span></span>

<span data-ttu-id="dd6c1-128">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="dd6c1-129">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *lpcbBytesReturned* apunta a un valor **DWORD** de cero.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="dd6c1-130">Si *lpOverlapped* es **NULL,** el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="dd6c1-131">Si el *parámetro lpOverlapped* no es **NULL** para los sockets superpuestos, se iniciarán las operaciones que no se pueden completar inmediatamente y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="dd6c1-132">El **valor DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que el tamaño de los datos almacenados no se puede determinar hasta que se complete la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="dd6c1-133">El estado de finalización final se puede recuperar cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="dd6c1-134">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="dd6c1-134">lpvOverlapped</span></span>

<span data-ttu-id="dd6c1-135">Puntero a una [**estructura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)</span><span class="sxs-lookup"><span data-stu-id="dd6c1-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dd6c1-136">Si se *crearon sockets* sin el atributo superpuesto, se omite el parámetro *lpOverlapped.*</span><span class="sxs-lookup"><span data-stu-id="dd6c1-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="dd6c1-137">Si *s* se abrió con el atributo superpuesto y el parámetro *lpOverlapped* no es **NULL,** la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="dd6c1-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="dd6c1-138">En este caso, *el parámetro lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dd6c1-139">En el caso de las operaciones superpuestas, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelve inmediatamente y se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="dd6c1-140">De lo contrario, la función no se devuelve hasta que se ha completado la operación o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="dd6c1-141">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="dd6c1-141">lpCompletionRoutine</span></span>

<span data-ttu-id="dd6c1-142">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="dd6c1-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="dd6c1-143">Puntero a la rutina de finalización a la que se llama cuando se ha completado la operación (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="dd6c1-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="dd6c1-144">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="dd6c1-144">lpThreadId</span></span>

<span data-ttu-id="dd6c1-145">Puntero a una [**estructura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que usará el proveedor en una llamada posterior a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="dd6c1-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="dd6c1-146">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)</span><span class="sxs-lookup"><span data-stu-id="dd6c1-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="dd6c1-147">**Nota**  Este parámetro solo se aplica a la **función WSPIoctl.**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="dd6c1-148">lpErrno</span><span class="sxs-lookup"><span data-stu-id="dd6c1-148">lpErrno</span></span>

<span data-ttu-id="dd6c1-149">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-149">A pointer to the error code.</span></span>

<span data-ttu-id="dd6c1-150">**Nota**  Este parámetro solo se aplica a la **función WSPIoctl.**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd6c1-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd6c1-151">Return value</span></span>

<span data-ttu-id="dd6c1-152">Si la operación se completa correctamente, la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="dd6c1-153">Si se produce un error en la operación o está pendiente, la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve **SOCKET \_ ERROR**.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="dd6c1-154">Para obtener información de error extendida, llame [**a WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="dd6c1-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="dd6c1-155">Código de error</span><span class="sxs-lookup"><span data-stu-id="dd6c1-155">Error code</span></span> | <span data-ttu-id="dd6c1-156">Significado</span><span class="sxs-lookup"><span data-stu-id="dd6c1-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="dd6c1-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="dd6c1-158">El puntero al búfer de entrada era **NULL** o el tamaño especificado del búfer de entrada no era correcto.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="dd6c1-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-159">**WSAEINVAL**</span></span> | <span data-ttu-id="dd6c1-160">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-160">An invalid argument was supplied.</span></span> <span data-ttu-id="dd6c1-161">Este error se devuelve si el parámetro *dwIoControlCode* no es un comando válido, un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="dd6c1-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd6c1-162">Remarks</span></span>

<span data-ttu-id="dd6c1-163">A diferencia de la recuperación de estadísticas TCP con la función [**GetPerTcpConnectionEStats,**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) la recuperación de estadísticas TCP con este código de control no requiere que el código de usuario cargue, almacene y filtre la tabla de conexión TCP, y no requiere privilegios elevados para su uso.</span><span class="sxs-lookup"><span data-stu-id="dd6c1-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd6c1-164">Consulta también</span><span class="sxs-lookup"><span data-stu-id="dd6c1-164">See also</span></span>

[<span data-ttu-id="dd6c1-165">Zócalo</span><span class="sxs-lookup"><span data-stu-id="dd6c1-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="dd6c1-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="dd6c1-167">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="dd6c1-168">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="dd6c1-169">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="dd6c1-170">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="dd6c1-171">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="dd6c1-172">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="dd6c1-173">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="dd6c1-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
