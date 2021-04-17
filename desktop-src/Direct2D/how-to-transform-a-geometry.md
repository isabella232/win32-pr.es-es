---
title: Cómo transformar una geometría
description: Muestra cómo transformar una geometría mediante Direct2D.
ms.assetid: de434615-14b1-4b66-b09b-e90468e03d58
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ae15d0b1da304f9dfe24ff5de33a9f1582e2ca05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656379"
---
# <a name="how-to-transform-a-geometry"></a><span data-ttu-id="327f7-103">Cómo transformar una geometría</span><span class="sxs-lookup"><span data-stu-id="327f7-103">How to Transform a Geometry</span></span>

<span data-ttu-id="327f7-104">Para transformar una geometría, puede aplicar la transformación al destino de representación llamando a [**SetTransform**](id2d1rendertarget-settransform.md) o aplicar la transformación a la geometría llamando a [**CreateTransformedGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="327f7-104">To transform a geometry, you can either apply the transform to the render target by calling [**SetTransform**](id2d1rendertarget-settransform.md) or apply the transform to the geometry by calling [**CreateTransformedGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span></span> <span data-ttu-id="327f7-105">Aunque ambos enfoques transforman una geometría, tienen algunas diferencias fundamentales.</span><span class="sxs-lookup"><span data-stu-id="327f7-105">Although both approaches transform a geometry, they have some fundamental differences.</span></span> <span data-ttu-id="327f7-106">**CreateTransformedGeometry** afecta al relleno, pero no afecta al ancho del trazo.</span><span class="sxs-lookup"><span data-stu-id="327f7-106">**CreateTransformedGeometry** affects the fill, but does not affect the stroke width.</span></span> <span data-ttu-id="327f7-107">Además, **CreateTransformedGeometry** transforma la geometría por sí sola sin afectar a otras formas en el destino de representación, mientras que [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) aplica la transformación a todas las formas del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="327f7-107">Further, **CreateTransformedGeometry** transforms the geometry alone without impacting other shapes on the render target, whereas [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) applies the transform to all shapes on the render target.</span></span>

<span data-ttu-id="327f7-108">En este tema de procedimientos se describe cómo transformar una geometría llamando a [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="327f7-108">This how-to topic describes how to transform a geometry by calling [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span></span>

<span data-ttu-id="327f7-109">**Para transformar una geometría**</span><span class="sxs-lookup"><span data-stu-id="327f7-109">**To transform a geometry**</span></span>

1.  <span data-ttu-id="327f7-110">Declare una variable [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) .</span><span class="sxs-lookup"><span data-stu-id="327f7-110">Declare an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) variable.</span></span>
2.  <span data-ttu-id="327f7-111">Llame al método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) para crear una geometría transformada.</span><span class="sxs-lookup"><span data-stu-id="327f7-111">Call the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to create a transformed geometry.</span></span>

<span data-ttu-id="327f7-112">En el código siguiente se muestra cómo crear un reloj horario, transformar el reloj horario y dibujar las gafas de hora originales y resultantes.</span><span class="sxs-lookup"><span data-stu-id="327f7-112">The following code shows how to create an hour glass, transform the hour glass, and draw the original and resulting hour glasses.</span></span>


```C++
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

if (SUCCEEDED(hr))
{
    // Create a transformed geometry which is tilted at an angle to the previous geometry
    hr = m_pD2DFactory->CreateTransformedGeometry(
        m_pPathGeometry,
        D2D1::Matrix3x2F::Rotation(
            45.f,
            D2D1::Point2F(100, 100)),
        &m_pTransformedGeometry
        );
}
```



 

 