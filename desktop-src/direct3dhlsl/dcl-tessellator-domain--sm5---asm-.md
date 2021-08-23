---
title: dcl_tessellator_domain (sm5 - asm)
description: Declare el dominio de teselador en una sección de declaración de sombreador de casco y el sombreador de dominio.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a027e9fab091cf31e8577266015e974ec78033fe19a9542f0aa3c6ca4651db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986715"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>Dominio \_ de tessellator \_ dcl (sm5 - asm)

Declare el dominio de teselador en una sección de declaración de sombreador de casco y el sombreador de dominio.



| dcl \_ tessellator \_ domain {domain \_ isoline \| domain \_ tri \| domain \_ quad} |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                | Descripción                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*quad \_ de dominio tri de dominio \| \_ \| isolínea de \_ dominio*<br/> | \[en \] El dominio.<br/> |



 

## <a name="remarks"></a>Comentarios

El comportamiento es indefinido si el sombreador de casco y el sombreador de dominio proporcionan dominios no coincidentes o cualquier otra descalarización en conflicto.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco                 | Domain | Geometría | Píxel | Proceso |
|--------|----------------------|--------|----------|-------|---------|
|        | Sección Declaraciones | X      |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





