---
description: La combinación de mezclas hace referencia a la aplicación del factor de fusión a los colores de los objetos y a los colores del objeto para producir el color final que aparece en una escena, como se describe en Fórmulas de fusión (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Blending de Blend (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60f3402daf71a3fce14af936334c3d96e928d3469452eafb94d139594bb0b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894025"
---
# <a name="fog-blending-direct3d-9"></a>Blending de Blend (Direct3D 9)

La combinación de mezclas hace referencia a la aplicación del factor de fusión a los colores de los objetos y los colores del objeto para producir el color final que aparece en una escena, como se describe en Fórmulas de fusión [(Direct3D 9).](fog-formulas.md) D3DRS COMBINEENABLE representa la mezcla de controles \_ de estado de fusión. Establezca este estado de representación en **TRUE para** habilitar la combinación de mezcla, como se muestra en el código de ejemplo siguiente. El valor predeterminado es **FALSE.**


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



Debe habilitar la mezcla de mezcla para el ángulo de píxeles y el vértice. Para obtener información sobre el uso de estos tipos de vértices, vea [Pixel Vertex (Direct3D 9)](pixel-fog.md) y [Vertex Vertex (Direct3D 9).](vertex-fog.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de vaselina](fog-types.md)
</dt> </dl>

 

 



