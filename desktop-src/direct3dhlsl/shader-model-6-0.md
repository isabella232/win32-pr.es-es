---
title: Modelo de sombreador 6
description: El modelo de sombreador 6,0 agrega un intervalo de intrínsecos de operación de onda para los sombreadores de píxeles y de cálculo.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33eb4eab2a92e929bdefdc1df0f9cb1e0d84909a
ms.sourcegitcommit: 39fe65a8a7c1cbea382c78820663c548f4e77079
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149728"
---
# <a name="shader-model-6"></a>Modelo de sombreador 6

Todos los intrínsecos de onda no cuádruples están disponibles en todas las fases del sombreador. Los intrínsecos de cuatro Wave solo están disponibles en píxeles y sombreadores de cálculo.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md)<br/> | Devuelve el valor local especificado que se lee desde la calle opuesta en diagonal en esta cuádruple.<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | Devuelve el valor de origen especificado de la calle identificada por el ID. de calle dentro del cuádruple actual.<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | Devuelve el valor local especificado leído de la otra calle de este cuádruple en la dirección X.<br/>                                                                    |
| [**QuadReadAcrossY**](quadswapy.md)<br/>                      | Devuelve el valor de origen especificado leído de la otra calle de este cuádruple en la dirección Y.<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | Devuelve true si la expresión es la misma para cada carril activo de la ola actual (y, por tanto, uniforme en ella).<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | Devuelve el bit a bit y de todos los valores de la expresión en todas las calles activas de la onda actual y lo replica de nuevo en todas las calles activas. <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | Devuelve la operación OR bit a bit de todos los valores de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas. <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | Devuelve el XOR bit a bit de todos los valores de la expresión en todas las calles activas de la onda actual y lo replica de nuevo en todas las calles activas. <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | Cuenta el número de variables Booleanas que se evalúan como true en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda.<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | Devuelve el valor máximo de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas. <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | Devuelve el valor mínimo de la expresión en todas las calles activas de la onda actual lo replica de nuevo en todas las calles activas. <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | Multiplica los valores de la expresión en todas las calles activas de la ola actual y los replica de nuevo en todas las calles activas.<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | Suma el valor de la expresión en todas las calles activas de la ola actual y lo replica en todas las calles de la ola actual.<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | Devuelve true si la expresión es verdadera en todas las calles activas de la ola actual.<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | Devuelve true si la expresión es verdadera en cualquiera de las calles activas de la onda actual.<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | Devuelve una máscara de bits de entero sin signo de 4 bits de la evaluación de la expresión booleana para todas las calles activas de la onda especificada. <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | Devuelve el número de calles de una onda en esta arquitectura. <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | Devuelve el índice de la calle actual dentro de la onda actual. <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | Devuelve true solo para el carril activo en la ola actual con el índice más pequeño. <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | Devuelve la suma de todas las variables Booleanas especificadas establecidas en true en todas las calles activas con índices más pequeños que la calle actual. <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | Devuelve el producto de todos los valores de las calles activas en esta ola con índices inferiores a esta calle.<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | Devuelve la suma de todos los valores de las calles activas con índices más pequeños que este.<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | Devuelve el valor de la expresión para el carril activo de la onda actual con el índice más pequeño. <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | Devuelve el valor de la expresión para el índice de la calle especificado dentro de la onda especificada.<br/>                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





