---
title: imad (sm4 - asm)
description: Entero con signo, multiplique y agregue.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d8222e613b94481dd58bc6315ef4e7558ed5bad7b58ad5aca021b32f4fcf10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982415"
---
# <a name="imad-sm4---asm"></a>imad (sm4 - asm)

Entero con signo, multiplique y agregue.



| imad dest \[ .mask \] , \[ - \] src0 \[ .swzzle, \] \[ - \] src1 \[ .sw sw \] zzle, \[ - \] src2 \[ .swzzle |
|---------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Valor para multiplicar por *src1.*<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Valor que se va a multiplicar por *src0.*<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] Valor que se va a agregar al producto de *src0* y *src1.*<br/> |



 

## <a name="remarks"></a>Comentarios

Imul [](imul--sm4---asm-.md) por componente de operandos de 32 bits *src0* y *src1* (con firma), lo que mantiene un mínimo de 32 bits (por componente) del resultado, seguido de un [iadd](iadd--sm4---asm-.md) de *src2,* que genera el resultado de 32 bits (por componente) bajo correcto. Los resultados de 32 bits se colocan en *dest*.

El modificador negate opcional en operandos de origen toma el complemento de 2 antes de realizar la operación aritmética.

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

 

 





