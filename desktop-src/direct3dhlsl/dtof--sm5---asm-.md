---
title: dtof (sm5 - asm)
description: Conversión por componente de datos de punto flotante de precisión doble a datos de punto flotante de precisión sencilla.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d16ddf79b1a201bf78e0b45d1206169576bee4193b8c8158469055131768efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792332"
---
# <a name="dtof-sm5---asm"></a>dtof (sm5 - asm)

Conversión por componente de datos de punto flotante de precisión doble a datos de punto flotante de precisión sencilla.



| dtof dest \[ .mask \] , \[ - \] src \[ .swprendle \] , |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los datos convertidos.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los datos que se convertirán.<br/>          |



 

## <a name="remarks"></a>Observaciones

Cada componente del origen se convierte de la representación de precisión doble a la representación de precisión sencilla mediante el redondeo round-to-nearest-even.

Los swzzles válidos para el parámetro de origen son .xyzw, .xyxy, .zwxy, .zwzw.

Las *máscaras dest* válidas son uno o dos componentes. Es decir: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw El resultado de la primera conversión va al primer componente de la máscara y el resultado del segundo componente se encuentra en el segundo componente de la máscara, si está presente.

*Los componentes dest* son float32.

*src* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB) después de swzzle.

Para las conversiones<->float32, las implementaciones pueden respetar los desnormados float32 o vaciarlos.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





