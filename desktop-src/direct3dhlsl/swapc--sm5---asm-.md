---
title: swapc (SM5-ASM)
description: Realiza un intercambio condicional en componentes de los valores entre dos registros de entrada.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996912"
---
# <a name="swapc-sm5---asm"></a>swapc (SM5-ASM)

Realiza un intercambio condicional en componentes de los valores entre dos registros de entrada.



| swapc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                               | Descripción                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[en \] el registro con máscaras de escritura no vacías arbitrarias. Debe ser diferente de *dest1*.<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[en \] el registro con máscaras de escritura no vacías arbitrarias. Debe ser diferente de *dest0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[en \] proporciona 4 condiciones. Un valor entero distinto de cero significa **true**. <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/>    | \[en \] uno de los valores que se van a intercambiar.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/>    | \[en \] uno de los valores que se van a intercambiar.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

La codificación de esta instrucción intenta expresar de forma compacta varios intercambios condicionales paralelos de escalares en registros de componentes 2 4, con una flexibilidad menor en la disposición de los pares de números implicados en el intercambio.

La elección del registro y el valor para *src0*, *SRC1* y *src2* no están restringidos de ningún modo, como [MOVC](movc--sm4---asm-.md).

La semántica de esta instrucción se puede describir mediante las operaciones equivalentes con la instrucción **MOVC** . El peor de los casos se muestra en el ejemplo siguiente, asegurándose de que los registros de destino no se actualizan hasta el final.

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

Puede elegir cómo abordar la tarea, si no directamente. Por ejemplo, se puede lograr el mismo efecto mediante una secuencia de hasta 4 intercambios condicionales simples escalares, o como arriba, dos instrucciones **MOVC** vectoriales, además de cualquier sobrecarga para asegurarse de que los valores de origen no se clobbered por operaciones anteriores en medio de la expansión.

Use esta instrucción para la ordenación.

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

 

 





