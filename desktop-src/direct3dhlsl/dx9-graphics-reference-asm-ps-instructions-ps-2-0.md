---
title: ps_2_0 instrucciones
description: Esta sección contiene información de referencia para las instrucciones de la versión 2 0 del sombreador \_ de píxeles.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 292263ed6331c8cc878d6dbd9cfa3e4d766c193d2242b841afb926b296675ccf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067995"
---
# <a name="ps_2_0-instructions"></a>ps \_ 2 \_ 0 Instrucciones

Esta sección contiene información de referencia para las instrucciones de la versión 2 0 del sombreador \_ de píxeles.

Hay varios tipos de instrucciones de sombreador de píxeles, como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucción: número de espacios de instrucciones usados por cada instrucción.
-   Configuración: un sombreador de píxeles debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Textura: estas instrucciones se usan para cargar y muestrear datos de textura, y para modificar las coordenadas de textura.
-   Nuevo: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                             | Descripción                                                                                      | Ranuras de instrucción | Configurar | Aritméticos | Textura | Nuevo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [abs - ps](abs---ps.md)                                         | Valor absoluto                                                                                   | 1                 |       | x          |         | x   |
| [add - ps](add---ps.md)                                         | Agregar dos vectores                                                                                  | 1                 |       | x          |         |     |
| [cmp: ps](cmp---ps.md)                                         | Comparar origen con 0                                                                              | 1                 |       | x          |         |     |
| [crs- ps](crs---ps.md)                                         | Producto cruzado                                                                                    | 2                 |       | x          |         | x   |
| [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) | Declarar la dimensión de textura para un muestreador                                                      | 0                 | x     |            |         | x   |
| [dcl - (sm2, sm3 - ps asm)](dcl---ps.md)                        | Declare la asociación entre los registros de salida del sombreador de vértices y los registros de entrada del sombreador de píxeles. | 0                 | x     |            |         | x   |
| [def - ps](def---ps.md)                                         | Definición de constantes                                                                                 | 0                 | x     |            |         |     |
| [dp2add - ps](dp2add---ps.md)                                   | Producto de punto 2D y adición                                                                           | 2                 |       | x          |         | x   |
| [dp3: ps](dp3---ps.md)                                         | Producto de punto 3D                                                                                   | 1                 |       | x          |         |     |
| [dp4- ps](dp4---ps.md)                                         | Producto de punto 4D                                                                                   | 1                 |       | x          |         |     |
| [exp - ps](exp---ps.md)                                         | Precisión completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [frc - ps](frc---ps.md)                                         | Componente fraccional                                                                             | 1                 |       | x          |         | x   |
| [log: ps](log---ps.md)                                         | Registro de precisión completa(x)                                                                           | 1                 |       | x          |         | x   |
| [lrp : ps](lrp---ps.md)                                         | Interpolación lineal                                                                               | 2                 |       | x          |         |     |
| [m3x2 - ps](m3x2---ps.md)                                       | Multiplicación de 3x2                                                                                     | 2                 |       | x          |         | x   |
| [m3x3 - ps](m3x3---ps.md)                                       | Multiplicación de 3x3                                                                                     | 3                 |       | x          |         | x   |
| [m3x4 - ps](m3x4---ps.md)                                       | Multiplicación de 3x4                                                                                     | 4                 |       | x          |         | x   |
| [m4x3 - ps](m4x3---ps.md)                                       | Multiplicación de 4x3                                                                                     | 3                 |       | x          |         | x   |
| [m4x4 - ps](m4x4---ps.md)                                       | Multiplicación de 4x4                                                                                     | 4                 |       | x          |         | x   |
| [mad - ps](mad---ps.md)                                         | Multiplicar y agregar                                                                                 | 1                 |       | x          |         |     |
| [max - ps](max---ps.md)                                         | Máximo                                                                                          | 1                 |       | x          |         | x   |
| [min - ps](min---ps.md)                                         | Mínima                                                                                          | 1                 |       | x          |         | x   |
| [mov - ps](mov---ps.md)                                         | Move                                                                                             | 1                 |       | x          |         |     |
| [mul - ps](mul---ps.md)                                         | Multiplicar                                                                                         | 1                 |       | x          |         |     |
| [nop - ps](nop---ps.md)                                         | No hay ninguna operación                                                                                     | 1                 |       | x          |         |     |
| [nrm - ps](nrm---ps.md)                                         | Normalizar                                                                                        | 3                 |       | x          |         | x   |
| [pow : ps](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [ps](ps---ps.md)                                                | Versión                                                                                          | 0                 | x     |            |         |     |
| [rcp - ps](rcp---ps.md)                                         | Recíproco                                                                                       | 1                 |       | x          |         | x   |
| [rsq - ps](rsq---ps.md)                                         | Raíz cuadrada recíproca                                                                           | 1                 |       | x          |         | x   |
| [sincos: ps](sincos---ps.md)                                   | Seno y coseno                                                                                  | 8                 |       | x          |         | x   |
| [sub - ps](sub---ps.md)                                         | Restar                                                                                         | 1                 |       | x          |         |     |
| [texkill - ps](texkill---ps.md)                                 | Eliminación de la representación de píxeles                                                                                | 1                 |       |            | x       |     |
| [texld: ps \_ 2 \_ 0 y up](texld---ps-2-0.md)                    | Muestrear una textura                                                                                 | 1                 |       |            | x       | x   |
| [texldb: ps](texldb---ps.md)                                   | Muestreo de textura con sesgo de nivel de detalle de w-component                                      | 1                 |       |            | x       | x   |
| [texldp: ps](texldp---ps.md)                                   | Muestreo de textura con división projectiva por w-component                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




