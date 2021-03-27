---
title: Instrucciones de ps_3_0
description: Esta sección contiene información de referencia para las instrucciones del sombreador de píxeles versión 3 \_ 0.
ms.assetid: 36972b9b-a4e7-45b4-83f5-959e75d270de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d43f17ef765feb5899c7dd4537a1770155b4aa59
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903892"
---
# <a name="ps_3_0-instructions"></a>Instrucciones de PS \_ 3 \_ 0

Esta sección contiene información de referencia para las instrucciones del sombreador de píxeles versión 3 \_ 0.

Hay varios tipos de instrucciones de sombreador de píxeles, tal como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucciones: número de ranuras de instrucciones usadas por cada instrucción.
-   Configuración: un sombreador de píxeles debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Texture: estas instrucciones se usan para cargar y muestrear los datos de textura y para modificar las coordenadas de textura.
-   Control de flujo: estas instrucciones proporcionan control de flujo estático y dinámico a la ejecución de instrucciones.
-   Nuevas: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                             | Descripción                                                                          | Ranuras de instrucciones | Configurar | Aritméticos | Textura | Control de flujo | Nuevo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-PS](abs---ps.md)                                         | Valor absoluto                                                                       | 1                 |       | x          |         |              |     |
| [Agregar-PS](add---ps.md)                                         | Agregar dos vectores                                                                      | 1                 |       | x          |         |              |     |
| [Break-PS](break---ps.md)                                     | Salir de un bucle... ENDLOOP o Rep... bloque endrep                                  | 1                 |       |            |         | x            |     |
| [Break \_ COMP-PS](break-comp---ps.md)                          | Interrumpir condicionalmente un bucle... ENDLOOP o Rep... bloque endrep, con una comparación | 3                 |       |            |         | x            |     |
| [breakp-PS](break-p---ps.md)                                  | salir de un bucle... ENDLOOP o Rep... bloque endrep, basado en un predicado            | 3                 |       |            |         | x            |     |
| [llamada a PS](call---ps.md)                                       | Llamar a una subrutina                                                                    | 2                 |       |            |         | x            |     |
| [callnz bool-PS](callnz-bool---ps.md)                         | Llamar a una subrutina si un registro booleano no es cero                                  | 3                 |       |            |         | x            |     |
| [callnz Pred-PS](callnz-pred---ps.md)                         | Llamar a una subrutina si un registro de predicado no es cero                                | 3                 |       |            |         | x            |     |
| [CMP-PS](cmp---ps.md)                                         | Comparar origen con 0                                                                  | 1                 |       | x          |         |              |     |
| [CRS-PS](crs---ps.md)                                         | Producto cruzado                                                                        | 2                 |       | x          |         |              |     |
| [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Declarar la dimensión de textura para una muestra                                          | 0                 | x     |            |         |              |     |
| [\_semántica de DCL (SM3-PS ASM)](dcl-usage---ps.md)              | Declarar registros de entrada y salida                                                   | 0                 | x     |            |         |              | x   |
| [DEF-PS](def---ps.md)                                         | Definir constantes                                                                     | 0                 | x     |            |         |              |     |
| [defb-PS](defb---ps.md)                                       | Definir una constante booleana                                                            | 0                 | x     |            |         |              |     |
| [defi-PS](defi---ps.md)                                       | Definir una constante de tipo entero                                                           | 0                 | x     |            |         |              |     |
| [dp2add-PS](dp2add---ps.md)                                   | producto de punto 2D y agregar                                                               | 2                 |       | x          |         |              |     |
| [DP3-PS](dp3---ps.md)                                         | producto de punto 3D                                                                       | 1                 |       | x          |         |              |     |
| [DP4-PS](dp4---ps.md)                                         | 4D DOT producto                                                                       | 1                 |       | x          |         |              |     |
| [DSX-PS](dsx---ps.md)                                         | Velocidad de cambio en la dirección x                                                    | 2                 |       | x          |         |              |     |
| [DSY-PS](dsy---ps.md)                                         | Velocidad de cambio en la dirección y                                                    | 2                 |       | x          |         |              |     |
| [Else-PS](else---ps.md)                                       | Comenzar un bloque else                                                                  | 1                 |       |            |         | x            |     |
| [endif-PS](endif---ps.md)                                     | Finalizar un if... bloque else                                                               | 1                 |       |            |         | x            |     |
| [ENDLOOP-PS](endloop---ps.md)                                 | Finalizar un bucle                                                                           | 2                 |       |            |         | x            | x   |
| [endrep-PS](endrep---ps.md)                                   | Final de un bloque de repetición                                                                | 2                 |       |            |         | x            |     |
| [EXP-PS](exp---ps.md)                                         | Precisión completa 2<sup>x</sup>                                                         | 1                 |       | x          |         |              |     |
| [FRC-PS](frc---ps.md)                                         | Componente fraccionario                                                                 | 1                 |       | x          |         |              |     |
| [Si es bool-PS](if-bool---ps.md)                                 | Iniciar un bloque if                                                                    | 3                 |       |            |         | x            |     |
| [Si \_ COMP-PS](if-comp---ps.md)                                | Comenzar un bloque if con una comparación                                                  | 3                 |       |            |         | x            |     |
| [Si Pred-PS](if-pred---ps.md)                                 | Comenzar un bloque if con predication                                                   | 3                 |       |            |         | x            |     |
| [etiqueta-PS](label---ps.md)                                     | Etiqueta                                                                                | 0                 |       |            |         | x            |     |
| [registro: PS](log---ps.md)                                         | ₂ de registro de precisión completa (x)                                                               | 1                 |       | x          |         |              |     |
| [bucle-PS](loop---ps.md)                                       | Loop                                                                                 | 3                 |       |            |         | x            | x   |
| [LRP-PS](lrp---ps.md)                                         | Interpolación lineal                                                                   | 2                 |       | x          |         |              |     |
| [m3x2-PS](m3x2---ps.md)                                       | 3x2 multiplicar                                                                         | 2                 |       | x          |         |              |     |
| [M3x3-PS](m3x3---ps.md)                                       | multiplicar 3x3                                                                         | 3                 |       | x          |         |              |     |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 multiplicar                                                                         | 4                 |       | x          |         |              |     |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 multiplicar                                                                         | 3                 |       | x          |         |              |     |
| [M4x4-PS](m4x4---ps.md)                                       | multiplicar 4x4                                                                         | 4                 |       | x          |         |              |     |
| [Mad-PS](mad---ps.md)                                         | Multiplicar y agregar                                                                     | 1                 |       | x          |         |              |     |
| [Max-PS](max---ps.md)                                         | Máxima                                                                              | 1                 |       | x          |         |              |     |
| [min-PS](min---ps.md)                                         | Mínima                                                                              | 1                 |       | x          |         |              |     |
| [MOV-PS](mov---ps.md)                                         | Move                                                                                 | 1                 |       | x          |         |              |     |
| [mul-PS](mul---ps.md)                                         | Multiplicar                                                                             | 1                 |       | x          |         |              |     |
| [NOP-PS](nop---ps.md)                                         | No hay ninguna operación                                                                         | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normalizar                                                                            | 3                 |       | x          |         |              |     |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                        | 3                 |       | x          |         |              |     |
| [PS](ps---ps.md)                                                | Versión                                                                              | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Quede                                                                           | 1                 |       | x          |         |              |     |
| [REP-PS](rep---ps.md)                                         | Repetir                                                                               | 3                 |       |            |         | x            |     |
| [RET-PS](ret---ps.md)                                         | Final de una subrutina                                                                  | 1                 |       |            |         | x            |     |
| [RSQ-PS](rsq---ps.md)                                         | Raíz cuadrada recíproca                                                               | 1                 |       | x          |         |              |     |
| [comp. SETP \_](setp-comp---ps.md)                                 | Establecimiento del registro de predicado                                                           | 1                 |       |            |         | x            |     |
| [sincos (-PS](sincos---ps.md)                                   | Seno y coseno                                                                      | 8                 |       | x          |         |              |     |
| [Sub-PS](sub---ps.md)                                         | Restar                                                                             | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Detener la representación de píxeles                                                                    | 2                 |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 y arriba](texld---ps-2-0.md)                    | Muestra de una textura                                                                     | Vea la nota 1        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Muestreo de textura con la diferencia de nivel de detalle del componente w                          | 6                 |       |            | x       |              |     |
| [texldl-PS](texldl---ps.md)                                   | Muestreo de textura con el nivel de detalle del componente w                               | Consulte la nota 2.        |       |            | x       |              | x   |
| [texldd-PS](texldd---ps.md)                                   | Muestreo de textura con degradados proporcionados por el usuario                                        | 3                 |       |            | x       |              |     |
| [texldp-PS](texldp---ps.md)                                   | Muestreo de textura con división proyectada por componente w                               | Vea la nota 3        |       |            | x       |              |     |



 

Notas:

1.  Si la textura es un mapa de cubo, ranuras = 4; en caso contrario, ranuras = 1.
2.  Si la textura es un mapa de cubo, ranuras = 5; en caso contrario, ranuras = 2.
3.  Si la textura es un mapa de cubo, ranuras = 4; en caso contrario, ranuras = 3.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




