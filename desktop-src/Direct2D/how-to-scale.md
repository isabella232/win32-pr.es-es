---
title: Cómo escalar un objeto
description: Muestra cómo escalar un objeto.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d833ea44e4a38672729dd7647063e8ed9f8de3574d820a3db40d5a848064ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259155"
---
# <a name="how-to-scale-an-object"></a>Cómo escalar un objeto

En este tema se describe cómo escalar un objeto mediante la [**clase Matrix3x2F.**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) Escalar un objeto significa hacer que el objeto sea mayor o menor. Puede llamar a uno de los dos métodos siguientes para escalar un objeto.

-   **Matrix3x2F::Scale(D2D1 \_ SIZE \_ F scalefactor, D2D1 \_ POINT \_ 2F centerpoint)**
-   **Matrix3x2F::Scale(float scalex, float scaley, D2D1 \_ POINT \_ 2F centerpoint)**

El primer método almacena *scalex* y *scaley* como un par ordenado de valores de punto flotante en la [**estructura D2D1 \_ SIZE \_ F.**](/windows/desktop/Direct2D/d2d1-size-f) El segundo método define *scalex* y *scaley como* parámetros individuales.

Independientemente del método que use, debe especificar los factores *scalex* *y scaley.* El *valor de scalex* es el factor de escala en la dirección x. Por ejemplo, un *valor de scalex* de 1,5 ajusta el objeto al 150 por ciento a lo largo del eje X. Del mismo modo, *el valor de escala* es el factor de escala en la dirección y. Por ejemplo, un *valor de* escala de 0,5 reduce el alto del objeto en un 50 por ciento a lo largo del eje Y.

Para especificar un punto como centro de la operación de escalado, use el *parámetro centerpoint.* De forma predeterminada, un objeto se centra en su origen (0,0).

El código de ejemplo siguiente crea una transformación de escala para aumentar el tamaño de un cuadrado al 130 % de su tamaño original. El *punto central* se establece para que sea la esquina superior izquierda del cuadrado original.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



En la ilustración siguiente se muestra el efecto de aplicar la transformación de escala al cuadrado. El cuadrado original es un contorno de puntos y el cuadrado escalado es un contorno sólido.

![ilustración de cuadrado cambiado de tamaño al 130 % de su tamaño original](images/scale-ovw.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a las transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 