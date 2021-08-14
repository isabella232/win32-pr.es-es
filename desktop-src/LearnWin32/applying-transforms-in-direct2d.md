---
title: Aplicación de transformaciones en Direct2D
description: Aplicación de transformaciones en Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83cb9a7981ada944de07e362c2f568889a84a4f90f2171150fbab948ab3a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388529"
---
# <a name="applying-transforms-in-direct2d"></a>Aplicación de transformaciones en Direct2D

En Dibujo con [Direct2D,](drawing-with-direct2d.md)vimos que el método [**ID2D1RenderTarget::FillVelopse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dibuja una elipse alineada con los ejes x e y. Pero supongamos que quiere dibujar una elipse inclinada en un ángulo.

![imagen que muestra una elipse inclinada.](images/graphics16.png)

Mediante el uso de transformaciones, puede modificar una forma de las maneras siguientes.

-   Rotación alrededor de un punto.
-   Ajustar la escala.
-   Traducción (desplazamiento en dirección X o Y).
-   Sesgo (también conocido como *cizalla ).*

Una transformación es una operación matemática que asigna un conjunto de puntos a un nuevo conjunto de puntos. Por ejemplo, en el diagrama siguiente se muestra un triángulo girado alrededor del punto P3. Una vez aplicada la rotación, el punto P1 se asigna a P1', el punto P2 se asigna a P2' y el punto P3 se asigna a sí mismo.

![diagrama que muestra la rotación alrededor de un punto.](images/graphics17.png)

Las transformaciones se implementan mediante matrices. Sin embargo, no es necesario comprender las matemáticas de las matrices para poder usarlas. Si desea obtener más información sobre las [matemáticas, vea Apéndice: Transformaciones de matriz](appendix--matrix-transforms.md).

Para aplicar una transformación en Direct2D, llame al [**método ID2D1RenderTarget::SetTransform.**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) Este método toma una [**estructura D2D1 \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) que define la transformación. Puede inicializar esta estructura llamando a métodos en la [**clase D2D1::Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) Esta clase contiene métodos estáticos que devuelven una matriz para cada tipo de transformación:

-   [**Matrix3x2F::Rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F::Skew**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Por ejemplo, el código siguiente aplica una rotación de 20 grados alrededor del punto (100, 100).


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

La transformación se aplica a todas las operaciones de dibujo posteriores hasta que se llama de nuevo [**a SetTransform.**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) Para quitar la transformación actual, llame a **SetTransform** con la matriz de identidad. Para crear la matriz de identidades, llame a [**la función Matrix3x2F::Identity.**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix)


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Dibujar las manos del reloj

Vamos a poner transformaciones para usarlas mediante la conversión de nuestro programa circle en un reloj análogo. Para ello, se pueden agregar líneas para las manos.

![una captura de pantalla del programa de reloj analógico.](images/graphics18.png)

En lugar de calcular las coordenadas de las líneas, podemos calcular el ángulo y luego aplicar una transformación de rotación. El código siguiente muestra una función que dibuja una mano de reloj. El *parámetro fAngle* proporciona el ángulo de la mano, en grados.

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

Este código dibuja una línea vertical, empezando desde el centro de la cara del reloj y finalizando en el punto *de conexión.* La línea se gira alrededor del centro de la elipse aplicando una transformación de rotación. El punto central de la rotación es el centro de la elipse que forma la cara del reloj.

![diagrama que muestra la rotación de la mano del reloj.](images/graphics19.png)

El código siguiente muestra cómo se dibuja toda la cara del reloj.

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

Puede descargar el proyecto de Visual Studio completo del ejemplo [de reloj de Direct2D.](direct2d-clock-sample.md) (Solo por divertido, la versión de descarga agrega un gradiant radial a la cara del reloj).

## <a name="combining-transforms"></a>Combinar transformaciones

Las cuatro transformaciones básicas se pueden combinar multiplicando dos o más matrices. Por ejemplo, el código siguiente combina una rotación con una traducción.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

La [**clase Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) proporciona [**el operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para la multiplicación de matrices. El orden en el que se multiplican las matrices es importante. Establecer una transformación (M × N) significa "Aplicar M primero, seguido de N". Por ejemplo, este es el giro seguido de la traducción:

![diagrama que muestra la rotación seguida de la traducción.](images/graphics20.png)

Este es el código de esta transformación:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Ahora compare esa transformación con una transformación en el orden inverso, la traducción seguida de la rotación.

![diagrama que muestra la traducción seguida de la rotación.](images/graphics21.png)

La rotación se realiza alrededor del centro del rectángulo original. Este es el código de esta transformación.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Como puede ver, las matrices son las mismas, pero el orden de las operaciones ha cambiado. Esto sucede porque la multiplicación de matrices no es conmutativa: M × N ≠ N × M.

## <a name="next"></a>Siguientes

[Apéndice: Transformaciones de matriz](appendix--matrix-transforms.md)