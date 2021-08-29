---
title: dge (sm5 - asm)
description: Comparación de precisión doble por componente mayor o igual que.
ms.assetid: 2E769077-E861-4EFA-817F-7D1AE998746C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffe30c2ef0b2b8d3e8f4b8c9b200ab1685ff45342f7ae1d30ca490dbff01f149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855235"
---
# <a name="dge-sm5---asm"></a>dge (sm5 - asm)

Comparación de precisión doble por componente mayor o igual que.



| dge \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .swzzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | Componentes que se comparan con *src1.*<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | Componentes que se comparan con *src0.*<br/>                |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza la comparación de punto flotante de precisión doble (*src0*  >=  *src1*) para cada componente y escribe el resultado en *dest*.

Si la comparación es verdadera, se devuelven 0xFFFFFFFF de 32 bits para ese componente. De lo contrario, se devuelve 0x00000000 de 32 bits.

La comparación con NaN devuelve false.

Las máscaras *dest* válidas son uno o dos componentes. Es decir: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw El primer componente *dest* de la máscara recibe el resultado de 32 bits para la primera comparación doble. El segundo componente de la máscara, si está presente, recibe el resultado de 32 bits para la segunda comparación doble.

Los swzzles válidos para los parámetros de origen son .xyzw, .xyxy, .zwxy, .zwzw. Las siguientes *asignaciones de src* son posteriores a swzzle:

-   *src0* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src1* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





