---
description: Algunas aplicaciones traducen (o desplazan) objetos dibujados en el área de cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987703"
---
# <a name="translation"></a>Traducción

Algunas aplicaciones traducen (o desplazan) objetos dibujados en el área de cliente. llamando a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer el espacio universal adecuado en la transformación de espacio en la página. La función SetWorldTransform recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eDx y eDy de XFORM especifican los componentes de traslación horizontal y vertical, respectivamente.

Cuando se produce la *conversión* , cada punto de un objeto se desplaza verticalmente, horizontalmente o ambos en una cantidad especificada. En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades que se ha traducido a la derecha 10 unidades cuando se copia del espacio de coordenadas universal en el espacio de coordenadas de la página.

![Ilustración que muestra un rectángulo en una posición en el espacio del mundo y en una posición diferente en el espacio de la página](images/cstrn-09.png)

En la ilustración anterior, la coordenada x de cada punto del rectángulo es de 10 unidades mayor que la coordenada x original.

La traducción horizontal se puede representar mediante el siguiente algoritmo.

``` syntax
x' = x + Dx 
```

Donde x es la nueva coordenada x, x es la coordenada x original y DX es la distancia horizontal movida.

La traducción vertical se puede representar mediante el siguiente algoritmo.

``` syntax
y' = y + Dy 
```

Donde y ' es la nueva coordenada y, y es la coordenada y original, y DY es la distancia vertical movida.

Las transformaciones de traslación horizontal y vertical se pueden combinar en una sola operación mediante una matriz de 3 por 3.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(Las reglas del estado de multiplicación de matrices que indica que el número de filas de una matriz debe ser igual al número de columnas del otro. El entero 1 de la matriz \| x y 1 \| es un marcador de posición que se agregó para cumplir este requisito.)

La matriz de 3 por 3 que generó la transformación de traducción ilustrada contiene los siguientes valores.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



