---
description: 'Cuando se usa IDirect3DDevice9:: UpdateSurface, se pasa un rectángulo en la superficie de origen o se usa NULL para especificar toda la superficie.'
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Copiar en superficies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496631"
---
# <a name="copying-to-surfaces-direct3d-9"></a><span data-ttu-id="80b9a-103">Copiar en superficies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="80b9a-103">Copying to Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="80b9a-104">Cuando se usa [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), se pasa un rectángulo en la superficie de origen o se usa **null** para especificar toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="80b9a-104">When using [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), pass a rectangle on the source surface, or use **NULL** to specify the entire surface.</span></span> <span data-ttu-id="80b9a-105">También se pasa un punto en la superficie de destino en la que se copia la posición superior izquierda del rectángulo en la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="80b9a-105">You also pass a point on the destination surface to which the upper left position of the rectangle on the source image is copied.</span></span> <span data-ttu-id="80b9a-106">Este método no admite el recorte.</span><span class="sxs-lookup"><span data-stu-id="80b9a-106">This method does not support clipping.</span></span> <span data-ttu-id="80b9a-107">Se producirá un error en la operación a menos que el rectángulo de origen y el rectángulo de destino correspondiente estén completamente incluidos en las superficies de origen y de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="80b9a-107">The operation will fail unless the source rectangle and the corresponding destination rectangle are completely contained within the source and destination surfaces respectively.</span></span> <span data-ttu-id="80b9a-108">Este método no admite la combinación alfa, las claves de color o la conversión de formato.</span><span class="sxs-lookup"><span data-stu-id="80b9a-108">This method does not support alpha blending, color keys, or format conversion.</span></span> <span data-ttu-id="80b9a-109">Tenga en cuenta que las superficies de origen y de destino deben ser distintas.</span><span class="sxs-lookup"><span data-stu-id="80b9a-109">Note that the destination and source surfaces must be distinct.</span></span>

<span data-ttu-id="80b9a-110">Para otras restricciones al usar UpdateSurface, vea [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span><span class="sxs-lookup"><span data-stu-id="80b9a-110">For other restrictions when using UpdateSurface, see [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span></span>

<span data-ttu-id="80b9a-111">Los métodos siguientes también están disponibles en C++/C para copiar imágenes en una superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="80b9a-111">The following methods are also available in C++/C for copying images to a Direct3D surface.</span></span>

-   [<span data-ttu-id="80b9a-112">**D3DXLoadSurfaceFromFile**</span><span class="sxs-lookup"><span data-stu-id="80b9a-112">**D3DXLoadSurfaceFromFile**</span></span>](d3dxloadsurfacefromfile.md)
-   [<span data-ttu-id="80b9a-113">**D3DXLoadSurfaceFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="80b9a-113">**D3DXLoadSurfaceFromFileInMemory**</span></span>](d3dxloadsurfacefromfileinmemory.md)
-   [<span data-ttu-id="80b9a-114">**D3DXLoadSurfaceFromMemory**</span><span class="sxs-lookup"><span data-stu-id="80b9a-114">**D3DXLoadSurfaceFromMemory**</span></span>](d3dxloadsurfacefrommemory.md)
-   [<span data-ttu-id="80b9a-115">**D3DXLoadSurfaceFromResource**</span><span class="sxs-lookup"><span data-stu-id="80b9a-115">**D3DXLoadSurfaceFromResource**</span></span>](d3dxloadsurfacefromresource.md)
-   [<span data-ttu-id="80b9a-116">**D3DXLoadSurfaceFromSurface**</span><span class="sxs-lookup"><span data-stu-id="80b9a-116">**D3DXLoadSurfaceFromSurface**</span></span>](d3dxloadsurfacefromsurface.md)
-   [<span data-ttu-id="80b9a-117">**IDirect3DDevice9::UpdateSurface**</span><span class="sxs-lookup"><span data-stu-id="80b9a-117">**IDirect3DDevice9::UpdateSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a><span data-ttu-id="80b9a-118">Ejemplo de UpdateSurface</span><span class="sxs-lookup"><span data-stu-id="80b9a-118">UpdateSurface Example</span></span>

<span data-ttu-id="80b9a-119">En el ejemplo siguiente se copian dos rectángulos de la superficie de origen en una superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="80b9a-119">The following example copies two rectangles from the source surface to a destination surface.</span></span> <span data-ttu-id="80b9a-120">El primer rectángulo se copia de (0,0, 50, 50) en la superficie de origen a la misma ubicación en la superficie de destino y el segundo rectángulo se copia de (50, 50, 100, 100) en la superficie de origen a (150, 150, 200, 200) en la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="80b9a-120">The first rectangle is copied from (0, 0, 50, 50) on the source surface to the same location on the destination surface, and the second rectangle is copied from (50, 50, 100, 100) on the source surface to (150, 150, 200, 200) on the destination surface.</span></span>


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a><span data-ttu-id="80b9a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80b9a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80b9a-122">Superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="80b9a-122">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="80b9a-123">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="80b9a-123">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
