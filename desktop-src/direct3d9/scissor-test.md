---
description: La prueba de tijera selecciona los píxeles que están fuera del rectángulo de tijeras, una subsección rectangular definida por el usuario del destino de representación.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Prueba de tijeras (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696092"
---
# <a name="scissor-test-direct3d-9"></a>Prueba de tijeras (Direct3D 9)

La prueba de tijera selecciona los píxeles que están fuera del rectángulo de tijeras, una subsección rectangular definida por el usuario del destino de representación.

El rectángulo en tijeras puede usarse para indicar el área del destino de representación en la que se dibuja el mundo del juego. El área fuera del rectángulo se selecciona y podría estar dedicada a la GUI de un juego. La prueba de tijera no puede desactivar áreas no rectangulares.

Los rectángulos con tijeras no se pueden establecer en un valor mayor que el destino de representación, pero se pueden establecer en un valor mayor que el de la ventanilla.

El rectángulo en tijera se administra mediante un estado de representación del dispositivo. Una prueba de tijera está habilitada o deshabilitada estableciendo renderstate en **true** o **false**. Esta prueba se realiza después de calcular el color del fragmento, pero antes de la prueba alfa. [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) restablece el rectángulo de tijeras en el destino de representación completo, análogo al restablecimiento de la ventanilla. [**IDirect3DDevice9:: SetScissorRect**](/windows/desktop/api) se registra con Stateblocks y [**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) con la configuración de todos los Estados (D3DSBT \_ todos los valores en [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)). La prueba de tijeras también afecta a la operación Device [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) .


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



El rectángulo entre tijeras predeterminado es la ventanilla completa.

La prueba de tijeras se realiza justo después de que un sombreador de píxeles o la canalización de función fija complete el procesamiento de píxeles, tal y como se muestra en el diagrama siguiente.

![diagrama de Cuándo se realiza la prueba de tijeras en relación con otros pasos](images/scissor-test.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
