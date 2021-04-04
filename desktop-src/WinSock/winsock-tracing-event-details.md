---
description: Detalles de seguimiento de eventos de red Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Detalles de seguimiento de eventos de red Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278091"
---
# <a name="winsock-network-event-tracing-details"></a><span data-ttu-id="611f9-103">Detalles de seguimiento de eventos de red Winsock</span><span class="sxs-lookup"><span data-stu-id="611f9-103">Winsock Network Event Tracing Details</span></span>

<span data-ttu-id="611f9-104">A continuación se detalla cada uno de los eventos de red Winsock de los que se puede realizar un seguimiento y se describen los parámetros y la información que se registran.</span><span class="sxs-lookup"><span data-stu-id="611f9-104">The following details each of the Winsock network events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="socket-creation"></a><span data-ttu-id="611f9-105">Creación de sockets</span><span class="sxs-lookup"><span data-stu-id="611f9-105">Socket Creation</span></span>

<span data-ttu-id="611f9-106">ID. de evento = 1</span><span class="sxs-lookup"><span data-stu-id="611f9-106">Event ID = 1</span></span>

<span data-ttu-id="611f9-107">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-107">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-108">Se realiza un seguimiento de los siguientes eventos Winsock para la creación de Sockets:</span><span class="sxs-lookup"><span data-stu-id="611f9-108">The following Winsock events are traced for socket creation:</span></span>

-   <span data-ttu-id="611f9-109">Identificadores de socket creados por llamadas a las funciones [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="611f9-109">Socket handles created by calls to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) functions.</span></span>
-   <span data-ttu-id="611f9-110">Identificadores de socket aceptados en sockets de escucha.</span><span class="sxs-lookup"><span data-stu-id="611f9-110">Accepted socket handles on listening sockets.</span></span>
-   <span data-ttu-id="611f9-111">Identificadores de socket creados mediante llamadas a la función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="611f9-111">Socket handles created by calls to the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="611f9-112">Los identificadores de socket reutilizados por las llamadas a las funciones [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) o [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .</span><span class="sxs-lookup"><span data-stu-id="611f9-112">Socket handles re-used by calls to the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) or [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) functions.</span></span>

<span data-ttu-id="611f9-113">Los parámetros siguientes se registran para un evento de creación de Sockets:</span><span class="sxs-lookup"><span data-stu-id="611f9-113">The following parameters are logged for a socket creation event:</span></span>



| <span data-ttu-id="611f9-114">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-114">Parameter</span></span>                                                                                                        | <span data-ttu-id="611f9-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="611f9-117">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-117">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>             | <span data-ttu-id="611f9-119">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-119">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span><span class="sxs-lookup"><span data-stu-id="611f9-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span></span><br/>     | <span data-ttu-id="611f9-121">Tipo del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-121">The type of the socket.</span></span><br/>                                                     |
| <span data-ttu-id="611f9-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>N°</span><span class="sxs-lookup"><span data-stu-id="611f9-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocol</span></span><br/>             | <span data-ttu-id="611f9-123">Protocolo del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-123">The protocol of the socket.</span></span><br/>                                                 |
| <span data-ttu-id="611f9-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span><span class="sxs-lookup"><span data-stu-id="611f9-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span></span><br/> | <span data-ttu-id="611f9-125">IDENTIFICADOR de proceso del modo de usuario que creó el socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-125">The user-mode process ID that created the socket.</span></span><br/>                           |



 

## <a name="socket-bind"></a><span data-ttu-id="611f9-126">Enlace de socket</span><span class="sxs-lookup"><span data-stu-id="611f9-126">Socket Bind</span></span>

<span data-ttu-id="611f9-127">ID. de evento = 2 (IPv4), ID. de evento = 3 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-127">Event ID = 2 (IPv4), Event ID = 3 (IPv6)</span></span>

<span data-ttu-id="611f9-128">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-128">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-129">Se realiza un seguimiento de los siguientes eventos Winsock para una operación de enlace:</span><span class="sxs-lookup"><span data-stu-id="611f9-129">The following Winsock events are traced for a bind operation:</span></span>

-   <span data-ttu-id="611f9-130">Enlace implícito o explícito de un identificador de socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-130">Implicit or explicit binding of a socket handle.</span></span>

<span data-ttu-id="611f9-131">Los parámetros siguientes se registran para un evento de enlace:</span><span class="sxs-lookup"><span data-stu-id="611f9-131">The following parameters are logged for a bind event:</span></span>



| <span data-ttu-id="611f9-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-132">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-133">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-135">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-135">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-137">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-137">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="611f9-139">Dirección IP local.</span><span class="sxs-lookup"><span data-stu-id="611f9-139">The local IP address.</span></span><br/>                                                       |
| <span data-ttu-id="611f9-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="611f9-141">El número de puerto IP local.</span><span class="sxs-lookup"><span data-stu-id="611f9-141">The local IP port number.</span></span><br/>                                                   |
| <span data-ttu-id="611f9-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estatus</span><span class="sxs-lookup"><span data-stu-id="611f9-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="611f9-143">El código de estado o de error devuelto para la operación de enlace.</span><span class="sxs-lookup"><span data-stu-id="611f9-143">The status or error code returned for the bind operation.</span></span><br/>                   |



 

## <a name="failed-bind"></a><span data-ttu-id="611f9-144">Error de enlace</span><span class="sxs-lookup"><span data-stu-id="611f9-144">Failed Bind</span></span>

<span data-ttu-id="611f9-145">ID. de evento = 40</span><span class="sxs-lookup"><span data-stu-id="611f9-145">Event ID = 40</span></span>

<span data-ttu-id="611f9-146">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-146">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-147">Se realiza un seguimiento de los siguientes eventos Winsock para una operación de enlace con error:</span><span class="sxs-lookup"><span data-stu-id="611f9-147">The following Winsock events are traced for a failed bind operation:</span></span>

-   <span data-ttu-id="611f9-148">Enlace implícito o explícito de un identificador de socket que produce un error.</span><span class="sxs-lookup"><span data-stu-id="611f9-148">Implicit or explicit binding of a socket handle that fails.</span></span>

<span data-ttu-id="611f9-149">Los parámetros siguientes se registran para un evento de enlace con errores:</span><span class="sxs-lookup"><span data-stu-id="611f9-149">The following parameters are logged for a failed bind event:</span></span>



| <span data-ttu-id="611f9-150">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-150">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-151">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-153">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-153">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-155">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-155">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-157">Código de error devuelto para la operación de enlace con error.</span><span class="sxs-lookup"><span data-stu-id="611f9-157">The error code returned for the failing bind operation.</span></span><br/>                     |



 

## <a name="socket-connect"></a><span data-ttu-id="611f9-158">Conexión de socket</span><span class="sxs-lookup"><span data-stu-id="611f9-158">Socket Connect</span></span>

<span data-ttu-id="611f9-159">ID. de evento = 4 (IPv4), ID. de evento = 5 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-159">Event ID = 4 (IPv4), Event ID = 5 (IPv6)</span></span>

<span data-ttu-id="611f9-160">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-160">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-161">Se realiza un seguimiento de los siguientes eventos Winsock para una solicitud de operación de conexión (una llamada a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ):</span><span class="sxs-lookup"><span data-stu-id="611f9-161">The following Winsock events are traced for a connect operation request (a call to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function):</span></span>

