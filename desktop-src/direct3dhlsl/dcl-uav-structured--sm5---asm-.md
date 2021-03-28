---
title: dcl_uav_structured (SM5-ASM)
description: Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280016"
---
# <a name="dcl_uav_structured-sm5---asm"></a>DCL \_ UAV \_ estructurado (SM5-ASM)

Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador.



| DCL \_ UAV \_ Structured \[ \_ GLC \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descripción                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[en \] UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[en \] el tamaño de la estructura, en bytes.<br/> |



 

## <a name="remarks"></a>Observaciones

*dstUAV* es un \# registro u declarado como una referencia a un UnorderedAccessView de un búfer estructurado con el intervalo especificado que se debe enlazar a la ranura UAV \# en la API.

El contenido de la estructura no tiene ningún tipo; las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.

*structByteStride* es el tamaño de la estructura, en bytes, del búfer que se está declarando. Este valor debe ser mayor que cero. *structByteStride* es de tipo uint y debe ser un múltiplo de 4.

Las instrucciones que hacen referencia a una u estructurada \# toman una dirección 2D, donde el primer componente selecciona \[ struct \] , y el segundo componente selecciona \[ desplazamiento dentro de la estructura, en bytes alineados \] .

La \_ marca GLC significa "Globally coherente". La ausencia de \_ GLC significa que el UAV se declara solo como "coherente con el grupo" en el sombreador de cálculo o "localmente coherente" en una invocación del sombreador de un solo píxel.

La \_ marca OPC es el contador de conservar el orden. Indica que, si un UAV está enlazado a \# la ranura (u \# ), se debe haber creado con la marca de contador. Esto significa que las operaciones de consumo [atómico de IMM \_ \_ ](imm-atomic-alloc--sm5---asm-.md) o del [IMM \_ \_ atómico de IMM](imm-atomic-consume--sm5---asm-.md) en el sombreador manipulan un contador cuyos valores se pueden usar en el sombreador como una referencia permanente a una ubicación en el UAV. Los datos no se pueden reordenar una vez que el sombreador ha finalizado.

La ausencia de la \_ marca OPC significa que si el sombreador usa[la \_ \_ asignación atómica de IMM](imm-atomic-alloc--sm5---asm-.md) o las instrucciones de [ \_ \_ consumo atómico de IMM](imm-atomic-consume--sm5---asm-.md) y un UAV está enlazado a la ranura \# (u), se debe haber creado con la marca append, que proporciona un contador que no garantiza que el orden se conserva después de la invocación del sombreador.

Si la \_ marca OPC no está presente y el sombreador no contiene las instrucciones de uso de la [ \_ \_ asignación atómica de IMM](imm-atomic-alloc--sm5---asm-.md) o de [IMM \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) , se permite que se haya creado un UAV enlazado a \# la ranura (u) con la marca de contador (el contador pasará a no usarse por este sombreador), sin marca (ningún contador), pero no con la marca de anexado.

> [!Note]  
> CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten la **\_ TGSM \_ de DCL**, pero no la de [DCL \_ TGSM \_ raw](dcl-tgsm-raw--sm5---asm-.md).

 

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



 

> [!Note]  
> Esta instrucción es compatible con CS \_ 4 \_ 0 y CS \_ 4 \_ 1.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





