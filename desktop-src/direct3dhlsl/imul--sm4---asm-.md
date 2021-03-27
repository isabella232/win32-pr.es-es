---
title: imul (SM4-ASM)
description: Multiplicación de entero con signo.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784960"
---
# <a name="imul-sm4---asm"></a>imul (SM4-ASM)

Multiplicación de entero con signo.



| imul destHI \[ . Mask \] , destLO \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle\] |
|-------------------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[en \] la dirección de los bits 32 altos del resultado.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[en \] la dirección de los bits 32 inferiores del resultado.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[en \] el valor que se va a multiplicar por *SRC1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/>                                | \[en \] el valor que se va a multiplicar por *src0*.<br/>             |



 

## <a name="remarks"></a>Observaciones

La multiplicación por componentes de operandos de 32 bits *src0* y *SRC1* (ambas están firmadas), lo que produce el resultado de 64 bits completo correcto (por componente). Los bits 32 bajos (por componente) se colocan en *destLO*. Los bits 32 altos (por componente) se colocan en *destHI*.

*DestHI* o *destLO* se pueden especificar como null en lugar de especificar un registro, si no se necesitan los bits superiores o inferiores 32 del resultado de 64 bits.

El modificador opcional Negate en los operandos de origen toma el complemento de 2 antes de realizar la operación aritmética.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





