---
title: Creación de grupos de iconos
description: Un grupo de mosaicos se crea a través de la API de ID3D11Device CreateBuffer pasando la \_ marca D3D11 Resource \_ Misc del \_ \_ grupo de mosaicos en el miembro MiscFlags de la \_ estructura DESC del búfer D3D11 \_ al que apunta el parámetro pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996733"
---
# <a name="tile-pool-creation"></a><span data-ttu-id="0a2c5-103">Creación de grupos de iconos</span><span class="sxs-lookup"><span data-stu-id="0a2c5-103">Tile pool creation</span></span>

<span data-ttu-id="0a2c5-104">Un grupo de mosaicos se crea a través de la API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) pasando la marca [**D3D11 \_ Resource \_ Misc del \_ \_ grupo de mosaicos**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) en el miembro **MiscFlags** de la estructura [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a la que apunta el parámetro *pDesc* .</span><span class="sxs-lookup"><span data-stu-id="0a2c5-104">A tile pool is created via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API by passing the [**D3D11\_RESOURCE\_MISC\_TILE\_POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag in the **MiscFlags** member of the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure that the *pDesc* parameter points to.</span></span>

<span data-ttu-id="0a2c5-105">Las aplicaciones pueden crear uno o varios grupos de mosaicos por dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0a2c5-105">Applications can create one or more tile pools per Direct3D device.</span></span> <span data-ttu-id="0a2c5-106">El tamaño total de cada grupo de mosaicos está restringido al límite de tamaño de los recursos de Direct3D 11, que es aproximadamente 1/4 de RAM de unidad de procesamiento de gráficos (GPU).</span><span class="sxs-lookup"><span data-stu-id="0a2c5-106">The total size of each tile pool is restricted to Direct3D 11's resource size limit, which is roughly 1/4 of graphics processing unit (GPU) RAM.</span></span>

<span data-ttu-id="0a2c5-107">Un grupo de mosaicos se compone de mosaicos de 64 KB, pero el sistema operativo (Mostrar controlador) administra todo el grupo como una o más asignaciones en segundo plano; el desglose no es visible para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0a2c5-107">A tile pool is made of 64KB tiles, but the operating system (display driver) manages the entire pool as one or more allocations behind the scenes—the breakdown is not visible to applications.</span></span> <span data-ttu-id="0a2c5-108">Los recursos en mosaico definen el contenido apuntando a los mosaicos de un grupo de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="0a2c5-108">Tiled resources define content by pointing at tiles within a tile pool.</span></span> <span data-ttu-id="0a2c5-109">La desasignación de un icono de un recurso en mosaico se realiza apuntando el icono a **null**.</span><span class="sxs-lookup"><span data-stu-id="0a2c5-109">Unmapping a tile from a tiled resource is done by pointing the tile to **NULL**.</span></span> <span data-ttu-id="0a2c5-110">Estos mosaicos sin asignar tienen reglas sobre el comportamiento de las lecturas o escrituras.</span><span class="sxs-lookup"><span data-stu-id="0a2c5-110">Such unmapped tiles have rules about the behavior of reads or writes.</span></span> <span data-ttu-id="0a2c5-111">Para obtener información, consulte [seguimiento de peligros frente a recursos del grupo de mosaicos](hazard-tracking-versus-tile-pool-resources.md).</span><span class="sxs-lookup"><span data-stu-id="0a2c5-111">For info, see [Hazard tracking versus tile pool resources](hazard-tracking-versus-tile-pool-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a2c5-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a2c5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a2c5-113">Mapas en un grupo de iconos</span><span class="sxs-lookup"><span data-stu-id="0a2c5-113">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




