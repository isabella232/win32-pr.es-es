---
description: Devuelve la dirección local, el puerto local, la dirección remota, el puerto remoto, el tipo de socket y el protocolo utilizado por un socket.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Opción de socket de SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812445"
---
# <a name="so_bsp_state-socket-option"></a><span data-ttu-id="83b29-103">\_Opción de \_ socket de estado BSP</span><span class="sxs-lookup"><span data-stu-id="83b29-103">SO\_BSP\_STATE socket option</span></span>

<span data-ttu-id="83b29-104">La opción de socket de **\_ \_ Estado de BSP** devuelve la dirección local, el puerto local, la dirección remota, el puerto remoto, el tipo de socket y el protocolo que usa un socket.</span><span class="sxs-lookup"><span data-stu-id="83b29-104">The **SO\_BSP\_STATE** socket option returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span>

<span data-ttu-id="83b29-105">Para realizar esta operación, llame a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="83b29-105">To perform this operation, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="83b29-106">Valor de opción de socket</span><span class="sxs-lookup"><span data-stu-id="83b29-106">Socket option value</span></span>

<span data-ttu-id="83b29-107">La constante que representa esta opción de socket es 0x1009.</span><span class="sxs-lookup"><span data-stu-id="83b29-107">The constant that represents this socket option is 0x1009.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b29-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83b29-108">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a><span data-ttu-id="83b29-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83b29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b29-110">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="83b29-110">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b29-111">Un descriptor que identifica el socket.</span><span class="sxs-lookup"><span data-stu-id="83b29-111">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="83b29-112">*nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="83b29-112">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b29-113">Nivel en el que se define la opción.</span><span class="sxs-lookup"><span data-stu-id="83b29-113">The level at which the option is defined.</span></span> <span data-ttu-id="83b29-114">Use **el \_ socket sol** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="83b29-114">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="83b29-115">*optname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83b29-115">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b29-116">Opción de socket para la que se va a recuperar el valor.</span><span class="sxs-lookup"><span data-stu-id="83b29-116">The socket option for which the value is to be retrieved.</span></span> <span data-ttu-id="83b29-117">Use **el \_ \_ Estado de BSP** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="83b29-117">Use **SO\_BSP\_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="83b29-118">*optval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="83b29-118">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83b29-119">Puntero al búfer en el que se va a devolver el valor de la opción solicitada.</span><span class="sxs-lookup"><span data-stu-id="83b29-119">A pointer to the buffer in which the value for the requested option is to be returned.</span></span> <span data-ttu-id="83b29-120">Este parámetro debe apuntar al búfer igual o mayor que el tamaño de una estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="83b29-120">This parameter should point to buffer equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="83b29-121">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83b29-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83b29-122">Puntero al tamaño, en bytes, del búfer *optval* .</span><span class="sxs-lookup"><span data-stu-id="83b29-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="83b29-123">Este tamaño debe ser igual o mayor que el tamaño de una estructura [**de \_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="83b29-123">This size must be equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83b29-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83b29-124">Return value</span></span>

<span data-ttu-id="83b29-125">Si la operación se completa correctamente, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="83b29-125">If the operation completes successfully, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) returns zero.</span></span>

<span data-ttu-id="83b29-126">Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="83b29-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="83b29-127">Código de error</span><span class="sxs-lookup"><span data-stu-id="83b29-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="83b29-128">Significado</span><span class="sxs-lookup"><span data-stu-id="83b29-128">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83b29-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="83b29-130">Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.</span><span class="sxs-lookup"><span data-stu-id="83b29-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="83b29-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="83b29-132">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="83b29-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="83b29-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="83b29-134">Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="83b29-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="83b29-135">Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de una estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="83b29-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span><br/> |
| <dl> <span data-ttu-id="83b29-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="83b29-137">Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="83b29-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="83b29-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="83b29-139">El parámetro *LEVEL* es desconocido o no es válido.</span><span class="sxs-lookup"><span data-stu-id="83b29-139">The *level* parameter is unknown or invalid.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="83b29-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="83b29-141">La opción es desconocida o no es compatible con la familia del protocolo indicada.</span><span class="sxs-lookup"><span data-stu-id="83b29-141">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="83b29-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="83b29-143">El descriptor no es un socket.</span><span class="sxs-lookup"><span data-stu-id="83b29-143">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="83b29-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83b29-144">Remarks</span></span>

