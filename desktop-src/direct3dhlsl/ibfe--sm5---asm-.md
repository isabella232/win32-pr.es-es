---
title: ibfe (sm5 - asm)
description: Dado un intervalo de bits en un número, cambie esos bits al LSB y el signo extienda el MSB del intervalo.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b04bfcaea154a8a63e9b118da12a8994398357b7c6a022a4589353c6c06eb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949625"
---
# <a name="ibfe-sm5---asm"></a>ibfe (sm5 - asm)

Dado un intervalo de bits en un número, cambie esos bits al LSB y el signo extienda el MSB del intervalo.



| ibfe dest \[ .mask \] , src0 \[ .swzzle, \] src1 \[ .sw sw \] zzle, src2 \[ .swzzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El ancho del campo de bits.<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Desplazamiento del campo de bits.<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] El valor que se desplazará.<br/>                          |



 

## <a name="remarks"></a>Comentarios

Los 5 bits LSB de src0 proporcionan el ancho del campo de bits (0-31).

Los 5 bits LSB de src1 proporcionan el desplazamiento del campo de bits (0-31).

En el ejemplo siguiente se muestra cómo usar esta instrucción.

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

Use esta instrucción para desempaquetar enteros o marcas con signo.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





