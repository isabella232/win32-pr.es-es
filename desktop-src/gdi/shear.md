---
description: Algunas aplicaciones proporcionan características que cortan objetos dibujados en el área de cliente.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Esquileo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072447"
---
# <a name="shear"></a>Esquileo

Algunas aplicaciones proporcionan características que cortan objetos dibujados en el área de cliente. Las aplicaciones que usan funcionalidades de cizallación usan la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer los valores adecuados en la transformación espacio del mundo en espacio de página. Esta función recibe un puntero a una [**estructura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados. Los miembros eM12 y eM21 de XFORM especifican las constantes de proporcionalidad horizontal y vertical, respectivamente.

Hay dos componentes de la transformación *de cizalla.* La primera modifica las líneas verticales de un objeto ; el segundo modifica las líneas horizontales. En la ilustración siguiente se muestra un rectángulo de 20 por 20 unidades que se corta horizontalmente cuando se copia del espacio del mundo al espacio de página.

![ilustración que muestra un rectángulo en el espacio del mundo y un trapecio en el espacio de página](images/cstrn-13.png)

Una cizalla horizontal se puede representar mediante el algoritmo siguiente:

``` syntax
x' = x + (Sx * y) 
```

donde x es la coordenada X original, Sx es la constante de proporcionalidad y x' es el resultado de la transformación de cizalla.

Una cizalla vertical se puede representar mediante el algoritmo siguiente:

``` syntax
y' = y + (Sy * x) 
```

donde y es la coordenada y original, Sy es la constante de proporcionalidad e y' es el resultado de la transformación de cizalla.

Las transformaciones de cizalla horizontal y vertical se pueden combinar en una sola operación mediante una matriz 2 por 2.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

La matriz 2 por 2 que produjo la cizalla contiene los valores siguientes:

``` syntax
|1    1| 
|0    1| 
```

 

 



