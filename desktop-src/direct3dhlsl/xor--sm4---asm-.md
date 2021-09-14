---
title: xor (sm4 - asm)
description: Xor bit a bit.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966411"
---
# <a name="xor-sm4---asm"></a>xor (sm4 - asm)

Xor bit a bit.



| xor dest \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes de XOR con *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Componentes de XOR con *src0*.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un XOR lógico por componente de cada par de valores de 32 bits de *src0* y *src1.* Los resultados de 32 bits se colocan *en dest*.

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

 

 





