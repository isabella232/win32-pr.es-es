---
title: deq (sm5 - asm)
description: Comparación de igualdad de precisión doble por componente.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ed263deec975815f29050d2de0a877a312258c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360818"
---
# <a name="deq-sm5---asm"></a>deq (sm5 - asm)

Comparación de igualdad de precisión doble por componente.



| deq \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw sw maskle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes que se comparan con *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Los componentes que se comparan con *src0.*<br/>         |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza la comparación de punto flotante de precisión doble (*src0*  ==  *src1*) para cada componente y escribe el resultado en *dest*.

Si la comparación es verdadera, se devuelven 0xFFFFFFFF de 32 bits para ese componente. De lo contrario, se devuelven 0x00000000 de 32 bits.

La comparación con NaN devuelve false.

Las *máscaras dest* válidas son uno o dos componentes. Es decir: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw El primer componente *dest* de la máscara recibe el resultado de 32 bits para la primera comparación doble. El segundo componente de la máscara, si está presente, recibe el resultado de 32 bits para la segunda comparación doble.

Los swzzles válidos para los parámetros de origen son .xyzw, .xyxy, .zwxy, .zwzw. Las siguientes *asignaciones de src* son posteriores a swconfle:

-   *src0* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src1* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





