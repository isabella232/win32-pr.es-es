---
description: La mayoría de las aplicaciones de CAD y de dibujo proporcionan características que escalan la salida creada por el usuario.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Ampliación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985811"
---
# <a name="scaling"></a>Ampliación

La mayoría de las aplicaciones de CAD y de dibujo proporcionan características que escalan la salida creada por el usuario. Las aplicaciones que incluyen funcionalidades de escalado (o zoom) llaman a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer la transformación espacio universal adecuado en el espacio de la página. Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM11 y eM22 de XFORM especifican los componentes de escalado horizontal y vertical, respectivamente.

Cuando se produce el *escalado* , las líneas verticales y horizontales (o vectores) que constituyen un objeto se ajustan o se comprimen con respecto al eje x o y. En la ilustración siguiente se muestra un rectángulo de una unidad de 20 por 20 escalada verticalmente al doble de su altura original cuando se copia del espacio de coordenadas universal en el espacio de coordenadas de la página.

![Ilustración en la que se muestra un pequeño rectángulo en el espacio del mundo y otro más alto en el espacio de la página](images/cstrn-10.png)

En la ilustración anterior, las líneas verticales que definen la medida lateral del rectángulo original 20 unidades, mientras que las líneas verticales que definen los lados del rectángulo escalado miden 40 unidades.

El escalado vertical puede representarse mediante el siguiente algoritmo.

``` syntax
y' = y * Dy 
```

Donde y ' es la nueva longitud, y es la longitud original y DY es el factor de escala vertical.

El escalado horizontal se puede representar mediante el siguiente algoritmo.

``` syntax
x' = x * Dx 
```

Donde x es la nueva longitud, x es la longitud original y DX es el factor de escala horizontal.

Las transformaciones de escalado vertical y horizontal se pueden combinar en una sola operación mediante una matriz de 2 por 2.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

La matriz de 2 por 2 que generó la transformación de escala contiene los siguientes valores.

``` syntax
|1    0| 
|0    2| 
```

 

 



