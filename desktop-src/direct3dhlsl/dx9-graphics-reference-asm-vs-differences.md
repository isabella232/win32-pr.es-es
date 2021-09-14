---
title: Diferencias del sombreador de vértices
description: Diferencias del sombreador de vértices
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966556"
---
# <a name="vertex-shader-differences"></a>Diferencias del sombreador de vértices

## <a name="instruction-slots"></a>Ranuras de instrucciones

Cada versión admite un número diferente de ranuras de instrucción máximas.



| Versión  | Número máximo de ranuras de instrucción                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | 512 como mínimo y hasta el número de ranuras en D3DCAPS9. MaxVertexShader30InstructionSlots. Vea [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) |



 

Para obtener información sobre las limitaciones de los sombreadores de software, vea [Sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Flow Controlar límites de anidamiento

-   Vea [Flow control de anidamiento de controles](dx9-graphics-reference-asm-vs-instructions-flow-control.md).

## <a name="vs_1_1-features"></a>Frente \_ a \_ 1 1 Características

Nuevas instrucciones:

Vea [Instructions - vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Nuevos registros:

Vea [Registros: frente \_ a \_ 1 1.](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)

## <a name="vs_2_0-features"></a>Vs \_ 2 \_ 0 Features (Características de vs 2 0)

Características nuevas:

-   Control de flujo estático
-   Los cuatro componentes del registro [de direcciones](dx9-graphics-reference-asm-vs-registers-address.md) (a0) están disponibles.

Nuevas instrucciones:

-   Instrucciones de instalación : [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)
-   Instrucciones aritméticas [- abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)
-   Instrucciones de control de flujo estático - llamada [-](call---vs.md)frente a , [callnz bool -](callnz-bool---vs.md)vs , else [-](else---vs.md)vs , [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), if [bool - vs](if-bool---vs.md), label - [vs](label---vs.md), loop [- vs](loop---vs.md), rep - [vs](rep---vs.md), ret [- vs](ret---vs.md)

Nuevos registros:

-   [Registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Registro de enteros constantes](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Registro de contadores de](dx9-graphics-reference-asm-vs-registers-loop-counter.md) bucles (aL)

## <a name="vs_2_x-features"></a>vs \_ 2 \_ x Features

Nuevas características (D3DCAPS9. VS20Caps:

-   Control de flujo dinámico
-   Anidamiento para instrucciones de control de flujo dinámico y estático
-   Número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) aumentado
-   Predicación

Nuevas instrucciones:

-   Instrucciones de control de flujo dinámico : [break -](break---vs.md)vs , break comp [- \_ vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), if comp - [ \_ vs](if-comp---vs.md), si [pred - vs](if-pred---vs.md), [setp comp - \_ vs](setp-comp---vs.md)

Nuevos registros:

-   [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)

## <a name="vs_3_0-features"></a>Vs \_ 3 \_ 0 Features (Frente a 3 0 características)

Nuevas características:

-   Búsqueda de textura
-   Registros de [salida indexables](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )
-   Número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)(r) aumentado \# a 32

Nuevas instrucciones:

-   Instrucción de instalación: [dcl \_ samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)
-   Instrucción de textura [- texldl - vs](texldl---vs.md)

Nuevos registros:

-   [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 