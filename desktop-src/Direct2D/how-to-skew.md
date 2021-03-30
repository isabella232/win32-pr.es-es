---
title: Cómo sesgar un objeto
description: Muestra cómo sesgar un objeto.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904757"
---
# <a name="how-to-skew-an-object"></a>Cómo sesgar un objeto

Para sesgar (o distorsionar) un objeto significa distorsionar un objeto en un ángulo especificado desde el eje x, el eje y o ambos. Por ejemplo, al sesgar un cuadrado, se convierte en un paralelogramo.

El método [**Matrix3x2F:: Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) toma 3 parámetros:

-   *angleX*: ángulo de sesgado del eje x, que se mide en grados en sentido contrario a las agujas del reloj desde el eje y.
-   *ánguloy*: el ángulo de sesgado del eje y, que se mide en grados en el sentido de las agujas del reloj desde el eje x.
-   *centerPoint*: el punto sobre el que se realiza el sesgo.

Para predecir el efecto de una transformación de sesgo, tenga en cuenta que *angleX* es el ángulo de sesgo medido en grados en sentido contrario a las agujas del reloj desde el eje y. Por ejemplo, si *angleX* se establece en 30, el objeto sesga 30 grados en sentido contrario a las agujas del reloj a lo largo del eje y sobre *centerPoint*. En la ilustración siguiente se muestra un cuadrado sesgado horizontalmente 30 grados sobre la esquina superior izquierda del cuadrado.

![Ilustración de un cuadrado sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y](images/skewx.png)

Del mismo modo, el *ángulo* es un ángulo de sesgo medido en grados en el sentido de las agujas del reloj desde el eje x. Por ejemplo, si el *ángulo* está establecido en 30, el objeto sesga 30 grados en el sentido de las agujas del reloj a lo largo del eje x sobre el *centerPoint*. En la ilustración siguiente se muestra un cuadrado sesgado en vertical 30 grados sobre la esquina superior izquierda del cuadrado.

![Ilustración de un cuadrado sesgado de 30 grados en el sentido de las agujas del reloj desde el eje x](images/skewy.png)

Si establece tanto *angleX* como *angular* en 30 grados y el *centerPoint* en la esquina superior izquierda del cuadrado, verá el cuadrado sesgado siguiente (con un contorno sólido). Observe que el cuadrado sesgado está sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y y 30 grados en el sentido de las agujas del reloj desde el eje x.

![Ilustración de un cuadrado sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y y 30 grados en el sentido de las agujas del reloj desde el eje x](images/skewxy.png)

En el ejemplo de código siguiente se sesga el cuadrado 45 grados horizontalmente sobre la esquina superior izquierda del cuadrado.


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



En la ilustración siguiente se muestra el efecto de aplicar la transformación sesgado al cuadrado, donde el cuadrado original es un contorno punteado y el objeto sesgado (paralelogramo) es un contorno sólido. Observe que el ángulo de sesgo es de 45 grados en sentido contrario a las agujas del reloj desde el eje y.

![Ilustración de un cuadrado sesgado de 45 grados en sentido contrario a las agujas del reloj desde el eje y](images/skew-ovw.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 