---
title: Modificadores para ps_2_0 y superiores
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino. Obtenga información sobre los modificadores ps_2_0 y posteriores.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989290"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificadores para ps \_ 2 \_ 0 y superiores

Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.

Esta sección contiene información de referencia para los modificadores de instrucción implementados por el sombreador de píxeles versión 2 \_ 0 y posteriores.



| Nombre                                     | Sintaxis     | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Centroide](#centroid)                    | \_Centroide | x    | x    | x     | x    | x     |
| [Precisión \_ parcial](#partial-precision) | \_Pp       | x    | x    | x     | x    | x     |
| [Saturate](#saturate)                    | \_Sentado      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Centroide

El modificador centroide es un modificador opcional que fija la interpolación de atributos dentro del intervalo de la primitiva cuando un centro de píxeles de varias muestras no está cubierto por la primitiva. Esto se puede ver en [Muestreo de centroide.](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)

Puede aplicar el modificador centroide a una instrucción de ensamblado como se muestra aquí:


```
dcl_texcoord0_centroid v0
```



También puede aplicar el modificador centroide a una semántica, como se muestra aquí:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Además, cualquier [registro de color de](dx9-graphics-reference-asm-ps-registers-input-color.md) entrada (v ) declarado con una semántica de color se aplicará \# automáticamente. No se garantiza que los degradados calculados a partir de atributos muestreados en centroide sean precisos.

## <a name="partial-precision"></a>Precisión parcial

El modificador de instrucción de precisión parcial (pp) indica las áreas en las que la precisión parcial es aceptable, siempre que \_ la implementación subyacente lo admita. Las implementaciones siempre pueden omitir el modificador y realizar las operaciones afectadas con precisión completa.

El \_ modificador pp puede producirse en dos contextos:

-   En una declaración de coordenadas de textura para permitir pasar coordenadas de textura al sombreador de píxeles en forma de precisión parcial. Esto permite, por ejemplo, el uso de coordenadas de textura para retransmitir datos de color al sombreador de píxeles, que puede ser más rápido con precisión parcial que con precisión completa en algunas implementaciones. En ausencia de este modificador, las coordenadas de textura se deben pasar con precisión completa.
-   En cualquier instrucción, incluidas las instrucciones de carga de textura. Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial. En ausencia de un modificador explícito, la instrucción debe realizarse con precisión completa (independientemente de la precisión de entrada).

Ejemplos:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturar

El modificador de instrucción saturada (sat) satura (o fija) el resultado de la instrucción en el intervalo \_ 0, 1 antes de escribir en el \[ \] registro de destino.

El modificador de instrucción sat se puede usar con cualquier instrucción excepto \_ [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)y cualquier instrucción de \* texas.

Para ps \_ 2 \_ 0, ps 2 x y \_ ps \_ \_ 2 \_ sw, \_ [](dx9-graphics-reference-asm-ps-registers-output-color.md) [](dx9-graphics-reference-asm-ps-registers-output-depth.md)el modificador de instrucción sat no se puede usar con instrucciones que escriban en ningún registro de salida (Registro de color de salida o Registro de profundidad de salida). Esta restricción no se aplica a ps \_ 3 \_ 0 y posteriores.

Ejemplo:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




