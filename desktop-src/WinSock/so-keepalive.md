---
description: Está diseñado para permitir que una aplicación habilite los paquetes Keep-Alive para una conexión de socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Opción de socket de SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706827"
---
# <a name="so_keepalive-socket-option"></a><span data-ttu-id="42a54-103">\_Opción de socket KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="42a54-103">SO\_KEEPALIVE socket option</span></span>

<span data-ttu-id="42a54-104">La opción de socket **so \_ KEEPALIVE** está diseñada para permitir que una aplicación habilite los paquetes Keep-Alive para una conexión de socket.</span><span class="sxs-lookup"><span data-stu-id="42a54-104">The **SO\_KEEPALIVE** socket option is designed to allow an application to enable keep-alive packets for a socket connection.</span></span>

<span data-ttu-id="42a54-105">Para consultar el estado de esta opción de socket, llame a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="42a54-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="42a54-106">Para establecer esta opción, llame a [**la función del método de llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="42a54-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="42a54-107">Valor de opción de socket</span><span class="sxs-lookup"><span data-stu-id="42a54-107">Socket option value</span></span>

<span data-ttu-id="42a54-108">La constante que representa esta opción de socket es 0x0008.</span><span class="sxs-lookup"><span data-stu-id="42a54-108">The constant that represents this socket option is 0x0008.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a54-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42a54-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="42a54-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42a54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a54-111">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="42a54-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a54-112">Un descriptor que identifica el socket.</span><span class="sxs-lookup"><span data-stu-id="42a54-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="42a54-113">*nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="42a54-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a54-114">Nivel en el que se define la opción.</span><span class="sxs-lookup"><span data-stu-id="42a54-114">The level at which the option is defined.</span></span> <span data-ttu-id="42a54-115">Use **el \_ socket sol** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="42a54-115">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="42a54-116">*optname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42a54-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a54-117">Opción de socket para la que se va a establecer el valor.</span><span class="sxs-lookup"><span data-stu-id="42a54-117">The socket option for which the value is to be set.</span></span> <span data-ttu-id="42a54-118">Úselo **para \_** esta operación.</span><span class="sxs-lookup"><span data-stu-id="42a54-118">Use **SO\_KEEPALIVE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="42a54-119">*optval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="42a54-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42a54-120">Puntero al búfer que contiene el valor de la opción que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="42a54-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="42a54-121">Este parámetro debe apuntar al búfer igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="42a54-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="42a54-122">Este valor se trata como un valor booleano con 0 que se usa para indicar **false** (deshabilitado) y un valor distinto de cero para indicar **true** (habilitado).</span><span class="sxs-lookup"><span data-stu-id="42a54-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="42a54-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="42a54-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42a54-124">Puntero al tamaño, en bytes, del búfer *optval* .</span><span class="sxs-lookup"><span data-stu-id="42a54-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="42a54-125">Este tamaño debe ser igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="42a54-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a54-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42a54-126">Return value</span></span>

