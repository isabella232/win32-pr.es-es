---
title: Modelo de sombreador HLSL 6,0
description: Describe los intrínsecos de operación de onda agregados al modelo de sombreador de HLSL 6,0.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d082fc131c7cd08db9eb1861c4af39d600f40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984014"
---
# <a name="hlsl-shader-model-60"></a>Modelo de sombreador HLSL 6,0

Describe los intrínsecos de operación de onda agregados al modelo de sombreador de HLSL 6,0.

- [Modelo de sombreador 6,0](#shader-model-60)
- [Terminología](#terminology)
- [Intrínsecos del lenguaje de sombreado](#shading-language-intrinsics)
    - [Consulta de onda](#wave-query)
    - [Voto de onda](#wave-vote)
    - [Difusión de ondas](#wave-broadcast)
    - [Reducción de onda](#wave-reduction)
    - [Recorrido de onda y prefijo](#wave-scan-and-prefix)
    - [Operaciones de orden aleatorio de ancho cuádruple](#quad-wide-shuffle-operations)
- [Capacidad de hardware](#hardware-capability)
- [Temas relacionados](#related-topics)

## <a name="shader-model-60"></a>Modelo de sombreador 6,0

En el caso de los modelos de sombreador anteriores, la programación de HLSL solo expone un único subproceso de ejecución. Se proporcionan nuevas operaciones de nivel de onda, a partir del modelo 6,0, para aprovechar explícitamente el paralelismo de las GPU actuales: muchos subprocesos se pueden ejecutar en lógico en el mismo núcleo simultáneamente. Por ejemplo, los intrínsecos del modelo 6,0 permiten la eliminación de construcciones de barrera cuando el ámbito de sincronización está dentro del ancho del procesador SIMD, o algún otro conjunto de subprocesos que se sabe que son atómicos entre sí.

Entre los casos de uso posibles se incluyen: compactación de secuencias, reducciones, transposición de bloques, ordenación bitónica o transformaciones de Fourier rápidas (FFT), discretización, desduplicación de secuencias y escenarios similares.

La mayoría de los intrínsecos aparecen en sombreadores de píxeles y sombreadores de cálculo, aunque hay algunas excepciones (indicadas para cada función). Las funciones se han agregado a los requisitos del nivel de característica 12,0 de DirectX, en el nivel de API 12.

El *<type>* parámetro y el valor devuelto de estas funciones implican el tipo de la expresión, los tipos admitidos son los de la lista siguiente que *también* están presentes en el modelo de sombreador de destino de la aplicación:

- Half, half2, half3, half4
- Float, float2, float3, FLOAT4
- Double, double2, double3, double4
- int, INT2, INT3, INT4
- uint, uint2, UInt3, uint4
- Short, short2, short3, short4
- ushort, ushort2, ushort3, ushort4
- UInt64 \_ t, UInt64 \_ T2, UInt64 \_ T3, UInt64 \_ T4

Algunas operaciones (como los operadores bit a bit) solo admiten los tipos enteros.

## <a name="terminology"></a>Terminología

| | |
|-|-|
| **Término** | **Definición** |
| Carril | Un único subproceso de ejecución. Los modelos de sombreador anteriores a la versión 6,0 exponen solo uno de estos en el nivel de idioma, lo que mantiene la expansión al procesamiento de SIMD en paralelo completamente hasta la implementación. |
| Wave | Conjunto de calles (subprocesos) que se ejecutan simultáneamente en el procesador. No se requieren barreras explícitas para garantizar que se ejecuten en paralelo. Los conceptos similares incluyen "warp" y "Wavefront". |
| Calle inactivo | Una calle que no se ejecuta, por ejemplo, debido al flujo de control o trabajo insuficiente para rellenar el tamaño mínimo de la onda. |
| Active Lane | Lane para el que se realiza la ejecución. En los sombreadores de píxeles, puede incluir cualquier pasaje de píxel auxiliar. |
| Cuádruple | Un conjunto de 4 calles adyacentes correspondientes a píxeles organizados en un cuadrado de 2x2. Se usan para calcular degradados por diferencia en x o y. Una onda puede constar de varias cuádruples. Se ejecutan todos los píxeles de un cuádruple activo (y pueden ser "calles activas"), pero los que no producen resultados visibles se denominan "calles del ayudante". |
| Calle del ayudante | Una calle que se ejecuta únicamente con el propósito de los degradados en cuatro sombreadores de píxeles. La salida de este carril se descartará y, por tanto, no se representará en la superficie de destino. |

## <a name="shading-language-intrinsics"></a>Intrínsecos del lenguaje de sombreado

Todas las operaciones de este modelo de sombreador se han agregado en un intervalo de funciones intrínsecas.

### <a name="wave-query"></a>Consulta de onda

Intrínsecos para consultar una sola onda.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de cálculo** |
| [**WaveGetLaneCount**](wavegetlanecount.md) | Devuelve el número de calles de la onda actual. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Devuelve el índice de la calle actual dentro de la onda actual. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Devuelve true solo para el carril activo en la ola actual con el índice más pequeño. | \* | \* |

### <a name="wave-vote"></a>Voto de onda

Este conjunto de intrínsecos compara los valores entre los subprocesos activos actualmente desde la onda actual.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de cálculo** |
| [**WaveActiveAnyTrue**](waveanytrue.md) | Devuelve true si la expresión es verdadera en cualquier carril activo de la onda actual. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Devuelve true si la expresión es verdadera en todas las calles activas de la ola actual. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Devuelve una máscara de bits de entero sin signo de 64 bits de la evaluación de la expresión booleana para todas las calles activas de la onda especificada. | \* | \* |

### <a name="wave-broadcast"></a>Difusión de ondas

Estos intrínsecos permiten que todas las calles activas de la ola actual reciban el valor de la calle especificada y lo difundan eficazmente. El valor devuelto de una calle no válida es indefinido.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de cálculo** |
| [**WaveReadLaneAt**](wavereadlaneat.md) | Devuelve el valor de la expresión para el índice de la calle especificado dentro de la onda especificada. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Devuelve el valor de la expresión para el carril activo de la onda actual con el índice más pequeño. | \* | \* |

### <a name="wave-reduction"></a>Reducción de onda

Estos intrínsecos calculan la operación especificada en todas las calles activas de la onda y difunden el resultado final a todas las calles activas. Por lo tanto, la salida final se garantiza uniforme en toda la onda.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de cálculo** |
| [**WaveActiveAllEqual**](waveactiveallequal.md) | Devuelve true si la expresión es la misma para cada carril activo de la ola actual (y, por tanto, uniforme en ella). | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | Devuelve el AND bit a bit de todos los valores de la expresión en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | Devuelve la operación OR bit a bit de todos los valores de la expresión en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | Devuelve la operación OR exclusiva bit a bit de todos los valores de la expresión en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | Cuenta el número de variables Booleanas que se evalúan como true en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | Calcula el valor máximo de la expresión en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | Calcula el valor mínimo de la expresión en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | Multiplica los valores de la expresión en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | Suma el valor de la expresión en todas las calles activas de la onda actual y lo replica en todas las calles de la onda actual y replica el resultado en todas las calles de la onda. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Recorrido de onda y prefijo

Estos intrínsecos aplican la operación a cada calle y dejan cada resultado parcial del cálculo en la calle correspondiente.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de cálculo** |
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | Devuelve la suma de todas las variables Booleanas especificadas establecidas en true en todas las calles activas con índices más pequeños que la calle actual. | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | Devuelve la suma de todos los valores de las calles activas con índices más pequeños que este. | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | Devuelve el producto de todos los valores de las calles anteriores a esta ola especificada. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Operaciones de orden aleatorio de ancho cuádruple

Estos intrínsecos realizan operaciones de intercambio en los valores de una onda que se sabe que contienen cuatro sombreadores de píxeles, tal y como se define aquí. Los índices de los píxeles de la cuádruple se definen en la línea de análisis o en el orden de lectura, donde las coordenadas dentro de un cuádruple son:

+---------> X 

| [0] [1] 

| [2] [3] 

v 

Y 


Estas rutinas funcionan en sombreadores de cálculo o sombreadores de píxeles. En los sombreadores de cálculo, operan en cuádruples definidos como grupos divididos uniformemente de 4 dentro de una onda SIMD. En los sombreadores de píxeles, deben usarse en ondas capturadas por WaveQuadLanes; de lo contrario, los resultados son indefinidos.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de cálculo** |
| [**QuadReadLaneAt**](quadreadlaneat.md) | Devuelve el valor de origen especificado leído de la calle del cuádruple actual identificado por quadLaneID \[ 0.. 3, \] que debe ser uniforme en el cuádruple. | \* | |
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md) | Devuelve el valor local especificado que se lee desde la calle opuesta en diagonal en esta cuádruple. | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | Devuelve el valor de origen especificado leído de la otra calle de este cuádruple en la dirección X. | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | Devuelve el valor de origen especificado leído de la otra calle de este cuádruple en la dirección Y. | \* | |

## <a name="hardware-capability"></a>Capacidad de hardware

Para comprobar que las características de la operación de onda están disponibles en cualquier hardware específico, llame a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport), anotando la descripción y el uso de la estructura [**D3D12 \_ \_ Data \_ D3D12 \_ OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) .

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
* [Intrínsecos del modelo de sombreador 6](shader-model-6-0.md)