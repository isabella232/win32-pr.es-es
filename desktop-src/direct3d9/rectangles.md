---
description: En Direct3D y en la programación de ventanas, se hace referencia a los objetos de la pantalla en términos de rectángulos delimitadores.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rectángulos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151974"
---
# <a name="rectangles-direct3d-9"></a>Rectángulos (Direct3D 9)

En Direct3D y en la programación de ventanas, se hace referencia a los objetos de la pantalla en términos de rectángulos delimitadores. Los lados de un rectángulo delimitador siempre son paralelos a los lados de la pantalla, por lo que el rectángulo puede describirse mediante dos puntos, la esquina superior izquierda y la esquina inferior derecha. La mayoría de las aplicaciones usan la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para llevar información sobre un rectángulo delimitador que se usará al blitting a la pantalla o al realizar la detección de aciertos.

En C++, la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) tiene la siguiente definición.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



En el ejemplo anterior, los miembros izquierdo y superior son las coordenadas x e y de la esquina superior izquierda de un rectángulo delimitador. Del mismo modo, los miembros derecho e inferior forman las coordenadas de la esquina inferior derecha. En la ilustración siguiente se muestra cómo puede visualizar estos valores.

![Ilustración del rectángulo delimitado por los valores izquierdo, superior, derecho e inferior](images/rect.png)

La columna de píxeles en el borde derecho y la fila de píxeles en el borde inferior no se incluyen en el rectángulo. Por ejemplo, si se bloquea un RECT con miembros {10, 10, 138, 138}, se obtiene un objeto de 128 píxeles de ancho y alto.

En aras de la eficacia, la coherencia y la facilidad de uso, todas las funciones de presentación de Direct3D funcionan con los rectángulos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
