---
description: Enumera las funciones de matriz proporcionadas por DirectXMath.
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: Funciones de matriz de la biblioteca de DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9c6110db6bb3ce9ee883406445ad3a04681cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705948"
---
# <a name="directxmath-library-matrix-functions"></a>Funciones de matriz de la biblioteca de DirectXMath

Enumera las funciones de matriz proporcionadas por DirectXMath.

> [!Note]  
> DirectXMath ofrece versiones de las funciones de matriz que se entregan a la izquierda y a la derecha, pero siempre supone un formato de fila principal.

 

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | Compila una matriz de transformación afín.<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | Crea una matriz de transformación afín 2D en el plano XY. <br/>                                                                  |
| [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.<br/>                   |
| [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | Calcula el factor determinante de una matriz.<br/>                                                                                       |
| [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)<br/>                                             | Compila la matriz de identidad.<br/>                                                                                                 |
| [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)<br/>                                               | Calcula el inverso de una matriz.<br/>                                                                                           |
| [**XMMatrixIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisidentity)<br/>                                         | Comprueba si una matriz es la matriz de identidad.<br/>                                                                              |
| [**XMMatrixIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisinfinite)<br/>                                         | Comprueba si alguno de los elementos de una matriz es infinito positivo o negativo.<br/>                                            |
| [**XMMatrixIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisnan)<br/>                                                   | Comprueba si alguno de los elementos de una matriz es NaN.<br/>                                                                      |
| [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)<br/>                                             | Crea una matriz de vista para un sistema de coordenadas a la izquierda usando una posición de cámara, una dirección hacia arriba y un punto focal.<br/>       |
| [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)<br/>                                             | Crea una matriz de vista para un sistema de coordenadas a la derecha usando una posición de cámara, una dirección hacia arriba y un punto focal.<br/>      |
| [**XMMatrixLookToLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktolh)<br/>                                             | Crea una matriz de vista para un sistema de coordenadas a la izquierda usando una posición de cámara, una dirección hacia arriba y una dirección de cámara.<br/>  |
| [**XMMatrixLookToRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktorh)<br/>                                             | Crea una matriz de vista para un sistema de coordenadas a la derecha usando una posición de cámara, una dirección hacia arriba y una dirección de cámara.<br/> |
| [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)<br/>                                             | Calcula el producto de dos matrices.<br/>                                                                                       |
| [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | Calcula la transposición del producto de dos matrices.<br/>                                                                      |
| [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)<br/>                                 | Crea una matriz de proyección ortogonal para un sistema de coordenadas a la izquierda.<br/>                                                 |
| [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)<br/>               | Crea una matriz de proyección ortogonal personalizada para un sistema de coordenadas a la izquierda.<br/>                                           |
| [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)<br/>               | Crea una matriz de proyección ortogonal personalizada para un sistema de coordenadas a la derecha.<br/>                                          |
| [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)<br/>                                 | Crea una matriz de proyección ortogonal para un sistema de coordenadas a la derecha.<br/>                                                |
| [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)<br/>                             | Crea una matriz de proyección de perspectiva a la izquierda basada en un campo visual.<br/>                                                |
| [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)<br/>                             | Crea una matriz de proyección de perspectiva a la derecha basada en un campo visual.<br/>                                               |
| [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)<br/>                                   | Crea una matriz de proyección de perspectiva a la izquierda.<br/>                                                                         |
| [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)<br/>                 | Crea una versión personalizada de una matriz de proyección de perspectiva a la izquierda.<br/>                                                     |
| [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)<br/>                 | Crea una versión personalizada de una matriz de proyección de perspectiva a la derecha.<br/>                                                    |
| [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)<br/>                                   | Crea una matriz de proyección de perspectiva a la derecha.<br/>                                                                        |
| [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | Crea una matriz de transformación diseñada para reflejar los vectores a través de un plano determinado.<br/>                                           |
| [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | Crea una matriz que gira en torno a un eje arbitrario.<br/>                                                                      |
| [**XMMatrixRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | Crea una matriz que gira en torno a un vector normal arbitrario.<br/>                                                             |
| [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | Crea una matriz de rotación a partir de un cuaternión.<br/>                                                                                 |
| [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | Crea una matriz de rotación basada en un tono, guiñada y rollo determinados (ángulos de Euler).<br/>                                              |
| [**XMMatrixRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | Crea una matriz de rotación basada en un vector que contiene los ángulos de Euler (tono, guiñada y rollo).<br/>                              |
| [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | Crea una matriz que gira alrededor del eje x.<br/>                                                                             |
| [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | Crea una matriz que gira alrededor del eje y.<br/>                                                                             |
| [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | Crea una matriz que gira alrededor del eje z.<br/>                                                                             |
| [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | Crea una matriz que se escala a lo largo de los ejes x, y y z.<br/>                                                           |
| [**XMMatrixScalingFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | Crea una matriz de escala a partir de un vector 3D.<br/>                                                                                   |
| [**XMMatrixSet**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | Crea una matriz con valores **float** .<br/>                                                                                     |
| [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | Crea una matriz de transformación que alisa la geometría en un plano.<br/>                                                         |
| [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | Crea una matriz de transformación.<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | Crea una matriz de transformación 2D en el plano XY.<br/>                                                                          |
| [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | Crea una matriz de traslación a partir de los desplazamientos especificados.<br/>                                                                     |
| [**XMMatrixTranslationFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | Crea una matriz de traslación a partir de un vector.<br/>                                                                                  |
| [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | Calcula la transposición de una matriz.<br/>                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de la biblioteca de DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
