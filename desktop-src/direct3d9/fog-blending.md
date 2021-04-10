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
# <a name="fog-blending-direct3d-9"></a>Combinación de niebla (Direct3D 9)

La mezcla de niebla hace referencia a la aplicación del factor de niebla a los colores de niebla y de objeto para producir el color final que aparece en una escena, como se describe en [fórmulas de niebla (Direct3D 9)](fog-formulas.md). El estado de representación de D3DRS \_ FOGENABLE controla la combinación de niebla. Establezca este estado de representación en **true** para habilitar la combinación de niebla, tal como se muestra en el código de ejemplo siguiente. El valor predeterminado es **false**.


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



Debe habilitar la combinación de niebla para la niebla de píxeles y la niebla de vértice. Para obtener información sobre el uso de estos tipos de niebla, vea [niebla de píxeles (Direct3D 9)](pixel-fog.md) y [niebla de vértice (Direct3D 9)](vertex-fog.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de niebla](fog-types.md)
</dt> </dl>

 

 



