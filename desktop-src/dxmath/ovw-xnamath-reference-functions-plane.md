---
description: Muestra las funciones de plano proporcionadas por DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Funciones de plano de la biblioteca de DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705947"
---
# <a name="directxmath-library-plane-functions"></a>Funciones de plano de la biblioteca de DirectXMath

Muestra las funciones de plano proporcionadas por DirectXMath.

Estas funciones usan un vector de XMVECTOR 4 para representar los coeficientes de la ecuación de plano, AX + by + cz + D = 0, donde el componente X es un, el componente Y es B, el componente Z es C y el componente W es D.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | Calcula el producto escalar entre un plano de entrada y un vector 4D.<br/>                                    |
| [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | Calcula el producto escalar entre un plano de entrada y un vector 3D.<br/>                                    |
| [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | Calcula el producto de punto entre el vector normal de un plano y un vector 3D.<br/>                      |
| [**XMPlaneEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | Determina si dos planos son iguales.<br/>                                                                   |
| [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | Calcula la ecuación de un plano construido a partir de un punto del plano y un vector normal.<br/>           |
| [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | Calcula la ecuación de un plano construido a partir de tres puntos del plano.<br/>                          |
| [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | Busca la intersección entre un plano y una línea.<br/>                                                    |
| [**XMPlaneIntersectPlane**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | Busca la intersección de dos planos.<br/>                                                                 |
| [**XMPlaneIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | Comprueba si alguno de los coeficientes de un plano es infinito positivo o negativo.<br/>                    |
| [**XMPlaneIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | Comprueba si alguno de los coeficientes de un plano es un NaN.<br/>                                            |
| [**XMPlaneNearEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | Determina si dos planos son casi iguales.<br/>                                                       |
| [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | Normaliza los coeficientes de un plano para que los coeficientes de x, y y z formen un vector normal de unidad.<br/> |
| [**XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | Calcula los coeficientes de un plano de modo que los coeficientes de x, y y z formen un vector normal de unidad.<br/>  |
| [**XMPlaneNotEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | Determina si dos planos no son iguales.<br/>                                                                 |
| [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | Transforma un plano por una matriz determinada.<br/>                                                                 |
| [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | Transforma una secuencia de planos por una matriz determinada.<br/>                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de la biblioteca de DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