-   <span data-ttu-id="611f9-162">Conexión de un socket a un destino para un socket orientado a la conexión o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="611f9-162">Connecting a socket to a destination for either a connection-oriented or a connectionless socket.</span></span>

<span data-ttu-id="611f9-163">Los parámetros siguientes se registran para un evento de conexión:</span><span class="sxs-lookup"><span data-stu-id="611f9-163">The following parameters are logged for a connect event:</span></span>



| <span data-ttu-id="611f9-164">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-164">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-165">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-167">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-167">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-169">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-169">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="611f9-171">Dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="611f9-171">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="611f9-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="611f9-173">El número de puerto IP remoto.</span><span class="sxs-lookup"><span data-stu-id="611f9-173">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="connect-completed"></a><span data-ttu-id="611f9-174">Conexión completada</span><span class="sxs-lookup"><span data-stu-id="611f9-174">Connect Completed</span></span>

<span data-ttu-id="611f9-175">ID. de evento = 6</span><span class="sxs-lookup"><span data-stu-id="611f9-175">Event ID = 6</span></span>

<span data-ttu-id="611f9-176">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-176">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-177">Se realiza un seguimiento de los siguientes eventos Winsock para una conexión completada:</span><span class="sxs-lookup"><span data-stu-id="611f9-177">The following Winsock events are traced for a connect completed:</span></span>

-   <span data-ttu-id="611f9-178">Se completó la operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="611f9-178">The connect operation is completed.</span></span>

<span data-ttu-id="611f9-179">Los parámetros siguientes se registran para un evento de conexión completada:</span><span class="sxs-lookup"><span data-stu-id="611f9-179">The following parameters are logged for a connect completed event:</span></span>



| <span data-ttu-id="611f9-180">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-180">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-181">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-183">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-183">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-185">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-185">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-187">Código de error devuelto para la operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="611f9-187">The error code returned for the connect operation.</span></span><br/>                          |



 

## <a name="afd-initiated-abort"></a><span data-ttu-id="611f9-188">AFD-Initiated anular</span><span class="sxs-lookup"><span data-stu-id="611f9-188">AFD-Initiated Abort</span></span>

<span data-ttu-id="611f9-189">ID. de evento = 7</span><span class="sxs-lookup"><span data-stu-id="611f9-189">Event ID = 7</span></span>

<span data-ttu-id="611f9-190">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-190">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-191">Se realiza un seguimiento de los siguientes eventos Winsock para las anulaciones iniciadas por Winsock o las operaciones de cancelación:</span><span class="sxs-lookup"><span data-stu-id="611f9-191">The following Winsock events are traced for Winsock-initiated aborts or cancel operations:</span></span>

