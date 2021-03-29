---
title: Imad (SM4-ASM)
description: Entero con signo que se multiplica y agrega.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996860"
---
# <a name="imad-sm4---asm"></a>Imad (SM4-ASM)

Entero con signo que se multiplica y agrega.



| Imad dest \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle \] , \[ - \] src2 \[ . swizzle |
|---------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación.<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en el \] valor que se va a multiplicar por *SRC1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en el \] valor que se va a multiplicar por *src0*.<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] valor para agregar al producto de *src0* y *SRC1*.<br/> |



 

## <a name="remarks"></a>Observaciones

[Imul](imul--sm4---asm-.md) de componentes de los operandos de 32 bits *src0* y *SRC1* (signed), manteniendo un mínimo de 32 bits (por componente) del resultado, seguido de un [iadd](iadd--sm4---asm-.md) de *src2*, que genera el resultado correcto de 32 bits (por componente) correcto. Los resultados de 32 bits se colocan en *dest*.

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

 

 





