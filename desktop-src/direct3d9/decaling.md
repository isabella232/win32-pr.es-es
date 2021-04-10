---
description: Las aplicaciones de Direct3D usan las marcas para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación. Las aplicaciones aplican marcas a las imágenes de primitivas para permitir que los polígonos coplanoles se representen correctamente.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Marcas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152121"
---
# <a name="decaling-direct3d-9"></a><span data-ttu-id="031dc-104">Marcas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="031dc-104">Decaling (Direct3D 9)</span></span>

<span data-ttu-id="031dc-105">Las aplicaciones de Direct3D usan las marcas para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="031dc-105">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="031dc-106">Las aplicaciones aplican marcas a las imágenes de primitivas para permitir que los polígonos coplanoles se representen correctamente.</span><span class="sxs-lookup"><span data-stu-id="031dc-106">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="031dc-107">Por ejemplo, al aplicar las marcas de neumático y las líneas amarillas a un Roadway, las marcas deben aparecer directamente encima de la carretera.</span><span class="sxs-lookup"><span data-stu-id="031dc-107">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="031dc-108">Sin embargo, los valores z de las marcas y la carretera son los mismos.</span><span class="sxs-lookup"><span data-stu-id="031dc-108">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="031dc-109">Por lo tanto, es posible que el búfer de profundidad no produzca una separación limpia entre ambos.</span><span class="sxs-lookup"><span data-stu-id="031dc-109">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="031dc-110">Algunos píxeles de la primitiva inversa se pueden representar encima de la primitiva delantera y viceversa.</span><span class="sxs-lookup"><span data-stu-id="031dc-110">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="031dc-111">La imagen resultante parece Shimmer de fotograma a fotograma.</span><span class="sxs-lookup"><span data-stu-id="031dc-111">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="031dc-112">Este efecto se denomina *lucha z* o *flimmering*.</span><span class="sxs-lookup"><span data-stu-id="031dc-112">This effect is called *z-fighting* or *flimmering*.</span></span>

<span data-ttu-id="031dc-113">Para solucionar este problema, use una galería de símbolos para enmascarar la sección de la primitiva inversa en la que aparecerá la calcomanía.</span><span class="sxs-lookup"><span data-stu-id="031dc-113">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="031dc-114">Desactive el almacenamiento en búfer z y represente la imagen de la primitiva delantera en el área enmascarada de la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="031dc-114">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="031dc-115">Aunque se puede usar varias combinaciones de texturas para solucionar este problema, al hacerlo se limita el número de otros efectos especiales que puede producir la aplicación.</span><span class="sxs-lookup"><span data-stu-id="031dc-115">Although multiple texture blending can be used to solve this problem, doing so limits the number of other special effects that your application can produce.</span></span> <span data-ttu-id="031dc-116">El uso del búfer de la galería de símbolos para aplicar marcas libera las fases de fusión de texturas para otros efectos.</span><span class="sxs-lookup"><span data-stu-id="031dc-116">Using the stencil buffer to apply decals frees up texture blending stages for other effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="031dc-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="031dc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="031dc-118">Técnicas de búfer de estarcido</span><span class="sxs-lookup"><span data-stu-id="031dc-118">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



