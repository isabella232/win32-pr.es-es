---
title: Inicialización del enrutador
description: La información de configuración del enrutador, los administradores de enrutadores y los protocolos/clientes de enrutamiento se divide en información global y por interfaz, y se almacena en el registro y en el archivo de libreta de teléfonos del enrutador. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- enrutadores RRAS, inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772583"
---
# <a name="router-initialization"></a><span data-ttu-id="720c4-104">Inicialización del enrutador</span><span class="sxs-lookup"><span data-stu-id="720c4-104">Router Initialization</span></span>

<span data-ttu-id="720c4-105">La información de configuración del enrutador, los administradores de enrutadores y los protocolos/clientes de enrutamiento se divide en información global y por interfaz, y se almacena en el registro y en el archivo de libreta de teléfonos del enrutador. pbk.</span><span class="sxs-lookup"><span data-stu-id="720c4-105">Configuration information for the router, the router managers and the routing protocols/clients is divided into global information and per interface information and is stored in the registry and the router's phone-book file, Router.pbk.</span></span>

<span data-ttu-id="720c4-106">Cuando se inicia el proceso del enrutador, DIM (Dynamic interface Manager) lee la configuración del enrutador del registro.</span><span class="sxs-lookup"><span data-stu-id="720c4-106">When the router process starts, DIM (Dynamic Interface Manager) reads the router configuration from the registry.</span></span> <span data-ttu-id="720c4-107">DIM crea las interfaces especificadas por la información de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="720c4-107">DIM creates the interfaces that are specified by the interface information.</span></span>

<span data-ttu-id="720c4-108">DIM también recupera la información global del administrador de enrutador.</span><span class="sxs-lookup"><span data-stu-id="720c4-108">DIM also retrieves the global router manager information.</span></span> <span data-ttu-id="720c4-109">DIM inicia los administradores de enrutadores que corresponden a esta información y los pasa a la información.</span><span class="sxs-lookup"><span data-stu-id="720c4-109">DIM starts the router managers that correspond to this information, and passes them the information.</span></span> <span data-ttu-id="720c4-110">Por ejemplo, si DIM busca información global para el administrador de enrutadores IP en el registro, DIM inicia el administrador de enrutadores IP y le pasa la información global.</span><span class="sxs-lookup"><span data-stu-id="720c4-110">For example, if DIM finds global information for the IP router manager in the registry, DIM starts the IP router manager and passes it the global information.</span></span> <span data-ttu-id="720c4-111">Si no hay información global en el registro para un administrador de enrutador determinado, la dimensión no inicia ese administrador de enrutador.</span><span class="sxs-lookup"><span data-stu-id="720c4-111">If no global information is present in the registry for a particular router manager, DIM does not start that router manager.</span></span>

<span data-ttu-id="720c4-112">Los administradores de enrutadores examinan la información global recibida de DIM.</span><span class="sxs-lookup"><span data-stu-id="720c4-112">The router managers examine the global information received from DIM.</span></span> <span data-ttu-id="720c4-113">Si el administrador de enrutadores encuentra información específica de un cliente determinado dentro de la información global, el administrador de enrutador carga el archivo DLL para el cliente (por ejemplo IpNAT.dll) e inicializa el cliente llamando a las funciones [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) y [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) del cliente.</span><span class="sxs-lookup"><span data-stu-id="720c4-113">If the router manager finds information specific to a particular client within the global information, the router manager loads the DLL for the client (for example IpNAT.dll) and initializes the client by calling the client's [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) and [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) functions.</span></span> <span data-ttu-id="720c4-114">El administrador de enrutadores pasa la información global específica del cliente al cliente en la llamada a [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span><span class="sxs-lookup"><span data-stu-id="720c4-114">The router manager passes the client-specific global information to the client in the call to [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span></span>

<span data-ttu-id="720c4-115">En cada fase, la información que se pasa a la siguiente entidad es opaca en la entidad que lo precede.</span><span class="sxs-lookup"><span data-stu-id="720c4-115">At each stage, the information being passed to the next entity is opaque to the entity preceding it.</span></span> <span data-ttu-id="720c4-116">Es decir, la dimensión no interpreta la información global para el administrador de enrutadores IP, más allá del hecho de que la información está pensada para el administrador de enrutadores IP.</span><span class="sxs-lookup"><span data-stu-id="720c4-116">That is, DIM does not interpret the global information for the IP Router Manager, beyond the fact that the information is meant for the IP Router Manager.</span></span> <span data-ttu-id="720c4-117">Del mismo modo, el administrador de enrutamiento IP no interpreta la información específica de OSPF más allá del hecho de que es información de OSPF.</span><span class="sxs-lookup"><span data-stu-id="720c4-117">Similarly, the IP Router Manager does not interpret the OSPF specific information beyond the fact that it is OSPF information.</span></span>

 

 




