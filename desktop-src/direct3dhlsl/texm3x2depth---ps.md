---
title: texm3x2depth - ps
description: Calcule el valor de profundidad que se usará en las pruebas de profundidad para este píxel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 17d3f04cd722664992911759ae1f5f6a4bd5947e0b46e37dc61b62b999ac8d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892535"
---
# <a name="texm3x2depth---ps"></a>texm3x2depth - ps

Calcule el valor de profundidad que se usará en las pruebas de profundidad para este píxel.

## <a name="syntax"></a>Syntax



| texm3x2depth dst, src |
|-----------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2depth          |      |      | x    |      |      |      |       |      |       |



 

Esta instrucción debe usarse con la [instrucción texm3x2pad - ps.](texm3x2pad---ps.md)

Al usar estas dos instrucciones, los registros de textura deben usar la siguiente secuencia.


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



El cálculo de profundidad se realiza después de usar una operación de producto de puntos para buscar z y w. Este es un detalle más detallado sobre cómo se realiza el cálculo de profundidad.

La instrucción texm3x2pad calcula z.

z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

La instrucción texm3x2depth calcula w.

w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Calcule la profundidad y almacene el resultado en t(m+1).


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



La profundidad calculada se etiqueta para usarse en la prueba de profundidad del píxel, reemplazando el valor de prueba de profundidad existente para el píxel.

Asegúrese de fijar z/w para que esté en el intervalo de (0-1). Si z/w está fuera de este intervalo, el resultado almacenado en el búfer de profundidad será indefinido.

Después de ejecutar texm3x2depth, register t(m+1) ya no está disponible para su uso en el sombreador.

Al multimuestreo, el uso de esta instrucción elimina la mayor parte de la ventaja del búfer de profundidad de resolución superior. Dado que el sombreador de píxeles se ejecuta una vez por píxel, la salida de valor de profundidad única de texm3x2depth o [texdepth: ps](texdepth---ps.md) se usará para cada una de las pruebas de comparación de profundidad de subpíxel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




