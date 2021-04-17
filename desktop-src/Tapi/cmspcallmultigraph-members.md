---
description: Miembros de CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Miembros de CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677946"
---
# <a name="cmspcallmultigraph-members"></a><span data-ttu-id="c65dc-103">Miembros de CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="c65dc-103">CMSPCallMultiGraph Members</span></span>

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

<span data-ttu-id="c65dc-104">Los bloques de espera almacenan la información sobre la espera registrada en el grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c65dc-104">The wait blocks store the information about the wait registered to the thread pool.</span></span> <span data-ttu-id="c65dc-105">Incluye los identificadores de espera devueltos por la llamada [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) y un puntero a la estructura de contexto.</span><span class="sxs-lookup"><span data-stu-id="c65dc-105">It includes the wait handles returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) call and a pointer to the context structure.</span></span> <span data-ttu-id="c65dc-106">Cada bloque de la matriz es para un gráfico en uno de los objetos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="c65dc-106">Each block in the array is for a graph in one of the stream objects.</span></span> <span data-ttu-id="c65dc-107">El desplazamiento de un bloque en esta matriz es el mismo que el desplazamiento de la secuencia que posee el gráfico.</span><span class="sxs-lookup"><span data-stu-id="c65dc-107">The offset of a block in this array is the same as the offset of the stream that owns the graph.</span></span>

 

 
