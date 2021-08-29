---
description: Enumera las funciones de matriz proporcionadas por DirectXMath.
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: Funciones de matriz de directXMath Library
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f560d42e5bf2095c61cde60de1f8b3e5e78d31eb1c72b4a71561548ed89058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841255"
---
# <a name="directxmath-library-matrix-functions"></a>Funciones de matriz de directXMath Library

Enumera las funciones de matriz proporcionadas por DirectXMath.

> [!Note]  
> DirectXMath ofrece versiones a la izquierda y derecha de funciones de matriz con "entrega", pero siempre supone un formato de fila principal.

 

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | Crea una matriz de transformación afín.<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | Crea una matriz de transformación afín 2D en el plano xy. <br/>                                                                  |
| [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | Divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.<br/>                   |
| [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | Calcula el determinante de una matriz.<br/>                                                                                       |
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
| [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | Calcula la transpuesta del producto de dos matrices.<br/>                                                                      |
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
| [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | Crea una matriz de transformación diseñada para reflejar vectores a través de un plano determinado.<br/>                                           |
| [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | Crea una matriz que gira alrededor de un eje arbitrario.<br/>                                                                      |
| [**XMMatrixRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | Crea una matriz que gira alrededor de un vector normal arbitrario.<br/>                                                             |
| [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | Crea una matriz de rotación a partir de un cuaternión.<br/>                                                                                 |
| [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | Crea una matriz de rotación basada en un paso, una guia y un giro determinados (ángulos de Euler).<br/>                                              |
| [**XMMatrixRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | Crea una matriz de rotación basada en un vector que contiene los ángulos de Euler (inclinación, yaw y roll).<br/>                              |
| [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | Crea una matriz que gira alrededor del eje X.<br/>                                                                             |
| [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | Crea una matriz que gira alrededor del eje Y.<br/>                                                                             |
| [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | Crea una matriz que gira alrededor del eje Z.<br/>                                                                             |
| [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | Crea una matriz que se escala a lo largo del eje X, el eje Y y el eje Z.<br/>                                                           |
| [**XMMatrixScalingFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | Crea una matriz de escalado a partir de un vector 3D.<br/>                                                                                   |
| [**XMMatrixSet**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | Crea una matriz con **valores float.**<br/>                                                                                     |
| [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | Crea una matriz de transformación que aplana la geometría en un plano.<br/>                                                         |
| [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | Crea una matriz de transformación.<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | Crea una matriz de transformación 2D en el plano xy.<br/>                                                                          |
| [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | Genera una matriz de traducción a partir de los desplazamientos especificados.<br/>                                                                     |
| [**XMMatrixTranslationFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | Crea una matriz de traducción a partir de un vector.<br/>                                                                                  |
| [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | Calcula la transpuesta de una matriz.<br/>                                                                                         |
| [**XMMatrixVectorTensorProduct**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixvectortensorproduct)<br/>                                           | Calcula el tensor externo producto de 2 vectores.<br/>                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de biblioteca de DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
