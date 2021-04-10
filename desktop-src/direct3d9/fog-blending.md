---
description: La mezcla de niebla hace referencia a la aplicación del factor de niebla a los colores de niebla y de objeto para producir el color final que aparece en una escena, como se describe en fórmulas de niebla (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Combinación de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151946"
---
# <a name="fog-blending-direct3d-9"></a><span data-ttu-id="89f1e-103">Combinación de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="89f1e-103">Fog Blending (Direct3D 9)</span></span>

<span data-ttu-id="89f1e-104">La mezcla de niebla hace referencia a la aplicación del factor de niebla a los colores de niebla y de objeto para producir el color final que aparece en una escena, como se describe en [fórmulas de niebla (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="89f1e-104">Fog blending refers to the application of the fog factor to the fog and object colors to produce the final color that appears in a scene, as discussed in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="89f1e-105">El estado de representación de D3DRS \_ FOGENABLE controla la combinación de niebla.</span><span class="sxs-lookup"><span data-stu-id="89f1e-105">The D3DRS\_FOGENABLE render state controls fog blending.</span></span> <span data-ttu-id="89f1e-106">Establezca este estado de representación en **true** para habilitar la combinación de niebla, tal como se muestra en el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="89f1e-106">Set this render state to **TRUE** to enable fog blending as shown in the following example code.</span></span> <span data-ttu-id="89f1e-107">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="89f1e-107">The default is **FALSE**.</span></span>


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



<span data-ttu-id="89f1e-108">Debe habilitar la combinación de niebla para la niebla de píxeles y la niebla de vértice.</span><span class="sxs-lookup"><span data-stu-id="89f1e-108">You must enable fog blending for both pixel fog and vertex fog.</span></span> <span data-ttu-id="89f1e-109">Para obtener información sobre el uso de estos tipos de niebla, vea [niebla de píxeles (Direct3D 9)](pixel-fog.md) y [niebla de vértice (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="89f1e-109">For information about using these types of fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89f1e-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89f1e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f1e-111">Tipos de niebla</span><span class="sxs-lookup"><span data-stu-id="89f1e-111">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



