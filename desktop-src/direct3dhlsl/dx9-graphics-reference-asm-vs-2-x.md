---
title: vs_2_x
description: Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488039"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

La versión del sombreador de vértices frente \_ \_ a 2 x amplía el conjunto de características compatible con vs \_ 2 \_ 0. Cada característica adicional está representada por un límite correspondiente en la estructura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dentro de [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps). Para usar cualquiera de las características mejoradas representadas por estos Cap, la versión del sombreador de vértices debe especificarse como vs \_ 2 \_ x.

-   [Instrucciones: vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene una lista de las instrucciones disponibles.
-   [Registros: vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) enumera los distintos tipos de registros utilizados por el sombreador de vértices Alu.
-   Los [modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md) se utilizan para modificar la forma en que funciona una instrucción.
-   Los [modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.
-   [El registro de origen permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.
-   [El enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina los componentes del registro de destino que se van a escribir.

## <a name="new-features"></a>Nuevas características

Las nuevas características son las siguientes:

### <a name="dynamic-flow-control"></a>Control de flujo dinámico

Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, se admiten las siguientes instrucciones de control de flujo dinámico:

-   [If \_ COMP-vs](if-comp---vs.md)
-   [Inter-vs](break---vs.md)
-   [Break \_ COMP-vs](break-comp---vs.md)

Si también se establece [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , se admiten las siguientes instrucciones de control de flujo adicionales:

-   [\_COMP SETP-vs](setp-comp---vs.md)
-   [Si Pred-vs](if-pred---vs.md)
-   [callnz Pred-vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

El intervalo de valores para la profundidad de control de flujo dinámico es de 0 a 24 y es igual a la profundidad de anidamiento de las instrucciones de control de flujo dinámico (vea [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obtener más detalles). Si este extremo es cero, el dispositivo no admite las instrucciones de control de flujo dinámico.

### <a name="number-of-temporary-registers"></a>Número de registros temporales

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa el número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)admitidos por el dispositivo. El intervalo de valores para este Cap es de 12 a 32.

### <a name="static-flow-control-nesting-depth"></a>Profundidad de anidamiento de control de flujo estático

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa la profundidad de anidamiento de dos tipos de instrucciones de control de flujo estático: [Loop-vs](loop---vs.md) / [REP-vs](rep---vs.md) y [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [Si bool-vs](if-bool---vs.md). Loop-vs/REP-vs las instrucciones se pueden anidar hasta D3DVS20CAPS Deep. De forma independiente, Call-vs/callnz bool-las instrucciones de vs se pueden anidar hasta D3DVS20CAPS Deep. Si también se establece D3DVS20CAPS, [callnz Pred-vs](callnz-pred---vs.md) se cuenta para la profundidad de anidamiento de Call-vs/callnz bool-vs/if bool-vs (vea [límites de anidamiento del control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obtener detalles).

### <a name="predication"></a>Predicación

Si se establece [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , el dispositivo admite [SETP \_ COMP-vs](setp-comp---vs.md) e instruction predication. Si D3DVS20CAPS también es mayor que 0, se admiten las siguientes instrucciones de control de flujo dinámico adicionales:

-   [Si Pred-vs](if-pred---vs.md)
-   [callnz Pred-vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

### <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas. El número de instrucciones que se ejecutan puede ser mucho mayor (debido al soporte de bucle o representación) y está limitado por [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), que debe ser al menos 0xFFFF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 