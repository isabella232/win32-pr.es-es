---
title: emitThenCut (sm4 - asm)
description: Equivalente a un comando emit seguido de un comando de corte. | emitThenCut (sm4 - asm)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab83fa3eca853a75dca74ef32116e3d13da2dbe76f34fa407f9b0d5f2459d66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023865"
---
# <a name="emitthencut-sm4---asm"></a>emitThenCut (sm4 - asm)

Equivalente a un [comando de](emit--sm4---asm-.md) emisión seguido de un [comando de](cut--sm4---asm-.md) corte.



| emitThenCut |
|-------------|



 

## <a name="remarks"></a>Comentarios

Este comando es útil al generar a sabiendas el último vértice de una topología.

Si se han declarado secuencias, debe usar [emitthencut \_ stream](emitthencut-stream--sm5---asm-.md).

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




