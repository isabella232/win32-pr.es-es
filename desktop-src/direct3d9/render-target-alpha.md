---
description: El mezclador de búfer de fotogramas ahora puede mezclar canales alfa independientes de la combinación de canales de color en destinos de representación. Este control se habilita con un nuevo estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Alfa de destino de representación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536508"
---
# <a name="render-target-alpha-direct3d-9"></a><span data-ttu-id="295e7-104">Alfa de destino de representación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="295e7-104">Render Target Alpha (Direct3D 9)</span></span>

<span data-ttu-id="295e7-105">El mezclador de búfer de fotogramas ahora puede mezclar canales alfa independientes de la combinación de canales de color en destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="295e7-105">The frame buffer blender can now blend alpha channels independent from color-channel blending on render targets.</span></span> <span data-ttu-id="295e7-106">Este control se habilita con un nuevo estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="295e7-106">This control is enabled with a new render state, D3DRS\_SEPARATEALPHABLENDENABLE.</span></span>

<span data-ttu-id="295e7-107">Cuando D3DRS \_ SEPARATEALPHABLENDENABLE se establece en **false** (que es la condición predeterminada), los factores de mezcla y las operaciones de destino de representación que se aplican a Alpha son los mismos que los definidos para combinar los canales de color.</span><span class="sxs-lookup"><span data-stu-id="295e7-107">When D3DRS\_SEPARATEALPHABLENDENABLE is set to **FALSE** (which is the default condition), the render-target blending factors and operations applied to alpha are the same as those defined for blending color channels.</span></span> <span data-ttu-id="295e7-108">Un controlador debe establecer el límite de \_ SEPARATEALPHABLEND de D3DPMISCCAPS para indicar que puede admitir la combinación alfa de representación y destino.</span><span class="sxs-lookup"><span data-stu-id="295e7-108">A driver needs to set the D3DPMISCCAPS\_SEPARATEALPHABLEND cap to indicate that it can support render-target alpha blending.</span></span> <span data-ttu-id="295e7-109">Asegúrese de habilitar D3DRS \_ ALPHABLEND para indicar a la canalización que se necesita la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="295e7-109">Be sure to enable D3DRS\_ALPHABLEND to tell the pipeline that alpha blending is needed.</span></span>

<span data-ttu-id="295e7-110">Para controlar los factores del canal alfa de los mezcladores de destino de representación, se definen dos nuevos Estados de representación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="295e7-110">To control the factors in the alpha channel of the render-target blenders, two new render states are defined as follows:</span></span>


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



<span data-ttu-id="295e7-111">Al igual que D3DRS \_ SRCBLEND y D3DRS \_ DESTBLEND, se pueden establecer en uno de los valores de la enumeración [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="295e7-111">Like the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND, these can be set to one of the values in the [**D3DBLEND**](./d3dblend.md) enumeration.</span></span> <span data-ttu-id="295e7-112">La configuración de Blend de origen y de destino se puede combinar de varias maneras, dependiendo de la configuración de los miembros SrcBlendCaps y DestBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="295e7-112">The source and destination blend settings can be combined in several ways, depending on the settings in the SrcBlendCaps and DestBlendCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="295e7-113">La combinación alfa se realiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="295e7-113">The alpha blending is done as follows:</span></span>

<span data-ttu-id="295e7-114">renderTargetAlpha = (alpha<sub>en</sub> \* srcBlendOp) BlendOp (alpha<sub>RT</sub> \* destBlendOp)</span><span class="sxs-lookup"><span data-stu-id="295e7-114">renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)</span></span>

<span data-ttu-id="295e7-115">Donde:</span><span class="sxs-lookup"><span data-stu-id="295e7-115">Where:</span></span>

-   <span data-ttu-id="295e7-116">alfa es el valor alfa<sub>de</sub> entrada.</span><span class="sxs-lookup"><span data-stu-id="295e7-116">alpha<sub>in</sub> is the input alpha value.</span></span>
-   <span data-ttu-id="295e7-117">srcBlendOp es uno de los factores de mezcla de [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="295e7-117">srcBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="295e7-118">BlendOp es uno de los factores de mezcla de [**D3DBLENDOP**](./d3dblendop.md).</span><span class="sxs-lookup"><span data-stu-id="295e7-118">BlendOp is one of the blend factors in [**D3DBLENDOP**](./d3dblendop.md).</span></span>
-   <span data-ttu-id="295e7-119">alpha<sub>RT</sub> es el valor alfa de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="295e7-119">alpha<sub>rt</sub> is the render-target alpha value.</span></span>
-   <span data-ttu-id="295e7-120">destBlendOp es uno de los factores de mezcla de [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="295e7-120">destBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="295e7-121">renderTargetAlpha es el valor alfa mezclado final.</span><span class="sxs-lookup"><span data-stu-id="295e7-121">renderTargetAlpha is the final blended alpha value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="295e7-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="295e7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="295e7-123">Combinación alfa</span><span class="sxs-lookup"><span data-stu-id="295e7-123">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 