<span data-ttu-id="42a54-127">Si la operación se completa [**correctamente, el valor de la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="42a54-127">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="42a54-128">Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="42a54-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="42a54-129">Código de error</span><span class="sxs-lookup"><span data-stu-id="42a54-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="42a54-130">Significado</span><span class="sxs-lookup"><span data-stu-id="42a54-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42a54-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="42a54-132">Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.</span><span class="sxs-lookup"><span data-stu-id="42a54-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="42a54-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="42a54-134">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="42a54-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="42a54-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="42a54-136">Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="42a54-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="42a54-137">Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="42a54-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="42a54-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="42a54-139">Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="42a54-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="42a54-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="42a54-141">El parámetro *LEVEL* es desconocido o no es válido.</span><span class="sxs-lookup"><span data-stu-id="42a54-141">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="42a54-142">En Windows Vista y versiones posteriores, este error también se devuelve si el socket estaba en un estado de transición.</span><span class="sxs-lookup"><span data-stu-id="42a54-142">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="42a54-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="42a54-144">La opción es desconocida o no es compatible con la familia del protocolo indicada.</span><span class="sxs-lookup"><span data-stu-id="42a54-144">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="42a54-145">Se devuelve este error si el descriptor de socket pasado en el parámetro *s* era para un socket de datagramas.</span><span class="sxs-lookup"><span data-stu-id="42a54-145">This error is returned if the socket descriptor passed in the *s* parameter was for a datagram socket.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="42a54-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="42a54-147">El descriptor no es un socket.</span><span class="sxs-lookup"><span data-stu-id="42a54-147">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="42a54-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42a54-148">Remarks</span></span>

<span data-ttu-id="42a54-149">La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket **so \_ KEEPALIVE** permite que una aplicación recupere el estado actual de la opción keepalive, aunque esta característica no se utiliza normalmente.</span><span class="sxs-lookup"><span data-stu-id="42a54-149">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to retrieve the current state of the keepalive option, although this is feature not normally used.</span></span> <span data-ttu-id="42a54-150">Si una aplicación necesita habilitar paquetes keepalive en un socket, simplemente llama a la función de la [**función de llamada**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción.</span><span class="sxs-lookup"><span data-stu-id="42a54-150">If an application needs to enable keepalive packets on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="42a54-151">La [**función que**](/windows/desktop/api/winsock/nf-winsock-setsockopt) se llama con la opción de socket **so \_ KEEPALIVE** permite que una aplicación habilite los paquetes Keep-Alive para una conexión de socket.</span><span class="sxs-lookup"><span data-stu-id="42a54-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to enable keep-alive packets for a socket connection.</span></span> <span data-ttu-id="42a54-152">De forma predeterminada, la opción de **\_ KEEPALIVE** para un socket está deshabilitada (establecida en **false**).</span><span class="sxs-lookup"><span data-stu-id="42a54-152">The **SO\_KEEPALIVE** option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="42a54-153">Cuando esta opción de socket está habilitada, la pila TCP envía paquetes Keep-Alive cuando no se ha recibido ningún paquete de datos o de confirmación para la conexión dentro de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="42a54-153">When this socket option is enabled, the TCP stack sends keep-alive packets when no data or acknowledgement packets have been received for the connection within an interval.</span></span> <span data-ttu-id="42a54-154">Para obtener más información acerca de la opción Keep-Alive, consulte la sección 4.2.3.6 sobre los *requisitos de los hosts de Internet: las capas de comunicación* especificadas en RFC 1122 están disponibles en el [sitio web de IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="42a54-154">For more information on the keep-alive option, see section 4.2.3.6 on the *Requirements for Internet Hosts—Communication Layers* specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span> <span data-ttu-id="42a54-155">(Este recurso solo está disponible en inglés).</span><span class="sxs-lookup"><span data-stu-id="42a54-155">(This resource may only be available in English.)</span></span>

<span data-ttu-id="42a54-156">La opción de socket **so \_ KEEPALIVE** solo es válida para los protocolos que admiten la noción de Keep-Alive (protocolos orientados a la conexión).</span><span class="sxs-lookup"><span data-stu-id="42a54-156">The **SO\_KEEPALIVE** socket option is valid only for protocols that support the notion of keep-alive (connection-oriented protocols).</span></span> <span data-ttu-id="42a54-157">Para TCP, el tiempo de espera de mantenimiento de conexión predeterminado es de 2 horas y el intervalo de mantenimiento de conexión es de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="42a54-157">For TCP, the default keep-alive timeout is 2 hours and the keep-alive interval is 1 second.</span></span> <span data-ttu-id="42a54-158">El número predeterminado de sondeos Keep-Alive varía en función de la versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="42a54-158">The default number of keep-alive probes varies based on the version of Windows.</span></span>

<span data-ttu-id="42a54-159">El código de control [**SiO \_ KEEPALIVE \_ vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) se puede usar para habilitar o deshabilitar Keep-Alive, y ajustar el tiempo de espera y el intervalo para una única conexión.</span><span class="sxs-lookup"><span data-stu-id="42a54-159">The [**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control code can be used to enable or disable keep-alive, and adjust the timeout and interval, for a single connection.</span></span> <span data-ttu-id="42a54-160">Si Keep-Alive está habilitado con la opción **\_ KeepAlive**, se usará la configuración predeterminada de TCP para el tiempo de espera y el intervalo de mantenimiento de conexión, a menos que estos valores se hayan cambiado mediante **SiO \_ KEEPALIVE \_ vals**.</span><span class="sxs-lookup"><span data-stu-id="42a54-160">If keep-alive is enabled with **SO\_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="42a54-161">El valor predeterminado para todo el sistema del tiempo de espera de mantenimiento de conexión se controla mediante la configuración del registro [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) , que toma un valor en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="42a54-161">The default system-wide value of the keep-alive timeout is controllable through the [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="42a54-162">El valor predeterminado para todo el sistema del intervalo Keep-Alive se controla a través de la configuración del registro [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que toma un valor en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="42a54-162">The default system-wide value of the keep-alive interval is controllable through the [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span>

<span data-ttu-id="42a54-163">En Windows Vista y versiones posteriores, el número de sondeos Keep-Alive (retransmisiones de datos) se establece en 10 y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="42a54-163">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="42a54-164">En Windows Server 2003, Windows XP y Windows 2000, la configuración predeterminada para el número de sondeos Keep-Alive es 5.</span><span class="sxs-lookup"><span data-stu-id="42a54-164">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span> <span data-ttu-id="42a54-165">El número de sondeos Keep-Alive se controla a través de la configuración del registro [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) y [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="42a54-165">The number of keep-alive probes is controllable through the [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) and [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span> <span data-ttu-id="42a54-166">El número de sondeos Keep-Alive se establece en el mayor de los dos valores de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="42a54-166">The number of keep-alive probes is set to the larger of the two registry key values.</span></span> <span data-ttu-id="42a54-167">Si este número es 0, no se enviarán sondeos Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="42a54-167">If this number is 0, then keep-alive probes will not be sent.</span></span> <span data-ttu-id="42a54-168">Si este número es superior a 255, se ajusta a 255.</span><span class="sxs-lookup"><span data-stu-id="42a54-168">If this number is above 255, then it is adjusted to 255.</span></span>

<span data-ttu-id="42a54-169">En Windows Vista y versiones posteriores, la opción de socket **so \_ KEEPALIVE** solo se puede establecer con la función de llamada a la función [**de la función**](/windows/desktop/api/winsock/nf-winsock-setsockopt) del socket en un estado conocido, no un estado de transición.</span><span class="sxs-lookup"><span data-stu-id="42a54-169">On Windows Vista and later, the **SO\_KEEPALIVE** socket option can only be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is in a well-known state not a transitional state.</span></span> <span data-ttu-id="42a54-170">Para TCP, la opción de socket **so \_ KEEPALIVE** debe establecerse antes de que se llame a la función Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)), o después de que se haya completado la solicitud de conexión.</span><span class="sxs-lookup"><span data-stu-id="42a54-170">For TCP, the **SO\_KEEPALIVE** socket option should be set either before the connect function ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) is called, or after the connection request is actually completed.</span></span> <span data-ttu-id="42a54-171">Si se llamó a la función de conexión de forma asincrónica, esto requiere esperar la finalización de la conexión antes de intentar establecer la opción de socket **so \_ KEEPALIVE** .</span><span class="sxs-lookup"><span data-stu-id="42a54-171">If the connect function was called asynchronously, then this requires waiting for the connection completion before trying to set the **SO\_KEEPALIVE** socket option.</span></span> <span data-ttu-id="42a54-172">Si una aplicación intenta establecer la opción de socket **so \_ KEEPALIVE** cuando una solicitud de conexión todavía está en curso, se producirá un error **en la función** MUTE y se devolverá [WSAEINVAL](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="42a54-172">If an application attempts to set the **SO\_KEEPALIVE** socket option when a connection request is still in process, the **setsockopt** function will fail and return [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="42a54-173">En Windows Server 2003, Windows XP y Windows 2000, la opción de socket **so \_ KEEPALIVE** se puede establecer con la [**función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) llamada a la función de-r cuando el socket es un estado de transición (una solicitud de conexión todavía está en curso) y un estado conocido.</span><span class="sxs-lookup"><span data-stu-id="42a54-173">On Windows Server 2003, Windows XP, and Windows 2000, the **SO\_KEEPALIVE** socket option can be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is a transitional state (a connection request is still in progress) as well as a well-known state.</span></span>

<span data-ttu-id="42a54-174">Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.</span><span class="sxs-lookup"><span data-stu-id="42a54-174">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a54-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a54-175">Requirements</span></span>



| <span data-ttu-id="42a54-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a54-176">Requirement</span></span> | <span data-ttu-id="42a54-177">Value</span><span class="sxs-lookup"><span data-stu-id="42a54-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a54-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a54-178">Minimum supported client</span></span><br/> | <span data-ttu-id="42a54-179">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="42a54-179">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="42a54-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a54-180">Minimum supported server</span></span><br/> | <span data-ttu-id="42a54-181">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42a54-181">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42a54-182">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42a54-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a54-183"><dt>Ws2def. h (incluir WinSock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42a54-183"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a54-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="42a54-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a54-185">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="42a54-185">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="42a54-186">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="42a54-186">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

<span data-ttu-id="42a54-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="42a54-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="42a54-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="42a54-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="42a54-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="42a54-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="42a54-190">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="42a54-190">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

<span data-ttu-id="42a54-191">[**SIO \_ KEEPALIVE \_ vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42a54-191">[**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="42a54-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="42a54-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="42a54-193">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="42a54-193">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
