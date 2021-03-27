---
title: ubfe (SM5-ASM)
description: Dado un intervalo de bits en un número, desplace esos bits a LSB y establezca los bits restantes en 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904286"
---
# <a name="ubfe-sm5---asm"></a>ubfe (SM5-ASM)

Dado un intervalo de bits en un número, desplace esos bits a LSB y establezca los bits restantes en 0.



| ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] contiene los resultados de la instrucción.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] LSB 5 bits, proporcione el ancho de campo de bits (0-31).<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los 5 bits LSB de *SRC1* , proporcione el desplazamiento de campo de bits (0-31).<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] el número que se va a desplazar.<br/>                                         |



 

## <a name="remarks"></a>Observaciones

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

Use esta instrucción para desempaquetar los enteros o marcas sin signo.

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

 

 





