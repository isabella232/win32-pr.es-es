---
title: texm3x3vspec - ps
description: Realiza una multiplicación de matriz 3x3 y usa el resultado para realizar una búsqueda de textura.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c31305f70698ed59cbb0b6403547f5da51766b1a8859a453a8f6ab5cdfd56dc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949475"
---
# <a name="texm3x3vspec---ps"></a>texm3x3vspec - ps

Realiza una multiplicación de matriz 3x3 y usa el resultado para realizar una búsqueda de textura. Esto se puede usar para la reflexión especular y la asignación de entorno donde el vector de rayos oculares no es constante. texm3x3vspec debe usarse junto con dos [instrucciones de texm3x3pad: ps.](texm3x3pad---ps.md) Si el vector de rayos oculares es constante, la instrucción [texm3x3spec - ps](texm3x3spec---ps.md) realizará la misma multiplicación de matriz y búsqueda de textura.

## <a name="syntax"></a>Syntax



| texm3x3vspec dst, src |
|-----------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3vspec          | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción realiza la fila final de una operación de multiplicación de matriz 3x3, interpreta el vector resultante como un vector normal para reflejar un vector de rayos oculares y, a continuación, usa el vector reflejado como una dirección de textura para una búsqueda de textura. Funciona igual que [texm3x3spec - ps](texm3x3spec---ps.md), salvo que el vector de rayos oculares se toma del cuarto componente de las coordenadas de textura. La multiplicación de la matriz 3x3 suele ser útil para orientar un vector normal al espacio tangente correcto para la superficie que se representa.

La matriz 3x3 se compone de las coordenadas de textura de la tercera fase de textura y las dos fases de textura anteriores. El vector de reflexión posterior (UVW) resultante se usa para muestrear la textura en la fase 3. Se omite cualquier textura asignada a las dos fases de textura anteriores.

Esta instrucción debe usarse con la instrucción texm3x3pad. Los registros de textura deben usar la siguiente secuencia.


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



La primera instrucción de texm3x3pad realiza la primera fila de la multiplicación para buscar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub>

La segunda instrucción de texm3x3pad realiza la segunda fila de la multiplicación para buscar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La instrucción texm3x3spec realiza la tercera fila de la multiplicación para buscar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La instrucción texm3x3vspec también realiza un cálculo de reflexión.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* E)/(N \* N) \] \* N - E

donde la N normal la da

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

y el vector de rayos oculares E lo ofrece

E = (TextureCoordinates(stage m)<sub>Q</sub> ,

TextureCoordinates(stage m+1)<sub>Q</sub> ,

TextureCoordinates(stage m+2)<sub>Q</sub> )

Por último, la instrucción texm3x3vspec muestrea t(m+2) con (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) y almacena el resultado en t(m+2).

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates

## <a name="examples"></a>Ejemplos

Este es un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



En este ejemplo se requiere la siguiente configuración de la fase de textura.

-   A la fase 0 se le asigna un mapa de textura con datos normales. Esto se conoce a menudo como un mapa de protuberancias. Los datos son (XYZ) normales para cada texel. Las coordenadas de textura en la fase n definen cómo muestrear este mapa normal.
-   El conjunto de coordenadas de textura m se asigna a la fila 1 de la matriz 3x3. Se omite cualquier textura asignada a la fase m.
-   El conjunto de coordenadas de textura m+1 se asigna a la fila 2 de la matriz 3x3. Se omite cualquier textura asignada a la fase m+1.
-   El conjunto de coordenadas de textura m+2 se asigna a la fila 3 de la matriz 3x3. A la fase m+2 se le asigna un mapa de textura de volumen o cubo. La textura proporciona datos de color (RGBA).
-   El vector de rayos oculares E se pasa a la instrucción del cuarto componente (q) de los datos de coordenadas de textura en las fases m, m+1 y m+2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




