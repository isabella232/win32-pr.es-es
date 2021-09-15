---
title: imul (sm4 - asm)
description: Multiplicar entero con signo.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567764"
---
# <a name="imul-sm4---asm"></a>imul (sm4 - asm)

Multiplicar entero con signo.



| imul destHI \[ .mask \] , destLO \[ \] .mask, \[ - \] src0 \[ .swhible, \] \[ - \] src1 \[ .swhible\] |
|-------------------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[en \] La dirección de los 32 bits altos del resultado.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[en \] La dirección de los 32 bits inferiores del resultado.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[en \] El valor que se va a multiplicar por *src1.*<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[en \] El valor que se va a multiplicar por *src0.*<br/>             |



 

## <a name="remarks"></a>Observaciones

Multiplicación por componente de operandos de 32 bits *src0* y *src1* (ambos están firmados), lo que genera el resultado correcto completo de 64 bits (por componente). Los 32 bits bajos (por componente) se colocan *en destLO.* Los 32 bits altos (por componente) se colocan *en destHI.*

*DestHI* o *destLO* se pueden especificar como NULL en lugar de especificar un registro, si no se necesitan los 32 bits altos o bajos del resultado de 64 bits.

El modificador negate opcional en operandos de origen toma el complemento de 2 antes de realizar la operación aritmética.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





