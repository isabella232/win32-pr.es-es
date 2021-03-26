---
title: Diferencias entre el sombreador de píxeles
description: Diferencias entre el sombreador de píxeles
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420901"
---
# <a name="pixel-shader-differences"></a>Diferencias entre el sombreador de píxeles

## <a name="instruction-slots"></a>Ranuras de instrucciones

Cada versión admite un número diferente de ranuras de instrucciones máximas.



| Versión  | Número máximo de ranuras de instrucciones                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| PS \_ 1 \_ 1 | 4 textura + 8 aritméticos                                                                                              |
| PS \_ 1 \_ 2 | 4 textura + 8 aritméticos                                                                                              |
| PS \_ 1 \_ 3 | 4 textura + 8 aritméticos                                                                                              |
| PS \_ 1 \_ 4 | 6 textura + 8 aritmético por fase                                                                                    |
| PS \_ 2 \_ 0 | 32 textura + 64 aritmética                                                                                            |
| PS \_ 2 \_ x | 96 como mínimo y hasta el número de ranuras de D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots. Vea D3DPSHADERCAPS2 \_ 0. |
| PS \_ 3 \_ 0 | 512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxPixelShader30InstructionSlots. Vea D3DPSHADERCAPS2 \_ 0.      |



 

Para obtener información sobre las limitaciones de los sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Límites de anidamiento de control de flujo

-   Vea [limitaciones del control de flujo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).

## <a name="ps_1_x-features"></a>Características de PS \_ 1 \_ x

Nuevas instrucciones:

Consulte las instrucciones PS 1, PS 1 [ \_ \_ \_ \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).

Nuevos registros:

Vea [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="ps_2_0-features"></a>Características de PS \_ 2 \_ 0

Características nuevas:

-   Tres nuevos swizzles-. yzxw,. zxyw,. wzyx
-   El número de [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) aumentó a 12
-   El número de registros de [registro Float constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) aumentó a 32
-   El número de [registros de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t \# ) aumentó a 8

Nuevas instrucciones:

-   Instrucciones de instalación- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)
-   Instrucciones aritméticas- [ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [log-PS](log---ps.md), [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-](m3x4---ps.md)PS [, m4x3-PS,](m4x3---ps.md) [M4x4-PS](m4x4---ps.md), [Max-PS](max---ps.md), [min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [Pow-PS](pow---ps.md), [RCP-PS](rcp---ps.md), [RSQ-PS](rsq---ps.md), [sincos (-PS](sincos---ps.md)
-   Instrucciones de textura: [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md) (sintaxis diferente), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)

Nuevos registros:

-   [Muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# )

## <a name="ps_2_x-features"></a>Características de PS \_ 2 \_ x

Nuevas características (consulte [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):

-   Control de flujo dinámico
-   Control de flujo estático
-   Anidar instrucciones de control de flujo dinámico y estático
-   Número de [registros temporales](dx9-graphics-reference-asm-ps-registers-temporary.md) \# incrementados (r)
-   Swizzle de origen arbitrario
-   Instrucciones de degradado
-   Predicación
-   Límite de lectura de textura dependiente
-   No hay límite de instrucciones de textura

Nuevas instrucciones:

-   Instrucciones de control de flujo estático: [si es bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [REP-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [Label-PS](label---ps.md), [RET-PS](ret---ps.md)
-   Instrucciones de control de flujo dinámico- [break-PS](break---ps.md), [break \_ COMP-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz Pred-PS](callnz-pred---ps.md), [If \_ COMP-PS](if-comp---ps.md), si se PREA [-PS](if-pred---ps.md), [SETP \_ COMP-PS](setp-comp---ps.md)
-   Instrucciones aritméticas- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)
-   Instrucción de textura: [texldd-PS](texldd---ps.md)

Nuevos registros:

-   [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)

## <a name="ps_3_0-features"></a>Características de PS \_ 3 \_ 0

Características nuevas:

-   10 [registros de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidados (v \# )
-   Registro del [color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) indexable (v \# ) con el [contador de bucle Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al)
-   Número de [registros temporales](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) incrementados en 32
-   Número de [registros Float constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) aumentado a 224

Nuevas instrucciones:

-   Instrucción de configuración [: \_ semántica de DCL (SM3-PS ASM)](dcl-usage---ps.md)
-   Instrucciones de flujo estático: [Loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)
-   Instrucción aritmética- [sincos (-PS](sincos---ps.md) (nueva sintaxis)
-   Instrucción de textura: [texldl-PS](texldl---ps.md)

Nuevos registros:

-   [Registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )
-   [Registro de posición](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)
-   [Registro facial](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 