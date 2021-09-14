---
description: Enumera las funciones aritméticas vectoriales.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Funciones aritméticas vectoriales
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ad5149153b736ddf6d2f2af5b9671e32651f86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966311"
---
# <a name="vector-arithmetic-functions"></a>Funciones aritméticas vectoriales

Enumera las funciones aritméticas vectoriales.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Calcula el valor absoluto de cada componente de [**un XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Calcula la suma de dos vectores.<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Agrega dos vectores que representan ángulos.<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Calcula el límite máximo de cada componente de [**un XMVECTOR.**](xmvector-data-type.md)<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Fija los componentes de un vector a un intervalo mínimo y máximo especificado.<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Divide una instancia de `XMVECTOR` por una segunda instancia y devuelve el resultado en una tercera instancia.<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Calcula la planta de cada componente de [**un XMVECTOR.**](xmvector-data-type.md)<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Realiza una prueba por componente para +/- infinito en un vector.<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Realiza una prueba naN por componente en un vector.<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Realiza una comparación por componente entre dos vectores y devuelve un vector que contiene los componentes más grandes.<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Realiza una comparación por componente entre dos vectores y devuelve un vector que contiene los componentes más pequeños.<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Calcula el resto de punto flotante por componente del cociente de dos vectores.<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Calcula el módulo de ángulo por componente 2PI.<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Calcula el producto por componente de dos vectores.<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Calcula el producto de los dos primeros vectores agregados al tercer vector.<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Calcula la negación de un vector.<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Calcula la diferencia de un tercer vector y el producto de los dos primeros vectores.<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | Calcula *V1 elevado* a la potencia de *V2.*<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Calcula el recíproco por componente de un vector.<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Calcula el recíproco por componente de un vector.<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Calcula la raíz cuadrada mutua por componente de un vector.<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Calcula la raíz cuadrada mutua por componente de un vector.<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Redondea cada componente de un vector al entero más cercano.<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Satura cada componente de un vector hasta el intervalo de 0,0f a 1,0f.<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Escalar multiplica un vector por un valor de punto flotante.<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Calcula la raíz cuadrada por componente de un vector.<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Calcula la raíz cuadrada por componente de un vector.<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Calcula la diferencia de dos vectores.<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Resta dos vectores que representan ángulos.<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Calcula la suma horizontal de los componentes de [**un XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Redondea cada componente de un vector al valor entero más cercano en la dirección de cero.<br/>                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones vectoriales de la biblioteca DirectXMath](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
