---
title: Umad (SM4-ASM)
description: Entero sin signo de multiplicación y suma.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784930"
---
# <a name="umad-sm4---asm"></a>Umad (SM4-ASM)

Entero sin signo de multiplicación y suma.



| Umad dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el valor que se va a multiplicar por *SRC1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el valor que se va a multiplicar por *SRC1*.<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] el valor que se va a agregar al producto de *src0* y *SRC1*.<br/> |



 

## <a name="remarks"></a>Observaciones

[UMUL](umul--sm4---asm-.md) de componentes de los operandos de 32 bits *src0* y *SRC1* sin signo, manteniendo los 32 bits inferiores, por componente, del resultado. A continuación, esta instrucción realiza una [iadd](iadd--sm4---asm-.md) de *src2*, lo que genera el resultado correcto de 32 bits (por componente). Los resultados de 32 bits se colocan en *dest*.

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

 

 





