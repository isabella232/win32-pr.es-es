---
title: Terminología de enlace RPC esencial
description: Para ayudar mejor en una explicación del proceso de conexión de cliente/servidor, es útil conocer los siguientes términos.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- RPC llamada a procedimiento remoto, descripción, enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078202"
---
# <a name="essential-rpc-binding-terminology"></a><span data-ttu-id="442aa-104">Terminología de enlace RPC esencial</span><span class="sxs-lookup"><span data-stu-id="442aa-104">Essential RPC Binding Terminology</span></span>

<span data-ttu-id="442aa-105">Para ayudar mejor en una explicación del proceso de conexión de cliente/servidor, es útil conocer los siguientes términos.</span><span class="sxs-lookup"><span data-stu-id="442aa-105">To better aid in a discussion of the client/server connection process, it is helpful to know the following terms.</span></span>

## <a name="parameters"></a><span data-ttu-id="442aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="442aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="442aa-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Secuencia de protocolos</span><span class="sxs-lookup"><span data-stu-id="442aa-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protocol Sequence</span></span>
</dt> <dd>

<span data-ttu-id="442aa-108">Cuando los sistemas operativos de red se comunican entre sí, deben escuchar y hablar del mismo idioma.</span><span class="sxs-lookup"><span data-stu-id="442aa-108">When network operating systems communicate with each other, they must listen and speak the same language.</span></span> <span data-ttu-id="442aa-109">Estos idiomas se denominan *secuencias de protocolo*.</span><span class="sxs-lookup"><span data-stu-id="442aa-109">These languages are called *protocol sequences*.</span></span> <span data-ttu-id="442aa-110">Los programas de cliente y servidor deben usar secuencias de protocolo que admita la red que los conecta.</span><span class="sxs-lookup"><span data-stu-id="442aa-110">Client and server programs must use protocol sequences that the network connecting them supports.</span></span> <span data-ttu-id="442aa-111">Microsoft RPC admite una variedad de secuencias de protocolos.</span><span class="sxs-lookup"><span data-stu-id="442aa-111">Microsoft RPC supports a variety of protocol sequences.</span></span> <span data-ttu-id="442aa-112">Para obtener más información, consulte [seleccionar una secuencia de protocolo](selecting-a-protocol-sequence.md), [especificar secuencias de protocolos](specifying-protocol-sequences.md)y [**punto de conexión**](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="442aa-112">For details, see [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md), [Specifying Protocol Sequences](specifying-protocol-sequences.md), and [**endpoint**](/windows/desktop/Midl/endpoint).</span></span>

</dd> <dt>

<span data-ttu-id="442aa-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Equipo host del servidor o sistema host del servidor</span><span class="sxs-lookup"><span data-stu-id="442aa-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer or Server Host System</span></span>
</dt> <dd>

<span data-ttu-id="442aa-114">El programa de servidor se ejecuta en el equipo host del servidor.</span><span class="sxs-lookup"><span data-stu-id="442aa-114">The server program runs on the server host computer.</span></span> <span data-ttu-id="442aa-115">Sin embargo, en muchos casos, la informática cliente/servidor hace referencia tanto al programa de servidor como al equipo host del servidor como "servidor".</span><span class="sxs-lookup"><span data-stu-id="442aa-115">However, much literature on client/server computing refers to both the server program and the server host computer as the "server."</span></span> <span data-ttu-id="442aa-116">El resultado es que no siempre es evidente lo que se está analizando.</span><span class="sxs-lookup"><span data-stu-id="442aa-116">The result is that it is not always clear which is being discussed.</span></span>

</dd> <dt>

<span data-ttu-id="442aa-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales</span><span class="sxs-lookup"><span data-stu-id="442aa-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span>
</dt> <dd>

<span data-ttu-id="442aa-118">Los programas de servidor escuchan un puerto o un grupo de puertos en el equipo host del servidor para las solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="442aa-118">Server programs listen to a port or a group of ports on the server host computer for client requests.</span></span> <span data-ttu-id="442aa-119">Los sistemas host de servidor mantienen una base de datos de estos puertos, que se denominan puntos de conexión en RPC.</span><span class="sxs-lookup"><span data-stu-id="442aa-119">Server host systems maintain a database of these ports, which are called endpoints in RPC.</span></span> <span data-ttu-id="442aa-120">La base de datos se denomina asignación de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="442aa-120">The database is called the endpoint map.</span></span>

</dd> <dt>

<span data-ttu-id="442aa-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Enlace</span><span class="sxs-lookup"><span data-stu-id="442aa-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Binding</span></span>
</dt> <dd>

<span data-ttu-id="442aa-122">Los programas cliente crean un enlace con el servidor para establecer una sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="442aa-122">Client programs create a binding to the server to establish a communication session.</span></span> <span data-ttu-id="442aa-123">Un enlace contiene toda la información que las aplicaciones cliente necesitan para crear la sesión.</span><span class="sxs-lookup"><span data-stu-id="442aa-123">A binding contains all of the information the client applications needs to create the session.</span></span>

</dd> </dl>

 

 