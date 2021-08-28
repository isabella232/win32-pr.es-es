---
description: Los culls de prueba de la estructura que están fuera del rectángulo de rectángulos, una subsección rectangular definida por el usuario del destino de representación.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Prueba de indesa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d44b7670d67e7944e9d6e2587ed0011a6244eecef509495b90c71ff0753073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746525"
---
# <a name="scissor-test-direct3d-9"></a>Prueba de indesa (Direct3D 9)

Los culls de prueba de la estructura que están fuera del rectángulo de rectángulos, una subsección rectangular definida por el usuario del destino de representación.

El rectángulo de rectángulo se podría usar para indicar el área del destino de representación donde se dibuja el mundo del juego. El área fuera del rectángulo se encuentra en la selección y podría estar dedicada a la GUI de un juego. La prueba de torción no puede cull áreas no rectangulares.

Los rectángulos de relleno no se pueden establecer más grandes que el destino de representación, pero se pueden establecer más grandes que la ventanilla.

El rectángulo de rectángulo de rectángulos se administra mediante un estado de representación del dispositivo. Se habilita o deshabilita una prueba de si se establece renderstate en **TRUE** o **FALSE.** Esta prueba se realiza después de calcular el color del fragmento, pero antes de realizar pruebas alfa. [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) restablece el rectángulo de recorte al destino de representación completo, análogo al restablecimiento de la ventanilla. [**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) se registra mediante stateblocks e [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) con la configuración de todos los estados (valor D3DSBT \_ ALL en [**D3DSTATEBLOCKTYPE).**](./d3dstateblocktype.md) La prueba de sitiado también afecta a la operación [**IDirect3DDevice9::Clear del**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) dispositivo.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



El rectángulo de rectángulo de rectángulo predeterminado es la ventanilla completa.

Las pruebas de cálculo se realizan justo después de que un sombreador de píxeles o la canalización de funciones fijas completen el procesamiento de píxeles, como se muestra en el diagrama siguiente.

![diagrama de cuándo se realizan pruebas de examen con respecto a otros pasos](images/scissor-test.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
