---
title: deriv_rtx (SM4-ASM)
description: Velocidad de cambio de contenido de cada componente float32 de src0 (post-swizzle), con respecto a la dirección RenderTarget x Direction (RTX) o a la dirección de RenderTarget y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419895"
---
# <a name="deriv_rtx-sm4---asm"></a>derivar \_ RTX (SM4-ASM)

Velocidad de cambio de contenido de cada componente float32 de *src0* (post-swizzle), con respecto a la dirección rendertarget x Direction (RTX) o a la dirección de rendertarget y.



| derive \_ RTX \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el componente de la operación.<br/>             |



 

## <a name="remarks"></a>Observaciones

Solo se calcula un par derivado de x, y para cada sello de 2x2 de píxeles.

Esta operación depende del hardware.

Implementación de rasterizador de referencia para triángulos:

-   El sombreador de píxeles siempre ejecuta el sombreador en cuatro puntos de píxeles en lógico (incluso a través del control de flujo, enmascarando los píxeles deshabilitados).
-   Las cuádruples siempre tienen coordenadas de píxeles numeradas pares (x e y) para el píxel superior izquierdo.
-   Los píxeles ficticios se ejecutan en el primitivo si el primitivo es demasiado pequeño para rellenar un cuádruple 2x2.
-   **derive \_ RTX** se calcula seleccionando primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada y de la cuádruple. Después, el resultado se calcula como: *src0*(impar x píxel)- *src0*(incluso x píxeles) \[ por componente.\]
-   [derive \_ propiedad](deriv-rty--sm4---asm-.md) se calcula seleccionando primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada x de la cuádruple. A continuación, el resultado se calcula como: *src0*(impar y píxel)- *src0*(incluso píxel) \[ por componente.\]

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





