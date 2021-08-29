---
title: dcl_hs_max_tessfactor (sm5 - asm)
description: Declare maxTessFactor para la revisión.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1a11ddea971aca1d8e8d379f6c245fd78736ba6c73cf41a3e1d34167956fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606185"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a>dcl \_ hs \_ max \_ tessfactor (sm5 - asm)

Declare maxTessFactor para la revisión.



| dcl \_ hs \_ max \_ tessfactor n |
|----------------------------|



 



| Elemento                                                   | Descripción                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="n"></span><span id="N"></span>*N*<br/> | \[en \] MaxTessFactor.<br/> |



 

## <a name="remarks"></a>Comentarios

maxTessFactor es un valor float32 en el intervalo {1,0 ... 64.0}.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





