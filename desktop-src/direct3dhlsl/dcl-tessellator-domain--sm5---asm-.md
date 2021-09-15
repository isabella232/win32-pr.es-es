---
title: dcl_tessellator_domain (sm5 - asm)
description: Declare el dominio del teselador en una sección de declaración del sombreador de casco y el sombreador de dominio.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573896"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>dominio \_ de tessellator \_ dcl (sm5 - asm)

Declare el dominio del teselador en una sección de declaración del sombreador de casco y el sombreador de dominio.



| dcl \_ tessellator \_ domain {domain \_ isoline \| domain \_ tri \| domain \_ quad} |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                | Descripción                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*quad \_ de dominio tri de dominio \| \_ \| isolínea de \_ dominio*<br/> | \[en \] El dominio.<br/> |



 

## <a name="remarks"></a>Observaciones

El comportamiento no está definido si el sombreador de casco y el sombreador de dominio proporcionan dominios que no coincide o cualquier otra descalarización en conflicto.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco                 | Domain | Geometría | Píxel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Sección Declaraciones | X      |          |       |         |



 

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

 

 





