---
title: Operaciones disponibles en los recursos en mosaico
description: En esta sección se enumeran las operaciones que se pueden realizar en los recursos en mosaico.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076146"
---
# <a name="operations-available-on-tiled-resources"></a><span data-ttu-id="d70e9-103">Operaciones disponibles en los recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="d70e9-103">Operations available on tiled resources</span></span>

<span data-ttu-id="d70e9-104">En esta sección se enumeran las operaciones que se pueden realizar en los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="d70e9-104">This section lists operations that you can perform on tiled resources.</span></span>

-   <span data-ttu-id="d70e9-105">void [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) y [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations: estas ubicaciones de iconos de punto de operaciones en un recurso en mosaico en ubicaciones en grupos de mosaicos, o en null o en ambas.</span><span class="sxs-lookup"><span data-stu-id="d70e9-105">void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations - These operations point tile locations in a tiled resource to locations in tile pools, or to NULL, or to both.</span></span> <span data-ttu-id="d70e9-106">Estas operaciones pueden actualizar un subconjunto separado de los punteros en mosaico.</span><span class="sxs-lookup"><span data-stu-id="d70e9-106">These operations can update a disjoint subset of the tile pointers.</span></span>
-   <span data-ttu-id="d70e9-107">Operaciones de copia \* () y actualización \* (): todas las API que pueden copiar datos en una superficie de grupo predeterminada (por ejemplo, [**Id3d11devicecontext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) y [**id3d11devicecontext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) funcionan para los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="d70e9-107">Copy\*() and Update\*() operations - All the APIs that can copy data to and from a default pool surface (for example, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) and [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) work for tiled resources.</span></span> <span data-ttu-id="d70e9-108">La lectura desde mosaicos sin asignar produce 0 y las escrituras en mosaicos sin asignar se quitan.</span><span class="sxs-lookup"><span data-stu-id="d70e9-108">Reading from unmapped tiles produces 0 and writes to unmapped tiles are dropped.</span></span>
-   <span data-ttu-id="d70e9-109">[**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) y [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) : estas operaciones existen para copiar mosaicos con una granularidad de 64 KB en cualquier recurso en mosaico y un recurso de búfer en un diseño de memoria canónico.</span><span class="sxs-lookup"><span data-stu-id="d70e9-109">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) operations - These operations exist for copying tiles at 64KB granularity to and from any tiled resource and a buffer resource in a canonical memory layout.</span></span> <span data-ttu-id="d70e9-110">El controlador de pantalla y el hardware realizan cualquier memoria "permutación" necesaria para el recurso en mosaico.</span><span class="sxs-lookup"><span data-stu-id="d70e9-110">The display driver and hardware perform any memory "swizzling" necessary for the tiled resource.</span></span>
-   <span data-ttu-id="d70e9-111">Los enlaces de canalización de Direct3D y la creación y los enlaces de la vista que funcionarían en recursos no en mosaico también funcionan en recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="d70e9-111">Direct3D pipeline bindings and view creations / bindings that would work on non-tiled resources work on tiled resources as well.</span></span>

<span data-ttu-id="d70e9-112">Los controles de mosaico están disponibles en contextos inmediatos o aplazados (al igual que las actualizaciones de los recursos típicos) y en el impacto de la ejecución en los accesos posteriores a los mosaicos (no las operaciones enviadas previamente).</span><span class="sxs-lookup"><span data-stu-id="d70e9-112">Tile controls are available on immediate or deferred contexts (just like updates to typical resources) and upon execution impact subsequent accesses to the tiles (not previously submitted operations).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d70e9-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d70e9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d70e9-114">Crear recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="d70e9-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




