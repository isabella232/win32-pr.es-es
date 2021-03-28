---
title: XOR (SM4-ASM)
description: XOR bit a bit.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419887"
---
# <a name="xor-sm4---asm"></a>XOR (SM4-ASM)

XOR bit a bit.



| XOR dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación.<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes de a XOR con *SRC1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los componentes de a XOR con *src0*.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una XOR lógica lógica de componentes de cada par de valores de 32 bits de *src0* y *SRC1*. los resultados de 32 bits se colocan en el *destino*.

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

 

 





