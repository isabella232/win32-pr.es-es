---
title: Instrucciones de ps_2_x
description: Esta sección contiene información de referencia para las instrucciones del sombreador de píxeles versión 2 \_ x.
ms.assetid: a9b5f9dd-1139-4f80-ada6-e2fc0fb7effe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 047067d26f9b85ef981a007059d9f2e87ae28ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984039"
---
# <a name="ps_2_x-instructions"></a>Instrucciones de PS \_ 2 \_ x

Esta sección contiene información de referencia para las instrucciones del sombreador de píxeles versión 2 \_ x.

Hay varios tipos de instrucciones de sombreador de píxeles, tal como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucciones: número de ranuras de instrucciones usadas por cada instrucción.
-   Configuración: un sombreador de píxeles debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Texture: estas instrucciones se usan para cargar y muestrear los datos de textura y para modificar las coordenadas de textura.
-   Control de flujo: estas instrucciones proporcionan control de flujo estático y dinámico a la ejecución de instrucciones.
-   Nuevas: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                             | Descripción                                                                                      | Ranuras de instrucciones | Configurar | Aritméticos | Textura | Control de flujo | Nuevo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-PS](abs---ps.md)                                         | Valor absoluto                                                                                   | 1                 |       | x          |         |              |     |
| [Agregar-PS](add---ps.md)                                         | Agregar dos vectores                                                                                  | 1                 |       | x          |         |              |     |
| [Break-PS](break---ps.md)                                     | Salir de un representante... bloque endrep                                                                | 1                 |       |            |         | x            | x   |
| [Break \_ COMP-PS](break-comp---ps.md)                          | Desglose condicional de un representante... bloque endrep, con una comparación                               | 3                 |       |            |         | x            | x   |
| [breakp-PS](break-p---ps.md)                                  | Salir de un representante... bloque endrep, basado en un predicado                                          | 3                 |       |            |         | x            | x   |
| [llamada a PS](call---ps.md)                                       | Llamar a una subrutina                                                                                | 2                 |       |            |         | x            | x   |
| [callnz bool-PS](callnz-bool---ps.md)                         | Llamar a una subrutina si un registro booleano no es cero                                              | 3                 |       |            |         | x            | x   |
| [callnz Pred-PS](callnz-pred---ps.md)                         | Llamar a una subrutina si un registro de predicado no es cero                                            | 3                 |       |            |         | x            | x   |
| [CMP-PS](cmp---ps.md)                                         | Comparar origen con 0                                                                              | 1                 |       | x          |         |              |     |
| [CRS-PS](crs---ps.md)                                         | Producto cruzado                                                                                    | 2                 |       | x          |         |              |     |
| [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Declarar la dimensión de textura para una muestra                                                      | 0                 | x     |            |         |              |     |
| [DCL: (SM2, SM3-PS ASM)](dcl---ps.md)                        | Declare la asociación entre los registros de salida del sombreador de vértices y los registros de entrada del sombreador de píxeles. | 0                 | x     |            |         |              |     |
| [DEF-PS](def---ps.md)                                         | Definir constantes                                                                                 | 0                 | x     |            |         |              |     |
| [defb-PS](defb---ps.md)                                       | Definir una constante booleana                                                                        | 0                 | x     |            |         |              | x   |
| [defi-PS](defi---ps.md)                                       | Definir una constante de tipo entero                                                                       | 0                 | x     |            |         |              | x   |
| [dp2add-PS](dp2add---ps.md)                                   | producto de punto 2D y agregar                                                                           | 2                 |       | x          |         |              |     |
| [DP3-PS](dp3---ps.md)                                         | producto de punto 3D                                                                                   | 1                 |       | x          |         |              |     |
| [DP4-PS](dp4---ps.md)                                         | 4D DOT producto                                                                                   | 1                 |       | x          |         |              |     |
| [DSX-PS](dsx---ps.md)                                         | Velocidad de cambio en la dirección x                                                                | 2                 |       | x          |         |              | x   |
| [DSY-PS](dsy---ps.md)                                         | Velocidad de cambio en la dirección y                                                                | 2                 |       | x          |         |              | x   |
| [Else-PS](else---ps.md)                                       | Comenzar un bloque else                                                                              | 1                 |       |            |         | x            | x   |
| [endif-PS](endif---ps.md)                                     | Finalizar un if... bloque else                                                                           | 1                 |       |            |         | x            | x   |
| [endrep-PS](endrep---ps.md)                                   | Final de un bloque de repetición                                                                            | 2                 |       |            |         | x            | x   |
| [EXP-PS](exp---ps.md)                                         | Precisión completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         |              |     |
| [FRC-PS](frc---ps.md)                                         | Componente fraccionario                                                                             | 1                 |       | x          |         |              |     |
| [Si es bool-PS](if-bool---ps.md)                                 | Iniciar un bloque if                                                                                | 3                 |       |            |         | x            | x   |
| [Si \_ COMP-PS](if-comp---ps.md)                                | Comenzar un bloque if con una comparación                                                              | 3                 |       |            |         | x            | x   |
| [Si Pred-PS](if-pred---ps.md)                                 | Comenzar un bloque if con predication                                                               | 3                 |       |            |         | x            | x   |
| [etiqueta-PS](label---ps.md)                                     | Etiqueta                                                                                            | 0                 |       |            |         | x            | x   |
| [registro: PS](log---ps.md)                                         | ₂ de registro de precisión completa (x)                                                                           | 1                 |       | x          |         |              |     |
| [LRP-PS](lrp---ps.md)                                         | Interpolación lineal                                                                               | 2                 |       | x          |         |              |     |
| [m3x2-PS](m3x2---ps.md)                                       | 3x2 multiplicar                                                                                     | 2                 |       | x          |         |              |     |
| [M3x3-PS](m3x3---ps.md)                                       | multiplicar 3x3                                                                                     | 3                 |       | x          |         |              |     |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 multiplicar                                                                                     | 4                 |       | x          |         |              |     |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 multiplicar                                                                                     | 3                 |       | x          |         |              |     |
| [M4x4-PS](m4x4---ps.md)                                       | multiplicar 4x4                                                                                     | 4                 |       | x          |         |              |     |
| [Mad-PS](mad---ps.md)                                         | Multiplicar y agregar                                                                                 | 1                 |       | x          |         |              |     |
| [Max-PS](max---ps.md)                                         | Máxima                                                                                          | 1                 |       | x          |         |              |     |
| [min-PS](min---ps.md)                                         | Mínima                                                                                          | 1                 |       | x          |         |              |     |
| [MOV-PS](mov---ps.md)                                         | Move                                                                                             | 1                 |       | x          |         |              |     |
| [mul-PS](mul---ps.md)                                         | Multiplicar                                                                                         | 1                 |       | x          |         |              |     |
| [NOP-PS](nop---ps.md)                                         | No hay ninguna operación                                                                                     | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normalizar                                                                                        | 3                 |       | x          |         |              |     |
| [Pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         |              |     |
| [PS](ps---ps.md)                                                | Versión                                                                                          | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Quede                                                                                       | 1                 |       | x          |         |              |     |
| [REP-PS](rep---ps.md)                                         | Repetir                                                                                           | 3                 |       |            |         | x            | x   |
| [RET-PS](ret---ps.md)                                         | Final de una subrutina                                                                              | 1                 |       |            |         | x            | x   |
| [RSQ-PS](rsq---ps.md)                                         | Raíz cuadrada recíproca                                                                           | 1                 |       | x          |         |              |     |
| [comp. SETP \_](setp-comp---ps.md)                                 | Establecimiento del registro de predicado                                                                       | 1                 |       |            |         | x            | x   |
| [sincos (-PS](sincos---ps.md)                                   | Seno y coseno                                                                                  | 8                 |       | x          |         |              |     |
| [Sub-PS](sub---ps.md)                                         | Restar                                                                                         | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Detener la representación de píxeles                                                                                | Vea la nota 1        |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 y arriba](texld---ps-2-0.md)                    | Muestra de una textura                                                                                 | Consulte la nota 2.        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Muestreo de textura con la diferencia de nivel de detalle del componente w                                      | Vea la nota 3        |       |            | x       |              |     |
| [texldd-PS](texldd---ps.md)                                   | Muestreo de textura con degradados proporcionados por el usuario                                                    | 3                 |       |            | x       |              | x   |
| [texldp-PS](texldp---ps.md)                                   | Muestreo de textura con división proyectada por componente w                                           | Vea la nota 4        |       |            | x       |              |     |



 

Notas:

1.  Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , ranuras = 2; en caso contrario, ranuras = 1.
2.  Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) y la textura es un mapa de cubo, ranuras = 4; en caso contrario, ranura = 1.
3.  Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , ranuras = 6; de lo contrario, ranuras = 1.
4.  Si no se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , ranuras = 1; de lo contrario:
    -   Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) y la textura es un mapa de cubo, Slots = 4.
    -   Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) y la textura no es un mapa de cubo, Slots = 3.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 