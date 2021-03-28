---
title: DMín (SM5-ASM)
description: Mínimo de doble precisión de componentes.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077098"
---
# <a name="dmin-sm5---asm"></a>DMín (SM5-ASM)

Mínimo de doble precisión de componentes.



| dmin \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los resultados de la operación.<br/> *dest*  =  *src0*  <  *SRC1* ? *src0* : *SRC1*<br/> < se usa en lugar de <=, de modo que si es min (x, y) = x y después Max (x, y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes que se van a comparar con *SRC1*.<br/>                                                                                                                                                     |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los componentes que se van a comparar con *src0*.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

NaN tiene un tratamiento especial. Si un operando de origen es NaN, se devuelve el otro operando de origen. La elección se realiza por componente. Si ambos son NaN, se devuelve cualquier representación NaN.

El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw. Las máscaras de *destino* válidas son. XY,. ZW y. xyzw. Las siguientes asignaciones *src* son post-swizzle:

-   *dest* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
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

 

 





