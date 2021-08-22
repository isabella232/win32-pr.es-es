---
title: ps_2_x
description: Obtenga información ps_2_x, un sombreador de píxeles programable, que se conste de un conjunto de instrucciones que funcionan con datos de píxeles.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37bc9709effeb865651ca920a155094946b88753586174ecf6e1ab06eabd2fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489415"
---
# <a name="ps_2_x"></a>ps \_ 2 \_ x

Un sombreador de píxeles programable se forma de un conjunto de instrucciones que funcionan con datos de píxeles. Registra la transferencia de datos dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [ps \_ 2 \_ x Instructions contiene](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) una lista de las instrucciones disponibles.
-   [ps \_ 2 \_ x Registers enumera](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) los distintos tipos de registros usados por el sombreador de vértices ALU.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se usan para modificar el funcionamiento de una instrucción.
-   [Destination Register Write Mask determina](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) qué componentes del registro de destino se escriben.
-   [Los modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.
-   [El swling del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, copian o escriben.

## <a name="dynamic-flow-control"></a>Control de Flow dinámico

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa la profundidad de anidamiento de instrucciones de control de flujo dinámico: [si](if-bool---ps.md), si [ \_ comp](if-comp---ps.md), [si \_ pred](if-pred---ps.md), [break - ps](break---ps.md)y break comp - [ \_ ps](break-comp---ps.md). El valor es igual a la profundidad de anidamiento del bloque if \_ comp. Si este límite es cero, el dispositivo no admite instrucciones de control de flujo dinámico.

## <a name="number-of-temporary-registers"></a>Número de registros temporales

Número de registros temporales admitidos por el dispositivo. El intervalo es de 12 a 32.

## <a name="static-flow-control-nesting-depth"></a>Profundidad de anidamiento Flow control estático

[**StaticFlowControlDepth representa**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) la profundidad de anidamiento de dos tipos de instrucciones de control de flujo [estático:](loop---ps.md)loop  / [rep](rep---ps.md) y [call](call---ps.md)  / [callnz](callnz-bool---ps.md). Las instrucciones de loop /rep se pueden anidar hasta **StaticFlowControlDepth** deep. De forma independiente, las instrucciones /callnz se pueden anidar hasta **StaticFlowControlDepth** deep.

## <a name="number-of-instruction-slots"></a>Número de ranuras de instrucciones

El número de ranuras de instrucción puede oscilar entre 96 y un máximo de 512, y se especifica mediante [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0). **MaxPixelShaderInstructionsExecuted** define el número total de instrucciones que se pueden ejecutar. Esto puede ser mayor que el número de ranuras de instrucción debido a las llamadas de bucle y subrutina.

## <a name="arbitrary-swizzle"></a>Swzzle arbitrario

Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWZZLE,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) se admite el swzzle arbitrario. Vea [Source Register Swlingling (Swling del registro de origen).](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)

## <a name="gradient-instructions"></a>Instrucciones de degradado

Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) se admiten instrucciones de degradado. Vea [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)y [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Predicación

Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) se admite el predicado de instrucciones. Vea [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Límite de lectura dependiente

Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) no hay límites de lectura dependientes.

## <a name="texture-instruction-limit"></a>Límite de instrucciones de textura

Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTESTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) está establecido, no hay límite en las instrucciones de textura.

## <a name="sampler-count"></a>Recuento de muestreador

El número de muestreadores de textura disponibles es 16.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 