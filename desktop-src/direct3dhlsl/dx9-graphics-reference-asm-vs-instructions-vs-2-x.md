---
title: 'Instrucciones: vs_2_x'
description: Esta sección contiene información de referencia para las instrucciones x de la versión 2 del sombreador \_ de vértices.
ms.assetid: fac85f96-0f4b-49a8-9c00-9e68000d1c76
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9997e26625005abd0f2e38ab885b95b8f8febd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567804"
---
# <a name="instructions---vs_2_x"></a>Instrucciones: frente \_ a 2 \_ x

Esta sección contiene información de referencia para las instrucciones x de la versión 2 del sombreador \_ de vértices.

Hay varios tipos de instrucciones de sombreador de vértices, como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucción: número de ranuras de instrucción utilizadas por cada instrucción.
-   Configuración: instrucciones no aritméticas. Cada sombreador debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Flow control de flujo: estas instrucciones agregan funcionalidades de control de flujo, como [bucle, frente a](loop---vs.md)... [endloop - vs](endloop---vs.md), [if bool - vs](if-bool---vs.md)... [else](else---vs.md)... [endif](endif---vs.md)y llamadas subrutinas.
-   Nuevo: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                                           | Descripción                                                                                                                                                            | Ranuras de instrucción | Configurar | Aritméticos | Control de flujo | Nuevo |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [abs - vs](abs---vs.md)                                                       | Valor absoluto                                                                                                                                                         | 1                 |       | x          |              |     |
| [add - vs](add---vs.md)                                                       | Agregar dos vectores                                                                                                                                                        | 1                 |       | x          |              |     |
| [break- vs](break---vs.md)                                                   | Interrupción de un [bucle: vs...](loop---vs.md) [endloop- vs](endloop---vs.md) o [rep](rep---vs.md)... [endrep block](endrep---vs.md)                                  | 1                 |       |            | x            | x   |
| [break \_ comp - vs](break-comp---vs.md)                                        | Interrupción condicional de un [bucle: frente](loop---vs.md)a ... [endloop- vs](endloop---vs.md) o [rep](rep---vs.md)... [endrep](endrep---vs.md) block, con una comparación | 3                 |       |            | x            | x   |
| [breakp: vs](breakp---vs.md)                                                 | Interrupción de un [bucle: vs...](loop---vs.md) [endloop- vs](endloop---vs.md) o [rep](rep---vs.md)... [bloque endrep,](endrep---vs.md) basado en un predicado            | 3                 |       |            | x            | x   |
| [call - vs](call---vs.md)                                                     | Llamada a una subrutina                                                                                                                                                      | 2                 |       |            | x            |     |
| [callnz bool - vs](callnz-bool---vs.md)                                       | Llamar a una subrutina si un registro booleano no es cero                                                                                                                    | 3                 |       |            | x            |     |
| [callnz pred - vs](callnz-pred---vs.md)                                       | Llamar a una subrutina si un registro de predicado no es cero                                                                                                                  | 3                 |       |            | x            | x   |
| [crs- vs](crs---vs.md)                                                       | Producto cruzado                                                                                                                                                          | 2                 |       | x          |              |     |
| [dcl \_ usage input (sm1, sm2, sm3 - vs asm)](dcl-usage-input-register---vs.md) | Declarar registros de vértices de entrada [(vea Registros- frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md))                                                        | 0                 | x     |            |              |     |
| [def - vs](def---vs.md)                                                       | Definición de constantes                                                                                                                                                       | 0                 | x     |            |              |     |
| [defb - vs](defb---vs.md)                                                     | Definición de una constante booleana                                                                                                                                              | 0                 | x     |            |              |     |
| [defi- vs](defi---vs.md)                                                     | Definición de una constante de entero                                                                                                                                             | 0                 | x     |            |              |     |
| [dp3: vs](dp3---vs.md)                                                       | Producto de puntos de tres componentes                                                                                                                                            | 1                 |       | x          |              |     |
| [dp4: vs](dp4---vs.md)                                                       | Producto de punto de cuatro componentes                                                                                                                                             | 1                 |       | x          |              |     |
| [dst - vs](dst---vs.md)                                                       | Calcular el vector de distancia                                                                                                                                          | 1                 |       | x          |              |     |
| [else - vs](else---vs.md)                                                     | Begin an [else - vs](else---vs.md) block                                                                                                                              | 1                 |       |            | x            |     |
| [endif- vs](endif---vs.md)                                                   | End an [if bool - vs](if-bool---vs.md)... [else- vs](else---vs.md) block                                                                                             | 1                 |       |            | x            |     |
| [endloop- vs](endloop---vs.md)                                               | Fin de un [bucle: vs](loop---vs.md) block                                                                                                                              | 2                 |       |            | x            |     |
| [endrep- vs](endrep---vs.md)                                                 | Fin de un bloque de repetición                                                                                                                                                  | 2                 |       |            | x            |     |
| [exp : frente a](exp---vs.md)                                                       | Precisión completa 2<sup>x</sup>                                                                                                                                           | 1                 |       | x          |              |     |
| [exp : frente a](exp---vs.md)                                                       | Precisión parcial 2<sup>x</sup>                                                                                                                                        | 1                 |       | x          |              |     |
| [frc - vs](frc---vs.md)                                                       | Componente fraccionrio                                                                                                                                                   | 1                 |       | x          |              |     |
| [if bool - vs](if-bool---vs.md)                                               | Begin an [if bool - vs](if-bool---vs.md) block (con una condición booleana)                                                                                            | 3                 |       |            | x            |     |
| [if \_ comp - vs](if-comp---vs.md)                                              | Begin an [if bool - vs](if-bool---vs.md) block, with a comparison                                                                                                     | 3                 |       |            | x            | x   |
| [if pred - vs](if-pred---vs.md)                                               | Begin an [if bool - vs](if-bool---vs.md) block with a predicate condition                                                                                             | 3                 |       |            | x            | x   |
| [label - vs](label---vs.md)                                                   | Etiqueta                                                                                                                                                                  | 0                 |       |            | x            |     |
| [lit- vs](lit---vs.md)                                                       | Cálculo de iluminación parcial                                                                                                                                           | 3                 |       | x          |              |     |
| [log- vs](log---vs.md)                                                       | Registro de precisión completa( x)                                                                                                                                                 | 1                 |       | x          |              |     |
| [logp- vs](logp---vs.md)                                                     | Registro de precisión parcial( x)                                                                                                                                              | 1                 |       | x          |              |     |
| [loop: vs](loop---vs.md)                                                     | Loop                                                                                                                                                                   | 3                 |       |            | x            |     |
| [lrp - vs](lrp---vs.md)                                                       | Interpolación lineal                                                                                                                                                   | 2                 |       | x          |              |     |
| [m3x2- vs](m3x2---vs.md)                                                     | Multiplicación de 3x2                                                                                                                                                           | 2                 |       | x          |              |     |
| [m3x3- vs](m3x3---vs.md)                                                     | Multiplicación de 3x3                                                                                                                                                           | 3                 |       | x          |              |     |
| [m3x4: vs](m3x4---vs.md)                                                     | Multiplicación de 3x4                                                                                                                                                           | 4                 |       | x          |              |     |
| [m4x3: vs](m4x3---vs.md)                                                     | Multiplicación de 4x3                                                                                                                                                           | 3                 |       | x          |              |     |
| [m4x4: vs](m4x4---vs.md)                                                     | Multiplicación de 4x4                                                                                                                                                           | 4                 |       | x          |              |     |
| [loca: vs](mad---vs.md)                                                       | Multiplicar y agregar                                                                                                                                                       | 1                 |       | x          |              |     |
| [max - vs](max---vs.md)                                                       | Máxima                                                                                                                                                                | 1                 |       | x          |              |     |
| [min- vs](min---vs.md)                                                       | Mínima                                                                                                                                                                | 1                 |       | x          |              |     |
| [mov - vs](mov---vs.md)                                                       | Move                                                                                                                                                                   | 1                 |       | x          |              |     |
| [mova- vs](mova---vs.md)                                                     | Mover datos de un registro de punto flotante al registro de direcciones (a0)                                                                                                  | 1                 |       | x          |              |     |
| [mul - vs](mul---vs.md)                                                       | Multiplicar                                                                                                                                                               | 1                 |       | x          |              |     |
| [nop - vs](nop---vs.md)                                                       | No hay ninguna operación                                                                                                                                                           | 1                 |       | x          |              |     |
| [nrm: frente a](nrm---vs.md)                                                       | Normalización de un vector 4D                                                                                                                                                  | 3                 |       | x          |              |     |
| [pow - vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                                                                          | 3                 |       | x          |              |     |
| [rcp - vs](rcp---vs.md)                                                       | Recíproco                                                                                                                                                             | 1                 |       | x          |              |     |
| [rep - vs](rep---vs.md)                                                       | Repetir                                                                                                                                                                 | 3                 |       |            | x            |     |
| [ret - vs](ret---vs.md)                                                       | Fin de una subrutina o principal                                                                                                                                     | 1                 |       |            | x            |     |
| [rsq- vs](rsq---vs.md)                                                       | Raíz cuadrada recíproca                                                                                                                                                 | 1                 |       | x          |              |     |
| [setp \_ comp - vs](setp-comp---vs.md)                                          | Establecer el registro de predicado                                                                                                                                             | 1                 |       |            | x            | x   |
| [sge- vs](sge---vs.md)                                                       | Comparación mayor o igual                                                                                                                                          | 1                 |       | x          |              |     |
| [sgn - vs](sgn---vs.md)                                                       | Firma                                                                                                                                                                   | 3                 |       | x          |              |     |
| [sincos: frente a](sincos---vs.md)                                                 | Seno y coseno                                                                                                                                                        | 8                 |       | x          |              |     |
| [slt- vs](slt---vs.md)                                                       | Menor que compare                                                                                                                                                      | 1                 |       | x          |              |     |
| [sub - vs](sub---vs.md)                                                       | Restar                                                                                                                                                               | 1                 |       | x          |              |     |
| [Vs](vs---vs.md)                                                              | Version                                                                                                                                                                | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




