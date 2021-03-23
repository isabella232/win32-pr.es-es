---
title: Tablas de descriptores
description: Una tabla de descriptores es lógicamente una matriz de descriptores.
ms.assetid: 5faf294f-acd5-4b39-92f4-1d6b2abe3040
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10414f8458006029f3279203e949b43410911fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103672"
---
# <a name="descriptor-tables"></a><span data-ttu-id="1f293-103">Tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="1f293-103">Descriptor Tables</span></span>

<span data-ttu-id="1f293-104">Una tabla de descriptores es lógicamente una matriz de descriptores.</span><span class="sxs-lookup"><span data-stu-id="1f293-104">A descriptor table is logically an array of descriptors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1f293-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1f293-105">In this section</span></span>



| <span data-ttu-id="1f293-106">Tema</span><span class="sxs-lookup"><span data-stu-id="1f293-106">Topic</span></span>                                                                                 | <span data-ttu-id="1f293-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f293-107">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f293-108">Información general sobre tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="1f293-108">Descriptor Tables Overview</span></span>](descriptor-tables-overview.md)<br/>               | <span data-ttu-id="1f293-109">Cada tabla de descriptores almacena descriptores de uno o más tipos: SRVs, UAVe, CBVs y Samplers.</span><span class="sxs-lookup"><span data-stu-id="1f293-109">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="1f293-110">Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="1f293-110">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span><br/> |
| [<span data-ttu-id="1f293-111">Usar tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="1f293-111">Using Descriptor Tables</span></span>](using-descriptor-tables.md)<br/>                     | <span data-ttu-id="1f293-112">Las tablas de descriptores, cada una de las cuales identifican un intervalo en un montón de descriptores, se enlazan en las ranuras definidas por la firma raíz actual en una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="1f293-112">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span> <br/>                                                               |
| [<span data-ttu-id="1f293-113">Uso avanzado de las tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="1f293-113">Advanced Use of Descriptor Tables</span></span>](advanced-use-of-descriptor-tables.md)<br/> | <span data-ttu-id="1f293-114">En las secciones siguientes se proporciona información sobre el uso avanzado de las tablas de descriptores.</span><span class="sxs-lookup"><span data-stu-id="1f293-114">The following sections provide information about the advanced use of descriptor tables.</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="1f293-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f293-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f293-116">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="1f293-116">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="1f293-117">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="1f293-117">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="1f293-118">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="1f293-118">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





