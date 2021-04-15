---
description: El motor de iluminación combina la información sobre el color, el color del vértice y la iluminación para generar un color por vértice.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Combinación de texturas alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677229"
---
# <a name="alpha-texture-blending-direct3d-9"></a><span data-ttu-id="634f0-103">Combinación de texturas alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="634f0-103">Alpha Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="634f0-104">El motor de iluminación combina la información sobre el color, el color del vértice y la iluminación para generar un color por vértice.</span><span class="sxs-lookup"><span data-stu-id="634f0-104">The lighting engine combines material color, vertex color, and lighting information to generate a per-vertex color.</span></span> <span data-ttu-id="634f0-105">Una vez interpolado, esto genera un color por píxel que se escribe en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="634f0-105">Once interpolated, this generates a per-pixel color that is written to the frame buffer.</span></span> <span data-ttu-id="634f0-106">Si una aplicación habilita la combinación de texturas, el color del píxel se convertirá en una combinación del píxel actual en el búfer de fotogramas y un color de textura.</span><span class="sxs-lookup"><span data-stu-id="634f0-106">If an application enables texture blending, the pixel color will become a combination of the current pixel in the frame buffer and a texture color.</span></span>

<span data-ttu-id="634f0-107">Esta fórmula determina el color final de los píxeles combinados:</span><span class="sxs-lookup"><span data-stu-id="634f0-107">This formula determines the final blended pixel color:</span></span>


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



<span data-ttu-id="634f0-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="634f0-108">Where:</span></span>

-   <span data-ttu-id="634f0-109">Color es el color de los píxeles de salida.</span><span class="sxs-lookup"><span data-stu-id="634f0-109">Color is the output pixel color.</span></span>
-   <span data-ttu-id="634f0-110">TexelColor es el color de entrada después del filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="634f0-110">TexelColor is the input color after texture filtering.</span></span>
-   <span data-ttu-id="634f0-111">SourceBlend es el porcentaje del color final del píxel que se compone del color de textura de origen.</span><span class="sxs-lookup"><span data-stu-id="634f0-111">SourceBlend is the percentage of the final pixel color that is made up of the source texel color.</span></span>
-   <span data-ttu-id="634f0-112">CurrentPixelColor es el color del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="634f0-112">CurrentPixelColor is the color of the current pixel.</span></span>
-   <span data-ttu-id="634f0-113">DestBlend es el porcentaje del color final del píxel que se compone del color del píxel actual.</span><span class="sxs-lookup"><span data-stu-id="634f0-113">DestBlend is the percentage of the final pixel color that is made up of the current pixel color.</span></span>

<span data-ttu-id="634f0-114">La ecuación de combinación final se establece llamando a [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) y especificando el estado de representación de Blend (D3DRS \_ BLENDXXX) con un factor de mezcla correspondiente ([**D3DBLEND**](./d3dblend.md)).</span><span class="sxs-lookup"><span data-stu-id="634f0-114">The final blending equation is set by calling [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) and specifying the blend render state (D3DRS\_BLENDXXX) with a corresponding blending factor ([**D3DBLEND**](./d3dblend.md)).</span></span> <span data-ttu-id="634f0-115">Los valores de SourceBlend y DestBlend oscilan entre 0,0 (transparente) y 1,0 (opaco), ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="634f0-115">The values of SourceBlend and DestBlend range from 0.0 (transparent) to 1.0 (opaque) inclusive.</span></span> <span data-ttu-id="634f0-116">Además, una aplicación puede controlar la transparencia de un píxel estableciendo el valor alfa en una textura.</span><span class="sxs-lookup"><span data-stu-id="634f0-116">In addition, an application can control the transparency of a pixel by setting the alpha value in a texture.</span></span> <span data-ttu-id="634f0-117">En este caso, use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="634f0-117">In this case, use the following:</span></span>


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



<span data-ttu-id="634f0-118">La ecuación de fusión hará que el píxel representado sea transparente.</span><span class="sxs-lookup"><span data-stu-id="634f0-118">The blending equation will cause the rendered pixel to be transparent.</span></span> <span data-ttu-id="634f0-119">Los valores predeterminados son:</span><span class="sxs-lookup"><span data-stu-id="634f0-119">The default values are:</span></span>


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a><span data-ttu-id="634f0-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="634f0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="634f0-121">Combinación de texturas</span><span class="sxs-lookup"><span data-stu-id="634f0-121">Texture Blending</span></span>](texture-blending.md)
</dt> <dt>

[<span data-ttu-id="634f0-122">Filtrado de texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="634f0-122">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
</dt> <dt>

[<span data-ttu-id="634f0-123">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="634f0-123">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
