---
title: Registros de salida
description: Registros de salida
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cfa17c09315f4cdca98f5c5fc10f7ab15541eb8b774835963b06169c4afe225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457775"
---
# <a name="output-registers"></a>Registros de salida

-   Registro de color de vértice
-   Registro de bosque
-   Registro de \_ posición
-   Registro de \_ tamaño de \_ punto
-   Registro de \_ coordenadas de \_ textura

Los nombres de registro van precedidos de una letra minúscula o, lo que indica que los registros de salida son de solo escritura.

## <a name="vertex-color-register---od0-od1"></a>Registro de color de vértice: oD0, oD1

oD0 es el registro de color difuso. oD1 es el registro de color especular. El valor de oD0 está interpolado y se escribe en el registro de color de entrada 0 (v0) del sombreador de píxeles. El valor oD1 se interpola y se escribe en el registro de color de entrada 1 (v1) del sombreador de píxeles. Para obtener más información sobre los registros de color del sombreador de píxeles, vea Registros.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de color de vértice  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Registro de bosque: oFog

El valor de salida se registra. El valor es el factor de curva que se va a interpolar y, a continuación, se enruta a la tabla de nubes. Solo se usa el componente x escalar del rayo. Los valores se fijan entre cero y uno antes de pasar al rasterizador.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de bosque           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Registro de posición: oPos

Se registra la posición de salida. El valor es la posición en el espacio de recorte homogéneo. El sombreador de vértices debe escribir este valor.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de posición      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Registro de tamaño de punto: oPts

El tamaño del punto de salida se registra. Solo se usa el componente x escalar del tamaño de punto.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de tamaño de punto    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Registro de coordenadas de textura: de oT0 a oT7

Las coordenadas de textura de salida se registran. En concreto, se trata de una matriz de registros de datos de salida que las fases de muestreo de textura iteran y usan como coordenadas de textura enrutando los datos al sombreador de píxeles.



| Versiones del sombreador de vértices      | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura | x    | x    | x     | x    |      |       |



 

Al escribir en un registro de coordenadas de textura, se recomienda pasar solo tantos valores de punto flotante como la dimensión del mapa de textura correspondiente. Controlar los valores pasados con un modificador . Por ejemplo, use .xy para un mapa de textura 2D.

Cuando la proyección de textura está habilitada para una fase de textura, los cuatro valores de punto flotante deben escribirse en el registro de textura correspondiente.

Cualquiera de las marcas de transformación de textura D3DTTFF debe ser cero cuando se usa la canalización \* programable.

### <a name="texture-coordinate-range"></a>Rango de coordenadas de textura

Los datos de vértice de objeto suministran coordenadas de textura de entrada. Los objetos que no usan texturas en mosaico normalmente tienen coordenadas de textura en el \[ intervalo 0,1. \] Los objetos que usan texturas en mosaico, como el terreno, normalmente tienen coordenadas de textura que van desde \[ -?,+? \] donde ? puede ser un número de punto flotante grande.

La interpolación de coordenadas de textura se realiza en los datos de vértices para la rasterización. Durante la rasterización, las coordenadas de textura se interpolan entre los vértices de objeto, se modifican mediante el ajuste de textura y se escalan por el tamaño de la textura (también teniendo en cuenta el modo de dirección de textura) para generar un índice entero. A continuación, el índice se usa para realizar una búsqueda de textura. MaxTextureRepeat se puede usar para determinar cuántas veces se puede en mosaico una textura.

Si las coordenadas de textura se leen directamente en un sombreador de píxeles (mediante tejacoord o texcrd), el intervalo de coordenadas de textura depende de la instrucción y la versión del sombreador de píxeles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




