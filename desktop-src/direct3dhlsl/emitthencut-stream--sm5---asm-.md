---
title: emitThenCut_stream (sm5 - asm)
description: Equivalente a un comando de emisión seguido de un comando de corte. | emitThenCut_stream (sm5 - asm)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241617"
---
# <a name="emitthencut_stream-sm5---asm"></a>emitThenCut \_ stream (sm5 - asm)

Equivalente a un [comando de emisión](emit--sm4---asm-.md) seguido de un comando [de](cut--sm4---asm-.md) corte.



| emitThenCut \_ stream streamIndex |
|---------------------------------|



 



| Elemento                                                                                                               | Descripción                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[en \] El índice de secuencia.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta operación es útil cuando se genera a sabiendas el último vértice de una topología.

Si no se han declarado secuencias, debe usar [emitThenCut](emitthencut--sm4---asm-.md) en lugar de **emitThenCut. \_**

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





