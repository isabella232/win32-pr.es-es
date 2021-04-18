---
title: Ordenar (ADSI)
description: Un cliente puede solicitar a un servidor que ordene el conjunto de resultados.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "105656303"
---
# <a name="sorting-adsi"></a><span data-ttu-id="2285b-103">Ordenar (ADSI)</span><span class="sxs-lookup"><span data-stu-id="2285b-103">Sorting (ADSI)</span></span>

<span data-ttu-id="2285b-104">Un cliente puede solicitar a un servidor que ordene el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2285b-104">A client can request a server to sort the result set.</span></span> <span data-ttu-id="2285b-105">Puede especificar:</span><span class="sxs-lookup"><span data-stu-id="2285b-105">You can specify:</span></span>

-   <span data-ttu-id="2285b-106">Criterio de ordenación: se puede especificar el criterio de ordenación ascendente o descendente.</span><span class="sxs-lookup"><span data-stu-id="2285b-106">Sort order: Either ascending or descending sort order can be specified.</span></span>
-   <span data-ttu-id="2285b-107">Atributos de ordenación: se pueden especificar varios atributos en una cadena de ordenación.</span><span class="sxs-lookup"><span data-stu-id="2285b-107">Sort attributes: Multiple attributes can be specified in a sort string.</span></span> <span data-ttu-id="2285b-108">Por ejemplo, ordene por Apellido y luego por nombre.</span><span class="sxs-lookup"><span data-stu-id="2285b-108">For example, sort by Last Name, then First Name.</span></span>

<span data-ttu-id="2285b-109">Al especificar el criterio de ordenación, debe intentar usar uno de los atributos indizados.</span><span class="sxs-lookup"><span data-stu-id="2285b-109">When you specify sort order, you should try to use one of the indexed attributes.</span></span> <span data-ttu-id="2285b-110">De lo contrario, el servidor debe calcular un conjunto de resultados completo antes de enviarlo al cliente.</span><span class="sxs-lookup"><span data-stu-id="2285b-110">Otherwise, the server must calculate a complete result set before sending it to the client.</span></span> <span data-ttu-id="2285b-111">Esto es así incluso si ha solicitado una búsqueda paginada y ha especificado un tamaño de página.</span><span class="sxs-lookup"><span data-stu-id="2285b-111">This is true even if you have requested a paged search and specified a page size.</span></span>

> [!Note]  
> <span data-ttu-id="2285b-112">No todos los servidores de directorio admiten varias ordenaciones de atributos o criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="2285b-112">Not all directory servers support multiple attribute sorts or sort order.</span></span>

 

 

 