<span data-ttu-id="83b29-145">La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket de **\_ \_ Estado de BSP** recupera la dirección local, el puerto local, la dirección remota, el puerto remoto, el tipo de socket y el protocolo que usa un socket.</span><span class="sxs-lookup"><span data-stu-id="83b29-145">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_BSP\_STATE** socket option retrieves the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span> <span data-ttu-id="83b29-146">La opción de socket de **\_ \_ Estado de BSP** funciona con sockets IPv6 o IPv4 (las familias de direcciones **AF \_ inet6** y **AF \_ inet** ).</span><span class="sxs-lookup"><span data-stu-id="83b29-146">The **SO\_BSP\_STATE** socket option works with IPv6 or IPv4 sockets (the **AF\_INET6** and **AF\_INET** address families).</span></span>

<span data-ttu-id="83b29-147">Si la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) se ejecuta correctamente, la información se devuelve en una estructura [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) en el búfer al que apunta el parámetro *optval* .</span><span class="sxs-lookup"><span data-stu-id="83b29-147">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function is successful, the information is returned in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure in the buffer pointed to by the *optval* parameter.</span></span> <span data-ttu-id="83b29-148">El entero al que apunta *optlen* debe contener originalmente el tamaño de este búfer; en la devolución, se establecerá en la longitud, en bytes, del valor devuelto en el parámetro *optval* .</span><span class="sxs-lookup"><span data-stu-id="83b29-148">The integer pointed to by *optlen* should originally contain the size of this buffer; on return, it will be set to the length, in bytes, of the value returned in the *optval* parameter.</span></span>

<span data-ttu-id="83b29-149">Los miembros **iSocketType** y **iProtocol** de la estructura [**de \_ información CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) devuelta se rellenan para el descriptor de socket en el parámetro *s* .</span><span class="sxs-lookup"><span data-stu-id="83b29-149">The **iSocketType** and **iProtocol** members in the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure are filled in for the socket descriptor in the *s* parameter.</span></span>

<span data-ttu-id="83b29-150">Si el socket está en estado conectado o enlazado, el miembro **LocalAddr** de la estructura devuelta [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) se establecerá en una estructura [SOCKADDR](sockaddr-2.md) que represente la dirección local y el puerto.</span><span class="sxs-lookup"><span data-stu-id="83b29-150">If the socket is in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure will be set to a [SOCKADDR](sockaddr-2.md) structure representing the local address and port.</span></span> <span data-ttu-id="83b29-151">Si el socket está en estado conectado, el miembro **RemoteAddr** de la estructura de **\_ información de CSADDR** devuelta se establecerá en una estructura SOCKADDR que represente la dirección remota y el puerto.</span><span class="sxs-lookup"><span data-stu-id="83b29-151">If the socket is in a connected state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure will be set to a SOCKADDR structure representing the remote address and port.</span></span>

<span data-ttu-id="83b29-152">Si el socket no está en estado conectado o enlazado, se devuelve el miembro **LocalAddr** de la estructura de [**\_ información CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) devuelta con un puntero **nulo** en el miembro **lpSockaddr** y el miembro **iSockaddrLength** establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="83b29-152">If the socket is not in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span> <span data-ttu-id="83b29-153">Si el socket no está en un estado enlazado, se devuelve el miembro **RemoteAddr** de la estructura de **\_ información CSADDR** devuelta con un puntero **nulo** en el miembro **lpSockaddr** y el miembro **iSockaddrLength** establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="83b29-153">If the socket is not in a bound state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span>

<span data-ttu-id="83b29-154">Si se produce un error en la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , los parámetros *optval* y *optlen* se dejan sin cambios y el parámetro *optval* no apunta a una estructura de [**\_ información CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) devuelta.</span><span class="sxs-lookup"><span data-stu-id="83b29-154">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function fails, the *optval* and *optlen* parameters are left unchanged and the *optval* parameter does not point to a returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

<span data-ttu-id="83b29-155">Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.</span><span class="sxs-lookup"><span data-stu-id="83b29-155">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b29-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83b29-156">Requirements</span></span>



| <span data-ttu-id="83b29-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b29-157">Requirement</span></span> | <span data-ttu-id="83b29-158">Value</span><span class="sxs-lookup"><span data-stu-id="83b29-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83b29-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83b29-159">Minimum supported client</span></span><br/> | <span data-ttu-id="83b29-160">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83b29-160">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83b29-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83b29-161">Minimum supported server</span></span><br/> | <span data-ttu-id="83b29-162">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="83b29-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83b29-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83b29-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="83b29-164"><dt>Ws2def. h (incluir WinSock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83b29-164"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83b29-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="83b29-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b29-166">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="83b29-166">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="83b29-167">**información de CSADDR \_**</span><span class="sxs-lookup"><span data-stu-id="83b29-167">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="83b29-168">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="83b29-168">SOCKADDR</span></span>](sockaddr-2.md)
</dt> </dl>

 

 
