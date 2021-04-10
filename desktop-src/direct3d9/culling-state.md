---
description: Para mejorar el rendimiento de la representación, puede desechar (o quitar) un primitivo que se encuentre enfrente de la cámara.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Estado de selección (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153250"
---
# <a name="culling-state-direct3d-9"></a><span data-ttu-id="052ad-103">Estado de selección (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="052ad-103">Culling State (Direct3D 9)</span></span>

<span data-ttu-id="052ad-104">Para mejorar el rendimiento de la representación, puede desechar (o quitar) un primitivo que se encuentre enfrente de la cámara.</span><span class="sxs-lookup"><span data-stu-id="052ad-104">To improve rendering performance, you can cull out (or remove) a primitive that faces away from the camera.</span></span> <span data-ttu-id="052ad-105">En el caso de las primitivas de una sola cara, se ahorra tiempo de representación porque no está visible la cara posterior.</span><span class="sxs-lookup"><span data-stu-id="052ad-105">For single-sided primitives, this saves rendering time because a back-face is not visible.</span></span> <span data-ttu-id="052ad-106">Para habilitar el reactivado, debe conocer el orden de bobinado de los vértices (normalmente en el sentido contrario a las agujas del reloj).</span><span class="sxs-lookup"><span data-stu-id="052ad-106">To enable culling, you need to know the winding order of the vertices (typically counter-clockwise).</span></span> <span data-ttu-id="052ad-107">En este ejemplo se quitará cualquier primitiva cuya cara trasera esté mirando hacia delante (dado un orden de bobinado en el sentido contrario a las agujas del reloj):</span><span class="sxs-lookup"><span data-stu-id="052ad-107">This example will remove any primitive whose back face is facing forward (given a counter-clockwise winding order):</span></span>


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a><span data-ttu-id="052ad-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="052ad-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="052ad-109">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="052ad-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



