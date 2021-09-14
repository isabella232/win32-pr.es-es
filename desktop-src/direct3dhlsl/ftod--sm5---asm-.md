---
title: ftod (sm5 - asm)
description: Conversión por componente de datos de punto flotante de precisión sencilla a datos de punto flotante de precisión doble.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361573"
---
# <a name="ftod-sm5---asm"></a>ftod (sm5 - asm)

Conversión por componente de datos de punto flotante de precisión sencilla a datos de punto flotante de precisión doble.



| ftod dest \[ .mask \] , \[ - \] src \[ .swzzle \] , |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los datos convertidos.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los datos que se convertirán.<br/>          |



 

## <a name="remarks"></a>Observaciones

Cada componente del origen se convierte de la representación de precisión sencilla a la representación de precisión doble.

Las máscaras *dest* válidas son .xy, .zw y .xyzw. .xy recibe el resultado de la primera conversión y .zw recibe el resultado de la segunda conversión.

*dest* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).

*src* es un vec2 flotante entre x e y (zw omitido) (después de swzzle).

Para las conversiones<->float32, las implementaciones pueden respetar los desnormados float32 o vaciarlos.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





