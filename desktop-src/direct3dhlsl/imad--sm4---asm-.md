---
title: imad (sm4 - asm)
description: Entero con signo multiplicado y sumado.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567777"
---
# <a name="imad-sm4---asm"></a>imad (sm4 - asm)

Entero con signo multiplicado y sumado.



| imad dest \[ \] .mask, \[ - \] src0 \[ .swzzle, \] \[ - \] src1 \[ .swzzle, \] \[ - \] src2 \[ .swzzle |
|---------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Valor para multiplicar por *src1.*<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Valor que se va a multiplicar por *src0.*<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] Valor que se va a agregar al producto de *src0* y *src1*.<br/> |



 

## <a name="remarks"></a>Observaciones

Imul [](imul--sm4---asm-.md) por componente de operandos de 32 bits *src0* y *src1* (con firma), manteniendo un mínimo de 32 bits (por componente) del resultado, seguido de [un iadd](iadd--sm4---asm-.md) de *src2,* que genera el resultado de 32 bits bajo (por componente) correcto. Los resultados de 32 bits se colocan en *dest*.

El modificador negate opcional en operandos de origen toma el complemento de 2 antes de realizar la operación aritmética.

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

 

 





