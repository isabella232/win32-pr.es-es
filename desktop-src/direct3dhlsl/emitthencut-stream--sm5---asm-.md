---
title: emitThenCut_stream (sm5 - asm)
description: Equivalente a un comando emit seguido de un comando de corte. | emitThenCut_stream (sm5 - asm)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d2be28ae1d63617b8ba775f8f8839c270668aeeded8a4944ef9ae7554d598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067965"
---
# <a name="emitthencut_stream-sm5---asm"></a>emitThenCut \_ stream (sm5 - asm)

Equivalente a un [comando de](emit--sm4---asm-.md) emisión seguido de un [comando de](cut--sm4---asm-.md) corte.



| emitThenCut \_ stream streamIndex |
|---------------------------------|



 



| Elemento                                                                                                               | Descripción                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[en \] El índice de la secuencia.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta operación es útil al generar a sabiendas el último vértice de una topología.

Si no se han declarado secuencias, debe usar [emitThenCut](emitthencut--sm4---asm-.md) en lugar de **emitThenCut \_ stream**.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





