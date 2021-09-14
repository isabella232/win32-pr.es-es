---
title: Cómo sesgar un objeto
description: Muestra cómo sesgar un objeto.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163137"
---
# <a name="how-to-skew-an-object"></a>Cómo sesgar un objeto

Para sesgar (o sesgar) un objeto significa distorsionar un objeto mediante un ángulo especificado desde el eje X, el eje Y o ambos. Por ejemplo, al sesgar un cuadrado, se convierte en un paralelogramo.

El [**método Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) toma 3 parámetros:

-   *angleX:* ángulo de sesgo del eje X, que se mide en grados en sentido contrario a las agujas del reloj desde el eje Y.
-   *angleY:* ángulo de sesgo del eje Y, que se mide en grados en el sentido de las agujas del reloj desde el eje X.
-   *centerPoint:* punto sobre el que se realiza el sesgo.

Para predecir el efecto de una transformación de sesgo, tenga en cuenta que *angleX* es el ángulo de sesgo medido en grados en sentido contrario a las agujas del reloj desde el eje Y. Por ejemplo, si *angleX* se establece en 30, el objeto sesga 30 grados en sentido contrario a las agujas del reloj a lo largo del eje y sobre *el centerPoint*. En la ilustración siguiente se muestra un cuadrado sesgado horizontalmente 30 grados sobre la esquina superior izquierda del cuadrado.

![ilustración de un cuadrado sesgado 30 grados en sentido contrario a las agujas del reloj desde el eje Y](images/skewx.png)

De forma similar, *angleY es* un ángulo de sesgo medido en grados en el sentido de las agujas del reloj desde el eje X. Por ejemplo, si *angleY* se establece en 30, el objeto sesga 30 grados en el sentido de las agujas del reloj a lo largo del eje X sobre *centerPoint*. En la ilustración siguiente se muestra un cuadrado sesgado verticalmente 30 grados sobre la esquina superior izquierda del cuadrado.

![ilustración de un cuadrado sesgado a 30 grados en el sentido de las agujas del reloj desde el eje X](images/skewy.png)

Si establece *angleX* y *angleY* en 30 grados y *centerPoint* en la esquina superior izquierda del cuadrado, verá el siguiente cuadrado sesgado (con contorno sólido). Observe que el cuadrado sesgado está sesgado 30 grados en sentido contrario a las agujas del reloj desde el eje Y y 30 grados en el sentido de las agujas del reloj desde el eje X.

![ilustración de un cuadrado sesgado a 30 grados en sentido contrario a las agujas del reloj desde el eje Y y 30 grados en el sentido de las agujas del reloj desde el eje X](images/skewxy.png)

El ejemplo de código siguiente sesga el cuadrado 45 grados horizontalmente sobre la esquina superior izquierda del cuadrado.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



En la ilustración siguiente se muestra el efecto de aplicar la transformación de sesgo al cuadrado, donde el cuadrado original es un contorno de puntos y el objeto sesgado (paralelogramo) es un contorno sólido. Observe que el ángulo de sesgo es de 45 grados en sentido contrario a las agujas del reloj desde el eje Y.

![ilustración de un cuadrado sesgado 45 grados en sentido contrario a las agujas del reloj desde el eje Y](images/skew-ovw.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a las transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 