---
title: deriv_rtx (sm4 - asm)
description: Velocidad de cambio del contenido de cada componente float32 de src0 (posterior al swzzle), con respecto a la dirección x de RenderTarget (rtx) o renderTarget y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a9697372964135e5ecb3cb5e916b0509a6a6a860ff8fa01ea0daeb1b8be4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986655"
---
# <a name="deriv_rtx-sm4---asm"></a>deriv \_ rtx (sm4 - asm)

Velocidad de cambio de contenido de cada componente float32 de *src0* (posterior al swzzle), con respecto a la dirección x de RenderTarget (rtx) o renderTarget y.



| deriv \_ rtx \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El componente de la operación.<br/>             |



 

## <a name="remarks"></a>Comentarios

Solo se calcula un único par derivado x,y para cada marca de 2 x 2 píxeles.

Esta operación depende del hardware.

Implementación de rasterizador de referencia para triángulos:

-   Sombreador de píxeles siempre ejecuta Sombreador sobre 2 x 2 cuadránxeles en el paso de bloqueo (incluso a través del control de flujo, enmascaramiento de píxeles deshabilitados).
-   Los cuadránáxeles siempre tienen coordenadas de píxel numeradas (x e y) para el píxel superior izquierdo.
-   Los píxeles ficticios se ejecutan de forma primitiva si primitive es demasiado pequeño para rellenar un cuadránxel de 2x2.
-   **Deriv \_ rtx** se calcula eligiendo primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada y del cuadránxel. A continuación, el resultado se calcula como: *src0*(píxel x impar) - *src0*(incluso x píxeles) \[ por componente\]
-   [Deriv \_ rty](deriv-rty--sm4---asm-.md) se calcula eligiendo primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada x del cuadránxel. A continuación, el resultado se calcula como: *src0*(píxel impar y) - *src0*(píxel y par) \[ por componente\]

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





