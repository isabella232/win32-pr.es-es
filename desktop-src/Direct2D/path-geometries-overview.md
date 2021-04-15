---
title: Información general sobre las geometrías de ruta
description: Describe cómo usar las geometrías de ruta de acceso para definir formas complejas.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550231"
---
# <a name="path-geometries-overview"></a>Información general sobre las geometrías de ruta

En este tema se describe cómo usar las geometrías de ruta de acceso de Direct2D para crear dibujos complejos. Contiene las siguientes secciones:

-   [Requisitos previos](#prerequisites)
-   [Geometrías de ruta de acceso en Direct2D](#path-geometries-in-direct2d)
-   [Usar un ID2D1GeometrySink para rellenar una geometría de trazado](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Ejemplo: crear un dibujo complejo](#example-create-a-complex-drawing)
    -   [Crear una geometría de trazado para la montaña izquierda](#create-a-path-geometry-for-the-left-mountain)
    -   [Crear una geometría de trazado para la montaña derecha](#create-a-path-geometry-for-the-right-mountain)
    -   [Crear una geometría de trazado para el sol](#create-a-path-geometry-for-the-sun)
    -   [Crear una geometría de trazado para el río](#create-a-path-geometry-for-the-river)
    -   [Representar las geometrías de trazado en la pantalla](#render-the-path-geometries-onto-the-display)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

En esta información general se supone que está familiarizado con la creación de aplicaciones básicas de Direct2D, tal como se describe en [creación de una aplicación sencilla de direct2d](direct2d-quickstart.md). También se supone que está familiarizado con las características básicas de las geometrías de Direct2D, tal como se describe en la [información general sobre las geometrías](direct2d-geometries-overview.md).

## <a name="path-geometries-in-direct2d"></a>Geometrías de ruta de acceso en Direct2D

La interfaz [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) representa las geometrías de ruta de acceso. Para crear una instancia de la geometría de una ruta de acceso, llame al método [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) . Estos objetos se pueden usar para describir figuras geométricas complejas que se componen de segmentos como arcos, curvas y líneas. Para rellenar una geometría de trazado con figuras y segmentos, llame al método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para recuperar un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) y use los métodos del receptor de Geometry para agregar figuras y segmentos a la geometría del trazado.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Usar un ID2D1GeometrySink para rellenar una geometría de trazado

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describe un trazado geométrico que puede contener líneas, arcos, curvas Bézier cúbicas y curvas Bézier cuadráticas.

Un receptor de geometría se compone de una o más figuras. Cada ilustración se compone de uno o varios segmentos de línea, curva o arco. Para crear una figura, llame al método [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , pase el punto inicial de la figura y, a continuación, use sus métodos Add (como [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) y [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para agregar segmentos). Cuando haya terminado de agregar segmentos, llame al método [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) . Puede repetir esta secuencia para crear más figuras. Cuando haya terminado de crear las figuras, llame al método [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .

## <a name="example-create-a-complex-drawing"></a>Ejemplo: crear un dibujo complejo

En la ilustración siguiente se muestra un dibujo complejo con líneas, arcos y curvas Bézier. En el ejemplo de código siguiente se muestra cómo crear el dibujo usando cuatro objetos de geometría de trazado, uno para la montaña izquierda, otro para la montaña derecha, uno para el río y otro para el sol con destellos.

![Ilustración de un río, montañas y el sol mediante el uso de geometrías de trazado](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Crear una geometría de trazado para la montaña izquierda

En el ejemplo se crea primero una geometría de trazado para la montaña izquierda, tal como se muestra en la siguiente ilustración.

![Muestra un dibujo complejo de un polígono que muestra una montaña.](images/path-geo-leftmnt.png)

Para crear la montaña izquierda, el ejemplo llama al método [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para crear un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



A continuación, el ejemplo usa el método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para obtener un receptor de geometría de un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y lo almacena en la variable *pSink* .


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



A continuación, en el ejemplo se llama a [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), pasando [**D2D1 \_ figura \_ Begin \_ rellenada**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) que indica que esta figura se ha rellenado y, a continuación, llama a [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), pasando una matriz de [**D2D1 \_ Point \_ 2F**](d2d1-point-2f.md) Points, (267, 177), (236, 192), (212, 160), (156, 255) y (346, 255).

El código siguiente muestra cómo hacerlo.


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Crear una geometría de trazado para la montaña derecha

A continuación, en el ejemplo se crea otra geometría de ruta de acceso para la montaña derecha con puntos (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) y (575, 263). En la ilustración siguiente se muestra cómo se muestra la montaña derecha.

![Ilustración de un polígono que muestra una montaña](images/path-geo-rightmnt.png)

El código siguiente muestra cómo hacerlo.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a>Crear una geometría de trazado para el sol

A continuación, en el ejemplo se rellena otra geometría de ruta de acceso para el sol, tal como se muestra en la siguiente ilustración.

![Ilustración de curvas de arco y Bézier que muestran el sol](images/path-geo-sun.png)

Para ello, la geometría de trazado crea un receptor y agrega una figura para el arco y una figura para cada destello al receptor. Al repetir la secuencia de [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), sus métodos Add (como [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) y [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), se agregan varias figuras al receptor.

El código siguiente muestra cómo hacerlo.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a>Crear una geometría de trazado para el río

A continuación, en el ejemplo se crea otra ruta de acceso geométrica para el río que contiene curvas Bézier. En la ilustración siguiente se muestra cómo se muestra el río.

![Ilustración de las curvas de Bézier que muestran un río](images/path-geo-river.png)

El código siguiente muestra cómo hacerlo.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a>Representar las geometrías de trazado en la pantalla

En el código siguiente se muestra cómo representar las geometrías de trazado rellenadas en la pantalla. Primero dibuja y pinta la geometría del sol, después de la geometría de la montaña izquierda, la geometría del río y, por último, la geometría de la montaña derecha.


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



En el ejemplo completo se genera la siguiente ilustración.

![Ilustración de un río, montañas y el sol mediante el uso de geometrías de trazado](images/path-geo-mnts.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una aplicación de Direct2D simple](direct2d-quickstart.md)
</dt> <dt>

[Información general sobre las geometrías](direct2d-geometries-overview.md)
</dt> </dl>

 

 