---
title: 'Instrucciones: vs_3_0'
description: Esta sección contiene información de referencia para las instrucciones de la versión 3 0 del sombreador de vértices \_ .
ms.assetid: 2309a643-dec8-4f2a-a217-e7f1e90b5f43
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f134c47f5697381c211808ce5a46ab5ee23031b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994374"
---
# <a name="instructions---vs_3_0"></a>Instrucciones-vs \_ 3 \_ 0

Esta sección contiene información de referencia para las instrucciones de la versión 3 0 del sombreador de vértices \_ .

Hay varios tipos de instrucciones de sombreador de vértices, tal como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucciones: número de ranuras de instrucciones usadas por cada instrucción.
-   Instalación: instrucciones no aritméticas. Cada sombreador debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Texture: estas instrucciones admiten la búsqueda de direcciones de textura.
-   Control de flujo: estas instrucciones agregan control de flujo, como bucles, repeticiones y, [si es bool-vs](if-bool---vs.md)... [otra cosa](else---vs.md)... comparaciones de [endif](endif---vs.md) .
-   Nuevas: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                                           | Descripción                                                                                                                                                            | Ranuras de instrucciones | Configurar | Aritméticos | Textura | Control de flujo | Nuevo |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-vs](abs---vs.md)                                                       | Valor absoluto                                                                                                                                                         | 1                 |       | x          |         |              |     |
| [Agregar vs](add---vs.md)                                                       | Agregar dos vectores                                                                                                                                                        | 1                 |       | x          |         |              |     |
| [Inter-vs](break---vs.md)                                                   | Interrumpir un [bucle-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) o [REP](rep---vs.md)... bloque [endrep](endrep---vs.md)                                  | 1                 |       |            |         | x            |     |
| [Break \_ COMP-vs](break-comp---vs.md)                                        | Interrumpir condicionalmente un [bucle-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) o [REP](rep---vs.md)... bloque [endrep](endrep---vs.md) , con una comparación | 3                 |       |            |         | x            |     |
| [breakp-vs](breakp---vs.md)                                                 | Interrumpir un [bucle-vs](loop---vs.md)... [ENDLOOP-vs](endloop---vs.md) o [REP](rep---vs.md)... bloque [endrep](endrep---vs.md) , basado en un predicado            | 3                 |       |            |         | x            |     |
| [llamada-vs](call---vs.md)                                                     | Llamar a una subrutina                                                                                                                                                      | 2                 |       |            |         | x            |     |
| [callnz bool-vs](callnz-bool---vs.md)                                       | Llamar a una subrutina si un registro booleano no es cero                                                                                                                    | 3                 |       |            |         | x            |     |
| [callnz Pred-vs](callnz-pred---vs.md)                                       | Llamar a una subrutina si un registro de predicado no es cero                                                                                                                  | 3                 |       |            |         | x            |     |
| [CRS-vs](crs---vs.md)                                                       | Producto cruzado                                                                                                                                                          | 2                 |       | x          |         |              |     |
| [\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Declarar registros de vértices de entrada (consulte [registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md))                                                        | 0                 | x     |            |         |              |     |
| [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)                    | Declarar la dimensión de textura para una muestra                                                                                                                            | 0                 | x     |            |         |              | x   |
| [DEF-vs](def---vs.md)                                                       | Definir constantes                                                                                                                                                       | 0                 | x     |            |         |              |     |
| [defb-vs](defb---vs.md)                                                     | Declarar una constante booleana                                                                                                                                             | 0                 | x     |            |         |              |     |
| [defi-vs](defi---vs.md)                                                     | Declarar una constante de tipo entero                                                                                                                                            | 0                 | x     |            |         |              |     |
| [DP3-vs](dp3---vs.md)                                                       | Producto de tres componentes                                                                                                                                            | 1                 |       | x          |         |              |     |
| [DP4-vs](dp4---vs.md)                                                       | Producto de cuatro componentes                                                                                                                                             | 1                 |       | x          |         |              |     |
| [DST-vs](dst---vs.md)                                                       | Distancia                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [Else-vs](else---vs.md)                                                     | Comenzar un bloque [else](else---vs.md)                                                                                                                                   | 1                 |       |            |         | x            |     |
| [endif-vs](endif---vs.md)                                                   | Finalizar una expresión [If bool-vs](if-bool---vs.md)... bloque [else](else---vs.md)                                                                                                  | 1                 |       |            |         | x            |     |
| [ENDLOOP-vs](endloop---vs.md)                                               | Final de un [bucle: bloque vs](loop---vs.md)                                                                                                                              | 2                 |       |            |         | x            |     |
| [endrep-vs](endrep---vs.md)                                                 | Final de un bloque de repetición                                                                                                                                                  | 2                 |       |            |         | x            |     |
| [EXP-vs](exp---vs.md)                                                       | Precisión completa 2<sup>x</sup>                                                                                                                                           | 1                 |       | x          |         |              |     |
| [EXP-vs](exp---vs.md)                                                       | Precisión parcial 2<sup>x</sup>                                                                                                                                        | 1                 |       | x          |         |              |     |
| [FRC-vs](frc---vs.md)                                                       | Componente fraccionario                                                                                                                                                   | 1                 |       | x          |         |              |     |
| [Si es bool-vs](if-bool---vs.md)                                               | Comenzar un bloque [If bool-vs](if-bool---vs.md) (mediante una condición booleana)                                                                                            | 3                 |       |            |         | x            |     |
| [If \_ COMP-vs](if-comp---vs.md)                                              | Comenzar un bloque [If bool-vs](if-bool---vs.md) con una comparación                                                                                                     | 3                 |       |            |         | x            |     |
| [Si Pred-vs](if-pred---vs.md)                                               | Comienza un bloque [If bool-vs](if-bool---vs.md) con una condición de predicado                                                                                             | 3                 |       |            |         | x            |     |
| [etiqueta-frente](label---vs.md)                                                   | Etiqueta                                                                                                                                                                  | 0                 |       |            |         | x            |     |
| [Lit-vs](lit---vs.md)                                                       | Calcular iluminación                                                                                                                                                     | 3                 |       | x          |         |              |     |
| [log-vs](log---vs.md)                                                       | ₂ de registro de precisión completa (x)                                                                                                                                                 | 1                 |       | x          |         |              |     |
| [logP-vs](logp---vs.md)                                                     | Registro de precisión parcial ₂ (x)                                                                                                                                              | 1                 |       | x          |         |              |     |
| [bucle-vs](loop---vs.md)                                                     | Loop                                                                                                                                                                   | 3                 |       |            |         | x            |     |
| [LRP-vs](lrp---vs.md)                                                       | Interpolación lineal                                                                                                                                                   | 2                 |       | x          |         |              |     |
| [m3x2-vs](m3x2---vs.md)                                                     | 3x2 multiplicar                                                                                                                                                           | 2                 |       | x          |         |              |     |
| [M3x3-vs](m3x3---vs.md)                                                     | multiplicar 3x3                                                                                                                                                           | 3                 |       | x          |         |              |     |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 multiplicar                                                                                                                                                           | 4                 |       | x          |         |              |     |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 multiplicar                                                                                                                                                           | 3                 |       | x          |         |              |     |
| [M4x4-vs](m4x4---vs.md)                                                     | multiplicar 4x4                                                                                                                                                           | 4                 |       | x          |         |              |     |
| [Mad-vs](mad---vs.md)                                                       | Multiplicar y agregar                                                                                                                                                       | 1                 |       | x          |         |              |     |
| [Max-vs](max---vs.md)                                                       | Máxima                                                                                                                                                                | 1                 |       | x          |         |              |     |
| [min-vs](min---vs.md)                                                       | Mínima                                                                                                                                                                | 1                 |       | x          |         |              |     |
| [MOV-vs](mov---vs.md)                                                       | Move                                                                                                                                                                   | 1                 |       | x          |         |              |     |
| [mova-vs](mova---vs.md)                                                     | Movimiento de datos desde un registro de punto flotante a un registro entero                                                                                                        | 1                 |       | x          |         |              |     |
| [mul-vs](mul---vs.md)                                                       | Multiplicar                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [NOP-vs](nop---vs.md)                                                       | No hay ninguna operación                                                                                                                                                           | 1                 |       | x          |         |              |     |
| [NRM-vs](nrm---vs.md)                                                       | Normalizar                                                                                                                                                              | 3                 |       | x          |         |              |     |
| [Pow-vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                                                                          | 3                 |       | x          |         |              |     |
| [RCP-vs](rcp---vs.md)                                                       | Quede                                                                                                                                                             | 1                 |       | x          |         |              |     |
| [REP-vs](rep---vs.md)                                                       | Repetir                                                                                                                                                                 | 3                 |       |            |         | x            |     |
| [RET-vs](ret---vs.md)                                                       | Final de una subrutina                                                                                                                                                    | 1                 |       |            |         | x            |     |
| [RSQ-vs](rsq---vs.md)                                                       | Raíz cuadrada recíproca                                                                                                                                                 | 1                 |       | x          |         |              |     |
| [\_COMP SETP-vs](setp-comp---vs.md)                                          | Establecimiento del registro de predicado                                                                                                                                             | 1                 |       |            |         | x            |     |
| [SGE-vs](sge---vs.md)                                                       | Comparación mayor o igual que                                                                                                                                          | 1                 |       | x          |         |              |     |
| [SGN-vs](sgn---vs.md)                                                       | Firma                                                                                                                                                                   | 3                 |       | x          |         |              |     |
| [sincos (-vs](sincos---vs.md)                                                 | Seno y coseno                                                                                                                                                        | 8                 |       | x          |         |              |     |
| [SLT-vs](slt---vs.md)                                                       | Menor que comparar                                                                                                                                                      | 1                 |       | x          |         |              |     |
| [Sub-vs](sub---vs.md)                                                       | Restar                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [texldl-vs](texldl---vs.md)                                                 | Carga de textura con nivel de detalle ajustable por el usuario                                                                                                                      | Vea la nota 1        |       |            | x       |              | x   |
| [virtual](vs---vs.md)                                                              | Versión                                                                                                                                                                | 0                 | x     |            |         |              |     |



 

Notas:

-   Si la textura es un mapa de cubo, ranuras = 5; en caso contrario, ranuras = 2

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




