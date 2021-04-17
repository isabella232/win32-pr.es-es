---
description: Permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función WSARecvMsg en un socket IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: Opción de socket de IPV6_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696377"
---
# <a name="ipv6_pktinfo-socket-option"></a><span data-ttu-id="b6eec-103">IPV6 \_ PKTINFO socket, opción</span><span class="sxs-lookup"><span data-stu-id="b6eec-103">IPV6\_PKTINFO socket option</span></span>

<span data-ttu-id="b6eec-104">La \_ opción de socket PKTINFO de IPv6 permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) en un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="b6eec-104">The IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv6 socket..</span></span>

<span data-ttu-id="b6eec-105">Para consultar el estado de esta opción de socket, llame a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="b6eec-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="b6eec-106">Para establecer esta opción, llame a [**la función del método de llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="b6eec-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="b6eec-107">Valor de opción de socket</span><span class="sxs-lookup"><span data-stu-id="b6eec-107">Socket option value</span></span>

<span data-ttu-id="b6eec-108">La constante que representa esta opción de socket es 19.</span><span class="sxs-lookup"><span data-stu-id="b6eec-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6eec-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6eec-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="b6eec-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6eec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6eec-111">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b6eec-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6eec-112">Un descriptor que identifica el socket.</span><span class="sxs-lookup"><span data-stu-id="b6eec-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="b6eec-113">*nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b6eec-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6eec-114">Nivel en el que se define la opción.</span><span class="sxs-lookup"><span data-stu-id="b6eec-114">The level at which the option is defined.</span></span> <span data-ttu-id="b6eec-115">Use **IPPROTO \_ IPv6** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="b6eec-115">Use **IPPROTO\_IPV6** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="b6eec-116">*optname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6eec-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6eec-117">Opción de socket para la que se va a obtener o establecer el valor.</span><span class="sxs-lookup"><span data-stu-id="b6eec-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="b6eec-118">Use IPV6 \_ PKTINFO para esta operación.</span><span class="sxs-lookup"><span data-stu-id="b6eec-118">Use IPV6\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="b6eec-119">*optval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b6eec-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6eec-120">Puntero al búfer que contiene el valor de la opción que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b6eec-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="b6eec-121">Este parámetro debe apuntar al búfer igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b6eec-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="b6eec-122">Este valor se trata como un valor booleano con 0 que se usa para indicar **false** (deshabilitado) y un valor distinto de cero para indicar **true** (habilitado).</span><span class="sxs-lookup"><span data-stu-id="b6eec-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="b6eec-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b6eec-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6eec-124">Puntero al tamaño, en bytes, del búfer *optval* .</span><span class="sxs-lookup"><span data-stu-id="b6eec-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="b6eec-125">Este tamaño debe ser igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b6eec-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6eec-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6eec-126">Return value</span></span>

<span data-ttu-id="b6eec-127">Si la operación se completa correctamente, la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o el [**valor de My**](/windows/desktop/api/winsock/nf-winsock-setsockopt) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b6eec-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="b6eec-128">Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b6eec-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="b6eec-129">Código de error</span><span class="sxs-lookup"><span data-stu-id="b6eec-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="b6eec-130">Significado</span><span class="sxs-lookup"><span data-stu-id="b6eec-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6eec-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="b6eec-132">Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.</span><span class="sxs-lookup"><span data-stu-id="b6eec-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="b6eec-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="b6eec-134">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="b6eec-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="b6eec-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="b6eec-136">Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="b6eec-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="b6eec-137">Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b6eec-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="b6eec-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="b6eec-139">Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b6eec-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="b6eec-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="b6eec-141">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="b6eec-141">An invalid argument was supplied.</span></span> <span data-ttu-id="b6eec-142">Este error se devuelve si el parámetro *LEVEL* es desconocido o no es válido.</span><span class="sxs-lookup"><span data-stu-id="b6eec-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="b6eec-143">En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.</span><span class="sxs-lookup"><span data-stu-id="b6eec-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b6eec-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="b6eec-145">La opción es desconocida o no es compatible con la familia del protocolo indicada.</span><span class="sxs-lookup"><span data-stu-id="b6eec-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="b6eec-146">Se devuelve este error si el parámetro de *tipo* para el descriptor de socket pasado en el parámetro *s* no era **sock \_ DGRAM** o **sock \_ raw**.</span><span class="sxs-lookup"><span data-stu-id="b6eec-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="b6eec-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="b6eec-148">El descriptor no es un socket.</span><span class="sxs-lookup"><span data-stu-id="b6eec-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b6eec-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6eec-149">Remarks</span></span>

<span data-ttu-id="b6eec-150">La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la \_ opción de socket PKTINFO de IPv6 permite que una aplicación determine si la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)devolverá información de paquetes para un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="b6eec-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IPV6\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv6 socket.</span></span>

