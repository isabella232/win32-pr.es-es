---
title: texm3x3spec - ps
description: 'Realiza una multiplicación de matriz 3x3 y usa el resultado para realizar una búsqueda de textura. Se puede usar para la reflexión especular y la asignación de entorno. texm3x3spec debe usarse junto con dos instrucciones de texm3x3pad: ps.'
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b5fcef771d6d06a1691d5c5e953b76b1c445c7c8df7b2da37b8b4220bef2b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485435"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec - ps

Realiza una multiplicación de matriz 3x3 y usa el resultado para realizar una búsqueda de textura. Se puede usar para la reflexión especular y la asignación de entorno. texm3x3spec debe usarse junto con dos [instrucciones de texm3x3pad: ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Syntax



| texm3x3spec dst, src0, src1 |
|-----------------------------|



 

where

-   dst es el registro de destino.
-   src0 y src1 son registros de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción realiza la fila final de una multiplicación de matriz 3x3, usa el vector resultante como vector normal para reflejar un vector de rayos oculares y, a continuación, usa el vector reflejado para realizar una búsqueda de textura. El sombreador lee el vector de rayos oculares de un registro constante. La multiplicación de la matriz 3x3 suele ser útil para orientar un vector normal al espacio tangente correcto para la superficie que se representa.

La matriz 3x3 se compone de las coordenadas de textura de la tercera fase de textura y las dos fases de textura anteriores. El vector de reflexión posterior resultante (u,v,w) se usa para muestrear la textura en la fase de textura final. Se omite cualquier textura asignada a las dos fases de textura anteriores.

Esta instrucción debe usarse con dos instrucciones de texm3x3pad. Los registros de textura deben usar la siguiente secuencia.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



La primera instrucción de texm3x3pad realiza la primera fila de la multiplicación para buscar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La segunda instrucción texm3x3pad realiza la segunda fila de la multiplicación para buscar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La instrucción texm3x3spec realiza la tercera fila de la multiplicación para buscar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

A continuación, la instrucción texm3x3spec realiza un cálculo de reflexión.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* E)/(N \* N) \] \* N - E

donde la N normal la da

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

y el vector de rayos oculares E lo ofrece el registro constante.

E = c \# (se puede usar cualquier registro constante(c0, c1, c2, etc.)

Por último, la instrucción texm3x3spec muestrea t(m+2) con (u<sup>'</sup>,v<sup>'</sup>, w<sup>'</sup>) y almacena el resultado en t(m+2).

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates

## <a name="examples"></a>Ejemplos

Este es un sombreador de ejemplo con los mapas de textura y las fases de textura identificadas.


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



En este ejemplo se requiere la siguiente configuración de la fase de textura.

-   A la fase 0 se le asigna un mapa de textura con datos normales. Esto se conoce a menudo como un mapa de protuberancias. Los datos son (XYZ) normales para cada texel. Las coordenadas de textura de la fase n definen dónde se va a muestrear este mapa normal.
-   El conjunto de coordenadas de textura m se asigna a la fila 1 de la matriz 3x3. Se omite cualquier textura asignada a la fase m.
-   El conjunto de coordenadas de textura m+1 se asigna a la fila 2 de la matriz 3x3. Se omite cualquier textura asignada a la fase m+1.
-   El conjunto de coordenadas de textura m+2 se asigna a la fila 3 de la matriz 3x3. A la fase m+2 se le asigna un mapa de textura de volumen o cubo. La textura proporciona datos de color (RGBA).
-   El vector de rayos oculares E se da mediante un registro constante E = c \# .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




