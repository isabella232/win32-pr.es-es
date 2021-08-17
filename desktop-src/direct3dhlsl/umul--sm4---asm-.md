---
title: umul (sm4 - asm)
description: Entero sin signo multiplicado.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec63b3a95ffbdf1f71142c9fc508e21e718b44d988b725dad5d73775746871c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721839"
---
# <a name="umul-sm4---asm"></a>umul (sm4 - asm)

Entero sin signo multiplicado.



| umul destHI \[ .mask \] , destLO \[ \] .mask, src0 \[ .swhible, \] src1 \[ .swhible\] |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[en \] los 32 bits altos del resultado, por componente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[en \] los 32 bits inferiores del resultado, por componente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[en \] Los componentes por los que se va a multiplicar *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[en \] Los componentes por los que se va a multiplicar *src0*.<br/>    |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza una multiplicación por componente de operandos de 32 bits sin signo *src0* y *src1,* lo que genera el resultado completo correcto de 64 bits por componente. Los 32 bits inferiores por componente se colocan *en destLO.* Los 32 bits altos por componente se colocan en *destHI.*

Puede especificar *destHI* o *destLO* como NULL en lugar de especificar un registro si no se necesitan los 32 bits altos o bajos del resultado de 64 bits.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





