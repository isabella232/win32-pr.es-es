---
title: dcl_hs_max_tessfactor (sm5 - asm)
description: Declare maxTessFactor para la revisión.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573945"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a>dcl \_ hs \_ max \_ tessfactor (sm5 - asm)

Declare maxTessFactor para la revisión.



| dcl \_ hs \_ max \_ tessfactor n |
|----------------------------|



 



| Elemento                                                   | Descripción                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="n"></span><span id="N"></span>*N*<br/> | \[en \] MaxTessFactor.<br/> |



 

## <a name="remarks"></a>Observaciones

maxTessFactor es un valor float32 en el intervalo {1,0 ... 64.0}.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





