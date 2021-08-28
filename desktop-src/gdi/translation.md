---
description: Algunas aplicaciones traducen (o desplazan) objetos dibujados en el área de cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115af82d1e5b80fa4c50d081e6d042d2f2c9c8950f3b4b8f6ed09108df4c52bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613345"
---
# <a name="translation"></a>Traducción

Algunas aplicaciones traducen (o desplazan) objetos dibujados en el área de cliente. llamando a la [**función SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer la transformación espacio del mundo en espacio de página adecuada. La función SetWorldTransform recibe un puntero a una [**estructura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eDx y eDy de XFORM especifican los componentes de traducción horizontal y vertical, respectivamente.

Cuando *se* produce la traducción, cada punto de un objeto se desplaza vertical, horizontalmente o ambos, por una cantidad especificada. En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades que se ha traducido a la derecha en 10 unidades cuando se copia del espacio de coordenadas universales al espacio de coordenadas de página.

![ilustración que muestra un rectángulo en una posición del espacio del mundo y en una posición diferente en el espacio de página](images/cstrn-09.png)

En la ilustración anterior, la coordenada x de cada punto del rectángulo es 10 unidades mayor que la coordenada X original.

La traducción horizontal se puede representar mediante el algoritmo siguiente.

``` syntax
x' = x + Dx 
```

Donde x' es la nueva coordenada x, x es la coordenada X original y Dx es la distancia horizontal movida.

La traducción vertical se puede representar mediante el algoritmo siguiente.

``` syntax
y' = y + Dy 
```

Donde y' es la nueva coordenada Y, y es la coordenada Y original y Dy es la distancia vertical movida.

Las transformaciones de traducción horizontal y vertical se pueden combinar en una sola operación mediante una matriz 3 por 3.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(Las reglas de multiplicación de matrices muestran que el número de filas de una matriz debe ser igual al número de columnas de la otra. El entero 1 de la matriz x y 1 es un marcador de \| \| posición que se agregó para cumplir este requisito).

La matriz 3 por 3 que produjo la transformación de traducción ilustrada contiene los valores siguientes.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



