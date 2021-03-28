---
description: Algunas aplicaciones proporcionan características que distorsionan objetos dibujados en el área de cliente.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Sesgo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277853"
---
# <a name="shear"></a>Sesgo

Algunas aplicaciones proporcionan características que distorsionan objetos dibujados en el área de cliente. Las aplicaciones que usan funciones de recorte usan la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer los valores adecuados en la transformación espacio global en el espacio de página. Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM12 y eM21 de XFORM especifican las constantes de proporcionalidad horizontal y vertical, respectivamente.

Hay dos componentes de la *transformación de recorte*. El primero modifica las líneas verticales de un objeto; la segunda modifica las líneas horizontales. En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades distorsionado horizontalmente cuando se copia desde el espacio universal al espacio de la página.

![Ilustración en la que se muestra un rectángulo en el espacio del mundo y un trapeziod en el espacio de la página](images/cstrn-13.png)

Un recorte horizontal se puede representar mediante el siguiente algoritmo:

``` syntax
x' = x + (Sx * y) 
```

donde x es la coordenada x original, SX es la constante de proporcionalidad y x ' es el resultado de la transformación de recorte.

Un recorte vertical se puede representar mediante el siguiente algoritmo:

``` syntax
y' = y + (Sy * x) 
```

donde y es la coordenada y original, SY es la constante de proporcionalidad e y ' es el resultado de la transformación de recorte.

Las transformaciones de recorte horizontal y de recorte vertical se pueden combinar en una sola operación mediante una matriz de 2 por 2.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

La matriz de 2 por 2 que generó la cizalla contiene los siguientes valores:

``` syntax
|1    1| 
|0    1| 
```

 

 



