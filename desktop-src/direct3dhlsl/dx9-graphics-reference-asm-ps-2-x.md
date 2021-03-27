---
title: ps_2_x
description: Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997120"
---
# <a name="ps_2_x"></a>PS \_ 2 \_ x

Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [las \_ instrucciones de PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contienen una lista de las instrucciones disponibles.
-   [en \_ registros de PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) se enumeran los distintos tipos de registros utilizados por el sombreador de vértices Alu.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se utilizan para modificar la forma en que funciona una instrucción.
-   La [máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina los componentes del registro de destino que se van a escribir.
-   Los [modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.
-   [El registro de origen permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.

## <a name="dynamic-flow-control"></a>Control de flujo dinámico

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa la profundidad de anidamiento de las instrucciones de control de flujo dinámico: [si](if-bool---ps.md)es, si se ha [ \_ Compens](if-comp---ps.md), [si es \_ Pred](if-pred---ps.md), [break-PS](break---ps.md)y [break \_ COMP-PS](break-comp---ps.md). El valor es igual a la profundidad de anidamiento del bloque if \_ comp. Si este extremo es cero, el dispositivo no admite las instrucciones de control de flujo dinámico.

## <a name="number-of-temporary-registers"></a>Número de registros temporales

El número de registros temporales admitidos por el dispositivo. El intervalo está comprendido entre 12 y 32.

## <a name="static-flow-control-nesting-depth"></a>Profundidad de anidamiento de control de flujo estático

[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa la profundidad de anidamiento de dos tipos de instrucciones de control de flujo estático: [Loop](loop---ps.md)  / [REP](rep---ps.md) y [Call](call---ps.md)  / [callnz](callnz-bool---ps.md). las instrucciones de bucle/REP se pueden anidar hasta **StaticFlowControlDepth** Deep. De forma independiente, las instrucciones Call/callnz se pueden anidar hasta **StaticFlowControlDepth** Deep.

## <a name="number-of-instruction-slots"></a>Número de ranuras de instrucciones

El número de ranuras de instrucción puede oscilar entre 96 y un máximo de 512, y se especifica mediante [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0). El número total de instrucciones que se pueden ejecutar está definido por **MaxPixelShaderInstructionsExecuted**. Puede ser mayor que el número de ranuras de instrucciones debido a llamadas de bucle y subrutinas.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , se admite swizzle arbitrario. Consulte [source Register permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instrucciones de degradado

Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , se admiten las instrucciones de degradado. Consulte [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)y [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Predicación

Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , se admite la instrucción PREDICATION. Vea [registro de predicados](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Límite de lectura dependiente

Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , no hay ningún límite de lectura dependiente.

## <a name="texture-instruction-limit"></a>Límite de instrucciones de textura

Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , no hay ningún límite en las instrucciones de textura.

## <a name="sampler-count"></a>Recuento de muestras

El número de muestras de textura disponibles es 16.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 