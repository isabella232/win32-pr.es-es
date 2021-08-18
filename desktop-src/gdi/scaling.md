---
description: La mayoría de las aplicaciones de dibujo y CAD proporcionan características que escalan la salida creada por el usuario.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Ampliación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf8cb7293be4083c08de1d104bb8349b3cd5003a0abddf77d41922cfb294cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965245"
---
# <a name="scaling"></a>Ampliación

La mayoría de las aplicaciones de dibujo y CAD proporcionan características que escalan la salida creada por el usuario. Las aplicaciones que incluyen funcionalidades de escalado (o zoom) llaman a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer la transformación espacio del mundo adecuada en espacio de página. Esta función recibe un puntero a una [**estructura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM11 y eM22 de XFORM especifican los componentes de escalado horizontal y vertical, respectivamente.

Cuando *se* produce el escalado, las líneas verticales y horizontales (o vectores), que constituyen un objeto, se extienden o comprimen con respecto al eje x o y. En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades escalado verticalmente al doble de su altura original cuando se copia del espacio de coordenadas universales al espacio de coordenadas de página.

![ilustración que muestra un rectángulo pequeño en el espacio del mundo y uno más alto en el espacio de página](images/cstrn-10.png)

En la ilustración anterior, las líneas verticales que definen el lado del rectángulo original miden 20 unidades, mientras que las líneas verticales que definen los lados del rectángulo escalado miden 40 unidades.

El escalado vertical se puede representar mediante el algoritmo siguiente.

``` syntax
y' = y * Dy 
```

Donde y' es la nueva longitud, y es la longitud original y Dy es el factor de escalado vertical.

El escalado horizontal se puede representar mediante el algoritmo siguiente.

``` syntax
x' = x * Dx 
```

Donde x' es la nueva longitud, x es la longitud original y Dx es el factor de escalado horizontal.

Las transformaciones de escalado vertical y horizontal se pueden combinar en una sola operación mediante una matriz de 2 por 2.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

La matriz 2 por 2 que produjo la transformación de escalado contiene los valores siguientes.

``` syntax
|1    0| 
|0    2| 
```

 

 



