---
title: texm3x3tex - ps
description: 'Realiza una multiplicación de matriz 3x3 y usa el resultado para realizar una búsqueda de textura. texm3x3tex debe usarse con dos instrucciones de texm3x3pad: ps.'
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a40c78fddadde5d58186f9a1ebb01f4d021620862f9d3534e535842a848a2e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787564"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex - ps

Realiza una multiplicación de matriz 3x3 y usa el resultado para realizar una búsqueda de textura. texm3x3tex debe usarse con dos [instrucciones de texm3x3pad: ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Sintaxis



| texm3x3tex dst, src |
|---------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción se usa como final de tres instrucciones que representan una operación de multiplicación de matriz 3x3, seguida de una búsqueda de textura. La matriz 3x3 se compone de las coordenadas de textura de la tercera fase de textura y las dos fases de textura anteriores. El vector de tres componentes resultante (u,v,w) se usa para muestrear la textura en la fase 3. Se omite cualquier textura asignada a las dos fases de textura anteriores. La multiplicación de la matriz 3x3 suele ser útil para orientar un vector normal al espacio tangente correcto para la superficie que se representa.

Esta instrucción debe usarse con la instrucción texm3x3pad. Los registros de textura deben usar la siguiente secuencia.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



Este es un detalle más detallado sobre cómo se logra la multiplicación de 3x3.

La primera instrucción de texm3x3pad realiza la primera fila de la multiplicación para buscar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La segunda instrucción de texm3x3pad realiza la segunda fila de la multiplicación para buscar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La instrucción texm3x3spec realiza la tercera fila de la multiplicación para buscar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Por último, la instrucción texm3x3tex muestrea t(m+2) con (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) y almacena el resultado en t(m+2).

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> con (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas.

## <a name="examples"></a>Ejemplos

Este es un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



En este ejemplo se requiere la siguiente configuración de la fase de textura.

-   A la fase 0 se le asigna un mapa de textura con datos normales. Esto se conoce a menudo como un mapa de protuberancias. Los datos son (XYZ) normales para cada texel. El conjunto de coordenadas de textura 0 define cómo muestrear este mapa normal.
-   El conjunto de coordenadas de textura 1 se asigna a la fila 1 de la matriz 3x3. Se omite cualquier textura asignada a la fase 1.
-   El conjunto de coordenadas de textura 2 se asigna a la fila 2 de la matriz 3x3. Se omite cualquier textura asignada a la fase 2.
-   El conjunto de coordenadas de textura 3 se asigna a la fila 3 de la matriz 3x3. Una textura de volumen o cubo debe establecerse en la fase 3 para la búsqueda por el vector 3D transformado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




