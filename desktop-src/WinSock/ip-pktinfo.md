---
description: Permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función WSARecvMsg en un socket IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: Opción de socket de IP_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2134b31ead9efeb032b4ed72fcaedcd4cc9f67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360297"
---
# <a name="ip_pktinfo-socket-option"></a><span data-ttu-id="f90e1-103">IP \_ PKTINFO socket, opción</span><span class="sxs-lookup"><span data-stu-id="f90e1-103">IP\_PKTINFO socket option</span></span>

<span data-ttu-id="f90e1-104">La \_ opción de socket PKTINFO de IP permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) en un socket IPv4.</span><span class="sxs-lookup"><span data-stu-id="f90e1-104">The IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv4 socket..</span></span>

<span data-ttu-id="f90e1-105">Para consultar el estado de esta opción de socket, llame a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="f90e1-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="f90e1-106">Para establecer esta opción, llame a [**la función del método de llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f90e1-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="f90e1-107">Valor de opción de socket</span><span class="sxs-lookup"><span data-stu-id="f90e1-107">Socket option value</span></span>

<span data-ttu-id="f90e1-108">La constante que representa esta opción de socket es 19.</span><span class="sxs-lookup"><span data-stu-id="f90e1-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="f90e1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f90e1-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="f90e1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f90e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f90e1-111">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f90e1-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f90e1-112">Un descriptor que identifica el socket.</span><span class="sxs-lookup"><span data-stu-id="f90e1-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="f90e1-113">*nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f90e1-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f90e1-114">Nivel en el que se define la opción.</span><span class="sxs-lookup"><span data-stu-id="f90e1-114">The level at which the option is defined.</span></span> <span data-ttu-id="f90e1-115">Use **la \_ dirección IP de IPPROTO** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="f90e1-115">Use **IPPROTO\_IP** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f90e1-116">*optname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f90e1-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f90e1-117">Opción de socket para la que se va a obtener o establecer el valor.</span><span class="sxs-lookup"><span data-stu-id="f90e1-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="f90e1-118">Use \_ la PKTINFO IP para esta operación.</span><span class="sxs-lookup"><span data-stu-id="f90e1-118">Use IP\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f90e1-119">*optval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f90e1-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f90e1-120">Puntero al búfer que contiene el valor de la opción que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f90e1-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="f90e1-121">Este parámetro debe apuntar al búfer igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f90e1-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="f90e1-122">Este valor se trata como un valor booleano con 0 que se usa para indicar **false** (deshabilitado) y un valor distinto de cero para indicar **true** (habilitado).</span><span class="sxs-lookup"><span data-stu-id="f90e1-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="f90e1-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f90e1-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f90e1-124">Puntero al tamaño, en bytes, del búfer *optval* .</span><span class="sxs-lookup"><span data-stu-id="f90e1-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="f90e1-125">Este tamaño debe ser igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f90e1-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f90e1-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f90e1-126">Return value</span></span>

<span data-ttu-id="f90e1-127">Si la operación se completa correctamente, la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o el [**valor de My**](/windows/desktop/api/winsock/nf-winsock-setsockopt) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f90e1-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="f90e1-128">Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="f90e1-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="f90e1-129">Código de error</span><span class="sxs-lookup"><span data-stu-id="f90e1-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="f90e1-130">Significado</span><span class="sxs-lookup"><span data-stu-id="f90e1-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f90e1-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="f90e1-132">Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.</span><span class="sxs-lookup"><span data-stu-id="f90e1-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="f90e1-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="f90e1-134">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="f90e1-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="f90e1-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="f90e1-136">Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="f90e1-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="f90e1-137">Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f90e1-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="f90e1-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="f90e1-139">Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f90e1-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="f90e1-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="f90e1-141">Se proporcionó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="f90e1-141">An invalid argument was supplied.</span></span> <span data-ttu-id="f90e1-142">Este error se devuelve si el parámetro *LEVEL* es desconocido o no es válido.</span><span class="sxs-lookup"><span data-stu-id="f90e1-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="f90e1-143">En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.</span><span class="sxs-lookup"><span data-stu-id="f90e1-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f90e1-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="f90e1-145">La opción es desconocida o no es compatible con la familia del protocolo indicada.</span><span class="sxs-lookup"><span data-stu-id="f90e1-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="f90e1-146">Se devuelve este error si el parámetro de *tipo* para el descriptor de socket pasado en el parámetro *s* no era **sock \_ DGRAM** o **sock \_ raw**.</span><span class="sxs-lookup"><span data-stu-id="f90e1-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="f90e1-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="f90e1-148">El descriptor no es un socket.</span><span class="sxs-lookup"><span data-stu-id="f90e1-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f90e1-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f90e1-149">Remarks</span></span>

