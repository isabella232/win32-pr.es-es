---
title: y (SM4-ASM)
description: AND bit a bit.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784979"
---
# <a name="and-sm4---asm"></a>y (SM4-ASM)

And bit **a** bit.



| y dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el valor de 32 bits en **y** con *SRC1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el valor de 32 bits en **y** con *src0*.<br/>    |



 

## <a name="remarks"></a>Observaciones

Lógica de componentes **y** de cada par de valores de 32 bits de *src0* y *SRC1*. Los resultados de 32 bits se colocan en *dest*.

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

 

 





