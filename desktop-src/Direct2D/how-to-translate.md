---
title: Cómo trasladar un objeto
description: Muestra cómo trasladar un objeto.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359291"
---
# <a name="how-to-translate-an-object"></a>Cómo trasladar un objeto

Para traducir un objeto 2D, mueva el objeto a lo largo del eje x, el eje y o ambos. Puede llamar a uno de los dos métodos siguientes para crear una transformación de traslación.

-   [**Translation (D2D1 \_ tamaño \_ F tamaño)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): toma un par ordenado que define la distancia que se va a trasladar a lo largo del eje x y el eje y.
-   [**Translation (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): toma la distancia de la traslación a lo largo del eje x y la distancia que se va a trasladar a lo largo del eje y.

El código siguiente crea una matriz de transformación de traslación que mueve las 20 unidades cuadradas a la derecha a lo largo del eje x y 10 unidades hacia abajo a lo largo del eje y.


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



En la ilustración siguiente se muestra el efecto de aplicar la transformación traslación al cuadrado, donde el cuadrado original es un contorno punteado y el cuadrado traducido es un contorno sólido.

![la ilustración de un cuadrado ha desplazado 20 unidades a la derecha a lo largo del eje x y 10 unidades hacia abajo a lo largo del eje y.](images/translation-ovw.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> <dt>

[Información general sobre transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 