<span data-ttu-id="f90e1-150">La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) a la que se llama con la \_ opción IP PKTINFO socket permite que una aplicación determine si la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)devolverá información de paquetes para un socket IPv4.</span><span class="sxs-lookup"><span data-stu-id="f90e1-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IP\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv4 socket.</span></span>

<span data-ttu-id="f90e1-151">La [**función de la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la llamada con la \_ opción de socket PKTINFO de IP permite a una aplicación habilitar o deshabilitar la devolución de información de paquetes mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="f90e1-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="f90e1-152">De \_ forma predeterminada, la opción PKTINFO de IP para un socket está deshabilitada (establecida en **false**).</span><span class="sxs-lookup"><span data-stu-id="f90e1-152">The IP\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="f90e1-153">Cuando esta opción de socket está habilitada en un socket IPv4 de tipo **sock \_ DGRAM** o **sock \_ raw**, la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelve información de paquetes en la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) señalada por el parámetro *lpMsg* .</span><span class="sxs-lookup"><span data-stu-id="f90e1-153">When this socket option is enabled on an IPv4 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="f90e1-154">Uno de los objetos de datos de control de la estructura **WSAMSG** devuelta contendrá una estructura [**en \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) que se usa para almacenar la información de dirección de paquetes recibida.</span><span class="sxs-lookup"><span data-stu-id="f90e1-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="f90e1-155">En el caso de los datagramas recibidos por la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) a través de IPv4, el miembro de **control** de la estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recibida contendrá una estructura [**WSABUF utilizadas**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contiene una estructura **WSACMSGHDR** .</span><span class="sxs-lookup"><span data-stu-id="f90e1-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv4, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="f90e1-156">El miembro de **\_ nivel cmsg** de esta estructura **WSACMSGHDR** contendría **IPPROTO \_ IP**, el miembro de **\_ tipo cmsg** de esta estructura contendría **\_ PKTINFO IP** y el miembro de **\_ datos Cmsg** contendría una estructura [**in \_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) utilizada para almacenar la información de dirección de paquetes IPv4 recibida.</span><span class="sxs-lookup"><span data-stu-id="f90e1-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IP**, the **cmsg\_type** member of this structure would contain **IP\_PKTINFO**, and the **cmsg\_data** member would contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received IPv4 packet address information.</span></span> <span data-ttu-id="f90e1-157">La dirección IPv4 en la estructura **de \_ pktinfo** es la dirección IPv4 desde la que se recibió el paquete.</span><span class="sxs-lookup"><span data-stu-id="f90e1-157">The IPv4 address in the **in\_pktinfo** structure is the IPv4 address from which the packet was received.</span></span>

<span data-ttu-id="f90e1-158">En el caso de un socket de datagrama de pila doble, si una aplicación requiere la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) para devolver información de paquetes en una estructura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para los datagramas recibidos a través de IPv4, \_ la opción de socket de IP PKTINFO debe establecerse en true en el socket.</span><span class="sxs-lookup"><span data-stu-id="f90e1-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then IP\_PKTINFO socket option must be set to true on the socket.</span></span> <span data-ttu-id="f90e1-159">Si solo la [opción \_ PKTINFO de IPv6](ipv6-pktinfo.md) está establecida en true en el socket, se proporcionará información de paquetes para los datagramas recibidos a través de IPv6, pero es posible que no se proporcionen para los datagramas recibidos a través de IPv4.</span><span class="sxs-lookup"><span data-stu-id="f90e1-159">If only the [IPV6\_PKTINFO](ipv6-pktinfo.md) option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="f90e1-160">Si una aplicación intenta establecer la \_ opción de socket PKTINFO de IP en un socket de datagrama de pila doble e IPv4 está deshabilitado en el [](/windows/desktop/api/winsock/nf-winsock-setsockopt) sistema, se producirá un error en la función MUTE y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devolverá un error de [WSAEINVAL](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="f90e1-160">If an application tries to set the IP\_PKTINFO socket option on a dual-stack datagram socket and IPv4 is disabled on the system, then the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function will fail and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) will return with an error of [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="f90e1-161">Este mismo error **también lo devuelve la función** My como resultado de otros errores.</span><span class="sxs-lookup"><span data-stu-id="f90e1-161">This same error is also returned by the **setsockopt** function as a result of other errors.</span></span> <span data-ttu-id="f90e1-162">Si una aplicación intenta establecer una \_ opción de socket de nivel IP de IPPROTO en un socket de doble pila y se produce un error con [WSAEINVAL](windows-sockets-error-codes-2.md), la aplicación debe determinar si IPv4 está deshabilitado en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="f90e1-162">If an application tries to set an IPPROTO\_IP level socket option on a dual-stack socket and it fails with [WSAEINVAL](windows-sockets-error-codes-2.md), then the application should determine if IPv4 is disabled on the local computer.</span></span> <span data-ttu-id="f90e1-163">Un método que se puede usar para detectar si IPv4 está habilitado o deshabilitado es llamar a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con el parámetro *AF* establecido en AF \_ inet para probar y crear un socket IPv4.</span><span class="sxs-lookup"><span data-stu-id="f90e1-163">One method that can be used to detect if IPv4 is enabled or disabled is to call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function with the *af* parameter set to AF\_INET to try and create an IPv4 socket.</span></span> <span data-ttu-id="f90e1-164">Si se produce un error en la función de **socket** y **WSAGetLastError** devuelve un error de [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), significa que IPv4 no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f90e1-164">If the **socket** function fails and **WSAGetLastError** returns an error of [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), then it means IPv4 is not enabled.</span></span> <span data-ttu-id="f90e1-165">En este caso, la aplicación puede pasar por alto **un error de la** función de r al intentar establecer la \_ opción de socket PKTINFO de IP.</span><span class="sxs-lookup"><span data-stu-id="f90e1-165">In this case, a **setsockopt** function failure when attempting to set the IP\_PKTINFO socket option can be ignored by the application.</span></span> <span data-ttu-id="f90e1-166">De lo contrario, un error al intentar establecer la \_ opción de socket PKTINFO de IP debe tratarse como un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f90e1-166">Otherwise a failure when attempting to set the IP\_PKTINFO socket option should be treated as an unexpected error.</span></span>

