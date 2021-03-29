---
title: Aplicación de transformaciones en Direct2D
description: Aplicación de transformaciones en Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791655"
---
# <a name="applying-transforms-in-direct2d"></a>Aplicación de transformaciones en Direct2D

En el [dibujo con Direct2D](drawing-with-direct2d.md), vimos que el método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dibuja una elipse que se alinea con los ejes x e y. Pero supongamos que desea dibujar una elipse inclinada en un ángulo.

![imagen que muestra una elipse inclinada.](images/graphics16.png)

Mediante el uso de transformaciones, puede modificar una forma de las siguientes maneras.

-   Giro alrededor de un punto.
-   Ajustar la escala.
-   Translation (desplazamiento en la dirección X o Y).
-   Sesgado (también conocido como *recorte*).

Una transformación es una operación matemática que asigna un conjunto de puntos a un nuevo conjunto de puntos. Por ejemplo, en el diagrama siguiente se muestra un triángulo girado alrededor del punto P3. Una vez aplicado el giro, el punto P1 se asigna a P1 ', el punto P2 se asigna a P2 ' y el punto P3 se asigna a sí mismo.

![diagrama que muestra la rotación alrededor de un punto.](images/graphics17.png)

Las transformaciones se implementan mediante matrices. Sin embargo, no es necesario comprender las matemáticas de las matrices para poder utilizarlas. Si desea obtener más información sobre las matemáticas, consulte [Apéndice: transformaciones de matriz](appendix--matrix-transforms.md).

Para aplicar una transformación en Direct2D, llame al método [**ID2D1RenderTarget:: SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Este método toma una estructura [**D2D1 de \_ matriz \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) que define la transformación. Puede inicializar esta estructura llamando a métodos en la clase [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Esta clase contiene métodos estáticos que devuelven una matriz para cada tipo de transformación:

-   [**Matrix3x2F:: Rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F:: scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F:: Skew**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Por ejemplo, el código siguiente aplica una rotación de 20 grados alrededor del punto (100, 100).


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

La transformación se aplica a todas las operaciones de dibujo posteriores hasta que vuelva a llamar a [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Para quitar la transformación actual, llame a **SetTransform** con la matriz de identidad. Para crear la matriz de identidad, llame a la función [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Mano del reloj de dibujo

Vamos a colocar las transformaciones para usarlas convirtiendo el programa de círculo en un reloj analógico. Podemos hacer esto agregando líneas para las manos.

![captura de pantalla del programa de reloj analógico.](images/graphics18.png)

En lugar de calcular las coordenadas de las líneas, podemos calcular el ángulo y luego aplicar una transformación de giro. En el código siguiente se muestra una función que dibuja una mano del reloj. El parámetro *fAngle* proporciona el ángulo de la mano, en grados.

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

Este código dibuja una línea vertical, empezando desde el centro de la esfera del reloj hasta el punto de *conexión* del punto. La línea se gira alrededor del centro de la elipse aplicando una transformación de giro. El punto central de la rotación es el centro de la elipse que forma la esfera del reloj.

![diagrama que muestra el giro de la mano del reloj.](images/graphics19.png)

En el código siguiente se muestra cómo se dibuja toda la esfera del reloj.

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

Puede descargar el proyecto de Visual Studio completo desde el [ejemplo de reloj de Direct2D](direct2d-clock-sample.md). (Solo para diversión, la versión de descarga agrega un Gradiant radial a la esfera del reloj).

## <a name="combining-transforms"></a>Combinar transformaciones

Las cuatro transformaciones básicas se pueden combinar multiplicando dos o más matrices. Por ejemplo, el código siguiente combina una rotación con una traducción.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

La clase [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) proporciona el [**operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para la multiplicación de matrices. Es importante el orden en el que se multiplican las matrices. Establecer una transformación (M × N) significa "aplicar M primero, seguido de N". Por ejemplo, este es el giro seguido de la traducción:

![diagrama que muestra el giro seguido de la traslación.](images/graphics20.png)

Este es el código de esta transformación:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Ahora Compare la transformación con una transformación en el orden inverso, la traducción seguida de la rotación.

![diagrama que muestra la traslación seguido de la rotación.](images/graphics21.png)

La rotación se realiza alrededor del centro del rectángulo original. Este es el código de esta transformación.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Como puede ver, las matrices son las mismas, pero el orden de las operaciones ha cambiado. Esto sucede porque la multiplicación de matrices no es conmutativa: M × N ≠ N × M.

## <a name="next"></a>Siguientes

[Apéndice: transformaciones de matriz](appendix--matrix-transforms.md)