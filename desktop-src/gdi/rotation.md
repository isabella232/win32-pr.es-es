---
description: Muchas aplicaciones de CAD proporcionan características que giran los objetos dibujados en el área de cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985999"
---
# <a name="rotation"></a>Rotación

Muchas aplicaciones de CAD proporcionan características que giran los objetos dibujados en el área de cliente. Las aplicaciones que incluyen capacidades de rotación utilizan la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer la transformación espacio mundial adecuado en la página. Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM11, eM12, eM21 y eM22 de XFORM especifican respectivamente, el coseno, el seno, el seno negativo y el coseno del ángulo de rotación.

Cuando se produce la *rotación* , los puntos que constituyen un objeto se giran con respecto al origen del espacio de coordenadas. En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades girado 30 grados cuando se copia del espacio de coordenadas universal en el espacio de coordenadas de la página.

![Ilustración que muestra dos espacios de coordenadas; cada una tiene un Rectange en una ubicación diferente y con una rotación diferente](images/cstrn-11.png)

En la ilustración anterior, cada punto del rectángulo se giró 30 grados con respecto al origen del espacio de coordenadas.

El algoritmo siguiente calcula la nueva coordenada x (x ') de un punto (x, y) que se gira por el ángulo A con respecto al origen del espacio de coordenadas.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

El algoritmo siguiente calcula la coordenada y (y ') de un punto (x, y) que se gira por el ángulo A con respecto al origen.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

Las dos transformaciones de giro se pueden combinar en una matriz de 2 por 2 como se indica a continuación.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

La matriz de 2 por 2 que generó el giro contiene los valores siguientes.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Derivación del algoritmo de rotación

Los algoritmos de rotación se basan en la suma de Teorema de trigonometría, lo que indica que la función trigonométrica de una suma de dos ángulos (a1 y a2) se puede expresar en términos de las funciones trigonométricas de los dos ángulos.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

En la ilustración siguiente se muestra un punto p girado en sentido contrario a las agujas del reloj hacia la nueva posición p '. Además, muestra dos triángulos formados por una línea dibujada a partir del origen del espacio de coordenadas hasta cada punto y una línea dibujada a partir de cada punto a través del eje x.

![diagrama que muestra el origen, p y p y dos triángulos](images/cstrn-12.png)

Con trigonometría, la coordenada x del punto p se puede obtener multiplicando la longitud de la hipotenusa h por el coseno de a1.

``` syntax
x = h * cos A1 
```

La coordenada y del punto p se puede obtener multiplicando la longitud de la hipotenusa h por el seno de a1.

``` syntax
y = h * sin A1 
```

Del mismo modo, la coordenada x del punto p ' se puede obtener multiplicando la longitud de la hipotenusa h por el coseno de (a1 + a2).

``` syntax
x' = h * cos (A1 + A2) 
```

Por último, se puede obtener la coordenada y del punto p ' multiplicando la longitud de la hipotenusa h por el seno de (a1 + a2).

``` syntax
y' = h * sin (A1 + A2) 
```

Con la suma teorema, los algoritmos anteriores se convierten en los siguientes:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Los algoritmos de rotación de un punto determinado girados por el ángulo a2 se pueden obtener sustituyendo x por cada aparición de (h \* cos a1) y sustituyendo y por cada aparición de (h \* sin a1).

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



