---
title: Shader Model 6
description: El modelo de sombreador 6.0 agrega un intervalo de funciones intrínsecas de operación de onda para los sombreadores de cálculo y píxeles.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33eb4eab2a92e929bdefdc1df0f9cb1e0d84909a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573656"
---
# <a name="shader-model-6"></a>Shader Model 6

Todos los intrínsecos de onda no relacionados con cuadrándulas están disponibles en todas las fases del sombreador. Los intrínsecos de cuatro ondas solo están disponibles en sombreadores de cálculo y píxeles.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md)<br/> | Devuelve el valor local especificado que se lee desde el carril diagonalmente opuesto de este cuadrándido.<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | Devuelve el valor de origen especificado del camino identificado por el identificador de la calle dentro del cuadrándido actual.<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | Devuelve el valor local especificado leído desde el otro carril de este quad en la dirección X.<br/>                                                                    |
| [**QuadReadAcrossY**](quadswapy.md)<br/>                      | Devuelve el valor de origen especificado leído desde el otro carril de este quad en la dirección Y.<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | Devuelve true si la expresión es la misma para todos los carriles activos de la ola actual (y, por tanto, uniforme en ella).<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | Devuelve el and bit a bit de todos los valores de la expresión en todos los carriles activos de la ola actual y lo replica de nuevo en todos los carriles activos. <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | Devuelve el or bit a bit de todos los valores de la expresión en todos los carriles activos de la ola actual y lo replica de nuevo en todos los carriles activos. <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | Devuelve el XOR bit a bit de todos los valores de la expresión en todos los carriles activos de la ola actual y lo replica de nuevo en todos los carriles activos. <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | Cuenta el número de variables booleanas que se evalúan como true en todos los carriles activos de la ola actual y replica el resultado en todos los carriles de la onda.<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | Devuelve el valor máximo de la expresión en todos los carriles activos de la onda actual y la replica de nuevo en todos los carriles activos. <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | Devuelve el valor mínimo de la expresión en todos los carriles activos de la onda actual y la replica de nuevo en todos los carriles activos. <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | Multiplica los valores de la expresión entre todos los carriles activos de la ola actual y la replica de nuevo en todos los carriles activos.<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | Suma el valor de la expresión en todos los carriles activos de la onda actual y lo replica en todos los carriles de la onda actual.<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | Devuelve true si la expresión es true en todos los carriles activos de la ola actual.<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | Devuelve true si la expresión es true en cualquiera de los carriles activos de la ola actual.<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | Devuelve una máscara de bits de entero de 4 bits sin signo de la evaluación de la expresión booleana para todos los carriles activos de la onda especificada. <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | Devuelve el número de calles de una ola en esta arquitectura. <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | Devuelve el índice del carril actual dentro de la onda actual. <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | Devuelve true solo para el carril activo de la onda actual con el índice más pequeño. <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | Devuelve la suma de todas las variables booleanas especificadas establecidas en true en todos los carriles activos con índices menores que el actual. <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | Devuelve el producto de todos los valores de los carriles activos de esta ola con índices menores que este.<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | Devuelve la suma de todos los valores de los carriles activos con índices más pequeños que este.<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | Devuelve el valor de la expresión para el carril activo de la onda actual con el índice más pequeño. <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | Devuelve el valor de la expresión para el índice de lane especificado dentro de la ola especificada.<br/>                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





