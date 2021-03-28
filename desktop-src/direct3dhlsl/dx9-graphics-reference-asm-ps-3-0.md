---
title: ps_3_0
description: Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5aca251b1e8a462b4f2204241680922d76c45ba0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359122"
---
# <a name="ps_3_0"></a>PS \_ 3 \_ 0

Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [las \_ instrucciones de PS 3 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) contienen una lista de las instrucciones disponibles.
-   [en \_ registros de PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) se enumeran los distintos tipos de registros utilizados por el sombreador de píxeles Alu.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se utilizan para modificar la forma en que funciona una instrucción.
-   La [máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina los componentes del registro de destino que se van a escribir.
-   Los [modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.
-   [El registro de origen permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.

## <a name="new-features"></a>Nuevas características

Agregue un registro facial. Agregue un registro de posición. Los registros de color (v \# ) son ahora de punto flotante y los registros de coordenadas de textura (t \# ) se han consolidado. Las declaraciones de entrada toman los nombres de uso y se permiten varios usos para los componentes de un registro determinado.

## <a name="dynamic-flow-control"></a>Control de flujo dinámico

El dispositivo admite el control de flujo dinámico ([si es bool-PS](if-bool---ps.md), [break-PS](break---ps.md)y [break \_ COMP-PS](break-comp---ps.md)). La profundidad del anidamiento oscila entre 0 y 24.

## <a name="number-of-temporary-registers"></a>Número de registros temporales

El número de registros temporales admitidos es 32.

## <a name="static-flow-control-nesting-depth"></a>Profundidad de anidamiento de control de flujo estático

La llamada a callnz [llamada](call---ps.md)a / [](callnz-bool---ps.md)  / [ \_ Pred](callnz-pred---ps.md) puede estar anidada en una profundidad máxima de 4. Independientemente, [Loop-PS](loop---ps.md) / [REP-PS](rep---ps.md) las instrucciones se pueden anidar en una profundidad máxima de 4.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Se admite swizzle arbitrario. Consulte [source Register permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instrucciones de degradado

Se admiten las instrucciones de degradado. Consulte [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)y [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Predicación

Se admite la instrucción predication. Vea [registro de predicados](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Límite de lectura dependiente

No hay ningún límite de lectura dependiente.

## <a name="texture-instruction-limit"></a>Límite de instrucciones de textura

No hay ningún límite en las instrucciones de textura.

## <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de píxeles se permite desde 512 hasta el número de ranuras de MaxPixelShader30InstructionSlots (no superior a 32768). El número de instrucciones que se ejecutan puede ser mucho mayor debido a la compatibilidad con bucles. MaxPShaderInstructionsExecuted debe ser al menos 2 ^ 16.

## <a name="sampler-count"></a>Recuento de muestras

El número de muestras de textura disponibles es 16.

## <a name="device-caps"></a>Cap del dispositivo

Si \_ \_ se admite PS 3 0, se admiten los siguientes límites en el hardware (como mínimo):



| Punto                                                                                                          | Value                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 4K cada uno                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 K                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropy                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Se establecen los límites primitivos siguientes:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, D3DPMISCCAPS \_ CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ FOGINFVF, D3DPMISCCAPS \_ MASKZ                                                                                               |
| Se establecen los límites de trama siguientes:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ ANISOTROPÍA, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ SCISSORTEST in D3DCAPS9                                                                                                                                                                  |
| Compatibilidad total con la diferencia de profundidad, incluidos:                                                                       | D3DPRASTERCAPS \_ SLOPESCALEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Conjunto completo de comparaciones para la prueba de profundidad y alfa, incluidos:                                                  | Todos los D3DPCMPCAPS de D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Modos de fusión de origen                                                                                        | Todos los modos de fusión se admiten como un origen (excepto D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA y D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Se admiten los siguientes límites de textura:                                                                    | D3DPTEXTURECAPS \_ mapa, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ Perspective, D3DPTEXTURECAPS \_ previsto, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| Se admiten los siguientes elementos en los extremos de filtro de textura, los extremos de filtro de textura de volumen y los límites de filtro de textura de cubo: | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS MINFANISOTROPIC \_ (esto no es necesario para VolumeTextureFilterCaps y CUBETEXTUREFILTERCAPS), D3DPTFILTERCAPS \_ MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, D3DPTFILTERCAPS \_ MAGFPOINT, D3DPTFILTERCAPS \_ MAGFLINEAR             |
| Los siguientes modos de dirección de textura se admiten en fases de vértices y píxeles:                                | D3DPTADDRESSCAPS \_ Wrap, D3DPTADDRESSCAPS \_ Mirror, D3DPTADDRESSCAPS \_ Clamp, D3DPTADDRESSCAPS \_ Border, D3DPTADDRESSCAPS \_ INDEPENDENTUV, D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Se admiten todos los extremos del sombreador de píxeles.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Se admiten las características siguientes: predication, swizzles arbitrario e instrucciones de degradado. No hay ningún límite de lectura dependiente y ningún límite en la mezcla de instrucciones matemáticas y de textura. |
| Se admiten todas las operaciones de estarcido. Esto incluye dos galerías de símbolos a la derecha.                                   | Consulte [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Tamaño de punto de soporte de dispositivo por vértice                                                                         | D3DFVFCAPS \_ PSIZE D3DCAPS9                                                                                                                                                                                                                                                                         |
| No potencia de 2 compatibilidad con texturas.                                                                              | Compatibilidad completa o compatibilidad condicional sin Pow-2; el dispositivo no debe tener la limitación de textura cuadrada solo en D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Si el dispositivo admite varios Rendertargets, se admiten los siguientes límites:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Si \_ \_ se admite vs 3 0                                                                                     | MaxUserClipPlanes en D3DCAPS9 es 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 