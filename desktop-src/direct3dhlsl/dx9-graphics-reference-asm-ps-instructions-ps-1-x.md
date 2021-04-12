---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4 instrucciones
description: Esta sección contiene información de referencia para las instrucciones de la versión 1 X del sombreador de píxeles \_ .
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c3fa8e76e1075da321a60d05504dff074dbfcfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269466"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>Instrucciones PS 1 \_ \_ , PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4

Esta sección contiene información de referencia para las instrucciones de la versión 1 X del sombreador de píxeles \_ .

Hay varios tipos de instrucciones de sombreador de píxeles, tal como se muestra en la tabla siguiente.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Versión                                    |                                                                               | Ranuras de instrucciones | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [PS](ps---ps.md)                          | Número de versión                                                                | 0                 | x    | x    | x    | x    |
| Instrucciones de constantes                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [DEF-PS](def---ps.md)                   | Definir constantes                                                              | 0                 | x    | x    | x    | x    |
| Instrucciones de fase                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [fase: PS](phase---ps.md)               | Transición entre la fase 1 y la fase 2                                        | 0                 |      |      |      | x    |
| Instrucciones aritméticas                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Agregar-PS](add---ps.md)                   | Agregar dos vectores                                                               | 1                 | x    | x    | x    | x    |
| [BEM-PS](bem---ps.md)                   | Aplicar una transformación de mapa de entorno de rugosidad falsa                                   | 2                 |      |      |      | x    |
| [CMP-PS](cmp---ps.md)                   | Comparar origen con 0                                                           | 1 ¹                |      | x    | x    | x    |
| [CND-PS](cnd---ps.md)                   | Comparar origen con 0,5                                                         | 1                 | x    | x    | x    | x    |
| [DP3-PS](dp3---ps.md)                   | Producto de tres componentes                                                   | 1                 | x    | x    | x    | x    |
| [DP4-PS](dp4---ps.md)                   | Producto de cuatro componentes                                                    | 1 ¹                |      | x    | x    | x    |
| [LRP-PS](lrp---ps.md)                   | Interpolación lineal                                                            | 1                 | x    | x    | x    | x    |
| [Mad-PS](mad---ps.md)                   | Multiplicar y agregar                                                              | 1                 | x    | x    | x    | x    |
| [MOV-PS](mov---ps.md)                   | Move                                                                          | 1                 | x    | x    | x    | x    |
| [mul-PS](mul---ps.md)                   | Multiplicar                                                                      | 1                 | x    | x    | x    | x    |
| [NOP-PS](nop---ps.md)                   | No hay ninguna operación                                                                  | 0                 | x    | x    | x    | x    |
| [Sub-PS](sub---ps.md)                   | Restar                                                                      | 1                 | x    | x    | x    | x    |
| Instrucciones de textura                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Tex-PS](tex---ps.md)                   | Muestra de una textura                                                              | 1                 | x    | x    | x    |      |
| [texbem-PS](texbem---ps.md)             | Aplicar una transformación de mapa de entorno de rugosidad falsa                                   | 1                 | x    | x    | x    |      |
| [texbeml-PS](texbeml---ps.md)           | Aplicar una transformación de mapa de entorno de rugosidad falsa con corrección de luminancia         | 1 +1 ²              | x    | x    | x    |      |
| [texcoord-PS](texcoord---ps.md)         | Interpretar los datos de coordenadas de textura como datos de color                               | 1                 | x    | x    | x    |      |
| [texcrd-PS](texcrd---ps.md)             | Copiar los datos de coordenadas de textura como datos de color                                    | 1                 |      |      |      | x    |
| [texdepth-PS](texdepth---ps.md)         | Calcular valores de profundidad                                                        | 1                 |      |      |      | x    |
| [texdp3-PS](texdp3---ps.md)             | Producto de tres componentes entre los datos de textura y las coordenadas de textura  | 1                 |      | x    | x    |      |
| [texdp3tex-PS](texdp3tex---ps.md)       | Producto de tres componentes y búsqueda de textura 1D                             | 1                 |      | x    | x    |      |
| [texkill-PS](texkill---ps.md)           | Cancela la representación de píxeles en función de una comparación                             | 1                 | x    | x    | x    | x    |
| [texld-PS \_ 1 \_ 4](texld---ps-1-4.md)     | Muestra de una textura                                                              | 1                 |      |      |      | x    |
| [texm3x2depth-PS](texm3x2depth---ps.md) | Calcular valores de profundidad por píxel                                              | 1                 |      |      | x    |      |
| [texm3x2pad-PS](texm3x2pad---ps.md)     | Primera matriz de filas multiplicación de una multiplicación de una matriz de dos filas                        | 1                 | x    | x    | x    |      |
| [texm3x2tex-PS](texm3x2tex---ps.md)     | Multiplicación de la matriz de filas final de una multiplicación de una matriz de dos filas                        | 1                 | x    | x    | x    |      |
| [texm3x3-PS](texm3x3---ps.md)           | multiplicación de matriz de 3x3                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad-PS](texm3x3pad---ps.md)     | Multiplicación de la primera o la segunda fila de una matriz de tres filas                   | 1                 | x    | x    | x    |      |
| [texm3x3spec-PS](texm3x3spec---ps.md)   | Multiplicación final de la fila de una matriz de tres filas                             | 1                 | x    | x    | x    |      |
| [texm3x3tex-PS](texm3x3tex---ps.md)     | Búsqueda de textura mediante una multiplicación de matriz de 3x3                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec-PS](texm3x3vspec---ps.md) | Búsqueda de textura con una matriz de 3x3 multiplicación, con vector de rayo no constante | 1                 | x    | x    | x    |      |
| [texreg2ar-PS](texreg2ar---ps.md)       | Muestrear una textura con los componentes alfa y rojo                           | 1                 | x    | x    | x    |      |
| [texreg2gb-PS](texreg2gb---ps.md)       | Muestrear una textura con los componentes verde y azul                          | 1                 | x    | x    | x    |      |
| [texreg2rgb-PS](texreg2rgb---ps.md)     | Muestrear una textura con los componentes rojo, verde y azul                     | 1                 |      | x    | x    |      |



 

1.  1 ranura en PS \_ 1 \_ 4; 2 ranuras en PS \_ 1 \_ 2 y PS \_ 1 \_ 3
2.  1 + 1 = 1 instrucción aritmética + 1 instrucción de textura

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




