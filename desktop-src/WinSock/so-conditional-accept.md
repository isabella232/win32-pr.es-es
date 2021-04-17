---
description: Está diseñado para permitir que una aplicación decida si aceptar o no una conexión entrante en un socket de escucha.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Opción de socket de SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706828"
---
# <a name="so_conditional_accept-socket-option"></a><span data-ttu-id="eac9d-103">\_Opción de \_ socket de aceptación condicional</span><span class="sxs-lookup"><span data-stu-id="eac9d-103">SO\_CONDITIONAL\_ACCEPT socket option</span></span>

<span data-ttu-id="eac9d-104">La opción de socket de **\_ \_ aceptación condicional** está diseñada para permitir que una aplicación decida si acepta o no una conexión entrante en un socket de escucha.</span><span class="sxs-lookup"><span data-stu-id="eac9d-104">The **SO\_CONDITIONAL\_ACCEPT** socket option is designed to allow an application to decide whether or not to accept an incoming connection on a listening socket.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="eac9d-105">Valor de opción de socket</span><span class="sxs-lookup"><span data-stu-id="eac9d-105">Socket option value</span></span>

<span data-ttu-id="eac9d-106">La constante que representa esta opción de socket es 0x3002.</span><span class="sxs-lookup"><span data-stu-id="eac9d-106">The constant that represents this socket option is 0x3002.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac9d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eac9d-107">Syntax</span></span>


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="eac9d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eac9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eac9d-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="eac9d-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac9d-110">Un descriptor que identifica el socket.</span><span class="sxs-lookup"><span data-stu-id="eac9d-110">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="eac9d-111">*nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="eac9d-111">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac9d-112">Nivel en el que se define la opción.</span><span class="sxs-lookup"><span data-stu-id="eac9d-112">The level at which the option is defined.</span></span> <span data-ttu-id="eac9d-113">Use **el \_ socket sol** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="eac9d-113">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="eac9d-114">*optname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eac9d-114">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac9d-115">Opción de socket para la que se va a establecer el valor.</span><span class="sxs-lookup"><span data-stu-id="eac9d-115">The socket option for which the value is to be set.</span></span> <span data-ttu-id="eac9d-116">Use **la \_ \_ aceptación condicional** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="eac9d-116">Use **SO\_CONDITIONAL\_ACCEPT** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="eac9d-117">*optval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eac9d-117">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eac9d-118">Puntero al búfer que contiene el valor de la opción que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="eac9d-118">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="eac9d-119">Este parámetro debe apuntar al búfer igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="eac9d-119">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="eac9d-120">Este valor se trata como un valor booleano con 0 que se usa para indicar **false** (deshabilitado) y un valor distinto de cero para indicar **true** (habilitado).</span><span class="sxs-lookup"><span data-stu-id="eac9d-120">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="eac9d-121">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eac9d-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eac9d-122">Puntero al tamaño, en bytes, del búfer *optval* .</span><span class="sxs-lookup"><span data-stu-id="eac9d-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="eac9d-123">Este tamaño debe ser igual o mayor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="eac9d-123">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eac9d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eac9d-124">Return value</span></span>

<span data-ttu-id="eac9d-125">Si la operación se completa [**correctamente, el valor de la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="eac9d-125">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="eac9d-126">Si se produce un error en la operación, se devuelve un valor de error de SOCKET \_ y un código de error específico se puede recuperar llamando a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="eac9d-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="eac9d-127">Código de error</span><span class="sxs-lookup"><span data-stu-id="eac9d-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="eac9d-128">Significado</span><span class="sxs-lookup"><span data-stu-id="eac9d-128">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eac9d-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="eac9d-130">Se debe realizar una llamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) correcta antes de usar esta función.</span><span class="sxs-lookup"><span data-stu-id="eac9d-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="eac9d-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="eac9d-132">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="eac9d-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="eac9d-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="eac9d-134">Uno de los parámetros *optval* o *optlen* apunta a la memoria que no está en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="eac9d-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="eac9d-135">Este error también se devuelve si el valor al que apunta el parámetro *optlen* es menor que el tamaño de un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="eac9d-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="eac9d-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="eac9d-137">Hay una llamada de bloqueo de Windows Sockets 1,1 en curso, o el proveedor de servicios sigue procesando una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="eac9d-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="eac9d-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="eac9d-139">El parámetro *LEVEL* es desconocido o no es válido.</span><span class="sxs-lookup"><span data-stu-id="eac9d-139">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="eac9d-140">Este error también se devuelve si el socket ya estaba en un estado de escucha.</span><span class="sxs-lookup"><span data-stu-id="eac9d-140">This error is also returned if the socket was already in a listening state.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="eac9d-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="eac9d-142">La opción es desconocida o no es compatible con la familia del protocolo indicada.</span><span class="sxs-lookup"><span data-stu-id="eac9d-142">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="eac9d-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="eac9d-144">El descriptor no es un socket.</span><span class="sxs-lookup"><span data-stu-id="eac9d-144">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="eac9d-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eac9d-145">Remarks</span></span>

