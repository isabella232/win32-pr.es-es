---
title: Aplicar una técnica (Direct3D 11)
description: Obtenga información sobre cómo establecer el estado de efecto en el dispositivo para Direct3D 11 después de que se declaren e inicialicen las constantes, las texturas y el estado del sombreador.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d03f92957eaf1b3d501c0acd54aafde7e16d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072971"
---
# <a name="apply-a-technique-direct3d-11"></a>Aplicar una técnica (Direct3D 11)

Con las constantes, las texturas y el estado del sombreador declarados e inicializados, lo único que queda por hacer es establecer el estado de efecto en el dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Establecer el estado que no es de sombreador en el dispositivo

Un efecto no establece ningún estado de canalización. Por ejemplo, al borrar un destino de representación se prepara el destino de representación para los datos. Antes de establecer el estado de efecto en el dispositivo, este es un ejemplo de cómo borrar los búferes de salida.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Establecer el estado de efecto en el dispositivo

Para establecer el estado del efecto, se aplica el estado de efecto dentro del bucle de representación. Esto se hace desde fuera de . Es decir, seleccione una técnica y, a continuación, establezca el estado de cada uno de los pases (en función del resultado deseado).


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



Un efecto no representa nada, simplemente establece el estado del efecto en el dispositivo. Se llama al código de representación después de que el estado de efecto actualice el estado del dispositivo. En este ejemplo, la llamada DrawIndexed realiza la representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un efecto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




