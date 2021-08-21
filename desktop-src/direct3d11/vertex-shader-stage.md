---
title: Fase del sombreador de vértices
description: La fase sombreador de vértices (VS) procesa los vértices del ensamblador de entrada, realizando operaciones por vértice como transformaciones, descamblación, transformación e iluminación por vértice.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3815f4c26c97e68ac0b4b20b72849052710f2f6adc0722bb3e42f5c8bf7a1c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530413"
---
# <a name="vertex-shader-stage"></a>Fase del sombreador de vértices

La fase sombreador de vértices (VS) procesa los vértices del ensamblador de entrada, realizando operaciones por vértice como transformaciones, descamblación, transformación e iluminación por vértice. Los sombreadores de vértices siempre funcionan en un solo vértice de entrada y generan un solo vértice de salida. La fase del sombreador de vértices siempre debe estar activa para que se ejecute la canalización. Si no se requiere ninguna modificación o transformación de vértices, se debe crear y establecer un sombreador de vértices de paso a través en la canalización.

## <a name="the-vertex-shader"></a>Sombreador de vértices

Cada vértice de entrada del sombreador de vértices puede estar formado por hasta 16 vectores de 32 bits (hasta 4 componentes cada uno) y cada vértice de salida puede estar formado por hasta 16 vectores de 32 bits de 4 componentes. Todos los sombreadores de vértices deben tener un mínimo de una entrada y una salida, que puede ser tan solo un valor escalar.

La fase del sombreador de vértices puede consumir dos valores generados por el sistema del ensamblador de entrada: VertexID e InstanceID (vea Valores del sistema y Semántica). Dado que VertexID e InstanceID son significativos a nivel de vértice, y los identificadores generados por hardware solo se pueden insertar en la primera fase que los entienda, estos valores de identificador solo se pueden insertar en la fase del sombreador de vértices.

Los sombreadores de vértices siempre se ejecutan en todos los vértices, incluidos los vértices adyacentes en topologías primitivas de entrada con adyacencia. El número de veces que se ha ejecutado el sombreador de vértices se puede consultar desde la CPU mediante la estadística de canalización VSInvocations.

Un sombreador de vértices puede realizar operaciones de muestreo de carga y textura donde no se necesitan derivados del espacio de pantalla (mediante funciones intrínsecas HLSL: Sample (objeto de textura [HLSL de DirectX),](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample) [SampleCmpLevelZero (objeto](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)de textura HLSL de DirectX) y SampleGrad (objeto de textura [HLSL de DirectX).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 