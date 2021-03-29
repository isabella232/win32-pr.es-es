---
title: Acerca de la interfaz de protocolo de enrutamiento
description: En la siguiente documentación se describe la integración de protocolos de enrutamiento de terceros en el servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, interfaz de protocolo de enrutamiento
- RRAS del servicio de enrutamiento y acceso remoto, interfaz de protocolo de enrutamiento, descripción
- Interfaz de protocolo de enrutamiento RRAS
- Interfaz de protocolo de enrutamiento RRAS, descrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777376"
---
# <a name="about-routing-protocol-interface"></a><span data-ttu-id="244b4-107">Acerca de la interfaz de protocolo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="244b4-107">About Routing Protocol Interface</span></span>

<span data-ttu-id="244b4-108">En la siguiente documentación se describe la integración de protocolos de enrutamiento de terceros en el servicio de enrutamiento y acceso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="244b4-108">The following documentation describes the integration of third-party routing protocols into the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="244b4-109">RRAS es una característica de Windows que actúa como enrutador de varios protocolos.</span><span class="sxs-lookup"><span data-stu-id="244b4-109">RRAS is a feature of Windows that acts as a multi-protocol router.</span></span> <span data-ttu-id="244b4-110">RRAS define la interfaz entre el administrador de enrutadores y el protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="244b4-110">RRAS defines the interface between the router manager and the routing protocol.</span></span> <span data-ttu-id="244b4-111">El protocolo de enrutamiento se implementa en una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="244b4-111">The routing protocol is implemented in a dynamic link library (DLL).</span></span>

<span data-ttu-id="244b4-112">Use esta interfaz para implementar protocolos de enrutamiento, como IGRP, NLSP y BGP, como archivos dll de modo de usuario que funcionan con RRAS.</span><span class="sxs-lookup"><span data-stu-id="244b4-112">Use this interface to implement routing protocols, such as IGRP, NLSP, and BGP, as user-mode DLLs that work with RRAS.</span></span>

<span data-ttu-id="244b4-113">En esta documentación se describen los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="244b4-113">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="244b4-114">Adaptadores</span><span class="sxs-lookup"><span data-stu-id="244b4-114">Adapters</span></span>](adapters.md)
-   [<span data-ttu-id="244b4-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="244b4-115">Interfaces</span></span>](interfaces.md)
-   [<span data-ttu-id="244b4-116">Rutas estáticas y autoestáticas</span><span class="sxs-lookup"><span data-stu-id="244b4-116">Static and Autostatic Routes</span></span>](static-and-autostatic-routes.md)

 

 




