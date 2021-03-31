---
description: Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Aplicar una técnica (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496013"
---
# <a name="apply-a-technique-direct3d-10"></a>Aplicar una técnica (Direct3D 10)

Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Establecer el estado de no sombreador en el dispositivo

Algunos Estados de canalización no se establecen con un efecto. Por ejemplo, el borrado de un destino de representación prepara el destino de representación para los datos. Antes de establecer el estado del efecto en el dispositivo, este es un ejemplo de Cómo borrar los búferes de salida.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Establecer el estado del efecto en el dispositivo

El establecimiento del estado del efecto se realiza aplicando el estado del efecto en el bucle de representación. Esto se realiza desde fuera de. Es decir, seleccione una técnica y, a continuación, establezca el estado de cada una de las pasadas (dependiendo del resultado deseado).


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



Un efecto no representa nada, simplemente establece el estado del efecto en el dispositivo. El código de representación se llama después de que el estado del efecto actualice el estado del dispositivo. En este ejemplo, la llamada a DrawIndexed realiza la representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



