---
title: Cómo aplicar varias transformaciones a un objeto
description: Muestra cómo aplicar varias transformaciones a un objeto .
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d63db7899b79dd07a6a4a14a4efbbfaeefc5723ad09c71a3462ba5d2fd0c042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259695"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Cómo aplicar varias transformaciones a un objeto

Realizar varias transformaciones en un objeto significa combinar varias transformaciones en una. Es decir, tomar la salida de cada matriz de transformación y usarlo como entrada para la siguiente, obteniendo así los efectos acumulativos de todas las transformaciones de matriz.

Supongamos que dos matrices de transformación, rotación y traducción, se multiplican juntas. El resultado es una nueva matriz que realiza las funciones de rotación y traducción. Dado que la multiplicación de matrices no es conmutativa, una transformación de rotación multiplicada por una transformación de traducción es diferente de la transformación de traducción multiplicada por la transformación de rotación.

En los ejemplos de código siguientes se muestra cómo aplicar la rotación seguida de la traducción y, a continuación, la traducción seguida de la rotación. Observe que los resultados de la representación son diferentes.


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



El código genera la salida que se muestra en la ilustración siguiente.

![ilustración de un rectángulo que se ha traducido y luego girado y un rectángulo que se ha girado y, a continuación, se ha traducido](images/multipletransforms.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> <dt>

[Introducción a las transformaciones de Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 




