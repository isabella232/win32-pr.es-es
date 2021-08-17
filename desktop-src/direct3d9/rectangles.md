---
description: A lo largo de la programación de Direct3D y Window, se hace referencia a los objetos de la pantalla en términos de rectángulos delimitadores.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rectángulos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02dda6e8a4f10128ab11ffeb8b390e79be7cc0f698ed1625ca3f2c5df995d67e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119368884"
---
# <a name="rectangles-direct3d-9"></a>Rectángulos (Direct3D 9)

A lo largo de la programación de Direct3D y Window, se hace referencia a los objetos de la pantalla en términos de rectángulos delimitadores. Los lados de un rectángulo delimitador siempre son paralelos a los lados de la pantalla, por lo que el rectángulo se puede describir mediante dos puntos, la esquina superior izquierda y la esquina inferior derecha. La mayoría de las aplicaciones usan la [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para llevar información sobre un rectángulo delimitador que se usará al eliminar la pantalla o realizar la detección de impactos.

En C++, la [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) tiene la definición siguiente.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



En el ejemplo anterior, los miembros izquierdo y superior son las coordenadas x e y de la esquina superior izquierda de un rectángulo delimitador. De forma similar, los miembros derecho e inferior son las coordenadas de la esquina inferior derecha. En la ilustración siguiente se muestra cómo puede visualizar estos valores.

![ilustración del rectángulo delimitado por los valores izquierdo, superior, derecho e inferior](images/rect.png)

La columna de píxeles en el borde derecho y la fila de píxeles en el borde inferior no se incluyen en el RECT. Por ejemplo, bloquear un RECT con miembros {10, 10, 138, 138} da como resultado un objeto de 128 píxeles de ancho y alto.

En a favor de la eficacia, la coherencia y la facilidad de uso, todas las funciones de presentación de Direct3D funcionan con rectángulos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistemas de coordenadas y geometría](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
