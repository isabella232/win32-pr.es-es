---
title: Seguimiento de peligros frente a recursos de grupos de iconos
description: En el caso de los recursos no en mosaico, Direct3D puede evitar ciertas condiciones de riesgo durante la representación, pero como el seguimiento de peligros sería un nivel de mosaico para los recursos en mosaico, el seguimiento de condiciones de riesgo durante la representación de recursos en mosaico podría ser demasiado caro.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418426"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a><span data-ttu-id="e6ac2-103">Seguimiento de peligros frente a recursos de grupos de iconos</span><span class="sxs-lookup"><span data-stu-id="e6ac2-103">Hazard tracking versus tile pool resources</span></span>

<span data-ttu-id="e6ac2-104">En el caso de los recursos no en mosaico, Direct3D puede evitar ciertas condiciones de riesgo durante la representación, pero como el seguimiento de peligros sería un nivel de mosaico para los recursos en mosaico, el seguimiento de condiciones de riesgo durante la representación de recursos en mosaico podría ser demasiado caro.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-104">For non-tiled resources, Direct3D can prevent certain hazard conditions during rendering, but because hazard tracking would be at a tile level for tiled resources, tracking hazard conditions during rendering of tiled resources might be too expensive.</span></span>

<span data-ttu-id="e6ac2-105">Por ejemplo, en el caso de los recursos no en mosaico, el tiempo de ejecución no permite que se enlace ningún subrecurso dado como entrada (por ejemplo, un ShaderResourceView) y como salida (por ejemplo, un RenderTargetView) al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-105">For example, for non-tiled resources, the runtime doesn't allow any given SubResource to be bound as an input (such as a ShaderResourceView) and as an output (such as a RenderTargetView) at the same time.</span></span> <span data-ttu-id="e6ac2-106">Si se encuentra este caso, el tiempo de ejecución desenlaza la entrada.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-106">If such a case is encountered, the runtime unbinds the input.</span></span> <span data-ttu-id="e6ac2-107">Esta sobrecarga de seguimiento en tiempo de ejecución es barata y se realiza en el nivel de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-107">This tracking overhead in the runtime is cheap and is done at the SubResource level.</span></span> <span data-ttu-id="e6ac2-108">Una de las ventajas de esta sobrecarga de seguimiento es minimizar las posibilidades de que las aplicaciones dependan accidentalmente según el orden de ejecución del sombreador de hardware.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-108">One of the benefits of this tracking overhead is to minimize the chances of applications accidentally depending on hardware shader execution order.</span></span> <span data-ttu-id="e6ac2-109">El orden de ejecución del sombreador de hardware puede variar si no se trata de una unidad de procesamiento de gráficos (GPU) determinada y, en realidad, de distintas GPU.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-109">Hardware shader execution order can vary if not on a given graphics processing unit (GPU), then certainly across different GPUs.</span></span>

<span data-ttu-id="e6ac2-110">El seguimiento de cómo se enlazan los recursos puede ser demasiado caro para los recursos en mosaico porque el seguimiento se encuentra en un nivel de mosaico.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-110">Tracking how resources are bound might be too expensive for tiled resources because tracking is at a tile level.</span></span> <span data-ttu-id="e6ac2-111">Surgen nuevos problemas como, por ejemplo, la validación de los intentos de representación en un RenderTargetView con un mosaico asignado a varias áreas de la superficie simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-111">New issues arise such as possibly validating away attempts to render to an RenderTargetView with one tile mapped to multiple areas in the surface simultaneously.</span></span> <span data-ttu-id="e6ac2-112">Si este seguimiento de riesgos por mosaico es demasiado caro para el tiempo de ejecución, idealmente esto sería una opción en la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-112">If it turns out this per-tile hazard tracking is too expensive for the runtime, ideally this would at least be an option in the debug layer.</span></span>

<span data-ttu-id="e6ac2-113">Una aplicación debe informar al controlador de pantalla cuando se ha emitido una operación de lectura o escritura en un recurso en mosaico que hace referencia a la memoria del grupo de mosaicos al que también se hará referencia mediante recursos en mosaico independientes en las próximas operaciones de lectura o escritura que espera que la primera operación se complete antes de que puedan comenzar las siguientes operaciones.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-113">An application must inform the display driver when it has issued a write or read operation to a tiled resource that references tile pool memory that will also be referenced by separate tiled resources in upcoming read or write operations that it is expecting the first operation to complete before the following operations can begin.</span></span> <span data-ttu-id="e6ac2-114">Para obtener más información sobre esta condición, consulte [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-114">For more info about this condition, see [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6ac2-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6ac2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6ac2-116">Mapas en un grupo de iconos</span><span class="sxs-lookup"><span data-stu-id="e6ac2-116">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




