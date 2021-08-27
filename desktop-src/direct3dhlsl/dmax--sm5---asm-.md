---
title: dmax (sm5 - asm)
description: Máximo de precisión doble por componente.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6846da6fbf3ad5d42be5131322e1214fc49fe2627b824775798e4527de3d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068375"
---
# <a name="dmax-sm5---asm"></a>dmax (sm5 - asm)

Máximo de precisión doble por componente.



| dmax \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw swzzle\] |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> *dest*  =  *src0*  >=  *src1* ? *src0:* *src1*<br/> >= se usa en lugar de > para que si min(x,y) = x, max(x,y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El valor que se va a comparar con *src1*.<br/>                                                                                                                                                           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] El valor que se va a comparar con *src0*.<br/>                                                                                                                                                           |



 

## <a name="remarks"></a>Comentarios

NaN tiene un control especial. Si un operando de origen es NaN, se devuelve el otro operando de origen. La elección se realiza por componente. Si ambos son NaN, se devuelve cualquier representación de NaN.

Los swzzles válidos para los parámetros de origen son .xyzw, .xyxy, .zwxy, .zwzw. Las máscaras *dest* válidas son .xy, .zw y .xyzw. Las siguientes *asignaciones de src* son posteriores a swzzle:

-   *dest* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
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

 

 





