---
description: Los recursos de búfer de vértices administrados o de búfer de índice no se pueden declarar de forma dinámica mediante la especificación de D3DUSAGE \_ Dynamic en el momento de la creación.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed de recursos y estrategias de asignación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705257"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a><span data-ttu-id="7a452-103">Application-Managed de recursos y estrategias de asignación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7a452-103">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>

<span data-ttu-id="7a452-104">Los recursos de búfer de vértices administrados o de búfer de índice no se pueden declarar de forma dinámica mediante la especificación de D3DUSAGE \_ Dynamic en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="7a452-104">Managed vertex-buffer or index-buffer resources cannot be declared dynamic by specifying D3DUSAGE\_DYNAMIC at creation time.</span></span> <span data-ttu-id="7a452-105">Esto requeriría una copia adicional para cada modificación del contenido del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="7a452-105">This would require an additional copy for every modification to the vertex buffer contents.</span></span> <span data-ttu-id="7a452-106">Los búferes de vértices dinámicos están pensados para representar geometría dinámica y datos extraídos de árboles con particiones de espacio binario u otras estructuras de datos de visibilidad.</span><span class="sxs-lookup"><span data-stu-id="7a452-106">Dynamic vertex buffers are intended for rendering dynamic geometry and data pulled in from binary space partitioned trees or other visibility data structures.</span></span> <span data-ttu-id="7a452-107">Esto puede realizarse mediante la asignación previa de búferes del formato deseado.</span><span class="sxs-lookup"><span data-stu-id="7a452-107">This can be accomplished by pre-allocating buffers of the desired format.</span></span> <span data-ttu-id="7a452-108">A continuación, estos recursos se empaquetan para admitir las necesidades de la aplicación por parte de un administrador de recursos dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a452-108">These resources are then parceled out to support application needs by a resource manager within the application.</span></span> <span data-ttu-id="7a452-109">El número total de búferes dinámicos de vértices es pequeño porque una aplicación usará simultáneamente solo unos cuantos distintos vértices y, por tanto, solo se necesita un búfer de vértices diferente para los grandes progresos.</span><span class="sxs-lookup"><span data-stu-id="7a452-109">The total number of dynamic vertex buffers is small because an application will use simultaneously only a few different vertex strides and because a different vertex buffer is required only for unique strides.</span></span> <span data-ttu-id="7a452-110">Al administrar recursos dinámicos de esta manera, asegúrese de que las demandas de alta frecuencia de los recursos no disminuyan significativamente el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a452-110">When managing dynamic resources in this way, ensure that high-frequency demands on the resources do not significantly decrease the application's performance.</span></span>

<span data-ttu-id="7a452-111">Al usar recursos administrados por Direct3D y aplicaciones, asigne recursos administrados por la aplicación en la \_ memoria predeterminada de D3DPOOL antes de crear recursos administrados por Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7a452-111">When using resources managed by both Direct3D and applications, allocate application-managed resources in D3DPOOL\_DEFAULT memory prior to creating Direct3D-managed resources.</span></span> <span data-ttu-id="7a452-112">Esto permite al administrador de memoria mantener un recuento preciso de la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="7a452-112">This enables the memory manager to maintain an accurate count of available memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a452-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a452-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a452-114">Recursos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7a452-114">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



