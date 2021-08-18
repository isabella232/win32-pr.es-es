---
description: Con las constantes, las texturas y el estado del sombreador declarados e inicializados, lo único que queda por hacer es establecer el estado de efecto en el dispositivo.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Aplicar una técnica (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4c920cbc7323ba42f3b099688a962674e3f5c2305746df7a56d1e158330919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128417"
---
# <a name="apply-a-technique-direct3d-10"></a>Aplicar una técnica (Direct3D 10)

Con las constantes, las texturas y el estado del sombreador declarados e inicializados, lo único que queda por hacer es establecer el estado de efecto en el dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Establecer el estado que no es de sombreador en el dispositivo

Un efecto no establece ningún estado de canalización. Por ejemplo, al borrar un destino de representación se prepara el destino de representación para los datos. Antes de establecer el estado de efecto en el dispositivo, este es un ejemplo de cómo borrar los búferes de salida.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Establecer el estado de efecto en el dispositivo

La configuración del estado del efecto se realiza aplicando el estado de efecto dentro del bucle de representación. Esto se hace desde fuera de . Es decir, seleccione una técnica y, a continuación, establezca el estado de cada uno de los pases (en función del resultado deseado).


```
    D3D10_TECHNIQUE_DESC techDesc;
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



Un efecto no representa nada, simplemente establece el estado del efecto en el dispositivo. Se llama al código de representación después de que el estado de efecto actualice el estado del dispositivo. En este ejemplo, la llamada DrawIndexed realiza la representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



