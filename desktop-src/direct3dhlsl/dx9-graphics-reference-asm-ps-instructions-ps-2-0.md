---
title: Instrucciones de ps_2_0
description: Esta sección contiene información de referencia para las instrucciones del sombreador de píxeles versión 2 \_ 0.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bac2a70ed0147885174c2290d5e58c92ae3347e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996808"
---
# <a name="ps_2_0-instructions"></a>Instrucciones de PS \_ 2 \_ 0

Esta sección contiene información de referencia para las instrucciones del sombreador de píxeles versión 2 \_ 0.

Hay varios tipos de instrucciones de sombreador de píxeles, tal como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucciones: número de ranuras de instrucciones usadas por cada instrucción.
-   Configuración: un sombreador de píxeles debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Texture: estas instrucciones se usan para cargar y muestrear los datos de textura y para modificar las coordenadas de textura.
-   Nuevas: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                             | Descripción                                                                                      | Ranuras de instrucciones | Configurar | Aritméticos | Textura | Nuevo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [ABS-PS](abs---ps.md)                                         | Valor absoluto                                                                                   | 1                 |       | x          |         | x   |
| [Agregar-PS](add---ps.md)                                         | Agregar dos vectores                                                                                  | 1                 |       | x          |         |     |
| [CMP-PS](cmp---ps.md)                                         | Comparar origen con 0                                                                              | 1                 |       | x          |         |     |
| [CRS-PS](crs---ps.md)                                         | Producto cruzado                                                                                    | 2                 |       | x          |         | x   |
| [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Declarar la dimensión de textura para una muestra                                                      | 0                 | x     |            |         | x   |
| [DCL: (SM2, SM3-PS ASM)](dcl---ps.md)                        | Declare la asociación entre los registros de salida del sombreador de vértices y los registros de entrada del sombreador de píxeles. | 0                 | x     |            |         | x   |
| [DEF-PS](def---ps.md)                                         | Definir constantes                                                                                 | 0                 | x     |            |         |     |
| [dp2add-PS](dp2add---ps.md)                                   | producto de punto 2D y agregar                                                                           | 2                 |       | x          |         | x   |
| [DP3-PS](dp3---ps.md)                                         | producto de punto 3D                                                                                   | 1                 |       | x          |         |     |
| [DP4-PS](dp4---ps.md)                                         | 4D DOT producto                                                                                   | 1                 |       | x          |         |     |
| [EXP-PS](exp---ps.md)                                         | Precisión completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [FRC-PS](frc---ps.md)                                         | Componente fraccionario                                                                             | 1                 |       | x          |         | x   |
| [registro: PS](log---ps.md)                                         | ₂ de registro de precisión completa (x)                                                                           | 1                 |       | x          |         | x   |
| [LRP-PS](lrp---ps.md)                                         | Interpolación lineal                                                                               | 2                 |       | x          |         |     |
| [m3x2-PS](m3x2---ps.md)                                       | 3x2 multiplicar                                                                                     | 2                 |       | x          |         | x   |
| [M3x3-PS](m3x3---ps.md)                                       | multiplicar 3x3                                                                                     | 3                 |       | x          |         | x   |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 multiplicar                                                                                     | 4                 |       | x          |         | x   |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 multiplicar                                                                                     | 3                 |       | x          |         | x   |
| [M4x4-PS](m4x4---ps.md)                                       | multiplicar 4x4                                                                                     | 4                 |       | x          |         | x   |
| [Mad-PS](mad---ps.md)                                         | Multiplicar y agregar                                                                                 | 1                 |       | x          |         |     |
| [Max-PS](max---ps.md)                                         | Máxima                                                                                          | 1                 |       | x          |         | x   |
| [min-PS](min---ps.md)                                         | Mínima                                                                                          | 1                 |       | x          |         | x   |
| [MOV-PS](mov---ps.md)                                         | Move                                                                                             | 1                 |       | x          |         |     |
| [mul-PS](mul---ps.md)                                         | Multiplicar                                                                                         | 1                 |       | x          |         |     |
| [NOP-PS](nop---ps.md)                                         | No hay ninguna operación                                                                                     | 1                 |       | x          |         |     |
| [NRM-PS](nrm---ps.md)                                         | Normalizar                                                                                        | 3                 |       | x          |         | x   |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [PS](ps---ps.md)                                                | Versión                                                                                          | 0                 | x     |            |         |     |
| [RCP-PS](rcp---ps.md)                                         | Quede                                                                                       | 1                 |       | x          |         | x   |
| [RSQ-PS](rsq---ps.md)                                         | Raíz cuadrada recíproca                                                                           | 1                 |       | x          |         | x   |
| [sincos (-PS](sincos---ps.md)                                   | Seno y coseno                                                                                  | 8                 |       | x          |         | x   |
| [Sub-PS](sub---ps.md)                                         | Restar                                                                                         | 1                 |       | x          |         |     |
| [texkill-PS](texkill---ps.md)                                 | Detener la representación de píxeles                                                                                | 1                 |       |            | x       |     |
| [texld-PS \_ 2 \_ 0 y arriba](texld---ps-2-0.md)                    | Muestra de una textura                                                                                 | 1                 |       |            | x       | x   |
| [texldb-PS](texldb---ps.md)                                   | Muestreo de textura con la diferencia de nivel de detalle del componente w                                      | 1                 |       |            | x       | x   |
| [texldp-PS](texldp---ps.md)                                   | Muestreo de textura con división proyectada por componente w                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




