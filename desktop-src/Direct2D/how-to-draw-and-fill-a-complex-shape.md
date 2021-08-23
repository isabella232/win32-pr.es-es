---
title: Dibujar y rellenar una forma compleja
description: Direct2D proporciona la interfaz ID2D1PathGeometry para describir formas complejas que pueden contener curvas, arcos y líneas. En este tema se describe cómo definir y representar una geometría de ruta de acceso.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222d3d94eb1f9e944a1c5113baf938a7c3da6e86751a7be748798ace12a9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569215"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a>Dibujar y rellenar una forma compleja

Direct2D proporciona la [**interfaz ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) para describir formas complejas que pueden contener curvas, arcos y líneas. En este tema se describe cómo definir y representar una geometría de ruta de acceso.

Para definir una geometría de ruta de acceso, use primero el método [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para crear la geometría de ruta de acceso y, a continuación, use el método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) de la geometría de ruta de acceso para recuperar un [**elemento ID2D1GeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) A continuación, puede agregar líneas, curvas y arcos llamando a los distintos métodos Add del receptor.

En el ejemplo siguiente se crea [**un id2D1PathGeometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)se recupera un receptor y se usa para definir una forma de reloj de reloj.


```C++
ID2D1GeometrySink *pSink = NULL;

// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```

Tenga en cuenta que [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) es un recurso independiente del dispositivo y, por tanto, se puede crear una vez y conservarse durante la vida útil de la aplicación. (Para obtener más información sobre los distintos tipos de recursos, vea Información [general sobre los recursos).](resources-and-resource-domains.md)

En el ejemplo siguiente se crean dos pinceles que se usarán para pintar el contorno y el relleno de la geometría del trazado.


```C++
if (SUCCEEDED(hr))
{
    // Create a black brush.
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &m_pBlackBrush
        );
}

if (SUCCEEDED(hr))
{
    // Create a linear gradient.
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 0.25f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = m_pRenderTarget->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(100, 0),
                D2D1::Point2F(100, 200)),
            D2D1::BrushProperties(),
            pGradientStops,
            &m_pLGBrush
            );
    }

    SafeRelease(&pGradientStops);
}
```



En el ejemplo final se [**usan los métodos DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) para pintar el contorno y el interior de la geometría. En este ejemplo se genera la salida que se muestra en la ilustración siguiente.

![ilustración de una geometría con forma de reloj de reloj](images/transformgeometryexample-1.png)


```C++
void DemoApp::RenderGeometryExample()
{
    // Translate subsequent drawings by 20 device-independent pixels.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Translation(20.f, 20.f)
        );

    // Draw the hour glass geometry at the upper left corner of the client area.
    m_pRenderTarget->DrawGeometry(m_pPathGeometry, m_pBlackBrush, 10.f);
    m_pRenderTarget->FillGeometry(m_pPathGeometry, m_pLGBrush);
}
```

En este ejemplo se ha omitido el código. Para obtener más información sobre las geometrías, vea Información [general sobre geometrías.](direct2d-geometries-overview.md)
