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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077883"
---
# <a name="vertex-shader-differences"></a>Diferencias del sombreador de vértices

## <a name="instruction-slots"></a>Ranuras de instrucciones

Cada versión admite un número distinto de ranuras de instrucciones máximas.



| Versión  | Número máximo de ranuras de instrucciones                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | 512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxVertexShader30InstructionSlots. Vea [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Para obtener información sobre las limitaciones de los sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Límites de anidamiento de control de flujo

-   Consulte [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).

## <a name="vs_1_1-features"></a>vs \_ 1 \_ 1 características

Nuevas instrucciones:

Consulte las [instrucciones-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Nuevos registros:

Consulte [registros-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>vs \_ 2 \_ 0 características

Características nuevas:

-   Control de flujo estático
-   Los cuatro componentes del [registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md) (a0) están disponibles.

Nuevas instrucciones:

-   Instrucciones de instalación- [defb-vs](defb---vs.md), [defi-vs](defi---vs.md)
-   Instrucciones aritméticas- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [mova-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [Pow-vs](pow---vs.md), [SGN-vs](sgn---vs.md), [sincos (-vs](sincos---vs.md)
-   Instrucciones de control de flujo estático: [Call-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [endif-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [If bool-vs](if-bool---vs.md), [etiqueta-vs](label---vs.md), [Loop-vs](loop---vs.md), [REP-vs](rep---vs.md), [RET-vs](ret---vs.md)

Nuevos registros:

-   [Registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Registro de entero constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al)

## <a name="vs_2_x-features"></a>Características de vs \_ 2 \_ x

Nuevas características (D3DCAPS9. VS20Caps):

-   Control de flujo dinámico
-   Anidar instrucciones de control de flujo dinámico y estático
-   Número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md) \# incrementados (r)
-   Predicación

Nuevas instrucciones:

-   Instrucciones de control de flujo dinámico: [break-vs](break---vs.md), [break \_ COMP-vs](break-comp---vs.md), [breakp-vs](breakp---vs.md), [callnz Pred-vs](callnz-pred---vs.md), [If \_ COMP-vs](if-comp---vs.md), [si Pred-vs](if-pred---vs.md), [SETP \_ COMP-vs](setp-comp---vs.md)

Nuevos registros:

-   [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)

## <a name="vs_3_0-features"></a>vs \_ 3 \_ 0 características

Nuevas características:

-   Búsqueda de texturas
-   Registros de [salida](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indexables (o \# )
-   Número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) incrementados en 32

Nuevas instrucciones:

-   Instrucción de instalación- [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)
-   Instrucción de textura- [texldl-vs](texldl---vs.md)

Nuevos registros:

-   [Muestra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 