---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4 instrucciones
description: Esta sección contiene información de referencia para las instrucciones X de la versión 1 del sombreador \_ de píxeles.
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 217e207d2f60d39979c7117cb48e0cb033fd98c6fbfb419642ff43e59759d510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119739"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4 Instructions

Esta sección contiene información de referencia para las instrucciones X de la versión 1 del sombreador \_ de píxeles.

Hay varios tipos de instrucciones de sombreador de píxeles, como se muestra en la tabla siguiente.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Versión                                    | Descripción                                                                   | Ranuras de instrucción | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [ps](ps---ps.md)                          | Número de la versión                                                                | 0                 | x    | x    | x    | x    |
| Instrucciones constantes                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def - ps](def---ps.md)                   | Definición de constantes                                                              | 0                 | x    | x    | x    | x    |
| Instrucciones de fase                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [fase: ps](phase---ps.md)               | Transición entre las fases 1 y 2                                        | 0                 |      |      |      | x    |
| Instrucciones aritméticas                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [add - ps](add---ps.md)                   | Agregar dos vectores                                                               | 1                 | x    | x    | x    | x    |
| [bem - ps](bem---ps.md)                   | Aplicación de una transformación de mapa de entorno de protuberancia falsa                                   | 2                 |      |      |      | x    |
| [cmp - ps](cmp---ps.md)                   | Comparar origen con 0                                                           | 1¹                |      | x    | x    | x    |
| [cnd - ps](cnd---ps.md)                   | Comparación del origen con 0,5                                                         | 1                 | x    | x    | x    | x    |
| [dp3- ps](dp3---ps.md)                   | Producto de puntos de tres componentes                                                   | 1                 | x    | x    | x    | x    |
| [dp4 - ps](dp4---ps.md)                   | Producto de punto de cuatro componentes                                                    | 1¹                |      | x    | x    | x    |
| [lrp - ps](lrp---ps.md)                   | Interpolación lineal                                                            | 1                 | x    | x    | x    | x    |
| [loca- ps](mad---ps.md)                   | Multiplicar y agregar                                                              | 1                 | x    | x    | x    | x    |
| [mov - ps](mov---ps.md)                   | Move                                                                          | 1                 | x    | x    | x    | x    |
| [mul - ps](mul---ps.md)                   | Multiplicar                                                                      | 1                 | x    | x    | x    | x    |
| [nop - ps](nop---ps.md)                   | No hay ninguna operación                                                                  | 0                 | x    | x    | x    | x    |
| [sub - ps](sub---ps.md)                   | Restar                                                                      | 1                 | x    | x    | x    | x    |
| Instrucciones de textura                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [tex - ps](tex---ps.md)                   | Muestrear una textura                                                              | 1                 | x    | x    | x    |      |
| [texbem - ps](texbem---ps.md)             | Aplicación de una transformación de mapa de entorno de protuberancia falsa                                   | 1                 | x    | x    | x    |      |
| [texbeml - ps](texbeml---ps.md)           | Aplicación de una transformación de mapa de entorno de protuberancia falsa con corrección de luminosidad         | 1+1 además de 1              | x    | x    | x    |      |
| [texcoord - ps](texcoord---ps.md)         | Interpretación de los datos de coordenadas de textura como datos de color                               | 1                 | x    | x    | x    |      |
| [texcrd- ps](texcrd---ps.md)             | Copiar datos de coordenadas de textura como datos de color                                    | 1                 |      |      |      | x    |
| [texdepth- ps](texdepth---ps.md)         | Cálculo de valores de profundidad                                                        | 1                 |      |      |      | x    |
| [texdp3 - ps](texdp3---ps.md)             | Producto de puntos de tres componentes entre los datos de textura y las coordenadas de textura  | 1                 |      | x    | x    |      |
| [texdp3tex - ps](texdp3tex---ps.md)       | Producto de puntos de tres componentes y búsqueda de textura 1D                             | 1                 |      | x    | x    |      |
| [texkill - ps](texkill---ps.md)           | Cancela la representación de píxeles en función de una comparación                             | 1                 | x    | x    | x    | x    |
| [texld: ps \_ 1 \_ 4](texld---ps-1-4.md)     | Muestrear una textura                                                              | 1                 |      |      |      | x    |
| [texm3x2depth - ps](texm3x2depth---ps.md) | Cálculo de valores de profundidad por píxel                                              | 1                 |      |      | x    |      |
| [texm3x2pad - ps](texm3x2pad---ps.md)     | Multiplicación de la primera matriz de filas de una matriz de dos filas                        | 1                 | x    | x    | x    |      |
| [texm3x2tex - ps](texm3x2tex---ps.md)     | Multiplicación final de la matriz de filas de una matriz de dos filas                        | 1                 | x    | x    | x    |      |
| [texm3x3 - ps](texm3x3---ps.md)           | Multiplicación de matriz de 3x3                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad - ps](texm3x3pad---ps.md)     | Multiplicación de la primera o segunda fila de una matriz de tres filas                   | 1                 | x    | x    | x    |      |
| [texm3x3spec - ps](texm3x3spec---ps.md)   | Multiplicación final de filas de una matriz de tres filas multiplicada                             | 1                 | x    | x    | x    |      |
| [texm3x3tex - ps](texm3x3tex---ps.md)     | Buscar textura mediante una multiplicación de matriz de 3x3                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec - ps](texm3x3vspec---ps.md) | Búsqueda de textura mediante una multiplicación de matriz de 3x3, con vector de rayos oculares no constante | 1                 | x    | x    | x    |      |
| [texreg2ar - ps](texreg2ar---ps.md)       | Muestrear una textura mediante los componentes alfa y rojo                           | 1                 | x    | x    | x    |      |
| [texreg2gb - ps](texreg2gb---ps.md)       | Muestrear una textura mediante los componentes verde y azul                          | 1                 | x    | x    | x    |      |
| [texreg2rgb - ps](texreg2rgb---ps.md)     | Muestrear una textura mediante los componentes rojo, verde y azul                     | 1                 |      | x    | x    |      |



 

1.  1 ranura en ps \_ 1 \_ 4; 2 ranuras en ps \_ 1 \_ 2 y ps \_ 1 \_ 3
2.  1 + 1 = 1 instrucción aritmética + 1 instrucción de textura

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




