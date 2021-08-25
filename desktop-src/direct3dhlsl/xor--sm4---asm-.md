---
title: xor (sm4 - asm)
description: XOR bit a bit.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a4dae86a4c6ade427b749c2bb72974564b8a4b7a6baae6821edb3c0d63b2164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892415"
---
# <a name="xor-sm4---asm"></a>xor (sm4 - asm)

XOR bit a bit.



| xor dest \[ .mask \] , src0 \[ .swzzle, \] src1 \[ .sw swzzle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Componentes de XOR con *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Los componentes de XOR con *src0*.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza un XOR lógico por componente de cada par de valores de 32 bits de *src0* y *src1.* Los resultados de 32 bits se colocan *en dest*.

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

 

 





