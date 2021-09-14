---
title: vs_2_x
description: Obtenga información vs_2_x, un sombreador de vértices programable, que se forma de un conjunto de instrucciones que funcionan con datos de vértices.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974689"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Un sombreador de vértices programable se forma de un conjunto de instrucciones que funcionan con datos de vértices. Registra la transferencia de datos dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

La versión del sombreador de \_ vértices frente a 2 \_ x amplía el conjunto de características admitido por frente a \_ 2 \_ 0. Cada característica adicional se representa mediante un límite correspondiente en la estructura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dentro [de D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps). Para usar cualquiera de las características mejoradas representadas por estos límites, la versión del sombreador de vértices debe especificarse como \_ frente a 2 \_ x.

-   [Instrucciones: frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene una lista de las instrucciones disponibles.
-   [Registros: frente \_ a 2 \_ x,](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) se enumeran los distintos tipos de registros usados por el sombreador de vértices ALU.
-   [Los modificadores de registro del sombreador](dx9-graphics-reference-asm-vs-registers-modifiers.md) de vértices se usan para modificar el funcionamiento de una instrucción.
-   [Los modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.
-   [Source Register Swling proporciona](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.
-   [El enmascaramiento de registros de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina qué componentes del registro de destino se escriben.

## <a name="new-features"></a>Nuevas características

Las nuevas características son las siguientes:

### <a name="dynamic-flow-control"></a>Control de Flow dinámico

Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, se admiten las siguientes instrucciones de control de flujo dinámico:

-   [if \_ comp - vs](if-comp---vs.md)
-   [break- vs](break---vs.md)
-   [break \_ comp: vs](break-comp---vs.md)

Si [también se establece D3DVS20CAPS,](/windows/desktop/direct3d9/d3dvs20caps) se admiten las siguientes instrucciones de control de flujo adicionales:

-   [setp \_ comp - vs](setp-comp---vs.md)
-   [if pred - vs](if-pred---vs.md)
-   [callnz pred - vs](callnz-pred---vs.md)
-   [breakp: vs](breakp---vs.md)

El intervalo de valores para la profundidad de control de flujo dinámico es de 0 a 24 y es igual a la profundidad de anidamiento de las instrucciones de control de flujo dinámico (consulte [límites](dx9-graphics-reference-asm-vs-instructions-flow-control.md) de anidamiento de controles de Flow para obtener más información). Si este límite es cero, el dispositivo no admite instrucciones de control de flujo dinámico.

### <a name="number-of-temporary-registers"></a>Número de registros temporales

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa el número [de](dx9-graphics-reference-asm-vs-registers-temporary.md)registros temporales admitidos por el dispositivo. El intervalo de valores para este límite es de 12 a 32.

### <a name="static-flow-control-nesting-depth"></a>Profundidad Flow de anidamiento de controles estáticos

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa la profundidad de anidamiento de dos tipos de instrucciones de control de flujo estático: [loop - vs](loop---vs.md)rep - vs y call - vs callnz bool - vs if bool - vs . loop - vs/rep - vs instructions se pueden anidar hasta / [](rep---vs.md) [](call---vs.md) / [](callnz-bool---vs.md) / [](if-bool---vs.md)D3DVS20CAPS deep. De forma independiente, la llamada (vs/callnz bool) frente a las instrucciones se puede anidar hasta D3DVS20CAPS en profundidad. Si también se establece D3DVS20CAPS, [callnz pred - vs](callnz-pred---vs.md) se cuenta para la profundidad de anidamiento de la llamada - vs/callnz bool - vs/if bool - vs (vea [límites](dx9-graphics-reference-asm-vs-instructions-flow-control.md) de anidamiento de controles de Flow para obtener más información).

### <a name="predication"></a>Predicación

Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) está establecido, el dispositivo admite el [predicado setp comp - \_ vs](setp-comp---vs.md) y de instrucción. Si D3DVS20CAPS también es mayor que 0, se admiten las siguientes instrucciones de control de flujo dinámico adicionales:

-   [if pred - vs](if-pred---vs.md)
-   [callnz pred - vs](callnz-pred---vs.md)
-   [breakp: vs](breakp---vs.md)

### <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas. El número de instrucciones que se ejecutan puede ser mucho mayor (debido a la compatibilidad con bucles o representantes) y está limitado por [**D3DCAPS9,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)que debe ser al menos 0xFFFF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 