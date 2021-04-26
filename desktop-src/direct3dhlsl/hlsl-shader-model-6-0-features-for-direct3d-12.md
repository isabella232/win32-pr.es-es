---
title: Modelo de sombreador HLSL 6.0
description: Describe los intrínsecos de la operación de onda agregados al modelo de sombreador HLSL 6.0.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7e55661e3f91125597c8c7842a1be16129cefe0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995472"
---
# <a name="hlsl-shader-model-60"></a>Modelo de sombreador HLSL 6.0

Describe los intrínsecos de la operación de onda agregados al modelo de sombreador HLSL 6.0.

- [Modelo de sombreador 6.0](#shader-model-60)
- [Terminología](#terminology)
- [Funciones intrínsecas del lenguaje de sombreado](#shading-language-intrinsics)
    - [Consulta de onda](#wave-query)
    - [Wave Vote](#wave-vote)
    - [Difusión de onda](#wave-broadcast)
    - [Reducción de onda](#wave-reduction)
    - [Wave Scan y Prefix](#wave-scan-and-prefix)
    - [Operaciones de orden aleatorio de cuatro anchos](#quad-wide-shuffle-operations)
- [Funcionalidad de hardware](#hardware-capability)
- [Temas relacionados](#related-topics)

## <a name="shader-model-60"></a>Shader Model 6.0

Para los modelos de sombreador anteriores, la programación HLSL expone solo un único subproceso de ejecución. Se proporcionan nuevas operaciones de nivel de onda, a partir del modelo 6.0, para aprovechar explícitamente el paralelismo de las GPU actuales: muchos subprocesos pueden ejecutarse en el mismo núcleo simultáneamente. Por ejemplo, los intrínsecos del modelo 6.0 permiten la eliminación de construcciones de barrera cuando el ámbito de sincronización está dentro del ancho del procesador SIMD o algún otro conjunto de subprocesos que se sabe que son atómicos entre sí.

Entre los posibles casos de uso se incluyen: compactación de flujos, reducciones, transponer bloques, ordenación bitónica o transformaciones rápidas de Fourier (FFT), binning, desduplicación de flujos y escenarios similares.

La mayoría de los intrínsecos aparecen en sombreadores de píxeles y sombreadores de proceso, aunque hay algunas excepciones (anotadas para cada función). Las funciones se han agregado a los requisitos de Nivel de característica 12.0 de DirectX, en el nivel de API 12.

El parámetro y el valor devuelto de estas funciones implican el tipo de la expresión; los tipos admitidos son los de la lista siguiente que también están presentes en el modelo de sombreador de destino para *<type>* la aplicación: 

- half, half2, half3, half4
- float, float2, float3, float4
- double, double2, double3, double4
- int, int2, int3, int4
- uint, uint2, uint3, uint4
- short, short2, short3, short4
- ushort, ushort2, ushort3, ushort4
- uint64 \_ t, uint64 \_ t2, uint64 \_ t3, uint64 \_ t4

Algunas operaciones (como los operadores bit a bit) solo admiten los tipos enteros.

## <a name="terminology"></a>Terminología

| **Término** | **Definición** |
|-|-|
| Carril | Un único subproceso de ejecución. Los modelos de sombreador anteriores a la versión 6.0 exponen solo uno de ellos en el nivel de lenguaje, dejando la expansión al procesamiento SIMD paralelo completamente hasta la implementación. |
| Wave | Conjunto de pistas (subprocesos) ejecutadas simultáneamente en el procesador. No se requiere ninguna barrera explícita para garantizar que se ejecuten en paralelo. Entre los conceptos similares se incluyen "warp" y "wavefront". |
| Inactive Lane | Un camino que no se ejecuta, por ejemplo, debido al flujo de control, o trabajo insuficiente para rellenar el tamaño mínimo de la onda. |
| Active Lane | Un camino para el que se está realizando la ejecución. En los sombreadores de píxeles, puede incluir cualquier calle de píxel del asistente. |
| cuádruple | Un conjunto de 4 calles adyacentes correspondientes a píxeles organizados en un cuadrado de 2x2. Se usan para calcular degradados mediante la diferenciación en x o y. Una onda puede estar formada por varios cuadrántiplo. Todos los píxeles de un quad activo se ejecutan (y pueden ser "Active Lanes"), pero los que no producen resultados visibles se denominan "Helper Lanes". |
| Helper Lane | Un camino que se ejecuta únicamente con el fin de degradados en los quads del sombreador de píxeles. La salida de este tipo de ruta se descartará y, por tanto, no se representará en la superficie de destino. |

## <a name="shading-language-intrinsics"></a>Funciones intrínsecas del lenguaje de sombreado

Todas las operaciones de este modelo de sombreador se han agregado en un intervalo de funciones intrínsecas.

### <a name="wave-query"></a>Consulta de onda

Intrínsecos para consultar una sola onda.

| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de proceso** |
|-|-|-|-|
| [**WaveGetLaneCount**](wavegetlanecount.md) | Devuelve el número de pistas en la onda actual. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Devuelve el índice del carril actual dentro de la onda actual. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Devuelve true solo para el carril activo en la onda actual con el índice más pequeño. | \* | \* |

### <a name="wave-vote"></a>Wave Vote

Este conjunto de intrínsecos compara los valores de los subprocesos actualmente activos desde la onda actual.

| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de proceso** |
|-|-|-|-|
| [**WaveActiveAnyTrue**](waveanytrue.md) | Devuelve true si la expresión es true en cualquier calle activo de la ola actual. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Devuelve true si la expresión es true en todos los sentidos activos de la ola actual. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Devuelve una máscara de bits de entero sin signo de 64 bits de la evaluación de la expresión booleana para todos los calles activos de la onda especificada. | \* | \* |

### <a name="wave-broadcast"></a>Difusión de onda

Estos intrínsecos permiten que todos los canales activos de la onda actual reciban el valor del lane especificado y lo difundan de forma eficaz. El valor devuelto de un lane no válido es indefinido.

| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de proceso** |
|-|-|-|-|
| [**WaveReadLaneAt**](wavereadlaneat.md) | Devuelve el valor de la expresión para el índice de la cadena especificado dentro de la onda especificada. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Devuelve el valor de la expresión para el camino activo de la onda actual con el índice más pequeño. | \* | \* |

### <a name="wave-reduction"></a>Reducción de onda

Estos intrínsecos calculan la operación especificada en todos los calles activas de la ola y difunden el resultado final a todos los calles activos. Por lo tanto, la salida final se garantiza uniforme en toda la onda.

| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de proceso** |
|-|-|-|-|
| [**WaveActiveAllEqual**](waveactiveallequal.md) | Devuelve true si la expresión es la misma para todos los carriles activos de la ola actual (y, por tanto, uniforme en ella). | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | Devuelve el and bit a bit de todos los valores de la expresión en todos los carriles activos de la onda actual y replica el resultado en todos los carriles de la onda. | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | Devuelve el OR bit a bit de todos los valores de la expresión en todos los carriles activos de la onda actual y replica el resultado en todos los carriles de la onda. | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | Devuelve el OR exclusivo bit a bit de todos los valores de la expresión en todos los carriles activos de la ola actual y replica el resultado en todos los carriles de la ola. | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | Cuenta el número de variables booleanas que se evalúan como true en todos los carriles activos de la ola actual y replica el resultado en todos los carriles de la ola. | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | Calcula el valor máximo de la expresión en todos los carriles activos de la ola actual y replica el resultado en todos los carriles de la ola. | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | Calcula el valor mínimo de la expresión en todos los carriles activos de la onda actual y replica el resultado en todos los carriles de la onda. | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | Multiplica los valores de la expresión entre todos los carriles activos de la ola actual y replica el resultado en todos los carriles de la ola. | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | Suma el valor de la expresión en todos los carriles activos de la ola actual y la replica en todos los carriles de la ola actual y replica el resultado en todos los carriles de la ola. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Wave Scan y Prefix

Estos intrínsecos aplican la operación a cada calle y dejan cada resultado parcial del cálculo en el carril correspondiente.

| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de proceso** |
|-|-|-|-|
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | Devuelve la suma de todas las variables booleanas especificadas establecidas en true en todos los canales activos con índices menores que el actual. | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | Devuelve la suma de todos los valores de los canales activos con índices más pequeños que este. | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | Devuelve el producto de todos los valores de los calles anteriores a esta de la onda especificada. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Operaciones de orden aleatorio de cuatro anchos

Estos intrínsecos realizan operaciones de intercambio en los valores de una onda que se sabe que contienen cuadrándidos de sombreador de píxeles, tal y como se define aquí. Los índices de los píxeles del cuadrándice se definen en línea de examen o en orden de lectura, donde las coordenadas dentro de un cuadrándido son:

+---------> X 

| [0] [1] 

| [2] [3] 

v 

Y 


Estas rutinas funcionan en sombreadores de proceso o sombreadores de píxeles. En los sombreadores de proceso funcionan en cuadrándulas definidas como grupos divididos uniformemente de 4 dentro de una onda SIMD. En los sombreadores de píxeles se deben usar en las ondas capturadas por WaveQuadLanes; de lo contrario, los resultados son indefinidos.

| **Intrinsic** | **Descripción** | **Sombreador de píxeles** | **Sombreador de proceso** |
|-|-|-|-|
| [**QuadReadLaneAt**](quadreadlaneat.md) | Devuelve el valor de origen especificado leído desde el lado del cuadrándido actual identificado por quadLaneID \[ 0...3, que debe \] ser uniforme en el cuadrántico. | \* | |
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md) | Devuelve el valor local especificado que se lee desde el carril diagonalmente opuesto de este cuadrándido. | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | Devuelve el valor de origen especificado leído desde el otro carril de este quad en la dirección X. | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | Devuelve el valor de origen especificado leído desde el otro carril de este quad en la dirección Y. | \* | |

## <a name="hardware-capability"></a>Funcionalidad de hardware

Para comprobar que las características de la operación de onda están disponibles en cualquier hardware específico, llame a [**ID3D12Device::CheckFeatureSupport,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)y note la descripción y el uso de la estructura [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1)

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
* [Funciones intrínsecas del modelo 6 del sombreador](shader-model-6-0.md)
