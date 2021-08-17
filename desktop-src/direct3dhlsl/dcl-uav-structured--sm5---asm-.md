---
title: dcl_uav_structured (sm5 - asm)
description: Declare una vista de acceso no ordenado (UAV) para que la use un sombreador. | dcl_uav_structured (sm5 - asm)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b398dc8b59db6d8fc3a64effdf3cd93b56664881c4c7024a185ad6a212b9fb4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726803"
---
# <a name="dcl_uav_structured-sm5---asm"></a>dcl \_ uav \_ estructurado (sm5 - asm)

Declare una vista de acceso no ordenado (UAV) para que la use un sombreador.



| dcl \_ uav \_ structured \[ \_ glc \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descripción                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[en \] el UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[en \] Tamaño de la estructura en bytes.<br/> |



 

## <a name="remarks"></a>Comentarios

*dstUAV* es un registro u declarado como referencia a UnorderedAccessView de un búfer estructurado con el intervalo especificado que debe enlazarse a la ranura UAV en la \# \# API.

El contenido de la estructura no tiene ningún tipo; Las operaciones realizadas en la memoria pueden interpretar implícitamente que los datos tienen un tipo .

*structByteStride* es el tamaño de la estructura en bytes en el búfer que se declara. Este valor debe ser mayor que cero. *structByteStride* es de tipo uint y debe ser un múltiplo de 4.

Las instrucciones que hacen referencia a una u estructurada toman una dirección 2D, donde el primer componente elige struct y el segundo componente elige el desplazamiento dentro de \# \[ struct, en bytes \] \[ alineados \] .

La \_ marca glc significa "globalmente coherente". La ausencia de glc significa que el UAV se declara solo como "coherente de grupo" en el sombreador de proceso o "coherente localmente" en una invocación de sombreador de \_ píxeles único.

La \_ marca opc es el contador que conserva el orden. Indica que si un UAV está enlazado a la ranura (u ), se debe haber \# creado con la marca \# COUNTER. Esto significa que las operaciones de consumo atómico [ \_ \_ de imm atomic](imm-atomic-alloc--sm5---asm-.md) o [imm \_ \_ ](imm-atomic-consume--sm5---asm-.md) en el sombreador manipulan un contador cuyos valores se pueden usar en el sombreador como referencia permanente a una ubicación en el UAV. Los datos no se pueden reordenar una vez que el sombreador ha terminado.

La ausencia de la marca opc significa que si el sombreador usa instrucciones de consumo atómico de imm o imm atomic y un UAV está enlazado a la ranura (u), se debe haber creado con la marca APPEND, que proporciona un contador que no garantiza que el orden se conserve después de la invocación del \_ [ \_ \_ ](imm-atomic-alloc--sm5---asm-.md) [ \_ \_ ](imm-atomic-consume--sm5---asm-.md) \# sombreador.

Si la marca opc no está presente y el sombreador no contiene instrucciones de consumo atómico de imm o atómico \_ de [ \_ \_ imm,](imm-atomic-alloc--sm5---asm-.md) [ \_ \_ ](imm-atomic-consume--sm5---asm-.md) se permite que se haya creado un UAV enlazado a la ranura (u) con la marca COUNTER (el contador no se utilizará en este sombreador), ninguna marca (sin contador), pero no con la \# marca APPEND.

> [!Note]  
> cs \_ 4 \_ 0 y cs \_ 4 \_ 1 **admiten dcl \_ tgsm \_ estructurado,** pero no [dcl \_ tgsm \_ raw](dcl-tgsm-raw--sm5---asm-.md).

 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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



 

> [!Note]  
> Esta instrucción se admite en cs \_ 4 \_ 0 y cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





