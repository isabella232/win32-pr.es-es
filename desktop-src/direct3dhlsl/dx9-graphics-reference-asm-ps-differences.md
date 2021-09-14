---
title: Diferencias del sombreador de píxeles
description: Diferencias del sombreador de píxeles
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264084"
---
# <a name="pixel-shader-differences"></a>Diferencias del sombreador de píxeles

## <a name="instruction-slots"></a>Ranuras de instrucciones

Cada versión admite un número diferente de espacios de instrucciones máximos.



| Versión  | Número máximo de ranuras de instrucción                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| ps \_ 1 \_ 1 | 4 texturas + 8 aritméticas                                                                                              |
| ps \_ 1 \_ 2 | 4 texturas + 8 aritméticas                                                                                              |
| ps \_ 1 \_ 3 | 4 texturas + 8 aritméticas                                                                                              |
| ps \_ 1 \_ 4 | 6 texturas + 8 aritméticas por fase                                                                                    |
| ps \_ 2 \_ 0 | 32 textura + 64 aritméticas                                                                                            |
| ps \_ 2 \_ x | 96 como mínimo y hasta el número de ranuras en D3DCAPS9. D3DPSHADERCAPS2 \_ 0.NumInstructionSlots. Consulte D3DPSHADERCAPS2 \_ 0. |
| ps \_ 3 \_ 0 | 512 como mínimo y hasta el número de ranuras en D3DCAPS9. MaxPixelShader30InstructionSlots. Consulte D3DPSHADERCAPS2 \_ 0.      |



 

Para obtener información sobre las limitaciones de los sombreadores de software, vea [Sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Flow Controlar límites de anidamiento

-   Vea [Flow control de datos](dx9-graphics-reference-asm-ps-instructions-flow-control.md).

## <a name="ps_1_x-features"></a>ps \_ 1 \_ x Características

Nuevas instrucciones:

Consulte [ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).

Nuevos registros:

Vea [ps \_ 1 \_ 1 ps \_ \_ \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="ps_2_0-features"></a>ps \_ 2 \_ 0 Características

Características nuevas:

-   Tres nuevos swzyles: .yzxw, .zxyw, .wzyx
-   Número de [registros temporales](dx9-graphics-reference-asm-ps-registers-temporary.md) (r) aumentado \# a 12
-   Número de [registros de registro flotante](dx9-graphics-reference-asm-ps-registers-constant-float.md) constante (c) aumentado a \# 32
-   Número de [registros de coordenadas de](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)textura (t) aumentado a \# 8

Nuevas instrucciones:

-   Instrucciones de [configuración: dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)
-   Instrucciones aritméticas - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), exp - [ps](exp---ps.md), [frc - ps](frc---ps.md), log - [ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), max - [ps](max---ps.md), min [- ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)
-   Instrucciones de [textura- texld - ps \_ 2 \_ 0 y versiones](texld---ps-2-0.md) adicionales (sintaxis diferente), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)

Nuevos registros:

-   [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# )

## <a name="ps_2_x-features"></a>ps \_ 2 \_ x Características

Nuevas características (consulte [**D3DPSHADERCAPS2 \_ 0).**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)

-   Control de flujo dinámico
-   Control de flujo estático
-   Anidamiento para instrucciones de control de flujo dinámico y estático
-   Número de [registros temporales](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) aumentado
-   Swzzle de origen arbitrario
-   Instrucciones de degradado
-   Predicación
-   Sin límite de lectura de textura dependiente
-   Sin límite de instrucciones de textura

Nuevas instrucciones:

-   Instrucciones de control de flujo estático: [si bool - ps](if-bool---ps.md), llame a - [ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), else - [ps](else---ps.md), [endif - ps](endif---ps.md), rep - [ps](rep---ps.md), [endrep - ps](endrep---ps.md), label - [ps](label---ps.md), ret [- ps](ret---ps.md)
-   Instrucciones de control de flujo dinámico : [break - ps](break---ps.md), break comp - [ \_ ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), if comp - [ \_ ps](if-comp---ps.md), [si pred - ps](if-pred---ps.md), [setp comp - \_ ps](setp-comp---ps.md)
-   Instrucciones [aritméticas: dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)
-   Instrucción de [textura- texldd - ps](texldd---ps.md)

Nuevos registros:

-   [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)

## <a name="ps_3_0-features"></a>ps \_ 3 \_ 0 Características

Características nuevas:

-   10 registros [de entrada consolidados](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)(v \# )
-   Registro de [color de entrada indexable](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) con el registro de contador de [bucles](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)
-   Número de [registros temporales](dx9-graphics-reference-asm-ps-registers-temporary.md)(r) aumentado \# a 32
-   Número de [registros flotantes constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c) \# aumentado a 224

Nuevas instrucciones:

-   Instrucción de instalación: [semántica de dcl \_ (sm3 - ps asm)](dcl-usage---ps.md)
-   Instrucciones de flujo estático [: bucle - ps](loop---ps.md), [endloop - ps](endloop---ps.md)
-   Instrucción aritmética: [sincos - ps](sincos---ps.md) (nueva sintaxis)
-   Instrucción de [textura- texldl - ps](texldl---ps.md)

Nuevos registros:

-   [Registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )
-   [Registro de posición](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)
-   [Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 