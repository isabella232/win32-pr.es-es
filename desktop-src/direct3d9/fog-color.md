---
description: El color de color de color para píxeles y vértices se establece a través del estado de representación \_ D3DRSCOLOR DE COLOR. Los valores de estado de representación pueden ser cualquier color RGB, especificado como color RGBA. Se omite el componente alfa.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Color de color rojo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 395bb17c9d6495ade54bc7c761b8c8024c53fbd9a51f620a45ee3a807dc6e20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988005"
---
# <a name="fog-color-direct3d-9"></a>Color de color rojo (Direct3D 9)

El color de color de color para píxeles y vértices se establece a través del estado de representación \_ D3DRSCOLOR DE COLOR. Los valores de estado de representación pueden ser cualquier color RGB, especificado como color RGBA. Se omite el componente alfa.

En el siguiente ejemplo de C++ se establece el color de color blanco.


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



La canalización de función fija y la canalización programable aplican de manera diferente.

1.  Si el controlador admite \_ D3DPMISCCAPSANDSPECULARALPHA:
    -   Si se usa la canalización de función fija y D3DRS WLANCOLOR está establecido, v1.w (en el sombreador de píxeles) es igual al valor establecido en \_ renderstate de renderstate.
    -   Si se usa la canalización programable, v1.w (en el sombreador de píxeles) es igual a 0, incluso si oD1.w se escribe explícitamente en un sombreador de vértices.
2.  Si el controlador NO admite \_ D3DPMISCCAPSANDSPECULARALPHA:
    -   Si se usa la canalización de función fija y D3DRS WLANCOLOR está establecido, v1.w (en el sombreador de píxeles) es igual al valor establecido en \_ renderstate de renderstate.
    -   Si oFog se escribe explícitamente en un sombreador de vértices, v1.w (en el sombreador de píxeles) es igual a oFog, entre 0 y 1.
    -   Si no se aplica ninguno de los dos casos anteriores, v1.w (en el sombreador de píxeles) es igual a 0, incluso si oD1.w se escribe explícitamente en un sombreador de vértices.

Para obtener más información, [vea D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de vaselina](fog-types.md)
</dt> </dl>

 

 



