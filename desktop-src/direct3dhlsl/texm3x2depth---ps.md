---
title: texm3x2depth-PS
description: Calcular el valor de profundidad que se va a usar en las pruebas de profundidad para este píxel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983854"
---
# <a name="texm3x2depth---ps"></a>texm3x2depth-PS

Calcular el valor de profundidad que se va a usar en las pruebas de profundidad para este píxel.

## <a name="syntax"></a>Sintaxis



| texm3x2depth DST, src |
|-----------------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2depth          |      |      | x    |      |      |      |       |      |       |



 

Esta instrucción debe usarse con la instrucción [texm3x2pad-PS](texm3x2pad---ps.md) .

Al utilizar estas dos instrucciones, los registros de textura deben usar la siguiente secuencia.


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



El cálculo de profundidad se realiza después de usar una operación de producto punto para buscar z y w. Aquí encontrará más detalles sobre cómo se realiza el cálculo de profundidad.

La instrucción texm3x2pad calcula z.

z = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

La instrucción texm3x2depth calcula w.

w = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Calcule la profundidad y almacene el resultado en t (m + 1).


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



La profundidad calculada se etiqueta para usarse en la prueba de profundidad del píxel, reemplazando el valor de prueba de profundidad existente para el píxel.

Asegúrese de fijar z/w en el intervalo de (0-1). Si z/w está fuera de este intervalo, el resultado almacenado en el búfer de profundidad no estará definido.

Después de ejecutar texm3x2depth, el registro t (m + 1) ya no está disponible para su uso en el sombreador.

Cuando se usa el muestreo múltiple, el uso de esta instrucción elimina la mayoría de las ventajas del búfer de profundidad de mayor resolución. Dado que el sombreador de píxeles se ejecuta una vez por píxel, se usará la salida de un solo valor de profundidad por texm3x2depth o [texdepth-PS](texdepth---ps.md) para cada una de las pruebas de comparación de profundidad de subpíxeles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




