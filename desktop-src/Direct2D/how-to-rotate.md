---
title: Cómo girar un objeto
description: Muestra cómo girar un objeto.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995452"
---
# <a name="how-to-rotate-an-object"></a>Cómo girar un objeto

En este tema se describe cómo girar un objeto sobre un punto especificado. Para girar un objeto, llame al método [**Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) . Este método toma dos parámetros, el ángulo especificado y el punto central. El ángulo es un ángulo de rotación en el sentido de las agujas del reloj, en grados, y el punto central es el punto sobre el que gira el objeto. El punto central se expresa en el sistema de coordenadas del objeto que se transforma.

Por ejemplo, en el código siguiente se gira un cuadrado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



En la ilustración siguiente se muestra el efecto de aplicar la transformación rotación anterior al cuadrado. El cuadrado original es un contorno punteado y el cuadrado girado es un contorno sólido.

![Ilustración de un cuadrado girado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado original](images/rotate-ovw.png)

En la ilustración siguiente se muestra el efecto de girar en el mismo ángulo sobre un punto central diferente. Observe que los objetos girados se encuentran en posiciones diferentes en relación con el original. El cuadrado de la izquierda es el resultado de girar sobre el centro del cuadrado original y el cuadrado de la derecha es el resultado de girar sobre la esquina superior izquierda del cuadrado original.

![Ilustración de un cuadrado girado en el sentido de las agujas del reloj 45 grados sobre un punto central diferente](images/translate-rotationcompare.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> <dt>

[Información general sobre transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 