<span data-ttu-id="b6eec-151">La [**función de la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la llamada con la \_ opción de socket PKTINFO de IPv6 permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="b6eec-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="b6eec-152">De \_ forma predeterminada, la opción PKTINFO de IPv6 para un socket está deshabilitada (establecida en **false**).</span><span class="sxs-lookup"><span data-stu-id="b6eec-152">The IPV6\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="b6eec-153">Cuando esta opción de socket está habilitada en un socket IPv6 de tipo **sock \_ DGRAM** o **sock \_ raw**, la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelve información de paquetes en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) señalada por el parámetro *lpMsg* .</span><span class="sxs-lookup"><span data-stu-id="b6eec-153">When this socket option is enabled on an IPv6 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="b6eec-154">Uno de los objetos de datos de control de la estructura **WSAMSG** devuelta contendrá una estructura [**\_ pktinfo de IN6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) que se usa para almacenar la información de dirección de paquetes recibida.</span><span class="sxs-lookup"><span data-stu-id="b6eec-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="b6eec-155">En el caso de los datagramas recibidos por la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) a través de IPv6, el miembro de **control** de la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recibida contendrá una estructura [**WSABUF utilizadas**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contiene una estructura **WSACMSGHDR** .</span><span class="sxs-lookup"><span data-stu-id="b6eec-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv6, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="b6eec-156">El miembro de **\_ nivel cmsg** de esta estructura **WSACMSGHDR** contendría **IPPROTO \_ IPv6**, el miembro de **\_ tipo cmsg** de esta estructura contendría **IPv6 \_ PKTINFO** y el miembro de **\_ datos cmsg** contendría una estructura [**IN6 \_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) que se usa para almacenar la información de dirección de paquete IPv6 recibida.</span><span class="sxs-lookup"><span data-stu-id="b6eec-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IPV6**, the **cmsg\_type** member of this structure would contain **IPV6\_PKTINFO**, and the **cmsg\_data** member would contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received IPv6 packet address information.</span></span> <span data-ttu-id="b6eec-157">La dirección IPv6 de la estructura **IN6 \_ pktinfo** es la dirección IPv6 desde la que se recibió el paquete.</span><span class="sxs-lookup"><span data-stu-id="b6eec-157">The IPv6 address in the **in6\_pktinfo** structure is the IPv6 address from which the packet was received.</span></span>

<span data-ttu-id="b6eec-158">En el caso de un socket de datagrama de pila doble, si una aplicación requiere la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) para devolver información de paquetes en una estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para los datagramas recibidos a través de IPv4, la opción de socket de [IP \_ PKTINFO](ip-pktinfo.md) debe establecerse en true en el socket.</span><span class="sxs-lookup"><span data-stu-id="b6eec-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then [IP\_PKTINFO](ip-pktinfo.md) socket option must be set to true on the socket.</span></span> <span data-ttu-id="b6eec-159">Si solo la \_ opción PKTINFO de IPv6 está establecida en true en el socket, se proporcionará información de paquetes para los datagramas recibidos a través de IPv6, pero es posible que no se proporcionen para los datagramas recibidos a través de IPv4.</span><span class="sxs-lookup"><span data-stu-id="b6eec-159">If only the IPV6\_PKTINFO option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="b6eec-160">Tenga en cuenta que el archivo de encabezado *Ws2ipdef. h* se incluye automáticamente en *Ws2tcpip. h* y nunca se debe usar directamente.</span><span class="sxs-lookup"><span data-stu-id="b6eec-160">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6eec-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6eec-161">Requirements</span></span>



| <span data-ttu-id="b6eec-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6eec-162">Requirement</span></span> | <span data-ttu-id="b6eec-163">Value</span><span class="sxs-lookup"><span data-stu-id="b6eec-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6eec-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6eec-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b6eec-165">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b6eec-165">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="b6eec-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6eec-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b6eec-167">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6eec-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b6eec-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6eec-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6eec-169"><dt>Ws2ipdef. h (incluye Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6eec-169"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6eec-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6eec-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6eec-171">Sockets de doble pila</span><span class="sxs-lookup"><span data-stu-id="b6eec-171">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="b6eec-172">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="b6eec-172">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="b6eec-173">**IN6 \_ pktinfo**</span><span class="sxs-lookup"><span data-stu-id="b6eec-173">**in6\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[<span data-ttu-id="b6eec-174">\_PKTINFO IP</span><span class="sxs-lookup"><span data-stu-id="b6eec-174">IP\_PKTINFO</span></span>](ip-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="b6eec-175">**Opciones de socket de IPv6 de IPPROTO \_**</span><span class="sxs-lookup"><span data-stu-id="b6eec-175">**IPPROTO\_IPV6 Socket Options**</span></span>](ipproto-ipv6-socket-options.md)
</dt> <dt>

[<span data-ttu-id="b6eec-176">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="b6eec-176">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="b6eec-177">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="b6eec-177">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="b6eec-178">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="b6eec-178">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="b6eec-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="b6eec-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
