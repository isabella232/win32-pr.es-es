---
description: Muchas aplicaciones CAD proporcionan características que giran objetos dibujados en el área cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa6552411e2e018d04ff55cbeeb430d185fe62d61dc59d421d08dbe6e0d7174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602705"
---
# <a name="rotation"></a>Rotación

Muchas aplicaciones CAD proporcionan características que giran objetos dibujados en el área cliente. Las aplicaciones que incluyen funcionalidades de rotación usan [**la función SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer la transformación espacio del mundo adecuada en espacio de página. Esta función recibe un puntero a una [**estructura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM11, eM12, eM21 y eM22 de XFORM especifican respectivamente, el coseno, el seno, el seno negativo y el coseno del ángulo de rotación.

Cuando *se* produce la rotación, los puntos que constituyen un objeto se giran con respecto al origen del espacio de coordenadas. En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades girado 30 grados cuando se copia del espacio de coordenadas universales al espacio de coordenadas de página.

![ilustración que muestra dos espacios de coordenadas; cada tiene un rectarín en una ubicación diferente y con una rotación diferente](images/cstrn-11.png)

En la ilustración anterior, cada punto del rectángulo se giraba 30 grados con respecto al origen del espacio de coordenadas.

El algoritmo siguiente calcula la nueva coordenada x (x ') para un punto (x,y) que se gira mediante el ángulo A con respecto al origen del espacio de coordenadas.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

El algoritmo siguiente calcula la coordenada y (y ') para un punto (x,y) que gira el ángulo A con respecto al origen.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

Las dos transformaciones de rotación se pueden combinar en una matriz 2 por 2 como se muestra a continuación.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

La matriz 2 por 2 que produjo la rotación contiene los valores siguientes.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Derivación de algoritmos de rotación

Los algoritmos de rotación se basan en el teorema de adición de trigonometría que indica que la función trigonométrica de una suma de dos ángulos (A1 y A2) se puede expresar en términos de las funciones trigonométricas de los dos ángulos.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

En la ilustración siguiente se muestra un punto p girado en sentido contrario a las agujas del reloj a una nueva posición p'. Además, muestra dos triángulos formados por una línea dibujada desde el origen del espacio de coordenadas hasta cada punto y una línea dibujada desde cada punto a través del eje X.

![diagrama que muestra el origen, p y p', y dos triángulos](images/cstrn-12.png)

Mediante trigonometría, la coordenada x del punto p se puede obtener multiplicando la longitud de la hipotenusa h por el coseno de A1.

``` syntax
x = h * cos A1 
```

La coordenada y del punto p se puede obtener multiplicando la longitud de la hipotenusa h por el seno de A1.

``` syntax
y = h * sin A1 
```

Del mismo modo, la coordenada x del punto p' se puede obtener multiplicando la longitud de la hipotenusa h por el coseno de (A1 +A2).

``` syntax
x' = h * cos (A1 + A2) 
```

Por último, la coordenada y del punto p' se puede obtener multiplicando la longitud de la hipotenusa h por el seno de (A1 +A2).

``` syntax
y' = h * sin (A1 + A2) 
```

Con el teorema de suma, los algoritmos anteriores se convierten en los siguientes:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Los algoritmos de rotación para un punto determinado girado por ángulo A2 se pueden obtener sustituyendo x por cada aparición de (h cos A1) y sustituyendo y por cada aparición de \* (h \* sin A1).

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