-   <span data-ttu-id="611f9-192">Anulación debido a la recepción de datos no leídos almacenados en búfer después de cerrar.</span><span class="sxs-lookup"><span data-stu-id="611f9-192">An abort due to unread receive data buffered after close.</span></span>
-   <span data-ttu-id="611f9-193">Una anulación después de una llamada a la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con el parámetro *how* establecido en SD \_ Receive y una llamada a la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) con los datos de recepción pendientes.</span><span class="sxs-lookup"><span data-stu-id="611f9-193">An abort after a call to the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function with the *how* parameter set to SD\_RECEIVE and a call to the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function with receive data pending.</span></span>
-   <span data-ttu-id="611f9-194">Una anulación después de un error al intentar vaciar el extremo.</span><span class="sxs-lookup"><span data-stu-id="611f9-194">An abort after a failed attempt to flush the endpoint.</span></span>
-   <span data-ttu-id="611f9-195">Una anulación después de un error interno de Winsock.</span><span class="sxs-lookup"><span data-stu-id="611f9-195">An abort after an internal Winsock error occurred.</span></span>
-   <span data-ttu-id="611f9-196">Una anulación debido a una conexión con errores y la aplicación solicitó previamente que la conexión se anulara en determinadas circunstancias.</span><span class="sxs-lookup"><span data-stu-id="611f9-196">An abort due to a connection with errors and the application previously requested that the connection be aborted on certain circumstances.</span></span> <span data-ttu-id="611f9-197">Un ejemplo de este caso sería una aplicación que se establece de modo que sea \_ persistente con un tiempo de espera de cero y que todavía haya datos no confirmados en la conexión.</span><span class="sxs-lookup"><span data-stu-id="611f9-197">One example of this case would be an application that set SO\_LINGER with a timeout of zero and there is still unacknowledged data on the connection.</span></span>
-   <span data-ttu-id="611f9-198">Anulación de una conexión que no está totalmente asociada con el punto de conexión de aceptación.</span><span class="sxs-lookup"><span data-stu-id="611f9-198">An abort on a connection not fully associated with accepting endpoint.</span></span>
-   <span data-ttu-id="611f9-199">Una anulación en una llamada errónea a la función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) o [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .</span><span class="sxs-lookup"><span data-stu-id="611f9-199">An abort on a failed call to the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) or [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function.</span></span>
-   <span data-ttu-id="611f9-200">Anulación debido a una operación de recepción con errores.</span><span class="sxs-lookup"><span data-stu-id="611f9-200">An abort due to a failed receive operation.</span></span>
-   <span data-ttu-id="611f9-201">Anulación debido a un evento de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="611f9-201">An abort due to a Plug and Play event.</span></span>
-   <span data-ttu-id="611f9-202">Una anulación debido a una solicitud de vaciado con errores.</span><span class="sxs-lookup"><span data-stu-id="611f9-202">An abort due to a failed flush request.</span></span>
-   <span data-ttu-id="611f9-203">Una anulación debido a una solicitud de recepción de datos rápida con errores.</span><span class="sxs-lookup"><span data-stu-id="611f9-203">An abort due to a failed expedited data receive request.</span></span>
-   <span data-ttu-id="611f9-204">Una anulación debido a un error en una solicitud de envío.</span><span class="sxs-lookup"><span data-stu-id="611f9-204">An abort due to a failed send request.</span></span>
-   <span data-ttu-id="611f9-205">Anulación debido a una solicitud de envío cancelada.</span><span class="sxs-lookup"><span data-stu-id="611f9-205">An abort due to canceled send request.</span></span>
-   <span data-ttu-id="611f9-206">Anulación debido a que se ha cancelado la llamada a la función [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .</span><span class="sxs-lookup"><span data-stu-id="611f9-206">An abort due to a canceled called to the [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) function.</span></span>

<span data-ttu-id="611f9-207">Los parámetros siguientes se registran para una operación de anulación o cancelación iniciada por Winsock:</span><span class="sxs-lookup"><span data-stu-id="611f9-207">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="611f9-208">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-208">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-209">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-211">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-211">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-213">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-213">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Debido</span><span class="sxs-lookup"><span data-stu-id="611f9-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="611f9-215">Motivo de la operación de anulación o cancelación.</span><span class="sxs-lookup"><span data-stu-id="611f9-215">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="transport-initiated-abort"></a><span data-ttu-id="611f9-216">Transport-Initiated anular</span><span class="sxs-lookup"><span data-stu-id="611f9-216">Transport-Initiated Abort</span></span>

<span data-ttu-id="611f9-217">ID. de evento = 8</span><span class="sxs-lookup"><span data-stu-id="611f9-217">Event ID = 8</span></span>

<span data-ttu-id="611f9-218">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-218">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-219">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de anulación o cancelación iniciadas por el transporte:</span><span class="sxs-lookup"><span data-stu-id="611f9-219">The following Winsock events are traced for transport-initiated abort or cancel operations:</span></span>

-   <span data-ttu-id="611f9-220">Restablecimiento indicado por el transporte.</span><span class="sxs-lookup"><span data-stu-id="611f9-220">Reset indicated by the transport.</span></span>

<span data-ttu-id="611f9-221">Los parámetros siguientes se registran para una operación de anulación o cancelación iniciada por Winsock:</span><span class="sxs-lookup"><span data-stu-id="611f9-221">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="611f9-222">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-222">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-223">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-225">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-225">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-227">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-227">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Debido</span><span class="sxs-lookup"><span data-stu-id="611f9-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="611f9-229">Motivo de la operación de anulación o cancelación.</span><span class="sxs-lookup"><span data-stu-id="611f9-229">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="failed-send-request"></a><span data-ttu-id="611f9-230">Error de solicitud de envío</span><span class="sxs-lookup"><span data-stu-id="611f9-230">Failed Send Request</span></span>

<span data-ttu-id="611f9-231">ID. de evento = 9</span><span class="sxs-lookup"><span data-stu-id="611f9-231">Event ID = 9</span></span>

<span data-ttu-id="611f9-232">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-232">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-233">Se realiza un seguimiento de los siguientes eventos Winsock en busca de errores en las solicitudes [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :</span><span class="sxs-lookup"><span data-stu-id="611f9-233">The following Winsock events are traced for errors on [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests:</span></span>

-   <span data-ttu-id="611f9-234">Errores devueltos en solicitudes de [**envío**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) con error.</span><span class="sxs-lookup"><span data-stu-id="611f9-234">Errors returned on failed [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests.</span></span>

<span data-ttu-id="611f9-235">Los parámetros siguientes se registran para las solicitudes de envío que producen un error:</span><span class="sxs-lookup"><span data-stu-id="611f9-235">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="611f9-236">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-236">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-237">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-237">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-239">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-239">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-241">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-241">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-243">Código de error devuelto para la operación.</span><span class="sxs-lookup"><span data-stu-id="611f9-243">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a><span data-ttu-id="611f9-244">Error de solicitud WsaSendMsg</span><span class="sxs-lookup"><span data-stu-id="611f9-244">Failed WsaSendMsg Request</span></span>

<span data-ttu-id="611f9-245">ID. de evento = 10</span><span class="sxs-lookup"><span data-stu-id="611f9-245">Event ID = 10</span></span>

<span data-ttu-id="611f9-246">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-246">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-247">Se realiza un seguimiento de los siguientes eventos de Winsock en busca de errores en las solicitudes de [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="611f9-247">The following Winsock events are traced for errors on [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests:</span></span>

-   <span data-ttu-id="611f9-248">Errores devueltos en solicitudes [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) erróneas.</span><span class="sxs-lookup"><span data-stu-id="611f9-248">Errors returned on failed [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests.</span></span>

<span data-ttu-id="611f9-249">Los parámetros siguientes se registran para las solicitudes de envío que producen un error:</span><span class="sxs-lookup"><span data-stu-id="611f9-249">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="611f9-250">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-250">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-251">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-251">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-253">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-253">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-255">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-255">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-257">Código de error devuelto para la operación.</span><span class="sxs-lookup"><span data-stu-id="611f9-257">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recv-request"></a><span data-ttu-id="611f9-258">Solicitud de recepción errónea</span><span class="sxs-lookup"><span data-stu-id="611f9-258">Failed Recv Request</span></span>

<span data-ttu-id="611f9-259">ID. de evento = 11</span><span class="sxs-lookup"><span data-stu-id="611f9-259">Event ID = 11</span></span>

<span data-ttu-id="611f9-260">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-260">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-261">Se realiza un seguimiento de los siguientes eventos Winsock en busca de errores en las solicitudes [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)o [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :</span><span class="sxs-lookup"><span data-stu-id="611f9-261">The following Winsock events are traced for errors on [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), or [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) requests:</span></span>

-   <span data-ttu-id="611f9-262">Errores devueltos en solicitudes de recepción con error.</span><span class="sxs-lookup"><span data-stu-id="611f9-262">Errors returned on failed receive requests.</span></span>

<span data-ttu-id="611f9-263">Los parámetros siguientes se registran para las solicitudes de envío que producen un error:</span><span class="sxs-lookup"><span data-stu-id="611f9-263">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="611f9-264">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-264">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-265">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-265">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-267">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-267">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-269">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-269">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-271">Código de error devuelto para la operación.</span><span class="sxs-lookup"><span data-stu-id="611f9-271">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recvfrom-request"></a><span data-ttu-id="611f9-272">Error de solicitud recvfrom</span><span class="sxs-lookup"><span data-stu-id="611f9-272">Failed Recvfrom Request</span></span>

<span data-ttu-id="611f9-273">ID. de evento = 12</span><span class="sxs-lookup"><span data-stu-id="611f9-273">Event ID = 12</span></span>

<span data-ttu-id="611f9-274">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-274">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-275">Se realiza un seguimiento de los siguientes eventos de Winsock en busca de errores en las solicitudes de [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :</span><span class="sxs-lookup"><span data-stu-id="611f9-275">The following Winsock events are traced for errors on [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests:</span></span>

-   <span data-ttu-id="611f9-276">Errores devueltos en solicitudes [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) con error.</span><span class="sxs-lookup"><span data-stu-id="611f9-276">Errors returned on failed [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests.</span></span>

<span data-ttu-id="611f9-277">Los parámetros siguientes se registran para una solicitud [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) que produce un error:</span><span class="sxs-lookup"><span data-stu-id="611f9-277">The following parameters are logged for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) request that results in an error:</span></span>



| <span data-ttu-id="611f9-278">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-278">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-279">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-279">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-281">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-281">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-283">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-283">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-285">Código de error devuelto para la operación.</span><span class="sxs-lookup"><span data-stu-id="611f9-285">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="socket-close"></a><span data-ttu-id="611f9-286">Cerrar socket</span><span class="sxs-lookup"><span data-stu-id="611f9-286">Socket Close</span></span>

<span data-ttu-id="611f9-287">ID. de evento = 13</span><span class="sxs-lookup"><span data-stu-id="611f9-287">Event ID = 13</span></span>

<span data-ttu-id="611f9-288">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-288">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-289">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de cierre de socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-289">The following Winsock events are traced for socket close operations:</span></span>

-   <span data-ttu-id="611f9-290">Un identificador de socket está cerrado.</span><span class="sxs-lookup"><span data-stu-id="611f9-290">A socket handle is closed.</span></span>

<span data-ttu-id="611f9-291">Los parámetros siguientes se registran para un evento de cierre de socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-291">The following parameters are logged for a socket close event:</span></span>



| <span data-ttu-id="611f9-292">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-292">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-293">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-293">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-295">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-295">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-297">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-297">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-299">El valor devuelto para la operación de cierre del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-299">The return value for the socket close operation.</span></span><br/>                            |



 

## <a name="socket-cleanup"></a><span data-ttu-id="611f9-300">Limpieza de sockets</span><span class="sxs-lookup"><span data-stu-id="611f9-300">Socket Cleanup</span></span>

<span data-ttu-id="611f9-301">ID. de evento = 14</span><span class="sxs-lookup"><span data-stu-id="611f9-301">Event ID = 14</span></span>

<span data-ttu-id="611f9-302">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-302">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-303">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de limpieza de sockets (apagado):</span><span class="sxs-lookup"><span data-stu-id="611f9-303">The following Winsock events are traced for socket cleanup (shutdown) operations:</span></span>

-   <span data-ttu-id="611f9-304">Se llama a la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) en un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-304">The [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function is called on a socket.</span></span>
-   <span data-ttu-id="611f9-305">El transporte indica que se ha producido un error en la desconexión correcta.</span><span class="sxs-lookup"><span data-stu-id="611f9-305">The transport indicates a failed graceful disconnect.</span></span>

<span data-ttu-id="611f9-306">Los parámetros siguientes se registran para un evento de limpieza de socket (shutdown) o de cierre de socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-306">The following parameters are logged for a socket cleanup (shutdown) or socket close event:</span></span>



| <span data-ttu-id="611f9-307">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-307">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-308">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-310">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-310">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-312">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-312">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-314">El valor devuelto para la operación de limpieza de socket (shutdown).</span><span class="sxs-lookup"><span data-stu-id="611f9-314">The return value for the socket cleanup (shutdown) operation.</span></span><br/>               |



 

## <a name="socket-accept"></a><span data-ttu-id="611f9-315">Aceptación de socket</span><span class="sxs-lookup"><span data-stu-id="611f9-315">Socket Accept</span></span>

<span data-ttu-id="611f9-316">ID. de evento = 15 (IPv4), ID. de evento = 16 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-316">Event ID = 15 (IPv4), Event ID = 16 (IPv6)</span></span>

<span data-ttu-id="611f9-317">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-317">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-318">Se realiza un seguimiento de los siguientes eventos Winsock para una solicitud de función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) :</span><span class="sxs-lookup"><span data-stu-id="611f9-318">The following Winsock events are traced for an [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request:</span></span>

-   <span data-ttu-id="611f9-319">Una solicitud de función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) en un identificador de socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-319">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request on a socket handle.</span></span>

<span data-ttu-id="611f9-320">Los parámetros siguientes se registran para un evento Accept:</span><span class="sxs-lookup"><span data-stu-id="611f9-320">The following parameters are logged for an accept event:</span></span>



| <span data-ttu-id="611f9-321">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-321">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-322">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-322">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-324">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-324">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-326">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-326">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="611f9-328">Dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="611f9-328">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="611f9-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="611f9-330">El número de puerto IP remoto.</span><span class="sxs-lookup"><span data-stu-id="611f9-330">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="611f9-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estatus</span><span class="sxs-lookup"><span data-stu-id="611f9-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="611f9-332">El código de estado o de error devuelto para la operación de aceptación.</span><span class="sxs-lookup"><span data-stu-id="611f9-332">The status or error code returned for the accept operation.</span></span><br/>                 |



 

## <a name="accept-failed"></a><span data-ttu-id="611f9-333">Error de aceptación</span><span class="sxs-lookup"><span data-stu-id="611f9-333">Accept Failed</span></span>

<span data-ttu-id="611f9-334">ID. de evento = 17</span><span class="sxs-lookup"><span data-stu-id="611f9-334">Event ID = 17</span></span>

<span data-ttu-id="611f9-335">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="611f9-335">Level = 4 (Information)</span></span>

<span data-ttu-id="611f9-336">Se realiza un seguimiento de los siguientes eventos Winsock para una operación de aceptación errónea:</span><span class="sxs-lookup"><span data-stu-id="611f9-336">The following Winsock events are traced for a failed accept operation:</span></span>

-   <span data-ttu-id="611f9-337">Una solicitud [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) en un identificador de socket que produce un error.</span><span class="sxs-lookup"><span data-stu-id="611f9-337">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) request on a socket handle that fails.</span></span>

<span data-ttu-id="611f9-338">Los parámetros siguientes se registran para un evento de aceptación con errores:</span><span class="sxs-lookup"><span data-stu-id="611f9-338">The following parameters are logged for a failed accept event:</span></span>



| <span data-ttu-id="611f9-339">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-339">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-340">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-340">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-342">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-342">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-344">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-344">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-346">Código de error devuelto para la operación de aceptación con error.</span><span class="sxs-lookup"><span data-stu-id="611f9-346">The error code returned for the failing accept operation.</span></span><br/>                   |



 

## <a name="send-posted"></a><span data-ttu-id="611f9-347">Envío enviado</span><span class="sxs-lookup"><span data-stu-id="611f9-347">Send Posted</span></span>

<span data-ttu-id="611f9-348">ID. de evento = 18</span><span class="sxs-lookup"><span data-stu-id="611f9-348">Event ID = 18</span></span>

<span data-ttu-id="611f9-349">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-349">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-350">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-350">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-351">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones post de búfer de envío y recepción de socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-351">The following Winsock events are traced for socket send and receive buffer post operations:</span></span>

-   <span data-ttu-id="611f9-352">Una aplicación envía un envío.</span><span class="sxs-lookup"><span data-stu-id="611f9-352">An application posts a send.</span></span>
-   <span data-ttu-id="611f9-353">Una operación de envío se completa en Winsock.</span><span class="sxs-lookup"><span data-stu-id="611f9-353">A send operation completes to Winsock.</span></span>

<span data-ttu-id="611f9-354">Los parámetros siguientes se registran para las operaciones de envío de socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-354">The following parameters are logged for socket send operations:</span></span>



| <span data-ttu-id="611f9-355">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-355">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-356">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-356">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-358">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-358">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="611f9-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-360">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-360">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="611f9-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="611f9-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="611f9-362">Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.</span><span class="sxs-lookup"><span data-stu-id="611f9-362">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="611f9-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="611f9-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="611f9-364">Recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="611f9-364">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="611f9-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-366">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-366">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-367">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-367">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="611f9-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-369">Longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-369">The length of the buffer.</span></span> <span data-ttu-id="611f9-370">En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-370">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="611f9-371">Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-371">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="611f9-372">Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-372">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="receive-posted"></a><span data-ttu-id="611f9-373">Recepción enviada</span><span class="sxs-lookup"><span data-stu-id="611f9-373">Receive Posted</span></span>

<span data-ttu-id="611f9-374">ID. de evento = 19</span><span class="sxs-lookup"><span data-stu-id="611f9-374">Event ID = 19</span></span>

<span data-ttu-id="611f9-375">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-375">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-376">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-376">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-377">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones post de búfer de recepción de socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-377">The following Winsock events are traced for socket receive buffer post operations:</span></span>

-   <span data-ttu-id="611f9-378">Una aplicación envía una recepción.</span><span class="sxs-lookup"><span data-stu-id="611f9-378">An application posts a receive.</span></span>
-   <span data-ttu-id="611f9-379">Una operación de recepción se completa en Winsock.</span><span class="sxs-lookup"><span data-stu-id="611f9-379">A receive operation completes to Winsock.</span></span>

<span data-ttu-id="611f9-380">Los parámetros siguientes se registran para las operaciones de recepción de Sockets:</span><span class="sxs-lookup"><span data-stu-id="611f9-380">The following parameters are logged for socket receive operations:</span></span>



| <span data-ttu-id="611f9-381">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-381">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-382">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-382">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-384">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-384">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="611f9-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-386">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-386">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="611f9-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="611f9-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="611f9-388">Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.</span><span class="sxs-lookup"><span data-stu-id="611f9-388">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="611f9-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="611f9-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="611f9-390">Recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="611f9-390">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="611f9-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-392">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-392">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-393">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-393">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="611f9-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-395">Longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-395">The length of the buffer.</span></span> <span data-ttu-id="611f9-396">En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-396">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="611f9-397">Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-397">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="611f9-398">Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-398">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recvfrom-posted"></a><span data-ttu-id="611f9-399">RecvFrom enviado</span><span class="sxs-lookup"><span data-stu-id="611f9-399">RecvFrom Posted</span></span>

<span data-ttu-id="611f9-400">ID. de evento = 20</span><span class="sxs-lookup"><span data-stu-id="611f9-400">Event ID = 20</span></span>

<span data-ttu-id="611f9-401">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-401">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-402">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-402">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-403">Se realiza un seguimiento de los siguientes eventos Winsock para una operación post de búfer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) en un socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-403">The following Winsock events are traced for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="611f9-404">Una aplicación envía una operación Receive from.</span><span class="sxs-lookup"><span data-stu-id="611f9-404">An application posts a receive from operation.</span></span>

<span data-ttu-id="611f9-405">Los parámetros siguientes se registran para la operación recvfrom:</span><span class="sxs-lookup"><span data-stu-id="611f9-405">The following parameters are logged for the recvfrom operation:</span></span>



| <span data-ttu-id="611f9-406">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-406">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-407">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-407">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-409">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-409">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="611f9-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-411">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-411">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="611f9-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="611f9-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="611f9-413">Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.</span><span class="sxs-lookup"><span data-stu-id="611f9-413">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="611f9-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="611f9-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="611f9-415">Recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="611f9-415">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="611f9-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-417">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-417">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-418">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-418">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="611f9-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-420">Longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-420">The length of the buffer.</span></span> <span data-ttu-id="611f9-421">En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-421">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="611f9-422">Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-422">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="611f9-423">Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-423">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="sendto-posted"></a><span data-ttu-id="611f9-424">Enviar a enviado</span><span class="sxs-lookup"><span data-stu-id="611f9-424">SendTo Posted</span></span>

<span data-ttu-id="611f9-425">ID. de evento = 21 (IPv4), ID. de evento = 22 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-425">Event ID = 21 (IPv4), Event ID = 22 (IPv6)</span></span>

<span data-ttu-id="611f9-426">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-426">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-427">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-427">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-428">Se realiza un seguimiento de los siguientes eventos de Winsock para una operación de post de búfer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) en un socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-428">The following Winsock events are traced for a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="611f9-429">Una aplicación envía un envío desde.</span><span class="sxs-lookup"><span data-stu-id="611f9-429">An application posts a send from.</span></span>

<span data-ttu-id="611f9-430">Los parámetros siguientes se registran para la operación [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :</span><span class="sxs-lookup"><span data-stu-id="611f9-430">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation:</span></span>



| <span data-ttu-id="611f9-431">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-431">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-432">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-432">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-434">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-434">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="611f9-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-436">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-436">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="611f9-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="611f9-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="611f9-438">Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.</span><span class="sxs-lookup"><span data-stu-id="611f9-438">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="611f9-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="611f9-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="611f9-440">Recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="611f9-440">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="611f9-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-442">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-442">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-443">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-443">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="611f9-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-445">Longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-445">The length of the buffer.</span></span> <span data-ttu-id="611f9-446">En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-446">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |
| <span data-ttu-id="611f9-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="611f9-448">Dirección IP remota del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-448">The remote IP address of the socket.</span></span><br/>                                                                                            |
| <span data-ttu-id="611f9-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="611f9-450">Número de puerto IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-450">The remote IP port number of the socket.</span></span><br/>                                                                                        |



 

<span data-ttu-id="611f9-451">Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-451">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="611f9-452">Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.</span><span class="sxs-lookup"><span data-stu-id="611f9-452">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recv-completed"></a><span data-ttu-id="611f9-453">Recepción completada</span><span class="sxs-lookup"><span data-stu-id="611f9-453">Recv Completed</span></span>

<span data-ttu-id="611f9-454">ID. de evento = 23</span><span class="sxs-lookup"><span data-stu-id="611f9-454">Event ID = 23</span></span>

<span data-ttu-id="611f9-455">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-455">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-456">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-456">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-457">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de recepción de sockets completadas:</span><span class="sxs-lookup"><span data-stu-id="611f9-457">The following Winsock events are traced for socket receive completed operations:</span></span>

-   <span data-ttu-id="611f9-458">Una operación de envío se completa en el transporte.</span><span class="sxs-lookup"><span data-stu-id="611f9-458">A send operation completes to the transport.</span></span>
-   <span data-ttu-id="611f9-459">Una operación de recepción se completa en el transporte.</span><span class="sxs-lookup"><span data-stu-id="611f9-459">A receive operation completes to the transport.</span></span>

<span data-ttu-id="611f9-460">Los parámetros siguientes se registran para un envío completado o recibido:</span><span class="sxs-lookup"><span data-stu-id="611f9-460">The following parameters are logged for a send completed or receive completed:</span></span>



| <span data-ttu-id="611f9-461">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-461">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-462">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-462">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-464">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-464">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="611f9-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-466">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-466">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="611f9-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-468">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-468">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-469">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-469">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="611f9-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-471">Longitud del búfer de bytes recibido.</span><span class="sxs-lookup"><span data-stu-id="611f9-471">The length of the buffer of bytes received.</span></span> <span data-ttu-id="611f9-472">En el caso de los búferes encadenados, este parámetro es el total de bytes recibidos en todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-472">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |



 

## <a name="send-completed"></a><span data-ttu-id="611f9-473">Envío completado</span><span class="sxs-lookup"><span data-stu-id="611f9-473">Send Completed</span></span>

<span data-ttu-id="611f9-474">ID. de evento = 24</span><span class="sxs-lookup"><span data-stu-id="611f9-474">Event ID = 24</span></span>

<span data-ttu-id="611f9-475">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-475">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-476">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-476">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-477">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de envío de sockets completadas:</span><span class="sxs-lookup"><span data-stu-id="611f9-477">The following Winsock events are traced for socket send completed operations:</span></span>

-   <span data-ttu-id="611f9-478">Una operación de envío se completa en el transporte.</span><span class="sxs-lookup"><span data-stu-id="611f9-478">A send operation completes to the transport.</span></span>

<span data-ttu-id="611f9-479">Los parámetros siguientes se registran para un envío completado:</span><span class="sxs-lookup"><span data-stu-id="611f9-479">The following parameters are logged for a send completed:</span></span>



| <span data-ttu-id="611f9-480">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-480">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-481">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-481">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-483">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-483">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="611f9-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-485">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-485">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="611f9-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-487">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-487">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-488">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-488">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="611f9-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-490">Longitud del búfer de bytes enviados.</span><span class="sxs-lookup"><span data-stu-id="611f9-490">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="611f9-491">En el caso de los búferes encadenados, este parámetro es el total de bytes enviados desde todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-491">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |



 

## <a name="sendmsg-completed"></a><span data-ttu-id="611f9-492">SendMsg completado</span><span class="sxs-lookup"><span data-stu-id="611f9-492">SendMsg Completed</span></span>

<span data-ttu-id="611f9-493">ID. de evento = 25</span><span class="sxs-lookup"><span data-stu-id="611f9-493">Event ID = 25</span></span>

<span data-ttu-id="611f9-494">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-494">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-495">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-495">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-496">Se realiza un seguimiento de los siguientes eventos Winsock cuando se completa una operación post de búfer de [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) en un socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-496">The following Winsock events are traced when a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="611f9-497">Una aplicación completa una operación [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="611f9-497">An application completes a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) operation.</span></span>

<span data-ttu-id="611f9-498">Los parámetros siguientes se registran para la finalización de [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="611f9-498">The following parameters are logged for the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) completion:</span></span>



| <span data-ttu-id="611f9-499">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-499">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-500">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-500">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-502">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-502">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="611f9-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-504">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-504">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="611f9-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="611f9-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="611f9-506">Recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="611f9-506">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="611f9-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-508">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-508">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-509">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-509">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="611f9-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-511">Longitud del búfer de bytes enviados.</span><span class="sxs-lookup"><span data-stu-id="611f9-511">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="611f9-512">En el caso de los búferes encadenados, este parámetro es el total de bytes enviados desde todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-512">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="611f9-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="611f9-514">Dirección IP remota del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-514">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="611f9-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="611f9-516">Número de puerto IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-516">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="recvfrom-completed"></a><span data-ttu-id="611f9-517">RecvFrom completado</span><span class="sxs-lookup"><span data-stu-id="611f9-517">RecvFrom Completed</span></span>

<span data-ttu-id="611f9-518">ID. de evento = 26 (IPv4), ID. de evento = 27 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-518">Event ID = 26 (IPv4), Event ID = 27 (IPv6)</span></span>

<span data-ttu-id="611f9-519">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-519">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-520">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-520">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-521">Se realiza un seguimiento de los siguientes eventos Winsock cuando se completa una operación post de búfer de [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) en un socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-521">The following Winsock events are traced when a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="611f9-522">Una aplicación completa una operación [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .</span><span class="sxs-lookup"><span data-stu-id="611f9-522">An application completes a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) operation.</span></span>

<span data-ttu-id="611f9-523">Los parámetros siguientes se registran para la finalización de [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) :</span><span class="sxs-lookup"><span data-stu-id="611f9-523">The following parameters are logged for the [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) completion:</span></span>



| <span data-ttu-id="611f9-524">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-524">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-525">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-525">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-527">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-527">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="611f9-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-529">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-529">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="611f9-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="611f9-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="611f9-531">Recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="611f9-531">The buffer count.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="611f9-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-533">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-533">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-534">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-534">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="611f9-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-536">Longitud del búfer de bytes recibido.</span><span class="sxs-lookup"><span data-stu-id="611f9-536">The length of the buffer of bytes received.</span></span> <span data-ttu-id="611f9-537">En el caso de los búferes encadenados, este parámetro es el total de bytes recibidos en todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-537">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="611f9-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="611f9-539">Dirección IP remota del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-539">The remote IP address of the socket.</span></span><br/>                                                                                                     |
| <span data-ttu-id="611f9-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="611f9-541">Número de puerto IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-541">The remote IP port number of the socket.</span></span><br/>                                                                                                 |



 

## <a name="sendto-completed"></a><span data-ttu-id="611f9-542">Enviar a completado</span><span class="sxs-lookup"><span data-stu-id="611f9-542">SendTo Completed</span></span>

<span data-ttu-id="611f9-543">ID. de evento = 28</span><span class="sxs-lookup"><span data-stu-id="611f9-543">Event ID = 28</span></span>

<span data-ttu-id="611f9-544">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-544">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-545">Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="611f9-545">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="611f9-546">Se realiza un seguimiento de los siguientes eventos Winsock cuando se completa una operación de envío de búfer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) en un socket:</span><span class="sxs-lookup"><span data-stu-id="611f9-546">The following Winsock events are traced when a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="611f9-547">Una aplicación completa una operación [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) .</span><span class="sxs-lookup"><span data-stu-id="611f9-547">An application completes a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation.</span></span>

<span data-ttu-id="611f9-548">Los parámetros siguientes se registran para la finalización de [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :</span><span class="sxs-lookup"><span data-stu-id="611f9-548">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) completion:</span></span>



| <span data-ttu-id="611f9-549">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-549">Parameter</span></span>                                                                                                            | <span data-ttu-id="611f9-550">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-550">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="611f9-552">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-552">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="611f9-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="611f9-554">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-554">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="611f9-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="611f9-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="611f9-556">Recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="611f9-556">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="611f9-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer</span><span class="sxs-lookup"><span data-stu-id="611f9-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="611f9-558">Dirección virtual del búfer.</span><span class="sxs-lookup"><span data-stu-id="611f9-558">The virtual address of the buffer.</span></span> <span data-ttu-id="611f9-559">En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-559">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="611f9-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="611f9-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="611f9-561">Longitud del búfer de bytes enviados.</span><span class="sxs-lookup"><span data-stu-id="611f9-561">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="611f9-562">En el caso de los búferes encadenados, este parámetro es el total de bytes enviados desde todos los búferes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="611f9-562">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="611f9-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="611f9-564">Dirección IP remota del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-564">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="611f9-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="611f9-566">Número de puerto IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-566">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="socket-option-set"></a><span data-ttu-id="611f9-567">Conjunto de opciones de socket</span><span class="sxs-lookup"><span data-stu-id="611f9-567">Socket Option Set</span></span>

<span data-ttu-id="611f9-568">ID. de evento = 29</span><span class="sxs-lookup"><span data-stu-id="611f9-568">Event ID = 29</span></span>

<span data-ttu-id="611f9-569">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-569">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-570">Cada vez que una aplicación cambie determinados valores de opción de socket y ioctl, se registrarán los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="611f9-570">Whenever an application changes certain socket option values and Ioctls, the new values will be logged.</span></span> <span data-ttu-id="611f9-571">Las opciones registradas se pueden usar para diagnosticar un rendimiento deficiente o un comportamiento extraño en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="611f9-571">The options logged can be used to diagnose poor performance or strange behavior in applications.</span></span> <span data-ttu-id="611f9-572">Se realiza un seguimiento de los siguientes eventos Winsock para determinadas opciones de socket y ioctl:</span><span class="sxs-lookup"><span data-stu-id="611f9-572">The following Winsock events are traced for certain socket options and Ioctls:</span></span>

-   <span data-ttu-id="611f9-573">Por lo tanto, \_ SNDBUF cambia.</span><span class="sxs-lookup"><span data-stu-id="611f9-573">SO\_SNDBUF changes.</span></span>
-   <span data-ttu-id="611f9-574">Por lo tanto, \_ RCVBUF cambia.</span><span class="sxs-lookup"><span data-stu-id="611f9-574">SO\_RCVBUF changes.</span></span>
-   <span data-ttu-id="611f9-575">FIONBIO</span><span class="sxs-lookup"><span data-stu-id="611f9-575">FIONBIO</span></span>
-   <span data-ttu-id="611f9-576">SIO \_ habilitar \_ la \_ puesta en cola circular</span><span class="sxs-lookup"><span data-stu-id="611f9-576">SIO\_ENABLE\_CIRCULAR\_QUEUEING</span></span>
-   <span data-ttu-id="611f9-577">SIO \_ UDP \_ CONNRESET</span><span class="sxs-lookup"><span data-stu-id="611f9-577">SIO\_UDP\_CONNRESET</span></span>
-   <span data-ttu-id="611f9-578">\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="611f9-578">SO\_OOBINLINE</span></span>

<span data-ttu-id="611f9-579">Los parámetros siguientes se registran [**para las llamadas a la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) y que cambian cualquiera de los valores anteriores:</span><span class="sxs-lookup"><span data-stu-id="611f9-579">The following parameters are logged for [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function calls that change any of the above values:</span></span>



| <span data-ttu-id="611f9-580">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-580">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-581">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-581">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-583">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-583">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-585">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-585">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Desea</span><span class="sxs-lookup"><span data-stu-id="611f9-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span></span><br/>         | <span data-ttu-id="611f9-587">Opción de socket o IOCTL que se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="611f9-587">The socket option or Ioctl that is changed.</span></span> <br/>                                |
| <span data-ttu-id="611f9-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="611f9-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span><br/>             | <span data-ttu-id="611f9-589">Nuevo valor de la opción de socket o ioctl.</span><span class="sxs-lookup"><span data-stu-id="611f9-589">The new value for the socket option or Ioctl.</span></span> <br/>                              |



 

## <a name="selectpoll-posted"></a><span data-ttu-id="611f9-590">Seleccionar/sondeo publicado</span><span class="sxs-lookup"><span data-stu-id="611f9-590">Select/Poll Posted</span></span>

<span data-ttu-id="611f9-591">ID. de evento = 30</span><span class="sxs-lookup"><span data-stu-id="611f9-591">Event ID = 30</span></span>

<span data-ttu-id="611f9-592">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-592">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-593">Se realiza un seguimiento de los siguientes eventos Winsock cuando una aplicación llama a la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="611f9-593">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="611f9-594">La aplicación envía una solicitud [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="611f9-594">Application posts a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) request.</span></span>

<span data-ttu-id="611f9-595">Los parámetros siguientes se registran para los eventos [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="611f9-595">The following parameters are logged for [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) events:</span></span>



| <span data-ttu-id="611f9-596">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-596">Parameter</span></span>                                                                                                        | <span data-ttu-id="611f9-597">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-597">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="611f9-599">IDENTIFICADOR del proceso propietario.</span><span class="sxs-lookup"><span data-stu-id="611f9-599">The owning process ID.</span></span><br/>                                                                              |
| <span data-ttu-id="611f9-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span><span class="sxs-lookup"><span data-stu-id="611f9-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span></span><br/> | <span data-ttu-id="611f9-601">Número de identificadores pasados por la aplicación (solo válido en el evento de inicio).</span><span class="sxs-lookup"><span data-stu-id="611f9-601">The number of handles passed in by the application (only valid on the initiating event).</span></span><br/>            |
| <span data-ttu-id="611f9-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Super</span><span class="sxs-lookup"><span data-stu-id="611f9-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span></span><br/>                 | <span data-ttu-id="611f9-603">Tiempo máximo de espera de la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="611f9-603">The maximum time for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function to wait.</span></span><br/> |



 

## <a name="selectpoll-completed"></a><span data-ttu-id="611f9-604">Selección/sondeo completado</span><span class="sxs-lookup"><span data-stu-id="611f9-604">Select/Poll Completed</span></span>

<span data-ttu-id="611f9-605">ID. de evento = 31</span><span class="sxs-lookup"><span data-stu-id="611f9-605">Event ID = 31</span></span>

<span data-ttu-id="611f9-606">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-606">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-607">Se realiza un seguimiento de los siguientes eventos Winsock cuando una aplicación llama a la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="611f9-607">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="611f9-608">Winsock completa una llamada [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="611f9-608">Winsock completes a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) call.</span></span>

<span data-ttu-id="611f9-609">Los parámetros siguientes se registran cuando se completa una operación [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="611f9-609">The following parameters are logged when a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation completes:</span></span>



| <span data-ttu-id="611f9-610">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-610">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-611">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-611">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-613">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-613">The kernel EPROCESS structure address for the process.</span></span><br/>                                              |
| <span data-ttu-id="611f9-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-615">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-615">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                         |
| <span data-ttu-id="611f9-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span><span class="sxs-lookup"><span data-stu-id="611f9-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="611f9-617">Código de error devuelto para la operación [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="611f9-617">The error code returned for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation.</span></span><br/> |



 

## <a name="wsaeventselect"></a><span data-ttu-id="611f9-618">WSAEventSelect</span><span class="sxs-lookup"><span data-stu-id="611f9-618">WSAEventSelect</span></span>

<span data-ttu-id="611f9-619">ID. de evento = 32</span><span class="sxs-lookup"><span data-stu-id="611f9-619">Event ID = 32</span></span>

<span data-ttu-id="611f9-620">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-620">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-621">Se realiza un seguimiento de los siguientes eventos Winsock cuando una aplicación llama a la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :</span><span class="sxs-lookup"><span data-stu-id="611f9-621">The following Winsock events are traced when an application calls the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function:</span></span>

-   <span data-ttu-id="611f9-622">Registra la máscara de eventos pasada en la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="611f9-622">Log the event mask passed in the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

<span data-ttu-id="611f9-623">Los parámetros siguientes se registran para las llamadas de función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :</span><span class="sxs-lookup"><span data-stu-id="611f9-623">The following parameters are logged for [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function calls:</span></span>



| <span data-ttu-id="611f9-624">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-624">Parameter</span></span>                                                                                                | <span data-ttu-id="611f9-625">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-625">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>         | <span data-ttu-id="611f9-627">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-627">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>     | <span data-ttu-id="611f9-629">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-629">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span><span class="sxs-lookup"><span data-stu-id="611f9-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span></span><br/> | <span data-ttu-id="611f9-631">El valor de la máscara de eventos.</span><span class="sxs-lookup"><span data-stu-id="611f9-631">The value for the event mask.</span></span> <br/>                                              |



 

## <a name="dropped-datagram"></a><span data-ttu-id="611f9-632">Datagrama quitado</span><span class="sxs-lookup"><span data-stu-id="611f9-632">Dropped Datagram</span></span>

<span data-ttu-id="611f9-633">ID. de evento = 33 (IPv4), ID. de evento = 34 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-633">Event ID = 33 (IPv4), Event ID = 34 (IPv6)</span></span>

<span data-ttu-id="611f9-634">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-634">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-635">Para ayudar a diagnosticar problemas relacionados con las aplicaciones de datagramas, se realiza un seguimiento de los siguientes eventos de Winsock:</span><span class="sxs-lookup"><span data-stu-id="611f9-635">To help diagnose issues around datagram applications, the following Winsock events are traced:</span></span>

-   <span data-ttu-id="611f9-636">Cuando llega un datagrama y se quita en el espacio de búfer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="611f9-636">When a datagram arrives and it is dropped do to insufficient buffer space.</span></span>
-   <span data-ttu-id="611f9-637">En un datagrama conectado, si los datos llegan de un origen que no es el destino conectado.</span><span class="sxs-lookup"><span data-stu-id="611f9-637">On a connected datagram, if data arrives from a source other than connected destination.</span></span>

<span data-ttu-id="611f9-638">Los parámetros siguientes se registran para los datagramas que se han quitado:</span><span class="sxs-lookup"><span data-stu-id="611f9-638">The following parameters are logged for dropped datagrams:</span></span>



| <span data-ttu-id="611f9-639">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-639">Parameter</span></span>                                                                                                    | <span data-ttu-id="611f9-640">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-640">Description</span></span>                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>             | <span data-ttu-id="611f9-642">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-642">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>         | <span data-ttu-id="611f9-644">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-644">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span><span class="sxs-lookup"><span data-stu-id="611f9-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span></span><br/> | <span data-ttu-id="611f9-646">Tamaño del paquete que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="611f9-646">The size of the packet that was dropped.</span></span> <br/>                                   |
| <span data-ttu-id="611f9-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>             | <span data-ttu-id="611f9-648">Dirección IP del origen del paquete.</span><span class="sxs-lookup"><span data-stu-id="611f9-648">The IP address of the source of the packet.</span></span> <br/>                                |
| <span data-ttu-id="611f9-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                         | <span data-ttu-id="611f9-650">Número de puerto IP del origen del paquete.</span><span class="sxs-lookup"><span data-stu-id="611f9-650">The IP port number of the source of the packet.</span></span><br/>                             |
| <span data-ttu-id="611f9-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Debido</span><span class="sxs-lookup"><span data-stu-id="611f9-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>                 | <span data-ttu-id="611f9-652">El código de error o la razón por la que se quitó el paquete.</span><span class="sxs-lookup"><span data-stu-id="611f9-652">The error code or reason the packet was dropped.</span></span><br/>                            |



 

## <a name="connection-indicated"></a><span data-ttu-id="611f9-653">Conexión indicada</span><span class="sxs-lookup"><span data-stu-id="611f9-653">Connection Indicated</span></span>

<span data-ttu-id="611f9-654">ID. de evento = 35 (IPv4), ID. de evento = 36 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-654">Event ID = 35 (IPv4), Event ID = 36 (IPv6)</span></span>

<span data-ttu-id="611f9-655">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-655">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-656">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones indicadas para la conexión:</span><span class="sxs-lookup"><span data-stu-id="611f9-656">The following Winsock events are traced for connection indicated operations:</span></span>

-   <span data-ttu-id="611f9-657">Una aplicación recibe una solicitud de conexión.</span><span class="sxs-lookup"><span data-stu-id="611f9-657">An application receives a connection request.</span></span>

<span data-ttu-id="611f9-658">Los parámetros siguientes se registran para las conexiones indicadas desde los eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="611f9-658">The following parameters are logged for connections indicated from transport events:</span></span>



| <span data-ttu-id="611f9-659">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-659">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-660">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-660">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-662">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-662">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-664">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-664">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="611f9-666">Dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="611f9-666">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="611f9-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="611f9-668">El número de puerto IP remoto.</span><span class="sxs-lookup"><span data-stu-id="611f9-668">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="data-indicated"></a><span data-ttu-id="611f9-669">Datos indicados</span><span class="sxs-lookup"><span data-stu-id="611f9-669">Data Indicated</span></span>

<span data-ttu-id="611f9-670">ID. de evento = 37</span><span class="sxs-lookup"><span data-stu-id="611f9-670">Event ID = 37</span></span>

<span data-ttu-id="611f9-671">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-671">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-672">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones indicadas:</span><span class="sxs-lookup"><span data-stu-id="611f9-672">The following Winsock events are traced for data indicated operations:</span></span>

-   <span data-ttu-id="611f9-673">Una aplicación recibe datos en un socket conectado.</span><span class="sxs-lookup"><span data-stu-id="611f9-673">An application receives data on a connected socket.</span></span>

<span data-ttu-id="611f9-674">Los parámetros siguientes se registran para los datos indicados en los eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="611f9-674">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="611f9-675">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-675">Parameter</span></span>                                                                                                                        | <span data-ttu-id="611f9-676">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-676">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="611f9-678">IDENTIFICADOR del proceso propietario.</span><span class="sxs-lookup"><span data-stu-id="611f9-678">The owning process ID.</span></span><br/>                                                      |
| <span data-ttu-id="611f9-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="611f9-680">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-680">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados</span><span class="sxs-lookup"><span data-stu-id="611f9-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="611f9-682">Número de bytes recibidos en el socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-682">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="data-indicated-from-transport"></a><span data-ttu-id="611f9-683">Datos indicados desde el transporte</span><span class="sxs-lookup"><span data-stu-id="611f9-683">Data Indicated from Transport</span></span>

<span data-ttu-id="611f9-684">ID. de evento = 38 (IPv4), ID. de evento = 39 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="611f9-684">Event ID = 38 (IPv4), Event ID = 39 (IPv6)</span></span>

<span data-ttu-id="611f9-685">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-685">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-686">Se realiza un seguimiento de los siguientes eventos Winsock para los datos indicados en las operaciones de transporte:</span><span class="sxs-lookup"><span data-stu-id="611f9-686">The following Winsock events are traced for data indicated from transport operations:</span></span>

-   <span data-ttu-id="611f9-687">Una aplicación envía una solicitud de recepción y recibe datos.</span><span class="sxs-lookup"><span data-stu-id="611f9-687">An application posts a receive request and receives data.</span></span>

<span data-ttu-id="611f9-688">Los parámetros siguientes se registran para los datos indicados en los eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="611f9-688">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="611f9-689">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-689">Parameter</span></span>                                                                                                                        | <span data-ttu-id="611f9-690">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-690">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="611f9-692">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-692">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="611f9-694">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-694">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="611f9-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección</span><span class="sxs-lookup"><span data-stu-id="611f9-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                                 | <span data-ttu-id="611f9-696">Dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="611f9-696">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="611f9-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla</span><span class="sxs-lookup"><span data-stu-id="611f9-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                             | <span data-ttu-id="611f9-698">El número de puerto IP remoto.</span><span class="sxs-lookup"><span data-stu-id="611f9-698">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="611f9-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados</span><span class="sxs-lookup"><span data-stu-id="611f9-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="611f9-700">Número de bytes recibidos en el socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-700">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a><span data-ttu-id="611f9-701">Desconexión indicada del transporte</span><span class="sxs-lookup"><span data-stu-id="611f9-701">Disconnect Indicated from Transport</span></span>

<span data-ttu-id="611f9-702">ID. de evento = 41</span><span class="sxs-lookup"><span data-stu-id="611f9-702">Event ID = 41</span></span>

<span data-ttu-id="611f9-703">Nivel = 5 (detallado)</span><span class="sxs-lookup"><span data-stu-id="611f9-703">Level = 5 (Verbose)</span></span>

<span data-ttu-id="611f9-704">Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de desconexión indicadas:</span><span class="sxs-lookup"><span data-stu-id="611f9-704">The following Winsock events are traced for disconnect indicated operations:</span></span>

-   <span data-ttu-id="611f9-705">Una aplicación recibe una indicación de desconexión.</span><span class="sxs-lookup"><span data-stu-id="611f9-705">An application receives a disconnect indication.</span></span>

<span data-ttu-id="611f9-706">Los parámetros siguientes se registran para la desconexión indicada en los eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="611f9-706">The following parameters are logged for disconnect indicated from transport events:</span></span>



| <span data-ttu-id="611f9-707">Parámetro</span><span class="sxs-lookup"><span data-stu-id="611f9-707">Parameter</span></span>                                                                                            | <span data-ttu-id="611f9-708">Descripción</span><span class="sxs-lookup"><span data-stu-id="611f9-708">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="611f9-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese</span><span class="sxs-lookup"><span data-stu-id="611f9-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="611f9-710">Dirección de la estructura del EPROCESS de kernel para el proceso.</span><span class="sxs-lookup"><span data-stu-id="611f9-710">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="611f9-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="611f9-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="611f9-712">Dirección del socket del kernel Winsock utilizada como identificador único de un socket.</span><span class="sxs-lookup"><span data-stu-id="611f9-712">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="611f9-713">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="611f9-713">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="611f9-714">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="611f9-714">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="611f9-715">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="611f9-715">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="611f9-716">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="611f9-716">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="611f9-717">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="611f9-717">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
