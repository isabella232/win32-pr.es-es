---
title: texdepth- ps
description: Calcule los valores de profundidad que se usarán en la prueba de comparación del búfer de profundidad para este píxel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f39135c34c07a9a20f03c9ebc979647733884b37680ef07b9bc666b882052690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284179"
---
# <a name="texdepth---ps"></a>texdepth- ps

Calcule los valores de profundidad que se usarán en la prueba de comparación del búfer de profundidad para este píxel.

## <a name="syntax"></a>Syntax



| texdepth dst |
|--------------|



 

where

-   dst es el registro de destino.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | x    |      |      |       |      |       |



 

Esta instrucción usa r5.r/r5.g en la prueba de comparación del búfer de profundidad para este píxel. Los datos de los canales azul y alfa se omiten. Si r5.g = 0, el resultado de r5.r /r5.g = 1.0.

El registro temporal r5 es el único registro que puede usar esta instrucción.

Después de ejecutar esta instrucción, el registro temporal r5 no está disponible para su uso adicional en el sombreador.

Al multimuestreo, el uso de esta instrucción elimina la mayor parte de la ventaja del búfer de profundidad de resolución superior. Dado que el sombreador de píxeles se ejecuta una vez por píxel, la salida de valor de profundidad única de [texm3x2depth - ps](texm3x2depth---ps.md) o texdepth se usará para cada una de las pruebas de comparación de profundidad de subpíxel.

## <a name="examples"></a>Ejemplos

Este es un ejemplo de uso de texasdepth.


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

 

 




