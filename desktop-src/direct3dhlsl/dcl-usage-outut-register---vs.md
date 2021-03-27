---
title: dcl_usage salida (SM1, SM2, SM3-vs ASM)
description: Los distintos tipos de registros de salida se han contraído en doce registros de salida (dos para el color, ocho para la textura, uno para la posición y otro para la niebla y el tamaño de los puntos).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997129"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>\_salida de uso de DCL (SM1, SM2, SM3-vs ASM)

Los distintos tipos de registros de salida se han contraído en doce registros de salida (dos para el color, ocho para la textura, uno para la posición y otro para la niebla y el tamaño de los puntos). Se pueden usar para cualquier elemento que el usuario quiera interpolar para el sombreador de píxeles: coordenadas de textura, colores, niebla, etc.

Los registros de salida requieren declaraciones que incluyen la semántica. Por ejemplo, los registros de posición y de tamaño de punto antiguos se reemplazan declarando un registro de salida con una posición o semántica de tamaño de punto.

De los doce registros de salida, los diez (no necesariamente O0 a O9) tienen cuatro componentes (xyzw), otro se debe declarar como Position (y también debe incluir los cuatro componentes) y, opcionalmente, uno más puede ser un tamaño de punto escalar.

## <a name="syntax"></a>Sintaxis

La sintaxis para declarar registros de salida es similar a las declaraciones del registro de entrada:



|                                  |
|----------------------------------|
| semántica de DCL \_ o \[ . máscara de escritura \_\] |



 

Donde:

-   la \_ semántica de DCL puede usar el mismo conjunto de semántica que para la declaración de entrada. Los nombres semánticos proceden de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (y se emparejan con un índice, como position3). Siempre debe haber un registro de salida con la semántica positiont0 cuando no se usa para el procesamiento de vértices. La semántica positiont0 y la semántica pointsize0 son las únicas que tienen un significado más allá, simplemente permiten la vinculación de los sombreadores de vértices a píxeles. En el caso de los sombreadores con control de flujo, se supone que se declara el resultado peor de los casos. No hay valores predeterminados si un sombreador no genera realmente lo que declara debe (debido al control de flujo).
-   o es un registro de salida. Consulte [ \_ registros de salida](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).
-   escribir \_ máscara indica el mismo registro de salida que se puede declarar varias veces (de modo que se pueden aplicar diferentes semánticas a componentes individuales), cada vez con una máscara de escritura única. Sin embargo, no se puede usar la misma semántica varias veces en una declaración. Esto significa que los vectores deben tener cuatro componentes o menos y no pueden pasar por los límites de registro de cuatro componentes (registros individuales). Cuando se usa la semántica de tamaño de punto, debe tener una máscara de escritura completa porque se considera un escalar. Cuando se usa la semántica de posición, debe tener una máscara de escritura completa porque se deben escribir los cuatro componentes.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 3 \_ 0 | 3 \_ SW |
|------------------------|------|-------|
| uso de DCL \_             | x    | x     |



 

Todas las instrucciones de [ \_ uso de DCL](dcl-usage-input-register---vs.md) deben aparecer antes de la primera instrucción ejecutable.

## <a name="declaration-examples"></a>Ejemplos de declaraciones


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 