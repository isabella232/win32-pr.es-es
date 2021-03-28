---
title: BFI (SM5-ASM)
description: Dado un intervalo de bits del LSB de un número, coloque el número de bits en otro número en cualquier desplazamiento.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077106"
---
# <a name="bfi-sm5---asm"></a>BFI (SM5-ASM)

Dado un intervalo de bits del LSB de un número, coloque el número de bits en otro número en cualquier desplazamiento.



| BFI dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle \] , src3 \[ . swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los resultados.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el ancho del campo de bits que se tomará de *src2*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el desplazamiento de bits para reemplazar bits en *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] el número desde el que se toman los bits. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[en \] el número de bits que se va a reemplazar.<br/>              |



 

## <a name="remarks"></a>Observaciones

Los LSB 5 bits de *src0* proporcionan el ancho del campo de bits (0-31) que se va a tomar de *src2*.

Los 5 bits LSB de *SRC1* proporcionan el desplazamiento de bits de bits (0-31) para empezar a reemplazar los bits en el número leído de *src3*.

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Esta instrucción se usa para empaquetar enteros o marcas.

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

 

 





