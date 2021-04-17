---
description: En la tabla siguiente se resumen algunas de las opciones de socket para Windows Sockets 2.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opciones de socket y ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716630"
---
# <a name="socket-options-and-ioctls"></a><span data-ttu-id="81cf2-103">Opciones de socket y ioctl</span><span class="sxs-lookup"><span data-stu-id="81cf2-103">Socket Options and IOCTLs</span></span>

<span data-ttu-id="81cf2-104">En la tabla siguiente se resumen algunas de las opciones de socket para Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="81cf2-104">Some of the socket options for Windows Sockets 2 are summarized in the following table.</span></span> <span data-ttu-id="81cf2-105">En la sección 4, en [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) y/o [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)), se proporciona información más detallada.</span><span class="sxs-lookup"><span data-stu-id="81cf2-105">More detailed information is provided in section 4 under [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span></span> <span data-ttu-id="81cf2-106">Hay otras nuevas opciones de socket específicas del protocolo que se pueden encontrar en el anexo Protocol-Specific.</span><span class="sxs-lookup"><span data-stu-id="81cf2-106">There are other new protocol-specific socket options which can be found in the Protocol-Specific Annex.</span></span> <span data-ttu-id="81cf2-107">Puede encontrar una lista completa de [**las opciones de socket**](socket-options.md) para Windows Sockets en la referencia de Winsock.</span><span class="sxs-lookup"><span data-stu-id="81cf2-107">A complete list of [**Socket Options**](socket-options.md) for Windows Sockets are available in the Winsock reference.</span></span>

<span data-ttu-id="81cf2-108">Para obtener un resumen de algunos de los ioctl de Winsock, consulte [Summary of socket ioctl opcodesing](summary-of-socket-ioctl-opcodes-2.md).</span><span class="sxs-lookup"><span data-stu-id="81cf2-108">For a a summary of some of the Winsock Ioctls, see [Summary of Socket Ioctl Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span></span> <span data-ttu-id="81cf2-109">Puede encontrar una lista completa de los [**ioctl de Winsock**](winsock-ioctls.md) en la referencia de Winsock.</span><span class="sxs-lookup"><span data-stu-id="81cf2-109">A complete list of [**Winsock IOCTLs**](winsock-ioctls.md) are available in the Winsock reference.</span></span>

## <a name="summary-of-common-socket-options"></a><span data-ttu-id="81cf2-110">Resumen de opciones de socket comunes</span><span class="sxs-lookup"><span data-stu-id="81cf2-110">Summary of Common Socket Options</span></span>

<span data-ttu-id="81cf2-111">Un proveedor de servicios Winsock debe reconocer todas estas opciones, y (para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) devolverá los valores de plausible para cada uno.</span><span class="sxs-lookup"><span data-stu-id="81cf2-111">A Winsock service provider must recognize all of these options, and (for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) return plausible values for each.</span></span> <span data-ttu-id="81cf2-112">En la tabla siguiente se muestra el valor predeterminado de cada opción.</span><span class="sxs-lookup"><span data-stu-id="81cf2-112">The default value for each option is shown in the following table.</span></span>

<span data-ttu-id="81cf2-113">Value</span><span class="sxs-lookup"><span data-stu-id="81cf2-113">Value</span></span>

<span data-ttu-id="81cf2-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="81cf2-114">Type</span></span>

<span data-ttu-id="81cf2-115">Significado</span><span class="sxs-lookup"><span data-stu-id="81cf2-115">Meaning</span></span>

<span data-ttu-id="81cf2-116">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="81cf2-116">Default</span></span>

<span data-ttu-id="81cf2-117">Nota</span><span class="sxs-lookup"><span data-stu-id="81cf2-117">Note</span></span>

<span data-ttu-id="81cf2-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN</span><span class="sxs-lookup"><span data-stu-id="81cf2-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO\_ACCEPTCONN</span></span>

<span data-ttu-id="81cf2-119">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-119">BOOL</span></span>

<span data-ttu-id="81cf2-120">El socket está escuchando.</span><span class="sxs-lookup"><span data-stu-id="81cf2-120">Socket is listening.</span></span>

<span data-ttu-id="81cf2-121">FALSE, a menos que se haya realizado un [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="81cf2-121">FALSE unless a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) has been performed.</span></span>

<span data-ttu-id="81cf2-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_difundir</span><span class="sxs-lookup"><span data-stu-id="81cf2-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO\_BROADCAST</span></span>

<span data-ttu-id="81cf2-123">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-123">BOOL</span></span>

<span data-ttu-id="81cf2-124">Socket está configurado para la transmisión y recepción de mensajes de difusión.</span><span class="sxs-lookup"><span data-stu-id="81cf2-124">Socket is configured for the transmission and receipt of broadcast messages.</span></span>

<span data-ttu-id="81cf2-125">false</span><span class="sxs-lookup"><span data-stu-id="81cf2-125">FALSE</span></span>

<span data-ttu-id="81cf2-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>\_depurar</span><span class="sxs-lookup"><span data-stu-id="81cf2-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>SO\_DEBUG</span></span>

<span data-ttu-id="81cf2-127">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-127">BOOL</span></span>

<span data-ttu-id="81cf2-128">La depuración está habilitada.</span><span class="sxs-lookup"><span data-stu-id="81cf2-128">Debugging is enabled.</span></span>

<span data-ttu-id="81cf2-129">false</span><span class="sxs-lookup"><span data-stu-id="81cf2-129">FALSE</span></span>

<span data-ttu-id="81cf2-130">Configur</span><span class="sxs-lookup"><span data-stu-id="81cf2-130">(i)</span></span>

<span data-ttu-id="81cf2-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER</span><span class="sxs-lookup"><span data-stu-id="81cf2-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>SO\_DONTLINGER</span></span>

<span data-ttu-id="81cf2-132">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-132">BOOL</span></span>

<span data-ttu-id="81cf2-133">Si es true, la \_ opción de permanencia está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="81cf2-133">If true, the SO\_LINGER option is disabled.</span></span>

<span data-ttu-id="81cf2-134">TRUE</span><span class="sxs-lookup"><span data-stu-id="81cf2-134">TRUE</span></span>

<span data-ttu-id="81cf2-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="81cf2-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO\_DONTROUTE</span></span>

<span data-ttu-id="81cf2-136">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-136">BOOL</span></span>

<span data-ttu-id="81cf2-137">El enrutamiento está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="81cf2-137">Routing is disabled.</span></span> <span data-ttu-id="81cf2-138">Se realiza correctamente, pero se omite en los \_ sockets de AF inet; produce un error en los \_ sockets de AF inet6 con [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="81cf2-138">Succeeds but is ignored on AF\_INET sockets; fails on AF\_INET6 sockets with [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="81cf2-139">No se admite en sockets ATM (se produce un error).</span><span class="sxs-lookup"><span data-stu-id="81cf2-139">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="81cf2-140">false</span><span class="sxs-lookup"><span data-stu-id="81cf2-140">FALSE</span></span>

<span data-ttu-id="81cf2-141">Configur</span><span class="sxs-lookup"><span data-stu-id="81cf2-141">(i)</span></span>

<span data-ttu-id="81cf2-142"><span id="SO_ERROR"></span><span id="so_error"></span>\_error</span><span class="sxs-lookup"><span data-stu-id="81cf2-142"><span id="SO_ERROR"></span><span id="so_error"></span>SO\_ERROR</span></span>

<span data-ttu-id="81cf2-143">int</span><span class="sxs-lookup"><span data-stu-id="81cf2-143">int</span></span>

<span data-ttu-id="81cf2-144">Recupera el estado de error y borra.</span><span class="sxs-lookup"><span data-stu-id="81cf2-144">Retrieves error status and clear.</span></span>

<span data-ttu-id="81cf2-145">0</span><span class="sxs-lookup"><span data-stu-id="81cf2-145">0</span></span>

<span data-ttu-id="81cf2-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_identificador de grupo \_</span><span class="sxs-lookup"><span data-stu-id="81cf2-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO\_GROUP\_ID</span></span>

<span data-ttu-id="81cf2-147">GROUP</span><span class="sxs-lookup"><span data-stu-id="81cf2-147">GROUP</span></span>

<span data-ttu-id="81cf2-148">Reservado.</span><span class="sxs-lookup"><span data-stu-id="81cf2-148">Reserved.</span></span>

<span data-ttu-id="81cf2-149">NULL</span><span class="sxs-lookup"><span data-stu-id="81cf2-149">NULL</span></span>

<span data-ttu-id="81cf2-150">Obtener solo</span><span class="sxs-lookup"><span data-stu-id="81cf2-150">Get only</span></span>

<span data-ttu-id="81cf2-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_prioridad de grupo \_</span><span class="sxs-lookup"><span data-stu-id="81cf2-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO\_GROUP\_PRIORITY</span></span>

<span data-ttu-id="81cf2-152">int</span><span class="sxs-lookup"><span data-stu-id="81cf2-152">int</span></span>

<span data-ttu-id="81cf2-153">Reservado.</span><span class="sxs-lookup"><span data-stu-id="81cf2-153">Reserved.</span></span>

<span data-ttu-id="81cf2-154">0</span><span class="sxs-lookup"><span data-stu-id="81cf2-154">0</span></span>

[<span data-ttu-id="81cf2-155">**\_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="81cf2-155">**SO\_KEEPALIVE**</span></span>](so-keepalive.md)

<span data-ttu-id="81cf2-156">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-156">BOOL</span></span>

<span data-ttu-id="81cf2-157">Se están enviando Keepalives.</span><span class="sxs-lookup"><span data-stu-id="81cf2-157">Keepalives are being sent.</span></span> <span data-ttu-id="81cf2-158">No se admite en sockets ATM (se produce un error).</span><span class="sxs-lookup"><span data-stu-id="81cf2-158">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="81cf2-159">false</span><span class="sxs-lookup"><span data-stu-id="81cf2-159">FALSE</span></span>

<span data-ttu-id="81cf2-160">Configur</span><span class="sxs-lookup"><span data-stu-id="81cf2-160">(i)</span></span>

<span data-ttu-id="81cf2-161"><span id="SO_LINGER"></span><span id="so_linger"></span>por tanto, \_ permanencia</span><span class="sxs-lookup"><span data-stu-id="81cf2-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO\_LINGER</span></span>

<span data-ttu-id="81cf2-162">Permanencia de estructura</span><span class="sxs-lookup"><span data-stu-id="81cf2-162">Structure linger</span></span>

<span data-ttu-id="81cf2-163">Devuelve las opciones de permanencia actual.</span><span class="sxs-lookup"><span data-stu-id="81cf2-163">Returns the current linger options.</span></span>

<span data-ttu-id="81cf2-164">l \_ OnOff es 0</span><span class="sxs-lookup"><span data-stu-id="81cf2-164">l\_onoff is 0</span></span>

<span data-ttu-id="81cf2-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_tamaño de \_ mensaje \_ máximo</span><span class="sxs-lookup"><span data-stu-id="81cf2-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO\_MAX\_MSG\_SIZE</span></span>

<span data-ttu-id="81cf2-166">int</span><span class="sxs-lookup"><span data-stu-id="81cf2-166">int</span></span>

<span data-ttu-id="81cf2-167">Tamaño máximo de salida de un mensaje para los tipos de sockets de mensajes.</span><span class="sxs-lookup"><span data-stu-id="81cf2-167">Maximum outbound size of a message for message socket types.</span></span> <span data-ttu-id="81cf2-168">No hay ninguna disposición para determinar el tamaño máximo de los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="81cf2-168">There is no provision to determine the maximum inbound message size.</span></span> <span data-ttu-id="81cf2-169">No tiene ningún significado para los sockets orientados a flujos.</span><span class="sxs-lookup"><span data-stu-id="81cf2-169">Has no meaning for stream-oriented sockets.</span></span>

<span data-ttu-id="81cf2-170">Dependiente de la implementación</span><span class="sxs-lookup"><span data-stu-id="81cf2-170">Implementation dependent</span></span>

<span data-ttu-id="81cf2-171">Obtener solo</span><span class="sxs-lookup"><span data-stu-id="81cf2-171">Get only</span></span>

<span data-ttu-id="81cf2-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="81cf2-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO\_OOBINLINE</span></span>

<span data-ttu-id="81cf2-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-173">BOOL</span></span>

<span data-ttu-id="81cf2-174">Los datos OOB se reciben en el flujo de datos normal.</span><span class="sxs-lookup"><span data-stu-id="81cf2-174">OOB data is being received in the normal data stream.</span></span>

<span data-ttu-id="81cf2-175">false</span><span class="sxs-lookup"><span data-stu-id="81cf2-175">FALSE</span></span>

<span data-ttu-id="81cf2-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_Protocolo \_ INFOW</span><span class="sxs-lookup"><span data-stu-id="81cf2-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO\_PROTOCOL\_INFOW</span></span>

<span data-ttu-id="81cf2-177">[ **\_ información de WSAPROTOCOL** de estructura](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span><span class="sxs-lookup"><span data-stu-id="81cf2-177">structure [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span></span>

<span data-ttu-id="81cf2-178">Descripción de la información de protocolo para el protocolo que está enlazado a este socket.</span><span class="sxs-lookup"><span data-stu-id="81cf2-178">Description of protocol information for the protocol that is bound to this socket.</span></span>

<span data-ttu-id="81cf2-179">Dependiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="81cf2-179">Protocol dependent</span></span>

<span data-ttu-id="81cf2-180">Obtener solo</span><span class="sxs-lookup"><span data-stu-id="81cf2-180">Get only</span></span>

<span data-ttu-id="81cf2-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF</span><span class="sxs-lookup"><span data-stu-id="81cf2-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO\_RCVBUF</span></span>

<span data-ttu-id="81cf2-182">int</span><span class="sxs-lookup"><span data-stu-id="81cf2-182">int</span></span>

<span data-ttu-id="81cf2-183">Espacio total de búfer por socket reservado para las recepciones.</span><span class="sxs-lookup"><span data-stu-id="81cf2-183">The total per-socket buffer space reserved for receives.</span></span> <span data-ttu-id="81cf2-184">Esto no está relacionado con \_ \_ \_ el tamaño máximo del mensaje y no se corresponde necesariamente con el tamaño de la ventana de recepción de TCP.</span><span class="sxs-lookup"><span data-stu-id="81cf2-184">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of the TCP receive window.</span></span>

<span data-ttu-id="81cf2-185">Dependiente de la implementación</span><span class="sxs-lookup"><span data-stu-id="81cf2-185">Implementation dependent</span></span>

<span data-ttu-id="81cf2-186">Configur</span><span class="sxs-lookup"><span data-stu-id="81cf2-186">(i)</span></span>

<span data-ttu-id="81cf2-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="81cf2-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO\_REUSEADDR</span></span>

<span data-ttu-id="81cf2-188">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-188">BOOL</span></span>

<span data-ttu-id="81cf2-189">Otros usuarios pueden usar la dirección a la que está enlazado este socket.</span><span class="sxs-lookup"><span data-stu-id="81cf2-189">The address to which this socket is bound can be used by others.</span></span> <span data-ttu-id="81cf2-190">No es aplicable en sockets ATM.</span><span class="sxs-lookup"><span data-stu-id="81cf2-190">Not applicable on ATM sockets.</span></span>

<span data-ttu-id="81cf2-191">false</span><span class="sxs-lookup"><span data-stu-id="81cf2-191">FALSE</span></span>

<span data-ttu-id="81cf2-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF</span><span class="sxs-lookup"><span data-stu-id="81cf2-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO\_SNDBUF</span></span>

<span data-ttu-id="81cf2-193">int</span><span class="sxs-lookup"><span data-stu-id="81cf2-193">int</span></span>

<span data-ttu-id="81cf2-194">Espacio total de búfer por socket reservado para los envíos.</span><span class="sxs-lookup"><span data-stu-id="81cf2-194">The total per-socket buffer space reserved for sends.</span></span> <span data-ttu-id="81cf2-195">Esto no está relacionado con \_ \_ \_ el tamaño máximo del mensaje y no se corresponde necesariamente con el tamaño de una ventana de envío TCP.</span><span class="sxs-lookup"><span data-stu-id="81cf2-195">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of a TCP send window.</span></span>

<span data-ttu-id="81cf2-196">Dependiente de la implementación</span><span class="sxs-lookup"><span data-stu-id="81cf2-196">Implementation dependent</span></span>

<span data-ttu-id="81cf2-197">Configur</span><span class="sxs-lookup"><span data-stu-id="81cf2-197">(i)</span></span>

<span data-ttu-id="81cf2-198"><span id="SO_TYPE"></span><span id="so_type"></span>\_Escriba</span><span class="sxs-lookup"><span data-stu-id="81cf2-198"><span id="SO_TYPE"></span><span id="so_type"></span>SO\_TYPE</span></span>

<span data-ttu-id="81cf2-199">int</span><span class="sxs-lookup"><span data-stu-id="81cf2-199">int</span></span>

<span data-ttu-id="81cf2-200">Tipo del socket (por ejemplo, SOCK \_ Stream).</span><span class="sxs-lookup"><span data-stu-id="81cf2-200">The type of the socket (for example, SOCK\_STREAM).</span></span>

<span data-ttu-id="81cf2-201">Tal como se creó a través de socket.</span><span class="sxs-lookup"><span data-stu-id="81cf2-201">As created through socket.</span></span>

<span data-ttu-id="81cf2-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>configuración de PVD \_</span><span class="sxs-lookup"><span data-stu-id="81cf2-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD\_CONFIG</span></span>

<span data-ttu-id="81cf2-203">char FAR \*</span><span class="sxs-lookup"><span data-stu-id="81cf2-203">char FAR \*</span></span>

<span data-ttu-id="81cf2-204">Objeto de estructura de datos opaco que contiene información de configuración del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="81cf2-204">An opaque data structure object containing configuration information of the service provider.</span></span>

<span data-ttu-id="81cf2-205">Dependiente de la implementación</span><span class="sxs-lookup"><span data-stu-id="81cf2-205">Implementation dependent</span></span>

<span data-ttu-id="81cf2-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>retardo de TCP \_</span><span class="sxs-lookup"><span data-stu-id="81cf2-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP\_NODELAY</span></span>

<span data-ttu-id="81cf2-207">BOOL</span><span class="sxs-lookup"><span data-stu-id="81cf2-207">BOOL</span></span>

<span data-ttu-id="81cf2-208">Deshabilita el algoritmo de Nagle para la fusión de envíos.</span><span class="sxs-lookup"><span data-stu-id="81cf2-208">Disables the Nagle algorithm for send coalescing.</span></span>

<span data-ttu-id="81cf2-209">Dependiente de la implementación</span><span class="sxs-lookup"><span data-stu-id="81cf2-209">Implementation dependent</span></span>

<span data-ttu-id="81cf2-210">(i) un proveedor de servicios puede omitir esta opción de forma silenciosa en [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) y devolver un valor constante para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), o puede aceptar un valor para **WSPSetSockOpt** y devolver el valor correspondiente en **WSPGetSockOpt** sin usar el valor de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="81cf2-210">(i) A service provider may silently ignore this option on [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) and return a constant value for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), or it may accept a value for **WSPSetSockOpt** and return the corresponding value in **WSPGetSockOpt** without using the value in any way.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="81cf2-211">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81cf2-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81cf2-212">**Opciones de socket**</span><span class="sxs-lookup"><span data-stu-id="81cf2-212">**Socket Options**</span></span>](socket-options.md)
</dt> <dt>

[<span data-ttu-id="81cf2-213">**\_Opciones de socket de socket sol**</span><span class="sxs-lookup"><span data-stu-id="81cf2-213">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="81cf2-214">**\_Opciones de socket TCP de IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="81cf2-214">**IPPROTO\_TCP Socket Options**</span></span>](ipproto-tcp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="81cf2-215">**\_Opciones de socket UDP de IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="81cf2-215">**IPPROTO\_UDP Socket Options**</span></span>](ipproto-udp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="81cf2-216">**Ioctl de Winsock**</span><span class="sxs-lookup"><span data-stu-id="81cf2-216">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