<span data-ttu-id="eac9d-146">La [**función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la función de la llamada con la opción de socket de **\_ \_ aceptación condicional** permite a una aplicación decidir si aceptar o no una conexión entrante en un socket de escucha.</span><span class="sxs-lookup"><span data-stu-id="eac9d-146">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to decide whether or not to accept an incoming connection on a listening socket.</span></span> <span data-ttu-id="eac9d-147">De forma predeterminada, la opción de aceptación condicional de un socket está deshabilitada (establecida en **false**).</span><span class="sxs-lookup"><span data-stu-id="eac9d-147">The conditional accept option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="eac9d-148">Cuando se habilita esta opción de socket, la pila TCP no acepta conexiones automáticamente.</span><span class="sxs-lookup"><span data-stu-id="eac9d-148">When this socket option is enabled, the TCP stack does not automatically accept connections.</span></span> <span data-ttu-id="eac9d-149">Espera a que la aplicación indique que acepta la conexión a través de la devolución de llamada de aceptación condicional registrada con la función [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) .</span><span class="sxs-lookup"><span data-stu-id="eac9d-149">It waits for the application to indicate that it accepts the connection via the conditional accept callback registered with [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function.</span></span> <span data-ttu-id="eac9d-150">Una vez que se recibe una solicitud de conexión, Winsock invoca la devolución de llamada de aceptación condicional registrada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eac9d-150">Once a connection request is received, Winsock invokes the conditional accept callback registered by the application.</span></span> <span data-ttu-id="eac9d-151">Solo si la devolución de llamada de aceptación condicional devuelve **CF \_ Accept** , Winsock notificará al transporte que acepte la conexión por completo.</span><span class="sxs-lookup"><span data-stu-id="eac9d-151">Only when the conditional accept callback returns **CF\_ACCEPT** will Winsock notify the transport to fully accept the connection.</span></span>

<span data-ttu-id="eac9d-152">Cuando la opción de socket de **\_ \_ aceptación condicional** está establecida en habilitado (establecido en **true**), esto tiene varios efectos secundarios en el socket:</span><span class="sxs-lookup"><span data-stu-id="eac9d-152">When the **SO\_CONDITIONAL\_ACCEPT** socket option is set to enabled (set to **TRUE**), this has several side effects on the socket:</span></span>

-   <span data-ttu-id="eac9d-153">Esto deshabilita las defensas integradas de protección contra ataques SYN de la pila TCP, ya que la aplicación ahora toma la propiedad de aceptar conexiones.</span><span class="sxs-lookup"><span data-stu-id="eac9d-153">This disables the TCP stack's built-in SYN attack protection defenses, since the application is now taking ownership of accepting connections.</span></span>
-   <span data-ttu-id="eac9d-154">De este modo, se deshabilita el trabajo pendiente de escucha, ya que no se aceptan conexiones en nombre de un socket de escucha.</span><span class="sxs-lookup"><span data-stu-id="eac9d-154">This effectively disables the listen backlog since connections aren't accepted on behalf of a listening socket.</span></span> <span data-ttu-id="eac9d-155">Una conexión nunca se acepta por completo hasta que la aplicación acepta por completo el uso del mecanismo de **\_ aceptación de CF** .</span><span class="sxs-lookup"><span data-stu-id="eac9d-155">A connection is never fully accepted until the application fully accepts using the **CF\_ACCEPT** mechanism.</span></span>
-   <span data-ttu-id="eac9d-156">Esto también significa que la aplicación se encarga de estar siempre en un estado para controlar fácilmente las devoluciones de llamada de aceptación para aceptar la conexión.</span><span class="sxs-lookup"><span data-stu-id="eac9d-156">This also means the application take care to always be in a state to readily handle the accept callbacks to accept the connection.</span></span> <span data-ttu-id="eac9d-157">Si la aplicación está ocupada en otro procesamiento, el cliente puede agotar el tiempo de espera antes de que la aplicación acepte realmente la conexión.</span><span class="sxs-lookup"><span data-stu-id="eac9d-157">If the application is busy doing other processing, then the client side may time out before the application actually accepts the connection.</span></span> <span data-ttu-id="eac9d-158">Esto conduce a una experiencia de cliente deficiente.</span><span class="sxs-lookup"><span data-stu-id="eac9d-158">This leads to a poor client experience.</span></span>

<span data-ttu-id="eac9d-159">Por lo general, el motivo principal por el que las aplicaciones usan la aceptación condicional es inspeccionar la dirección IP de origen o el puerto utilizado por el cliente que se conecta y, a continuación, decidir si aceptar o rechazar la conexión.</span><span class="sxs-lookup"><span data-stu-id="eac9d-159">Generally, the main reason applications use conditional accept is to inspect the source IP address or port used by the connecting client and then decide to accept or reject the connection.</span></span> <span data-ttu-id="eac9d-160">Sin embargo, es probable que las aplicaciones funcionen mejor si la \_ \_ opción de aceptación condicional no está habilitada y la aplicación permite que la pila TCP y el trabajo pendiente de escucha funcionen según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="eac9d-160">However, applications are likely to perform better if the SO\_CONDITIONAL\_ACCEPT option is not enabled and the application allows the TCP stack and the listen backlog to work as expected.</span></span> <span data-ttu-id="eac9d-161">Después, cuando la aplicación controla la conexión aceptada, si se trata de un puerto o una dirección de origen IP incorrectos, la aplicación solo puede cerrar el socket.</span><span class="sxs-lookup"><span data-stu-id="eac9d-161">Then when the application handles the accepted connection, if it is from a improper IP source address or port, the application can just close the socket.</span></span> <span data-ttu-id="eac9d-162">El inconveniente de seguridad de este comportamiento es que ahora el cliente ha confirmado que la aplicación está escuchando en una dirección IP y un puerto, ya que ha cerrado forzosamente la conexión previamente aceptada.</span><span class="sxs-lookup"><span data-stu-id="eac9d-162">The security drawback to this behavior is that now the client has confirmation that the application is listening on an IP address and port since it forcefully closed the previously accepted connection.</span></span> <span data-ttu-id="eac9d-163">Sin embargo, las desventajas de habilitar la **\_ \_ aceptación condicional** generalmente superan esta limitación.</span><span class="sxs-lookup"><span data-stu-id="eac9d-163">However, the drawbacks to enabling **SO\_CONDITIONAL\_ACCEPT** generally outweigh this limitation.</span></span>

<span data-ttu-id="eac9d-164">La función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) llamada con la opción de socket de **\_ \_ aceptación condicional** permite a una aplicación recuperar el estado actual de la opción de aceptación condicional, aunque esta característica no se utiliza normalmente.</span><span class="sxs-lookup"><span data-stu-id="eac9d-164">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to retrieve the current state of the conditional accept option, although this is feature not normally used.</span></span> <span data-ttu-id="eac9d-165">Si una aplicación necesita habilitar la aceptación condicional en un socket, simplemente llama a [**la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la función de llamada para habilitar la opción.</span><span class="sxs-lookup"><span data-stu-id="eac9d-165">If an application needs to enable conditional accept on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="eac9d-166">Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.</span><span class="sxs-lookup"><span data-stu-id="eac9d-166">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac9d-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eac9d-167">Requirements</span></span>



| <span data-ttu-id="eac9d-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac9d-168">Requirement</span></span> | <span data-ttu-id="eac9d-169">Value</span><span class="sxs-lookup"><span data-stu-id="eac9d-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac9d-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eac9d-170">Minimum supported client</span></span><br/> | <span data-ttu-id="eac9d-171">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eac9d-171">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eac9d-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eac9d-172">Minimum supported server</span></span><br/> | <span data-ttu-id="eac9d-173">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eac9d-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eac9d-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eac9d-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="eac9d-175"><dt>Ws2def. h (incluir WinSock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eac9d-175"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac9d-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="eac9d-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac9d-177">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="eac9d-177">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="eac9d-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="eac9d-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="eac9d-179">**WSAAccept**</span><span class="sxs-lookup"><span data-stu-id="eac9d-179">**WSAAccept**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




