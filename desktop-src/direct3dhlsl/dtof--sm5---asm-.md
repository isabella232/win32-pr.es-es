---
title: dtof (SM5-ASM)
description: Conversión de componentes de datos de punto flotante de precisión doble en datos de punto flotante de precisión sencilla.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358469"
---
# <a name="dtof-sm5---asm"></a>dtof (SM5-ASM)

Conversión de componentes de datos de punto flotante de precisión doble en datos de punto flotante de precisión sencilla.



| dtof dest \[ . Mask \] , \[ - \] src \[ . swizzle \] , |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los datos convertidos.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los datos que se van a convertir.<br/>          |



 

## <a name="remarks"></a>Observaciones

Cada componente del origen se convierte a partir de la representación de precisión doble en la representación de precisión sencilla mediante el redondeo de redondeo a la más cercana.

El swizzles válido para el parámetro de origen es. xyzw,. xyxy,. zwxy,. zwzw.

Las máscaras de *destino* válidas son uno o dos componentes. Es decir:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. YW,. ZW el resultado de la primera conversión va al primer componente de la máscara, y el resultado del segundo componente entra en el segundo componente de la máscara, si está presente.

los componentes de *dest* son float32.

*src* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB) post swizzle.

En el caso de las conversiones de tipo float32<->Double, las implementaciones pueden aceptar desnormativas float32 o vaciarlas.

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

 

 





