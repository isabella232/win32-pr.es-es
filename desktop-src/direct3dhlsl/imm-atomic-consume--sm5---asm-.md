---
title: imm_atomic_consume (SM5-ASM)
description: Disminuya de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el nuevo valor.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996932"
---
# <a name="imm_atomic_consume-sm5---asm"></a>IMM \_ Atomic \_ consume (SM5-ASM)

Disminuya de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el nuevo valor.



| IMM \_ Atomic \_ consumo dst0 \[ . \_ \_ máscara de componente único \] , dstUAV |
|---------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[en \] contiene el valor del contador original devuelto.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] un búfer estructurado UAV con la marca Count o Append. <br/> |



 

## <a name="remarks"></a>Observaciones

Vea [la \_ \_ asignación atómica de IMM](imm-atomic-alloc--sm5---asm-.md) para obtener una explicación sobre la validez del valor de recuento devuelto en función de si UAV es Count o Append. Lo mismo se aplica para el **\_ \_ consumo atómico de IMM**.

**el \_ \_ consumo atómico de IMM** realiza una reducción atómica del valor del contador y devuelve el nuevo valor a *dst0*.

No hay ninguna compresión del recuento, por lo que se ajusta en el subdesbordamiento.

El mismo sombreador no puede intentar usar la **\_ \_ asignación atómica de IMM** y el **IMM \_ atómico \_** en el mismo UAV. Además, la GPU no puede permitir que varias invocaciones del sombreador mezclen la **\_ \_ asignación atómica de IMM** y el **IMM atómico de IMM \_ \_** en el mismo UAV.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





