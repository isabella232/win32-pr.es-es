---
title: umad (sm4 - asm)
description: Entero sin signo multiplicado y sumado.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6a6c649a61c78eebee249b9fec5c032a07a8a0761a3d23d6e45da573be122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405995"
---
# <a name="umad-sm4---asm"></a>umad (sm4 - asm)

Entero sin signo multiplicado y sumado.



| umad dest \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle, \] src2 \[ .swzzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Valor que se va a multiplicar por *src1.*<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Valor que se va a multiplicar por *src1.*<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] El valor que se va a agregar al producto de *src0* y *src1*.<br/> |



 

## <a name="remarks"></a>Comentarios

Umul [por componente](umul--sm4---asm-.md) de operandos de 32 bits *src0* y *src1* sin signo, manteniendo los 32 bits bajos, por componente, del resultado. A continuación, esta instrucción realiza un [iadd](iadd--sm4---asm-.md) de *src2,* lo que genera el resultado de 32 bits bajo (por componente) correcto. Los resultados de 32 bits se colocan en *dest*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





