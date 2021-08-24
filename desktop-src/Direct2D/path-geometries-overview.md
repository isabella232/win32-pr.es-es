---
title: Introducción a las geometrías de ruta de acceso
description: Describe cómo usar geometrías de ruta de acceso para definir formas complejas.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5fb177cbbd82ef56a03ef2c8a6faa7ef6c11f7889423ce79102d11eb42090231
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636163"
---
# <a name="path-geometries-overview"></a>Introducción a las geometrías de ruta de acceso

En este tema se describe cómo usar geometrías de ruta de acceso de Direct2D para crear dibujos complejos. Contiene las siguientes secciones:

-   [Requisitos previos](#prerequisites)
-   [Geometrías de ruta de acceso en Direct2D](#path-geometries-in-direct2d)
-   [Usar un ID2D1GeometrySink para rellenar una geometría de ruta de acceso](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Ejemplo: Crear un dibujo complejo](#example-create-a-complex-drawing)
    -   [Creación de una geometría de trazado para la montaña izquierda](#create-a-path-geometry-for-the-left-mountain)
    -   [Creación de una geometría de trazado para la montaña derecha](#create-a-path-geometry-for-the-right-mountain)
    -   [Creación de una geometría de trazado para el sol](#create-a-path-geometry-for-the-sun)
    -   [Creación de una geometría de trazado para el cauce](#create-a-path-geometry-for-the-river)
    -   [Representar las geometrías de ruta de acceso en la pantalla](#render-the-path-geometries-onto-the-display)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Prerrequisitos

En esta introducción se da por supuesto que está familiarizado con la creación de aplicaciones básicas de Direct2D, como se describe en [Creación de una aplicación direct2D simple.](direct2d-quickstart.md) También se supone que está familiarizado con las características básicas de las geometrías de Direct2D, como se describe en Información general [sobre geometrías.](direct2d-geometries-overview.md)

## <a name="path-geometries-in-direct2d"></a>Geometrías de ruta de acceso en Direct2D

Las geometrías de ruta de acceso se representan mediante la [**interfaz ID2D1PathGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) Para crear instancias de una geometría de ruta de acceso, llame al [**método ID2D1Factory::CreatePathGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) Estos objetos se pueden usar para describir figuras geométricas complejas formadas por segmentos como arcos, curvas y líneas. Para rellenar una geometría de trazado con figuras y segmentos, llame al método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para recuperar un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) y use los métodos del receptor de geometría para agregar figuras y segmentos a la geometría del trazado.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Usar un ID2D1GeometrySink para rellenar una geometría de trazado

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describe un trazado geométrico que puede contener líneas, arcos, curvas Bézier cúbicas y curvas Bézier cuadráticas.

Un receptor de geometría consta de una o varias figuras. Cada ilustración se forma de uno o varios segmentos de línea, curva o arco. Para crear una ilustración, llame al método [**BeginFigure,**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) pasando el punto inicial de la ilustración y, a continuación, use sus métodos Add (como [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) y [**AddBezier)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para agregar segmentos. Cuando haya terminado de agregar segmentos, llame al [**método EndFigure.**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) Puede repetir esta secuencia para crear figuras adicionales. Cuando haya terminado de crear figuras, llame al [**método Close.**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close)

## <a name="example-create-a-complex-drawing"></a>Ejemplo: Crear un dibujo complejo

En la ilustración siguiente se muestra un dibujo complejo con líneas, arcos y curvas Bézier. En el ejemplo de código siguiente se muestra cómo crear el dibujo mediante cuatro objetos de geometría de trazado, uno para la montaña izquierda, otro para la montaña derecha, otro para el monte y otro para el sol con toboganes.

![ilustración de un monte, montañas y el sol, mediante geometrías de trazado](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Creación de una geometría de trazado para la montaña izquierda

En primer lugar, en el ejemplo se crea una geometría de trazado para la montaña izquierda, como se muestra en la ilustración siguiente.

![Muestra un dibujo complejo de un polígono que muestra una montaña.](images/path-geo-leftmnt.png)

Para crear la montaña izquierda, en el ejemplo se llama al método [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para crear un [**elemento ID2D1PathGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



A continuación, en el ejemplo se usa el método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para obtener un receptor geometry de [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y se almacena en la variable *pSink.*


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



A continuación, en el ejemplo se llama a [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), pasando [**D2D1 \_ FIGURE BEGIN \_ \_ FILLED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) que indica que esta figura se rellena y, a continuación, llama a [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), pasando una matriz de puntos [**D2D1 \_ POINT \_ 2F,**](d2d1-point-2f.md) (267, 177), (236, 192), (212, 160), (156, 255) y (346, 255).

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



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Creación de una geometría de trazado para la montaña derecha

A continuación, el ejemplo crea otra geometría de trazado para la montaña derecha con puntos (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) y (575, 263). En la ilustración siguiente se muestra cómo se muestra la montaña derecha.

![ilustración de un polígono que muestra una montaña](images/path-geo-rightmnt.png)

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



### <a name="create-a-path-geometry-for-the-sun"></a>Creación de una geometría de trazado para el sol

A continuación, el ejemplo rellena otra geometría de trazado para el sol, como se muestra en la ilustración siguiente.

![ilustración de un arco y curvas bézier que muestran el sol](images/path-geo-sun.png)

Para ello, la geometría de la ruta de acceso crea un receptor y agrega una figura para el arco y una figura para cada reboso al receptor. Al repetir la secuencia de [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), sus métodos Add (como [**AddBezier)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))y [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), se agregan varias figuras al receptor.

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



### <a name="create-a-path-geometry-for-the-river"></a>Creación de una geometría de trazado para el cauce

A continuación, en el ejemplo se crea otro trazado de geometría para el cauce que contiene curvas Bézier. En la ilustración siguiente se muestra cómo se muestra el agua.

![ilustración de curvas bézier que muestran un paseo](images/path-geo-river.png)

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



### <a name="render-the-path-geometries-onto-the-display"></a>Representar las geometrías de ruta de acceso en la pantalla

El código siguiente muestra cómo representar las geometrías de ruta de acceso rellenadas en la pantalla. En primer lugar, dibuja y pinta la geometría solar, después la geometría de la montaña izquierda, después la geometría de los montes y, por último, la geometría de la montaña derecha.


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



En el ejemplo completo se muestra la siguiente ilustración.

![ilustración de un monte, montañas y el sol, mediante geometrías de trazado](images/path-geo-mnts.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de una aplicación direct2D simple](direct2d-quickstart.md)
</dt> <dt>

[Información general sobre las geometrías](direct2d-geometries-overview.md)
</dt> </dl>

 

 