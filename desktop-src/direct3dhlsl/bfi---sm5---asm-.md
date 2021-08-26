---
title: bfi (sm5 - asm)
description: Dado un intervalo de bits del LSB de un número, coloque ese número de bits en otro número en cualquier desplazamiento.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1452b1f15525753738ee6f74a1bd43473f43033346c9b493cd72222eaab22cb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068535"
---
# <a name="bfi-sm5---asm"></a>bfi (sm5 - asm)

Dado un intervalo de bits del LSB de un número, coloque ese número de bits en otro número en cualquier desplazamiento.



| bfi dest \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle, \] src2 \[ .swzzle, \] src3 \[ .swzzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El ancho del campo de bits que se va a tomar de *src2*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Desplazamiento del campo de bits para reemplazar bits en *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] El número del que se toman los bits. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[en \] Número con bits que se reemplazarán.<br/>              |



 

## <a name="remarks"></a>Comentarios

Los 5 bits LSB de *src0* proporcionan el ancho del campo de bits (0-31) que se va a tomar de *src2.*

Los 5 bits LSB de *src1* proporcionan el desplazamiento del campo de bits (0-31) para empezar a reemplazar los bits en el número leído de *src3.*

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Esta instrucción se usa para empaquetar enteros o marcas.

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

 

 





