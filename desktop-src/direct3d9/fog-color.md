---
description: El color de niebla para la niebla de píxeles y vértices se establece mediante el estado de representación de FOGCOLOR de D3DRS \_ . Los valores de estado de representación pueden ser cualquier color RGB, especificado como color RGBA. Se omite el componente alfa.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Color de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079877"
---
# <a name="fog-color-direct3d-9"></a>Color de niebla (Direct3D 9)

El color de niebla para la niebla de píxeles y vértices se establece mediante el estado de representación de FOGCOLOR de D3DRS \_ . Los valores de estado de representación pueden ser cualquier color RGB, especificado como color RGBA. Se omite el componente alfa.

En el siguiente ejemplo de C++ se establece el color de niebla en blanco.


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



La niebla se aplica de forma diferente en la canalización de función fija y en la canalización programable.

1.  Si el controlador admite D3DPMISCCAPS \_ FOGANDSPECULARALPHA:
    -   Si se usa la canalización de función fija y se \_ establece D3DRS FOGCOLOR, v1. w (en el sombreador de píxeles) es igual al valor establecido en Fog renderstate.
    -   Si se usa la canalización programable, v1. w (en el sombreador de píxeles) es igual a 0, incluso si oD1. w se escribe explícitamente en un sombreador de vértices.
2.  Si el controlador no es compatible con D3DPMISCCAPS \_ FOGANDSPECULARALPHA:
    -   Si se usa la canalización de función fija y se \_ establece D3DRS FOGCOLOR, entonces v1. w (en el sombreador de píxeles) es igual al valor establecido en niebla renderstate.
    -   Si oFog se escribe explícitamente en un sombreador de vértices, v1. w (en el sombreador de píxeles) es igual a oFog, fijado entre 0 y 1.
    -   Si no se aplica ninguno de los dos casos anteriores, v1. w (en el sombreador de píxeles) es igual a 0, incluso si oD1. w se escribe explícitamente en un sombreador de vértices.

Para obtener más información, vea [D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de niebla](fog-types.md)
</dt> </dl>

 

 



