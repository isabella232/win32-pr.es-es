---
title: ibfe (sm5 - asm)
description: Dado un intervalo de bits en un número, cambie esos bits al LSB y el signo extienda el MSB del intervalo.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359012"
---
# <a name="ibfe-sm5---asm"></a>ibfe (sm5 - asm)

Dado un intervalo de bits en un número, cambie esos bits al LSB y el signo extienda el MSB del intervalo.



| ibfe dest \[ .mask \] , src0 \[ .swzzle, \] src1 \[ .swzzle \] , src2 \[ .swzzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El ancho del campo de bits.<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Desplazamiento del campo de bits.<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] El valor que se desplazará.<br/>                          |



 

## <a name="remarks"></a>Observaciones

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

Use esta instrucción para desempaquetar marcadores o enteros con signo.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





