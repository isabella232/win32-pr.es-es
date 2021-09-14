---
title: umul (sm4 - asm)
description: Número entero sin signo multiplicado.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063676"
---
# <a name="umul-sm4---asm"></a>umul (sm4 - asm)

Número entero sin signo multiplicado.



| umul destHI \[ \] .mask, destLO \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle\] |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[en \] Los 32 bits superiores del resultado, por componente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[en \] los 32 bits inferiores del resultado, por componente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[en \] Componentes por los que se va a multiplicar *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[en \] Componentes por los que se va a multiplicar *src0*.<br/>    |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una multiplicación por componente de operandos de 32 bits sin signo *src0* y *src1,* lo que genera el resultado completo correcto de 64 bits por componente. Los 32 bits inferiores por componente se colocan *en destLO*. Los 32 bits altos por componente se colocan *en destHI*.

Puede especificar *destHI* o *destLO* como NULL en lugar de especificar un registro si no se necesitan los 32 bits altos o bajos del resultado de 64 bits.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





