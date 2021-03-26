---
title: usubb (SM5-ASM)
description: Número entero sin signo que se resta con el préstamo.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419891"
---
# <a name="usubb-sm5---asm"></a>usubb (SM5-ASM)

Número entero sin signo que se resta con el préstamo.



| usubb dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                               | Descripción                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[en \] contiene los resultados de LSAB de la instrucción.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[en \] el componente correspondiente de *dest0* que especifica si se ha producido un préstamo.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[en \] el valor del que se va a restar.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/>    | \[en \] la cantidad que se va a restar de *src0*.<br/>                                             |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una resta sin signo de modo de componente de operandos de 32 bits *SRC1* de *src0*, y coloca la parte LSB del resultado de 32 bits en *dest0*.

El componente correspondiente de *dest1* se escribe con 1 si se produce un préstamo; de lo contrario, devuelve 0.

*dest1* puede ser null si no se necesita el préstamo.

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

 

 





