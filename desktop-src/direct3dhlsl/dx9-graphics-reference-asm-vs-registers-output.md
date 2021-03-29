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
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996744"
---
# <a name="output-registers"></a>Registros de salida

-   Registro de color de vértice
-   Registro de niebla
-   Registro de posición \_
-   \_Registro de tamaño de punto \_
-   \_Registro de coordenadas de textura \_

Los nombres de registro están precedidos por una letra minúscula o, lo que indica que los registros de salida son de solo escritura.

## <a name="vertex-color-register---od0-od1"></a>Color de vértice registro: oD0, oD1

oD0 es el registro de color difuso. oD1 es el registro de color especular. El valor de oD0 se interpola y se escribe en el registro de color de entrada 0 (V0) del sombreador de píxeles. El valor oD1 se interpola y se escribe en el registro del color de entrada 1 (V1) del sombreador de píxeles. Para obtener más información sobre los registros de color del sombreador de píxeles, consulte registros.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de color de vértice  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Registro de niebla: oFog

El valor de niebla de salida se registra. El valor es el factor de niebla que se va a interpolar y, a continuación, enrutar a la tabla de niebla. Solo se usa el componente x escalar de la niebla. Los valores se fijan entre cero y uno antes de pasar al rasterizador.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de niebla           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Posición Register-oPos

La posición de salida se registra. El valor es la posición en el espacio de recorte homogéneo. Este valor debe escribirse en el sombreador de vértices.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de posición      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Registro de tamaño de punto: OPC

Los registros de tamaño de punto de salida. Solo se usa el componente x escalar del tamaño de punto.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de tamaño de punto    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Coordenada de textura Register-oT0 a oT7

La textura de salida coordina los registros. En concreto, se trata de una matriz de registros de datos de salida que se iteran y usan como coordenadas de textura por las fases de muestreo de textura que enrutan los datos al sombreador de píxeles.



| Versiones del sombreador de vértices      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura | x    | x    | x     | x    |      |       |



 

Al escribir en un registro de coordenadas de textura, se recomienda pasar solo tantos valores de punto flotante como la dimensión del mapa de textura correspondiente. Controlan los valores que se pasan con un modificador. Por ejemplo, use. XY para un mapa de textura 2D.

Cuando se habilita la proyección de textura para una fase de textura, los cuatro valores de punto flotante se deben escribir en el registro de textura correspondiente.

Cualquiera de las marcas de D3DTTFF \* Texture Transform debe ser cero cuando se utiliza la canalización programable.

### <a name="texture-coordinate-range"></a>Rango de coordenadas de textura

Los datos de vértices de objeto proporcionan coordenadas de textura de entrada. Los objetos que no usan texturas en mosaico suelen tener coordenadas de textura en el intervalo de \[ 0 a 1 \] . Los objetos que usan texturas en mosaico, como Terrain, normalmente tienen coordenadas de textura que van desde \[ -?, +? \] Where? puede ser un número de punto flotante de gran tamaño.

La interpolación de coordenadas de textura se realiza en los datos de vértices para la rasterización. Durante la rasterización, las coordenadas de textura se interpolan entre los vértices de objetos, modificados por ajuste de textura y escalado por el tamaño de textura (también con el modo de dirección de textura de la cuenta) para generar un índice de entero. A continuación, el índice se utiliza para realizar una búsqueda de textura. MaxTextureRepeat se puede usar para determinar el número de veces que se puede poner en mosaico una textura.

Si las coordenadas de textura se leen directamente en un sombreador de píxeles (mediante texcoord o texcrd), el intervalo de coordenadas de textura depende de la instrucción y la versión del sombreador de píxeles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




