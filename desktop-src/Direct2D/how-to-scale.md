---
title: Cómo escalar un objeto
description: Muestra cómo escalar un objeto.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488078"
---
# <a name="how-to-scale-an-object"></a>Cómo escalar un objeto

En este tema se describe cómo escalar un objeto mediante la clase [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Para escalar un objeto significa que el objeto sea más grande o más pequeño. Puede llamar a uno de los dos métodos siguientes para escalar un objeto.

-   **Matrix3x2F:: Scale (D2D1 \_ size \_ F SCALEFACTOR, D2D1 \_ Point \_ 2F CenterPoint)**
-   **Matrix3x2F:: Scale (float scaleX, Float scaleY, D2D1 \_ Point \_ 2F CenterPoint)**

El primer método almacena *scaleX* y *scaleY* como un par ordenado de valores de punto flotante en la estructura de [**tamaño de D2D1 \_ \_ F**](/windows/desktop/Direct2D/d2d1-size-f) . El segundo método define *scaleX* y *scaleY* como parámetros individuales.

Independientemente del método que use, debe especificar los factores de *scaleX* y de *escalado* . El valor *scaleX* es el factor de escala en la dirección x. Por ejemplo, un valor de *scaleX* de 1,5 ajusta el objeto a 150 por ciento a lo largo del eje x. Del mismo modo, el valor de *escalado* es el factor de escala en la dirección y. Por ejemplo, un valor de *escalado* de 0,5 reduce la altura del objeto en un 50 por ciento a lo largo del eje y.

Para especificar un punto como centro de la operación de escalado, use el parámetro *CenterPoint* . De forma predeterminada, un objeto se centra en su origen (0,0).

En el ejemplo de código siguiente se crea una transformación de escala para aumentar el tamaño de un cuadrado al 130% de su tamaño original. El valor de *CenterPoint* se establece en la esquina superior izquierda del cuadrado original.


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



En la ilustración siguiente se muestra el efecto de aplicar la transformación de escala al cuadrado. El cuadrado original es un contorno punteado y el cuadrado en escala es un contorno sólido.

![Ilustración de tamaño cuadrado cambiado al 130% de su tamaño original](images/scale-ovw.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 