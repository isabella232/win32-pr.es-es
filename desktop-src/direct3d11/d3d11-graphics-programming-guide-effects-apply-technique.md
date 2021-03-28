---
title: Aplicar una técnica (Direct3D 11)
description: Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e67668b27c1f0271974f20edc62619a7b1ae8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075811"
---
# <a name="apply-a-technique-direct3d-11"></a>Aplicar una técnica (Direct3D 11)

Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Establecer el estado de no sombreador en el dispositivo

Algunos Estados de canalización no se establecen con un efecto. Por ejemplo, el borrado de un destino de representación prepara el destino de representación para los datos. Antes de establecer el estado del efecto en el dispositivo, este es un ejemplo de Cómo borrar los búferes de salida.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Establecer el estado del efecto en el dispositivo

El establecimiento del estado del efecto se realiza aplicando el estado del efecto en el bucle de representación. Esto se realiza desde fuera de. Es decir, seleccione una técnica y, a continuación, establezca el estado de cada una de las pasadas (dependiendo del resultado deseado).


```
    D3D11_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



Un efecto no representa nada, simplemente establece el estado del efecto en el dispositivo. El código de representación se llama después de que el estado del efecto actualice el estado del dispositivo. En este ejemplo, la llamada a DrawIndexed realiza la representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un efecto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




