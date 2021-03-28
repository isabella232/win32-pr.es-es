---
title: dcl_tessellator_domain (SM5-ASM)
description: Declare el dominio del teselador en una sección de declaración del sombreador de casco y en el sombreador de dominios.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419984"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>\_ \_ dominio de del teselador de DCL (SM5-ASM)

Declare el dominio del teselador en una sección de declaración del sombreador de casco y en el sombreador de dominios.



| \_dominio del teselador de DCL \_ {dominio \_ Isoline \| dominio \_ Tri \| dominio \_ cuádruple} |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                | Descripción                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*dominio \_ Isoline \| dominio \_ Tri \| dominio \_ cuádruple*<br/> | \[en \] el dominio.<br/> |



 

## <a name="remarks"></a>Observaciones

El comportamiento es indefinido si el sombreador de casco y el sombreador de dominios proporcionan dominios que no coinciden o cualquier otro decalarations en conflicto.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco                 | Dominio | Geometría | Píxel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Sección declaraciones | X      |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





