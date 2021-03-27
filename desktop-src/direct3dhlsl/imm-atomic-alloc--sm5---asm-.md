---
title: imm_atomic_alloc (SM5-ASM)
description: Incremente de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el valor original.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784961"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>\_asignación atómica \_ de Imm (SM5-ASM)

Incremente de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el valor original.



| \_ \_ dst0 de asignación atómica \[ de IMM \_ . \_ máscara \] de componente único, dstUAV |
|-------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[en \] contiene el valor del contador devuelto.<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] un búfer estructurado UAV con la marca Count o Append. <br/> |



 

## <a name="remarks"></a>Observaciones

Hay un valor de contador de entero de bits sin signo 32 oculto asociado a cada recuento o vista de búfer de anexión que se inicializa cuando la vista está enlazada a la canalización, incluida la opción para mantener el valor anterior.

Esta instrucción realiza un incremento atómico del valor del contador y devuelve el original a *dst0*.

En el caso de Append UAV, el valor devuelto solo es válido para la duración de la invocación del sombreador. después, la implementación puede reorganizar el diseño de memoria. Cualquier direccionamiento de memoria basado en el valor devuelto se debe limitar a la invocación del sombreador.

En el caso de Append UAV, dentro de la invocación del sombreador, el compilador de HLSL puede usar el valor devuelto como índice de estructura que se va a usar para tener acceso al búfer estructurado. El acceso a cualquier índice struct distinto de las ubicaciones devueltas por las llamadas a la **\_ \_ asignación atómica de IMM** o [ \_ consumo](imm-atomic-consume--sm5---asm-.md) producen resultados indefinidos en que exactamente la ubicación de memoria dentro del UAV al que se está accediendo es aleatoria y solo se fija para la duración de la invocación del sombreador.

En el caso de un UAV de recuento, la aplicación puede guardar el valor devuelto como referencia a una ubicación fija dentro de UAV que sea significativa después de que la invocación del sombreador haya finalizado. Siempre se puede tener acceso a cualquier ubicación de un UAV de recuento independientemente de cuál sea el valor de recuento.

No hay ninguna compresión del recuento, por lo que se ajusta en caso de desbordamiento.

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

 

 





