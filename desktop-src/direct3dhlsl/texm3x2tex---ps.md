---
title: texm3x2tex - ps
description: Realiza la fila final de una matriz 3x2 multiplicada y usa el resultado para realizar una búsqueda de textura. la instrucción texm3x2tex debe usarse junto con la instrucción texm3x2pad - ps.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9653325098b05959fcbd9e7a838801652a532d936bdaebc829055b717a49096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723023"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex - ps

Realiza la fila final de una matriz 3x2 multiplicada y usa el resultado para realizar una búsqueda de textura. la instrucción texm3x2tex debe usarse junto con la [instrucción texm3x2pad - ps.](texm3x2pad---ps.md)

## <a name="syntax"></a>Syntax



| texm3x2tex dst, src |
|---------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

La instrucción se usa como una de las dos instrucciones que representan una operación de multiplicación de matriz 3x2. Esta instrucción debe usarse con la instrucción [texm3x2pad - ps.](texm3x2pad---ps.md)

Al usar estas dos instrucciones, los registros de textura deben usar la secuencia siguiente.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



Este es un detalle más detallado sobre cómo se realiza la multiplicación de 3x2.

La instrucción texm3x2pad realiza la primera fila de la multiplicación para buscar u<sup>'</sup>.

u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub>

La instrucción texm3x2tex realiza la segunda fila de la multiplicación para buscar v<sup>'</sup>.

v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub>

La instrucción texm3x2tex muestrea la textura en el escenario (m+1) con (u<sup>'</sup>,v<sup>'</sup>) y almacena el resultado en t(m+1).

t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates

## <a name="examples"></a>Ejemplos

Este es un sombreador de ejemplo con los mapas de textura y las fases de textura identificadas.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Este ejemplo requiere las siguientes texturas en las siguientes fases de textura.

-   La fase 0 toma un mapa con (x,y,z) datos de la sustitución.
-   La fase 1 contiene coordenadas de textura. No se requiere ninguna textura en la fase de textura.
-   La fase 2 contiene las coordenadas de textura, así como un conjunto de texturas 2D en esa fase de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




