---
title: Fase del sombreador de vértices
description: La fase del sombreador de vértices (VS) procesa los vértices del ensamblador de entrada, realizando operaciones por vértice, como transformaciones, máscaras, transformación y iluminación por vértice.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a291b4abed572da54f9a2616ce19e926e1c6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077780"
---
# <a name="vertex-shader-stage"></a>Fase del sombreador de vértices

La fase del sombreador de vértices (VS) procesa los vértices del ensamblador de entrada, realizando operaciones por vértice, como transformaciones, máscaras, transformación y iluminación por vértice. Los sombreadores de vértices siempre operan en un solo vértice de entrada y producen un único vértice de salida. La fase del sombreador de vértices siempre debe estar activa para que se ejecute la canalización. Si no se requiere ninguna modificación o transformación de vértices, debe crearse un sombreador de vértices de paso a través y establecerse en la canalización.

## <a name="the-vertex-shader"></a>Sombreador de vértices

Cada vértice de entrada del sombreador de vértices puede estar formado por vectores de hasta 16 32 bits (hasta 4 componentes cada uno) y cada vértice de salida puede estar formado por un máximo de hasta 16 32 bits de componentes de 4 bits. Todos los sombreadores de vértices deben tener un mínimo de una entrada y una salida, que puede ser tan pequeña como un valor escalar.

La fase del sombreador de vértices puede consumir dos valores generados por el sistema del ensamblador de entrada: VertexID y InstanceID (consulte valores y semántica del sistema). Dado que VertexID y InstanceID son significativos en el nivel de vértice, y los identificadores generados por el hardware solo se pueden introducir en la primera fase que los comprenda, estos valores de identificador solo se pueden introducir en la fase del sombreador de vértices.

Los sombreadores de vértices siempre se ejecutan en todos los vértices, incluidos los vértices adyacentes en topologías primitivas de entrada con adyacencias. El número de veces que se ha ejecutado el sombreador de vértices se puede consultar desde la CPU mediante la estadística de canalización VSInvocations.

Un sombreador de vértices puede realizar operaciones de muestreo de la carga y de la textura en las que no se necesitan los derivados del espacio de pantalla (mediante las funciones intrínsecas de HLSL: [ejemplo (objeto de textura de HLSL de DirectX)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample), [SampleCmpLevelZero (objeto de textura de DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)y [SampleGrad (objeto de textura de HLSL de DirectX)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 