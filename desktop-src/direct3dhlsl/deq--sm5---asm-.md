---
title: DEQ (SM5-ASM)
description: Comparación de igualdad de doble precisión de componentes.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ed263deec975815f29050d2de0a877a312258c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532872"
---
# <a name="deq-sm5---asm"></a>DEQ (SM5-ASM)

Comparación de igualdad de doble precisión de componentes.



| DEQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes que se van a comparar con *SRC1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los componentes que se van a comparar con *src0*.<br/>         |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza la comparación de punto flotante de precisión doble (*src0*  ==  *SRC1*) para cada componente y escribe el resultado en *dest*.

Si la comparación es true, se devuelve 32-bit 0xFFFFFFFF para ese componente. De lo contrario, se devuelve 32-bit 0x00000000.

La comparación con NaN devuelve false.

Las máscaras de *destino* válidas son uno o dos componentes. Es decir:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. YW,. ZW el primer componente *dest* de la máscara recibe el resultado de 32 bits para la primera comparación Double. El segundo componente de la máscara, si está presente, recibe el resultado de 32 bits para la segunda comparación Double.

El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw. Las siguientes asignaciones *src* son post-swizzle:

-   *src0* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





