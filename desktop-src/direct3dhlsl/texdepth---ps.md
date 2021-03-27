---
title: texdepth-PS
description: Calcular los valores de profundidad que se van a usar en la prueba de comparación de búfer de profundidad para este píxel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904278"
---
# <a name="texdepth---ps"></a>texdepth-PS

Calcular los valores de profundidad que se van a usar en la prueba de comparación de búfer de profundidad para este píxel.

## <a name="syntax"></a>Sintaxis



| texdepth DST |
|--------------|



 

, donde

-   DST es el registro de destino.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | x    |      |      |       |      |       |



 

Esta instrucción usa R5. r/R5. g en la prueba de comparación del búfer de profundidad para este píxel. Se omiten los datos de los canales azul y alfa. Si R5. g = 0, el resultado de R5. r/R5. g = 1,0.

El registro temporal R5 es el único registro que puede usar esta instrucción.

Después de ejecutar esta instrucción, el registro no temporal R5 no está disponible para su uso adicional en el sombreador.

Cuando se usa el muestreo múltiple, el uso de esta instrucción elimina la mayoría de las ventajas del búfer de profundidad de mayor resolución. Dado que el sombreador de píxeles se ejecuta una vez por píxel, se usará la salida de valor de profundidad único de [texm3x2depth-PS](texm3x2depth---ps.md) o texdepth para cada una de las pruebas de comparación de profundidad de subpíxeles.

## <a name="examples"></a>Ejemplos

Este es un ejemplo de uso de texdepth.


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




