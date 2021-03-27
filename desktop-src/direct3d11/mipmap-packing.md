---
title: Empaquetado de mapas MIP
description: En función del nivel de compatibilidad de los recursos en mosaico, los mapas MIP con ciertas dimensiones no siguen las formas de mosaico estándar y se consideran que todos están empaquetados juntos entre sí de forma opaca para la aplicación.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075432"
---
# <a name="mipmap-packing"></a><span data-ttu-id="3b6f0-103">Empaquetado de mapas MIP</span><span class="sxs-lookup"><span data-stu-id="3b6f0-103">Mipmap packing</span></span>

<span data-ttu-id="3b6f0-104">En función del nivel de compatibilidad de los recursos [en](tiled-resources-features-tiers.md) mosaico, los mapas MIP con ciertas dimensiones no siguen las formas de mosaico estándar y se consideran que todos están empaquetados juntos entre sí de forma opaca para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-104">Depending on the [tier](tiled-resources-features-tiers.md) of tiled resources support, mipmaps with certain dimensions don't follow the standard tile shapes and are considered to all be packed together with one another in a manner that is opaque to the application.</span></span> <span data-ttu-id="3b6f0-105">Los niveles más altos de soporte técnico tienen garantías más amplias sobre qué tipos de dimensiones de superficie caben en las formas de mosaico estándar (y, por tanto, las aplicaciones pueden asignarlos de forma individual).</span><span class="sxs-lookup"><span data-stu-id="3b6f0-105">Higher tiers of support have broader guarantees about what types of surface dimensions fit in the standard tile shapes (and can therefore be individually mapped by applications).</span></span>

<span data-ttu-id="3b6f0-106">Lo que puede variar entre las implementaciones es que, dadas las dimensiones de un recurso en mosaico, el formato, el número de mapas de información y los segmentos de matriz, se puede empaquetar un número M de MIPS (por segmento de matriz) en un número N de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-106">What can vary between implementations is that—given a tiled resource's dimensions, format, number of mipmaps, and array slices—some number M of mips (per array slice) can be packed into some number N tiles.</span></span> <span data-ttu-id="3b6f0-107">La API [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) existe para permitir que el controlador informe a la aplicación Qué son M y N (entre otros detalles sobre la superficie que esta API notifica que son estándar y que no varían según el proveedor de hardware).</span><span class="sxs-lookup"><span data-stu-id="3b6f0-107">The [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API exists to allow the driver to report to the application what M and N are (among other details about the surface that this API reports that are standard and don't vary by hardware vendor).</span></span> <span data-ttu-id="3b6f0-108">El conjunto de mosaicos para el MIPS empaquetado sigue siendo de 64 KB y se puede asignar individualmente en ubicaciones dispares de un grupo de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-108">The set of tiles for the packed mips are still 64KB and can be individually mapped into disparate locations in a tile pool.</span></span> <span data-ttu-id="3b6f0-109">Pero la forma de píxeles de los mosaicos y el modo en que se ajustan los mipmaps en el conjunto de mosaicos es específica de un proveedor de hardware y es demasiado complejo de exponer.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-109">But the pixel shape of the tiles and how the mipmaps fit across the set of tiles is specific to a hardware vendor and too complex to expose.</span></span> <span data-ttu-id="3b6f0-110">Por lo tanto, las aplicaciones deben asignar todos los iconos que se designan como empaquetados o ninguno de ellos a la vez.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-110">So, applications are required to either map all of the tiles that are designated as packed, or none of them, at a time.</span></span> <span data-ttu-id="3b6f0-111">De lo contrario, el comportamiento para tener acceso al recurso en mosaico es indefinido.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-111">Otherwise, the behavior for accessing the tiled resource is undefined.</span></span>

<span data-ttu-id="3b6f0-112">En el caso de las superficies matrices, el conjunto de MIPs empaquetados y el número de mosaicos empaquetados que almacenan los MIPS (M y N descritos anteriormente) se aplican individualmente para cada segmento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-112">For arrayed surfaces, the set of packed mips and the number of packed tiles storing those mips (M and N described preceding) applies individually for each array slice.</span></span>

<span data-ttu-id="3b6f0-113">Las API dedicadas para copiar mosaicos ([**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) y [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) no pueden tener acceso a MIPS empaquetado.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-113">Dedicated APIs for copying tiles ([**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) can't access packed mips.</span></span> <span data-ttu-id="3b6f0-114">Las aplicaciones que desean copiar datos a y desde MIPS empaquetados pueden hacerlo mediante todas las API específicas de recursos no en mosaico para copiar y representar superficies.</span><span class="sxs-lookup"><span data-stu-id="3b6f0-114">Applications that want to copy data to and from packed mips can do so using all the non-tiled resource specific APIs for copying and rendering to surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b6f0-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b6f0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b6f0-116">Cómo se organiza en mosaico el área de un recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="3b6f0-116">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




