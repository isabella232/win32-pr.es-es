---
description: Para dibujar un rectángulo sombreado, defina una matriz de trivértices con dos elementos y una única estructura de rectángulo de DEGRADAdo \_ . En el ejemplo de código siguiente se muestra cómo dibujar un rectángulo sombreado mediante la función GradientFill con el modo de rectángulo de relleno DEGRADAdo \_ \_ definido.
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: Dibujar un rectángulo sombreado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544507"
---
# <a name="drawing-a-shaded-rectangle"></a>Dibujar un rectángulo sombreado

Para dibujar un rectángulo sombreado, defina una matriz de [**TRIvértices**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) con dos elementos y una única estructura de [**\_ rectángulo de degradado**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) . En el ejemplo de código siguiente se muestra cómo dibujar un rectángulo sombreado mediante la función [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) con el modo de rectángulo de relleno degradado \_ \_ definido.


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



En la imagen siguiente se muestra el resultado del dibujo del ejemplo de código anterior.

![Ilustración en la que se muestra un rectángulo con un relleno de degradado de oscuro en el lado izquierdo para iluminar en el lado derecho](images/gradientfillrectangle.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre mapas de bits](bitmaps.md)
</dt> <dt>

[Funciones de mapa de bits](bitmap-functions.md)
</dt> <dt>

[Dibujo de un triángulo sombreado](drawing-a-shaded-triangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**rectángulo de DEGRADAdo \_**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**Trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



