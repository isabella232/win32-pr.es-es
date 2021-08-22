---
title: swapc (sm5 - asm)
description: Realiza un intercambio condicional por componente de los valores entre dos registros de entrada.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d09d52bd497c7819500c11c4464907e4a7854bb305ed0e31d53b897ba4cf7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486265"
---
# <a name="swapc-sm5---asm"></a>swapc (sm5 - asm)

Realiza un intercambio condicional por componente de los valores entre dos registros de entrada.



| swapc dest0 \[ \] .mask, dest1 \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle, \] src2 \[ .swzzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                               | Descripción                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[en \] Register with arbitrary nonempty write masks (Registrar con máscaras de escritura no arbitrarias). Debe ser diferente de *dest1.*<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[en \] Register with arbitrary nonempty write masks (Registrar con máscaras de escritura no arbitrarias). Debe ser diferente de *dest0.*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[en \] Proporciona 4 condiciones. Un valor entero distinto de cero significa **true.** <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[en \] Uno de los valores que se va a intercambiar.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/>    | \[en \] Uno de los valores que se va a intercambiar.<br/>                                              |



 

## <a name="remarks"></a>Comentarios

La codificación de esta instrucción intenta expresar de forma compacta varios intercambios condicionales paralelos de escalares en dos registros de 4 componentes, con una pequeña flexibilidad en la organización de los pares de números implicados en el intercambio.

La elección del registro y el valor de *src0,* *src1* y *src2* no están restringidas de ninguna manera, como [movc](movc--sm4---asm-.md).

La semántica de esta instrucción se puede describir mediante las operaciones equivalentes con la **instrucción movc.** El peor de los casos se muestra en el ejemplo siguiente, asegurando de que los registros de destino no se actualizan hasta el final.

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

Puede elegir cómo abordar la tarea, si no directamente. Por ejemplo, el mismo efecto se puede lograr mediante una secuencia de hasta 4 intercambios condicionales escalares simples, o como se mencionó anteriormente, dos instrucciones **movc** vectoriales, además de cualquier sobrecarga para asegurarse de que las operaciones anteriores no atascaban los valores de origen en el entorno de la expansión.

Use esta instrucción para la ordenación.

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

 

 





