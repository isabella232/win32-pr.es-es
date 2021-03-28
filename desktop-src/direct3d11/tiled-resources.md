---
title: Recursos en mosaico
description: Los recursos en mosaico pueden considerarse como recursos lógicos de gran tamaño que utilizan pequeñas cantidades de memoria física.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903176"
---
# <a name="tiled-resources"></a><span data-ttu-id="c5ed4-103">Recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="c5ed4-103">Tiled resources</span></span>

<span data-ttu-id="c5ed4-104">Los recursos en mosaico pueden considerarse como recursos lógicos de gran tamaño que utilizan pequeñas cantidades de memoria física.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-104">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span>

<span data-ttu-id="c5ed4-105">En esta sección se describe por qué se necesitan recursos en mosaico y cómo crear y usar recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-105">This section describes why tiled resources are needed and how you create and use tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5ed4-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c5ed4-106">In this section</span></span>



| <span data-ttu-id="c5ed4-107">Tema</span><span class="sxs-lookup"><span data-stu-id="c5ed4-107">Topic</span></span>                                                                                   | <span data-ttu-id="c5ed4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5ed4-108">Description</span></span>                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5ed4-109">¿Por qué son necesarios los recursos en mosaico?</span><span class="sxs-lookup"><span data-stu-id="c5ed4-109">Why are tiled resources needed?</span></span>](why-are-tiled-resources-needed-.md)<br/>       | <span data-ttu-id="c5ed4-110">Los recursos en mosaico son necesarios, por lo que no se podrá tener acceso a la memoria de la unidad de procesamiento de gráficos (GPU), y el hardware puede comprender cómo filtrar por los mosaicos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-110">Tiled resources are needed so less graphics processing unit (GPU) memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span><br/>     |
| [<span data-ttu-id="c5ed4-111">Crear recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="c5ed4-111">Creating tiled resources</span></span>](creating-tiled-resources.md)<br/>                     | <span data-ttu-id="c5ed4-112">Los recursos en mosaico se crean mediante la especificación de la marca de [**\_ \_ \_ mosaico varios de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) cuando se crea un recurso.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-112">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag when you create a resource.</span></span><br/>                                                                                          |
| [<span data-ttu-id="c5ed4-113">API de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="c5ed4-113">Tiled Resource APIs</span></span>](tiled-resource-apis.md)<br/>                               | <span data-ttu-id="c5ed4-114">Las API descritas en esta sección funcionan con los recursos en mosaico y el grupo de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-114">The APIs described in this section work with tiled resources and tile pool.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="c5ed4-115">Acceso de canalización a recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="c5ed4-115">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)<br/> | <span data-ttu-id="c5ed4-116">Los recursos en mosaico se pueden usar en las vistas de recursos del sombreador (SRV), las vistas de destino de representación (RTV), las vistas de estarcido de profundidad (DSV) y las vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como los enlaces de búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-116">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <br/> |
| [<span data-ttu-id="c5ed4-117">Niveles de características de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="c5ed4-117">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)<br/>         | <span data-ttu-id="c5ed4-118">Direct3D 11,2 expone la compatibilidad con los recursos en mosaico en dos niveles con los valores de [**\_ nivel de \_ recursos \_ en mosaico D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="c5ed4-118">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span> <br/>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="c5ed4-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5ed4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5ed4-120">Recursos</span><span class="sxs-lookup"><span data-stu-id="c5ed4-120">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





