---
title: texm3x3-PS
description: Realiza una multiplicación de una matriz de 3x3 cuando se usa junto con dos instrucciones texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983838"
---
# <a name="texm3x3---ps"></a>texm3x3-PS

Realiza una multiplicación de una matriz de 3x3 cuando se usa junto con dos instrucciones [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Sintaxis



| texm3x3 DST, src |
|------------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Esta instrucción es la misma que la instrucción [texm3x3tex-PS](texm3x3tex---ps.md) , sin la búsqueda de textura.

Esta instrucción se utiliza como final de tres instrucciones que representan una operación de multiplicación de una matriz de 3x3. La matriz de 3x3 se compone de las coordenadas de textura de la tercera fase de textura y de las dos fases de textura anteriores. Se omite cualquier textura asignada a cualquiera de las tres fases de textura.

Esta instrucción debe usarse con dos instrucciones texm3x3pad. Los registros de textura deben seguir la siguiente secuencia.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Aquí encontrará más detalles sobre cómo se realiza la multiplicación de 3x3.

La primera instrucción texm3x3pad realiza la primera fila de Multiply para buscar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La segunda instrucción texm3x3pad realiza la segunda fila de la multiplicación para encontrar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates (Stage m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La instrucción texm3x3tex realiza la tercera fila de Multiply para buscar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Coloque el resultado de la multiplicación de la matriz en el registro de destino.

t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




