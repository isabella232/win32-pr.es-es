---
title: Modificadores para ps_2_0 y versiones posteriores
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903894"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificadores para PS \_ 2 \_ 0 y versiones posteriores

Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.

Esta sección contiene información de referencia para los modificadores de instrucción implementados por el sombreador de píxeles versión 2 \_ 0 y versiones posteriores.



| Nombre                                     | Sintaxis     | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Centroide](#centroid)                    | \_centroide | x    | x    | x     | x    | x     |
| [\_Precisión parcial](#partial-precision) | \_páginas       | x    | x    | x     | x    | x     |
| [Saturate](#saturate)                    | \_sábado      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Centroide

El modificador centroide es un modificador opcional que fija la interpolación de atributos dentro del intervalo de la primitiva cuando un centro de píxeles de muestreo Multimuestra no está incluido en el primitivo. Esto puede verse en el [muestreo de centroide](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).

Puede aplicar el modificador centroide a una instrucción de ensamblado como se muestra aquí:


```
dcl_texcoord0_centroid v0
```



También puede aplicar el modificador centroide a una semántica como se muestra aquí:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Además, cualquier [registro de color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) declarado con una semántica de color se aplicará automáticamente a centroide. No se garantiza que los degradados calculados a partir de los atributos que se centroide muestrean sean precisos.

## <a name="partial-precision"></a>Precisión parcial

El modificador de instrucciones de precisión parcial ( \_ PP) indica áreas en las que la precisión parcial es aceptable, siempre que la implementación subyacente la admita. Las implementaciones siempre son gratuitas para omitir el modificador y realizar las operaciones afectadas con precisión completa.

El \_ modificador PP puede producirse en dos contextos:

-   En una declaración de coordenadas de textura para habilitar el paso de coordenadas de textura al sombreador de píxeles en formato de precisión parcial. Esto permite, por ejemplo, el uso de coordenadas de textura para retransmitir datos de color al sombreador de píxeles, que puede ser más rápido con una precisión parcial que con precisión completa en algunas implementaciones. En ausencia de este modificador, las coordenadas de textura se deben pasar con precisión completa.
-   En cualquier instrucción, incluidas las instrucciones de carga de textura. Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial. En ausencia de un modificador explícito, la instrucción se debe realizar a plena precisión (independientemente de la precisión de entrada).

Ejemplos:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturar

El modificador de instrucciones saturadas ( \_ SAT) satura (o fija) el resultado de la instrucción en el intervalo de \[ 0 a 1 antes de \] escribir en el registro de destino.

El \_ modificador de instrucciones SAT se puede usar con cualquier instrucción excepto [FRC-PS](frc---ps.md), [sincos (-PS](sincos---ps.md)y cualquier instrucción Tex \* .

Para PS \_ 2 \_ 0, PS \_ 2 \_ x y PS \_ 2 \_ SW, \_ no se puede usar el modificador de instrucciones de SAT con instrucciones para escribir en los registros de salida (registro de[color de salida](dx9-graphics-reference-asm-ps-registers-output-color.md) o registro de [profundidad de salida](dx9-graphics-reference-asm-ps-registers-output-depth.md)). Esta restricción no se aplica a PS \_ 3 \_ 0 y versiones posteriores.

Ejemplo:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




