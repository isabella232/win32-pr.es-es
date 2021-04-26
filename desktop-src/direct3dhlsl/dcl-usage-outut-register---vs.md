---
title: dcl_usage salida (sm1, sm2, sm3 - vs asm)
description: Los distintos tipos de registros de salida se han contraído en doce registros de salida (dos para color, ocho para textura, uno para posición y otro para tamaño de punto y extremo).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 314c9c9a9a9e62915e9224b3cf165bc54d09a516
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999172"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>Salida de uso de dcl \_ (sm1, sm2, sm3 - vs asm)

Los distintos tipos de registros de salida se han contraído en doce registros de salida (dos para color, ocho para textura, uno para posición y otro para tamaño de punto y extremo). Se pueden usar para cualquier cosa que el usuario quiera interpolar para el sombreador de píxeles: coordenadas de textura, colores, color, color, y así sucesivamente.

Los registros de salida requieren declaraciones que incluyen semántica. Por ejemplo, los registros antiguos de posición y tamaño de punto se reemplazan declarando un registro de salida con una posición o semántica de tamaño de punto.

De los doce registros de salida, los diez (no necesariamente de o0 a o9) tienen cuatro componentes (xyzw), otro debe declararse como posición (y también debe incluir los cuatro componentes) y, opcionalmente, uno más puede ser un tamaño de punto escalar.

## <a name="syntax"></a>Sintaxis

La sintaxis para declarar registros de salida es similar a las declaraciones del registro de entrada:



|                                  |
|----------------------------------|
| dcl \_ semantics o \[ .write \_ mask\] |



 

Donde:

-   La semántica \_ dcl puede usar el mismo conjunto de semántica que para la declaración de entrada. Los nombres semánticos proceden de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (y se emparejan con un índice, como position3). Siempre debe haber un registro de salida con la semántica positiont0 cuando no se usa para procesar vértices. La semántica positiont0 y la semántica pointsize0 son las únicas que tienen significado más allá de simplemente permitir la vinculación de sombreadores de vértice a píxel. En el caso de los sombreadores con control de flujo, se supone que se declara la salida del peor caso. No hay valores predeterminados si un sombreador no genera realmente lo que declara que debe (debido al control de flujo).
-   o es un registro de salida. Vea [Registros \_ de salida.](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)
-   write mask indica el mismo registro de salida que se puede declarar varias veces (por lo que se puede aplicar una semántica diferente a componentes individuales), cada vez con una \_ máscara de escritura única. Sin embargo, la misma semántica no se puede usar varias veces en una declaración. Esto significa que los vectores deben ser cuatro componentes o menos y no pueden pasar por los límites de registro de cuatro componentes (registros individuales). Cuando se usa la semántica de tamaño de punto, debe tener una máscara de escritura completa porque se considera escalar. Cuando se usa la semántica de posición, debe tener una máscara de escritura completa porque se deben escribir los cuatro componentes.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 3 \_ 0 | 3 \_ sw |
|------------------------|------|-------|
| dcl \_ usage             | x    | x     |



 

Todas [las instrucciones de uso \_ de dcl](dcl-usage-input-register---vs.md) deben aparecer antes de la primera instrucción ejecutable.

## <a name="declaration-examples"></a>Ejemplos de declaración


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

 

 
