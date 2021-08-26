---
title: udiv (sm4 - asm)
description: División de enteros sin signo.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b1320d0518034129efe2222a42aa2694df0422db524da0714377cb43a2b9a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948985"
---
# <a name="udiv-sm4---asm"></a>udiv (sm4 - asm)

División de enteros sin signo.



| udiv destQUOT \[ .mask \] , destREM \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                   | Descripción                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[en \] La dirección del cociente resultante.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[en \] La dirección del resto resultante.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[en \] Los componentes que se dividirán por *src1*.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[en \] Los componentes por whch para dividir *src0*.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza una división sin signo por componente del operando de 32 bits *src0* por el operando de 32 bits *src1*. Los resultados de las divisiones son los cocientes de 32 bits colocados en *destQUOT* y los restos de 32 bits colocados *en destREM*.

Dividir por cero devuelve 0xffffffff para cociente y resto.

Puede especificar *destQUOT* o *destREM* como NULL en lugar de especificar un registro, si el cociente o el resto no son necesarios.

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

 

 





