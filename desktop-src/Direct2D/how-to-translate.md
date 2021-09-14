---
title: Cómo traducir un objeto
description: Muestra cómo traducir un objeto.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163130"
---
# <a name="how-to-translate-an-object"></a>Cómo traducir un objeto

Traducir un objeto 2D es mover el objeto a lo largo del eje X, el eje Y o ambos. Puede llamar a cualquiera de los dos métodos siguientes para crear una transformación de traducción.

-   [**Translation(D2D1 \_ SIZE \_ F size):**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))toma un par ordenado que define la distancia que se va a traducir a lo largo del eje X y el eje Y.
-   [**Translation(float x, float y):**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float))toma la distancia que se va a traducir a lo largo del eje X y la distancia que se va a traducir a lo largo del eje Y.

El código siguiente crea una matriz de transformación de traducción que mueve las 20 unidades cuadradas a la derecha a lo largo del eje X y 10 unidades hacia abajo a lo largo del eje Y.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



En la ilustración siguiente se muestra el efecto de aplicar la transformación de traducción al cuadrado, donde el cuadrado original es un contorno de puntos y el cuadrado traducido es un contorno sólido.

![ilustración de un cuadrado movido 20 unidades a la derecha a lo largo del eje X y 10 unidades hacia abajo a lo largo del eje Y](images/translation-ovw.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> <dt>

[Introducción a las transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 