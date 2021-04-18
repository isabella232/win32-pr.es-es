---
title: UMUL (SM4-ASM)
description: Multiplicación de enteros sin signo.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419927"
---
# <a name="umul-sm4---asm"></a>UMUL (SM4-ASM)

Multiplicación de enteros sin signo.



| UMUL destHI \[ . Mask \] , destLO \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[en \] los bits 32 altos del resultado, por componente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[en \] los bits 32 inferiores del resultado, por componente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[en \] los componentes por los que se va a multiplicar *SRC1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/>                                | \[en \] los componentes por los que se va a multiplicar *src0*.<br/>    |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una multiplicación por componentes de operandos de 32 bits sin signo *src0* y *SRC1*, lo que produce el resultado de 64 bits completo correcto por componente. Los bits inferiores 32 por componente se colocan en *destLO*. Los altos 32 bits por componente se colocan en *destHI*.

Puede especificar *destHI* o *destLO* como null en lugar de especificar un registro si no se necesitan los bits superiores o inferiores 32 del resultado de 64 bits.

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

 

 





