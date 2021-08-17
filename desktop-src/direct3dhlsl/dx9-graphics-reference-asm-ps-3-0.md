---
title: ps_3_0
description: Obtenga información ps_3_0, un sombreador de píxeles programable, que se forma de un conjunto de instrucciones que funcionan con datos de píxeles.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79145936709e43fab9b87602233225567a0067528a31036aacc11c5b425c0dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512899"
---
# <a name="ps_3_0"></a>ps \_ 3 \_ 0

Un sombreador de píxeles programable se forma de un conjunto de instrucciones que funcionan con datos de píxeles. Registra la transferencia de datos dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [ps \_ 3 \_ 0 Instructions contiene](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) una lista de las instrucciones disponibles.
-   [ps \_ 3 \_ 0 Registros enumera](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) los diferentes tipos de registros que usa el sombreador de píxeles ALU.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se usan para modificar el funcionamiento de una instrucción.
-   [Destination Register Write Mask determina](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) qué componentes del registro de destino se escriben.
-   [Los modificadores de registro de origen del sombreador de](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) píxeles modifican los datos de registro de origen antes de que se ejecute la instrucción.
-   [Source Register Swling proporciona](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.

## <a name="new-features"></a>Nuevas características

Agregue un registro de caras. Agregue un registro de posición. Los registros de color (v ) ahora son de punto flotante completo y los registros de coordenadas de textura \# \# (t) se han consolidado. Las declaraciones de entrada toman los nombres de uso y se permiten varios usos para los componentes de un registro determinado.

## <a name="dynamic-flow-control"></a>Control de Flow dinámico

El dispositivo admite el control de flujo dinámico ([si bool - ps](if-bool---ps.md), break - [ps](break---ps.md)y break comp [- \_ ps](break-comp---ps.md)). La profundidad del anidamiento va de 0 a 24.

## <a name="number-of-temporary-registers"></a>Número de registros temporales

El número de registros temporales admitidos es 32.

## <a name="static-flow-control-nesting-depth"></a>Profundidad Flow de anidamiento de controles estáticos

La [llamada a ps](call---ps.md) / [callnz](callnz-bool---ps.md)  / [ \_ pred](callnz-pred---ps.md) se puede anidar en una profundidad máxima de 4. De forma independiente, [las instrucciones de bucle - ps](loop---ps.md)rep - / [ps](rep---ps.md) se pueden anidar a una profundidad máxima de 4.

## <a name="arbitrary-swizzle"></a>Swzzle arbitrario

Se admite swzzle arbitrario. Consulte [Source Register Swlingling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instrucciones de degradado

Se admiten instrucciones de degradado. Vea [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)y [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Predicación

Se admite el predicado de instrucciones. Vea [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Límite de lectura dependiente

No hay límites de lectura dependientes.

## <a name="texture-instruction-limit"></a>Límite de instrucciones de textura

No hay ningún límite en las instrucciones de textura.

## <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de píxeles se permite desde 512 hasta el número de ranuras en MaxPixelShader30InstructionSlots (no más de 32768). El número de instrucciones que se ejecutan puede ser mucho mayor debido a la compatibilidad con bucles. MaxPShaderInstructionsExecuted debe ser al menos 2^16.

## <a name="sampler-count"></a>Sampler Count

El número de muestreadores de textura disponibles es 16.

## <a name="device-caps"></a>Límites de dispositivo

Si se admite ps 3 0, se admiten los siguientes límites en \_ hardware \_ (como mínimo):



| Tapa                                                                                                          | Valor                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 4K cada una                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 K                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropy                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Se establecen los siguientes límites primitivos:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, D3DPMISCCAPS \_ CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ MASKINFVF, D3DPMISCCAPS \_ MASKZ                                                                                               |
| Se establecen los siguientes límites de trama:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ ANISOTROPY, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ LAPRUEBATEST EN D3DCAPS9                                                                                                                                                                  |
| Compatibilidad total con el sesgo de profundidad, incluidos:                                                                       | D3DPRASTERCAPS \_ SESGOCALEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Conjunto completo de comparaciones para pruebas alfa y de profundidad, entre las que se incluyen:                                                  | Todos los D3DPCMPCAPS en D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Modos de combinación de origen                                                                                        | Todos los modos de combinación se admiten como origen (excepto D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA y D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Se admiten los siguientes límites de textura:                                                                    | D3DPTEXTURECAPS \_ CUBEMAP, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ PERSPECTIVE, D3DPTEXTURECAPS \_ PROJECTED, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| Se admite lo siguiente en los límites de filtro de textura, los límites de filtro de textura de volumen y los límites de filtro de textura de cubo: | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS MINFANISOTROPIC (esto no es necesario para \_ VolumeTextureFilterCaps y CubeTextureFilterCaps), \_ D3DPTFILTERCAPS MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, D3DPTFILTERCAPS \_ MAGFPOINT, D3DPTFILTERCAPS \_ MAGFLINEAR             |
| Los siguientes modos de dirección de textura se admiten en las fases de vértice y píxel:                                | D3DPTADDRESSCAPS \_ WRAP, D3DPTADDRESSCAPS \_ MIRROR, D3DPTADDRESSCAPS \_ CLAMP, D3DPTADDRESSCAPS \_ BORDER, D3DPTADDRESSCAPS \_ INDEPENDENTUV, D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Se admiten todos los límites del sombreador de píxeles.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Se admiten las siguientes características: predicación, remolinos arbitrarios e instrucciones de degradado. No hay ningún límite de lectura dependiente ni límite en la combinación de instrucciones matemáticas y de textura. |
| Se admiten todas las operaciones de galería de símbolos. Esto incluye la galería de símbolos de dos lados.                                   | Consulte [ **D3DSTENCILOP.**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Tamaño de punto de soporte de dispositivo por vértice                                                                         | D3DFVFCAPS \_ PSIZE en D3DCAPS9                                                                                                                                                                                                                                                                         |
| Compatibilidad sin potencia de 2 texturas.                                                                              | Compatibilidad completa o compatibilidad condicional no pow-2; El dispositivo no debe tener la limitación de textura cuadrada, como en D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Si el dispositivo admite varios destinos de representación, se admiten los siguientes límites:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Si se admite vs \_ \_ 3 0                                                                                     | MaxUserClipPlanes en D3DCAPS9 es 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 