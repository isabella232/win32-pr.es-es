---
title: ps_3_0 instrucciones
description: Esta sección contiene información de referencia para las instrucciones de la versión 3 0 del sombreador \_ de píxeles.
ms.assetid: 36972b9b-a4e7-45b4-83f5-959e75d270de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e44d13bfc726830a8c3fb770b34d5563fde2684f5c8bdf3fea54dec2312af4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982865"
---
# <a name="ps_3_0-instructions"></a>ps \_ 3 \_ 0 Instructions

Esta sección contiene información de referencia para las instrucciones de la versión 3 0 del sombreador \_ de píxeles.

Hay varios tipos de instrucciones de sombreador de píxeles, como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucción: número de ranuras de instrucción utilizadas por cada instrucción.
-   Configuración: un sombreador de píxeles debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Textura: estas instrucciones se usan para cargar y muestrear datos de textura, y para modificar las coordenadas de textura.
-   Flow control: estas instrucciones proporcionan control de flujo estático y dinámico para la ejecución de instrucciones.
-   Nuevo: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                             | Descripción                                                                          | Ranuras de instrucción | Configurar | Aritméticos | Textura | Control de flujo | Nuevo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [abs - ps](abs---ps.md)                                         | Valor absoluto                                                                       | 1                 |       | x          |         |              |     |
| [add - ps](add---ps.md)                                         | Agregar dos vectores                                                                      | 1                 |       | x          |         |              |     |
| [break- ps](break---ps.md)                                     | Interrupción de un bucle... endloop o rep... endrep block                                  | 1                 |       |            |         | x            |     |
| [break \_ comp - ps](break-comp---ps.md)                          | Interrupción condicional de un bucle... endloop o rep... endrep block, con una comparación | 3                 |       |            |         | x            |     |
| [breakp- ps](break-p---ps.md)                                  | interrumpir un bucle... endloop o rep... bloque endrep, basado en un predicado            | 3                 |       |            |         | x            |     |
| [call - ps](call---ps.md)                                       | Llamada a una subrutina                                                                    | 2                 |       |            |         | x            |     |
| [callnz bool - ps](callnz-bool---ps.md)                         | Llamar a una subrutina si un registro booleano no es cero                                  | 3                 |       |            |         | x            |     |
| [callnz pred - ps](callnz-pred---ps.md)                         | Llamar a una subrutina si un registro de predicado no es cero                                | 3                 |       |            |         | x            |     |
| [cmp - ps](cmp---ps.md)                                         | Comparar origen con 0                                                                  | 1                 |       | x          |         |              |     |
| [crs - ps](crs---ps.md)                                         | Producto cruzado                                                                        | 2                 |       | x          |         |              |     |
| [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) | Declarar la dimensión de textura de un muestreador                                          | 0                 | x     |            |         |              |     |
| [Semántica de dcl \_ (sm3 - ps asm)](dcl-usage---ps.md)              | Declarar registros de entrada y salida                                                   | 0                 | x     |            |         |              | x   |
| [def - ps](def---ps.md)                                         | Definición de constantes                                                                     | 0                 | x     |            |         |              |     |
| [defb - ps](defb---ps.md)                                       | Definición de una constante booleana                                                            | 0                 | x     |            |         |              |     |
| [defi - ps](defi---ps.md)                                       | Definición de una constante de entero                                                           | 0                 | x     |            |         |              |     |
| [dp2add - ps](dp2add---ps.md)                                   | Producto de punto 2D y adición                                                               | 2                 |       | x          |         |              |     |
| [dp3- ps](dp3---ps.md)                                         | Producto de punto 3D                                                                       | 1                 |       | x          |         |              |     |
| [dp4 - ps](dp4---ps.md)                                         | Producto de punto 4D                                                                       | 1                 |       | x          |         |              |     |
| [dsx - ps](dsx---ps.md)                                         | Velocidad de cambio en la dirección X                                                    | 2                 |       | x          |         |              |     |
| [dsy - ps](dsy---ps.md)                                         | Velocidad de cambio en la dirección y                                                    | 2                 |       | x          |         |              |     |
| [else: ps](else---ps.md)                                       | Iniciar un bloque else                                                                  | 1                 |       |            |         | x            |     |
| [endif: ps](endif---ps.md)                                     | Finalizar un if... bloque else                                                               | 1                 |       |            |         | x            |     |
| [endloop: ps](endloop---ps.md)                                 | Finalización de un bucle                                                                           | 2                 |       |            |         | x            | x   |
| [endrep - ps](endrep---ps.md)                                   | Final de un bloque de repetición                                                                | 2                 |       |            |         | x            |     |
| [exp - ps](exp---ps.md)                                         | Precisión completa 2<sup>x</sup>                                                         | 1                 |       | x          |         |              |     |
| [frc - ps](frc---ps.md)                                         | Componente fraccional                                                                 | 1                 |       | x          |         |              |     |
| [if bool - ps](if-bool---ps.md)                                 | Iniciar un bloque if                                                                    | 3                 |       |            |         | x            |     |
| [if \_ comp : ps](if-comp---ps.md)                                | Inicio de un bloque if con una comparación                                                  | 3                 |       |            |         | x            |     |
| [if pred - ps](if-pred---ps.md)                                 | Inicio de un bloque if con predicado                                                   | 3                 |       |            |         | x            |     |
| [label: ps](label---ps.md)                                     | Etiqueta                                                                                | 0                 |       |            |         | x            |     |
| [log: ps](log---ps.md)                                         | Registro de precisión completa(x)                                                               | 1                 |       | x          |         |              |     |
| [loop: ps](loop---ps.md)                                       | Loop                                                                                 | 3                 |       |            |         | x            | x   |
| [lrp : ps](lrp---ps.md)                                         | Interpolación lineal                                                                   | 2                 |       | x          |         |              |     |
| [m3x2 - ps](m3x2---ps.md)                                       | Multiplicación de 3x2                                                                         | 2                 |       | x          |         |              |     |
| [m3x3 - ps](m3x3---ps.md)                                       | Multiplicación de 3x3                                                                         | 3                 |       | x          |         |              |     |
| [m3x4 - ps](m3x4---ps.md)                                       | Multiplicación de 3x4                                                                         | 4                 |       | x          |         |              |     |
| [m4x3 - ps](m4x3---ps.md)                                       | Multiplicación de 4x3                                                                         | 3                 |       | x          |         |              |     |
| [m4x4 - ps](m4x4---ps.md)                                       | Multiplicación de 4x4                                                                         | 4                 |       | x          |         |              |     |
| [mad - ps](mad---ps.md)                                         | Multiplicar y agregar                                                                     | 1                 |       | x          |         |              |     |
| [max - ps](max---ps.md)                                         | Máximo                                                                              | 1                 |       | x          |         |              |     |
| [min - ps](min---ps.md)                                         | Mínima                                                                              | 1                 |       | x          |         |              |     |
| [mov - ps](mov---ps.md)                                         | Move                                                                                 | 1                 |       | x          |         |              |     |
| [mul - ps](mul---ps.md)                                         | Multiplicar                                                                             | 1                 |       | x          |         |              |     |
| [nop - ps](nop---ps.md)                                         | No hay ninguna operación                                                                         | 1                 |       | x          |         |              |     |
| [nrm - ps](nrm---ps.md)                                         | Normalizar                                                                            | 3                 |       | x          |         |              |     |
| [pow - ps](pow---ps.md)                                         | x<sup>y</sup>                                                                        | 3                 |       | x          |         |              |     |
| [ps](ps---ps.md)                                                | Versión                                                                              | 0                 | x     |            |         |              |     |
| [rcp - ps](rcp---ps.md)                                         | Recíproco                                                                           | 1                 |       | x          |         |              |     |
| [rep - ps](rep---ps.md)                                         | Repetir                                                                               | 3                 |       |            |         | x            |     |
| [ret - ps](ret---ps.md)                                         | Fin de una subrutina                                                                  | 1                 |       |            |         | x            |     |
| [rsq - ps](rsq---ps.md)                                         | Raíz cuadrada recíproca                                                               | 1                 |       | x          |         |              |     |
| [setp \_ comp](setp-comp---ps.md)                                 | Establecer el registro de predicado                                                           | 1                 |       |            |         | x            |     |
| [sincos- ps](sincos---ps.md)                                   | Seno y coseno                                                                      | 8                 |       | x          |         |              |     |
| [sub - ps](sub---ps.md)                                         | Restar                                                                             | 1                 |       | x          |         |              |     |
| [texkill - ps](texkill---ps.md)                                 | Eliminación de la representación de píxeles                                                                    | 2                 |       |            | x       |              |     |
| [ld- ps \_ 2 \_ 0 y up](texld---ps-2-0.md)                    | Muestrear una textura                                                                     | Consulte la nota 1.        |       |            | x       |              |     |
| [texldb - ps](texldb---ps.md)                                   | Muestreo de textura con sesgo de nivel de detalle de w-component                          | 6                 |       |            | x       |              |     |
| [texldl - ps](texldl---ps.md)                                   | Muestreo de textura con nivel de detalle de w-component                               | Consulte la nota 2.        |       |            | x       |              | x   |
| [texldd - ps](texldd---ps.md)                                   | Muestreo de textura con degradados proporcionados por el usuario                                        | 3                 |       |            | x       |              |     |
| [texldp - ps](texldp---ps.md)                                   | Muestreo de textura con división projective por w-component                               | Consulte la nota 3.        |       |            | x       |              |     |



 

Notas:

1.  Si la textura es un mapa de cubo, ranuras = 4; en caso contrario, ranuras = 1.
2.  Si la textura es un mapa de cubo, ranuras = 5; en caso contrario, ranuras = 2.
3.  Si la textura es un mapa de cubo, ranuras = 4; en caso contrario, ranuras = 3.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