<span data-ttu-id="f90e1-167">Tenga en cuenta que el archivo de encabezado *Ws2ipdef. h* se incluye automáticamente en *Ws2tcpip. h* y nunca se debe usar directamente.</span><span class="sxs-lookup"><span data-stu-id="f90e1-167">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="f90e1-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f90e1-168">Requirements</span></span>



| <span data-ttu-id="f90e1-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="f90e1-169">Requirement</span></span> | <span data-ttu-id="f90e1-170">Value</span><span class="sxs-lookup"><span data-stu-id="f90e1-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f90e1-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f90e1-171">Minimum supported client</span></span><br/> | <span data-ttu-id="f90e1-172">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f90e1-172">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="f90e1-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f90e1-173">Minimum supported server</span></span><br/> | <span data-ttu-id="f90e1-174">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f90e1-174">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f90e1-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f90e1-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="f90e1-176"><dt>Ws2ipdef. h (incluye Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f90e1-176"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f90e1-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="f90e1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f90e1-178">Sockets de doble pila</span><span class="sxs-lookup"><span data-stu-id="f90e1-178">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="f90e1-179">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="f90e1-179">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="f90e1-180">**en \_ pktinfo**</span><span class="sxs-lookup"><span data-stu-id="f90e1-180">**in\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[<span data-ttu-id="f90e1-181">**\_Opciones de socket IP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="f90e1-181">**IPPROTO\_IP Socket Options**</span></span>](ipproto-ip-socket-options.md)
</dt> <dt>

[<span data-ttu-id="f90e1-182">\_PKTINFO IPv6</span><span class="sxs-lookup"><span data-stu-id="f90e1-182">IPV6\_PKTINFO</span></span>](ipv6-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="f90e1-183">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="f90e1-183">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="f90e1-184">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="f90e1-184">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="f90e1-185">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="f90e1-185">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="f90e1-186">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="f90e1-186">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
