---
title: Cómo crear grupos de geometría
description: En este tema se describe cómo crear grupos de geometría.
ms.assetid: be364440-75ab-4d8f-a359-39da275272fd
keywords:
- Ejemplo de Direct2D, modo de relleno
- grupos de geometría
- Direct2D, grupos de geometría
- geometrías de ruta de acceso
- Direct2D, geometrías de ruta de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb4a0e63a3274473153e1871a8a085bb04d5146
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420817"
---
# <a name="how-to-create-geometry-groups"></a><span data-ttu-id="315af-108">Cómo crear grupos de geometría</span><span class="sxs-lookup"><span data-stu-id="315af-108">How to Create Geometry Groups</span></span>

<span data-ttu-id="315af-109">En este tema se describe cómo crear grupos de geometría.</span><span class="sxs-lookup"><span data-stu-id="315af-109">This topic describes how to create geometry groups.</span></span>

<span data-ttu-id="315af-110">Para crear un grupo de geometría, llame al método [**ID2D1Factory:: CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) y especifique una matriz de geometrías y un modo de relleno.</span><span class="sxs-lookup"><span data-stu-id="315af-110">To create a geometry group, call the [**ID2D1Factory::CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method and specify an array of geometries and a fill mode.</span></span>

<span data-ttu-id="315af-111">Al combinar las geometrías en un grupo de geometría, asegúrese de que las geometrías están orientadas de manera similar.</span><span class="sxs-lookup"><span data-stu-id="315af-111">When you combine geometries into a geometry group, ensure that the geometries are similarly oriented.</span></span> <span data-ttu-id="315af-112">Si no está seguro de la orientación de las geometrías, llame a [**ID2D1Geometry:: Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink)) en cada una de ellas individualmente y, a continuación, inserte las geometrías resultantes en el grupo Geometry.</span><span class="sxs-lookup"><span data-stu-id="315af-112">If you are unsure of the orientation of the geometries, call [**ID2D1Geometry::Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink)) on each of them individually, and then insert the resulting geometries into the geometry group.</span></span>

<span data-ttu-id="315af-113">En el ejemplo de código siguiente se muestra la creación de cuatro círculos concéntricos: el primer círculo tiene un radio de 25, el segundo 50, el tercero 75 y el cuarto de 100.</span><span class="sxs-lookup"><span data-stu-id="315af-113">The following code example shows the creation of four concentric circles: the first circle has a radius of 25, the second 50, the third 75, and the fourth 100.</span></span> <span data-ttu-id="315af-114">El código también muestra la creación de instancias de una matriz de geometrías, así como las dos llamadas a [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup).</span><span class="sxs-lookup"><span data-stu-id="315af-114">The code also shows the instantiation of an array of geometries, as well as the two calls to [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup).</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr;

    const D2D1_ELLIPSE ellipse1 = D2D1::Ellipse(
        D2D1::Point2F(105.0f, 105.0f),
        25.0f,
        25.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        ellipse1,
        &m_pEllipseGeometry1
        );

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse2 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse2,
            &m_pEllipseGeometry2
            );
    }

    if (SUCCEEDED(hr))
    {

        const D2D1_ELLIPSE ellipse3 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            75.0f,
            75.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse3,
            &m_pEllipseGeometry3
            );
    }

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse4 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            100.0f,
            100.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse4,
            &m_pEllipseGeometry4
            );
    }

    if (SUCCEEDED(hr))
    {
        ID2D1Geometry *ppGeometries[] =
        {
            m_pEllipseGeometry1,
            m_pEllipseGeometry2,
            m_pEllipseGeometry3,
            m_pEllipseGeometry4
        };

        hr = m_pD2DFactory->CreateGeometryGroup(
            D2D1_FILL_MODE_ALTERNATE,
            ppGeometries,
            ARRAYSIZE(ppGeometries),
            &m_pGeoGroup_AlternateFill
            );

        if (SUCCEEDED(hr))
        {
            hr = m_pD2DFactory->CreateGeometryGroup(
                D2D1_FILL_MODE_WINDING,
                ppGeometries,
                ARRAYSIZE(ppGeometries),
                &m_pGeoGroup_WindingFill
                );
        }

    }
    return hr;
}
```



## <a name="drawing-and-filling-of-geometry-groups"></a><span data-ttu-id="315af-115">Dibujo y relleno de grupos de geometría</span><span class="sxs-lookup"><span data-stu-id="315af-115">Drawing and Filling of Geometry Groups</span></span>

<span data-ttu-id="315af-116">Para dibujar y rellenar un grupo de geometría, use los métodos [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) y [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) .</span><span class="sxs-lookup"><span data-stu-id="315af-116">To draw and fill a geometry group, use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) and [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) methods.</span></span> <span data-ttu-id="315af-117">En el ejemplo de código siguiente se muestra cómo dibujar y rellenar un grupo de geometría.</span><span class="sxs-lookup"><span data-stu-id="315af-117">The following code example shows how to draw and fill a geometry group.</span></span>


```C++
HRESULT DemoApp::OnRender()
{
    HRESULT hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_fillModeAlternateText[] = L"D2D1_FILL_MODE_ALTERNATE";
        static const WCHAR sc_fillModeWindingText[] = L"D2D1_FILL_MODE_WINDING";

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, rtSize.width, rtSize.height),
            m_pGridPatternBitmapBrush
            );

        // Centers the text in a layout rectangle.
        hr = m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

        if (SUCCEEDED(hr))
        {
            // Fill the geometry group with D2D1_FILL_MODE_ALTERNATE and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_AlternateFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_AlternateFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeAlternateText,
                ARRAYSIZE(sc_fillModeAlternateText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

            // Fill the geometry group with D2D1_FILL_MODE_WINDING and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_WindingFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_WindingFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeWindingText,
                ARRAYSIZE(sc_fillModeWindingText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            hr = m_pRenderTarget->EndDraw();

            if (hr == D2DERR_RECREATE_TARGET)
            {
                hr = S_OK;
                DiscardDeviceResources();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="315af-118">El código genera el resultado que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="315af-118">The code produces the output shown in the following illustration.</span></span>

![Ilustración de dos conjuntos de cuatro círculos concéntricos, uno con la segunda y la cuarta anillos rellenados y otro con todos los anillos rellenados](images/create-geometry-group.png)

 

 