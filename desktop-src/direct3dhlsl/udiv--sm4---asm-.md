---
title: UDIV (SM4-ASM)
description: División de enteros sin signo.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419929"
---
# <a name="udiv-sm4---asm"></a>UDIV (SM4-ASM)

División de enteros sin signo.



| UDIV destQUOT \[ . Mask \] , destREM \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                   | Descripción                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[en \] la dirección del cociente resultante.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[en \] la dirección del resto resultante.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[en \] los componentes que se van a dividir por *SRC1*.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/>                                        | \[en \] los componentes de whch para dividir *src0*.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una división sin signo de modo de componente del operando de 32 bits *src0* por el operando de 32 bits *SRC1*. Los resultados de las divisiones son los cocientes de 32 bits colocados en *destQUOT* y los restos de 32 bits colocados en *destREM*.

La división por cero devuelve 0xFFFFFFFF para el cociente y el resto.

Puede especificar *destQUOT* o *destREM* como null en lugar de especificar un registro, si no se necesita el cociente o el resto.

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

 

 





