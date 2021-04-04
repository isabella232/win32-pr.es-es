---
title: Limpieza de entradas del servicio de nombres
description: Una entrada de servicio de nombres debe contener información que no cambia con frecuencia.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076055"
---
# <a name="name-service-entry-cleanup"></a><span data-ttu-id="95031-103">Limpieza de entradas del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="95031-103">Name Service Entry Cleanup</span></span>

<span data-ttu-id="95031-104">Una entrada de servicio de nombres debe contener información que no cambia con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="95031-104">A name service entry should contain information that does not change frequently.</span></span> <span data-ttu-id="95031-105">Por esta razón, no incluya puntos de conexión dinámicos en los identificadores de enlace exportados porque cambiarán en cada invocación del servidor y se amontonarán en la entrada del servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="95031-105">For this reason, do not include dynamic endpoints in your exported binding handles because they will change at each invocation of the server and will clutter up your name service entry.</span></span> <span data-ttu-id="95031-106">Para quitar estos identificadores de enlace, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span><span class="sxs-lookup"><span data-stu-id="95031-106">To remove these binding handles, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span></span>

<span data-ttu-id="95031-107">Por ejemplo, una secuencia de operaciones de servidor razonable sería:</span><span class="sxs-lookup"><span data-stu-id="95031-107">For example, a reasonable sequence of server operations would be:</span></span>

<span data-ttu-id="95031-108">Para más de un transporte:</span><span class="sxs-lookup"><span data-stu-id="95031-108">For more than one transport:</span></span>

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

<span data-ttu-id="95031-109">Para colocar enlaces en el asignador de extremos:</span><span class="sxs-lookup"><span data-stu-id="95031-109">To place bindings in the endpoint mapper:</span></span>

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

<span data-ttu-id="95031-110">Para quitar los puntos de conexión de los enlaces:</span><span class="sxs-lookup"><span data-stu-id="95031-110">To remove endpoints from bindings:</span></span>

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

<span data-ttu-id="95031-111">Para agregar enlaces al servicio de nombres:</span><span class="sxs-lookup"><span data-stu-id="95031-111">To add bindings to the name service:</span></span>

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




