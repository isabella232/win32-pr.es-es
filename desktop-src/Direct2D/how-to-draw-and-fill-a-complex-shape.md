---
title: Cómo dibujar y rellenar una forma compleja
description: Direct2D proporciona la interfaz ID2D1PathGeometry para describir formas complejas que pueden contener curvas, arcos y líneas. En este tema se describe cómo definir y representar una geometría de trazado.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a163e85d76a65f6b807ad1e4a9c9f740a32bf1
ms.sourcegitcommit: 4859402a45b9928c3e1354ded06b1d6a682a0be9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "105937674"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a><span data-ttu-id="ac73f-104">Cómo dibujar y rellenar una forma compleja</span><span class="sxs-lookup"><span data-stu-id="ac73f-104">How to Draw and Fill a Complex Shape</span></span>

<span data-ttu-id="ac73f-105">Direct2D proporciona la interfaz [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) para describir formas complejas que pueden contener curvas, arcos y líneas.</span><span class="sxs-lookup"><span data-stu-id="ac73f-105">Direct2D provides the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface for describing complex shapes that can contain curves, arcs, and lines.</span></span> <span data-ttu-id="ac73f-106">En este tema se describe cómo definir y representar una geometría de trazado.</span><span class="sxs-lookup"><span data-stu-id="ac73f-106">This topic describes how to define and render a path geometry.</span></span>

<span data-ttu-id="ac73f-107">Para definir una geometría de trazado, use primero el método [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para crear la geometría de trazado y, a continuación, use el método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) de la geometría de la ruta de acceso para recuperar una [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="ac73f-107">To define a path geometry, first use the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create the path geometry, then use the path geometry's [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="ac73f-108">Después, puede agregar líneas, curvas y arcos llamando a los distintos métodos Add del receptor.</span><span class="sxs-lookup"><span data-stu-id="ac73f-108">You can then add lines, curves, and arcs by calling the sink's various Add methods.</span></span>

<span data-ttu-id="ac73f-109">En el ejemplo siguiente se crea un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), se recupera un receptor y se usa para definir una forma de reloj de arena.</span><span class="sxs-lookup"><span data-stu-id="ac73f-109">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span>


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

<span data-ttu-id="ac73f-110">Tenga en cuenta que un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) es un recurso independiente del dispositivo y, por lo tanto, se puede crear una vez y conservar durante la vida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac73f-110">Note that an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) is a device-independent resource and can, therefore, be created once and retained for the life of the application.</span></span> <span data-ttu-id="ac73f-111">(Para obtener más información sobre los diferentes tipos de recursos, consulte la [información general](resources-and-resource-domains.md)sobre los recursos).</span><span class="sxs-lookup"><span data-stu-id="ac73f-111">(For more information about different types of resources, see the [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="ac73f-112">En el ejemplo siguiente se crean dos pinceles que se usarán para pintar el contorno y el relleno de la geometría de trazado.</span><span class="sxs-lookup"><span data-stu-id="ac73f-112">The next example creates two brushes that will be used to paint the path geometry's outline and fill.</span></span>


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



<span data-ttu-id="ac73f-113">En el ejemplo final se usan los métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) para pintar el contorno y el interior de la geometría.</span><span class="sxs-lookup"><span data-stu-id="ac73f-113">The final example uses the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods to paint the geometry's outline and interior.</span></span> <span data-ttu-id="ac73f-114">En este ejemplo se genera el resultado que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="ac73f-114">This example produces the output shown in the following illustration.</span></span>

![Ilustración de una geometría con forma de reloj de arena](images/transformgeometryexample-1.png)


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

<span data-ttu-id="ac73f-116">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac73f-116">Code has been omitted from this example.</span></span> <span data-ttu-id="ac73f-117">Para obtener más información sobre las geometrías, vea la [información general sobre las geometrías](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ac73f-117">For more information about geometries, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>
