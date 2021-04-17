---
title: Métodos ID2D1GeometrySink AddBezier (D2d1. h)
description: Crea una curva Bézier cúbica entre el punto actual y el punto final especificado y lo agrega al receptor de geometría.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Métodos de AddBezier Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660916"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a><span data-ttu-id="902f6-104">ID2D1GeometrySink:: AddBezier (métodos)</span><span class="sxs-lookup"><span data-stu-id="902f6-104">ID2D1GeometrySink::AddBezier methods</span></span>

<span data-ttu-id="902f6-105">Crea una curva Bézier cúbica entre el punto actual y el punto final especificado y lo agrega al receptor de geometría.</span><span class="sxs-lookup"><span data-stu-id="902f6-105">Creates a cubic Bezier curve between the current point and the specified end point and adds it to the geometry sink.</span></span>

### <a name="overload-list"></a><span data-ttu-id="902f6-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="902f6-106">Overload list</span></span>



| <span data-ttu-id="902f6-107">Método</span><span class="sxs-lookup"><span data-stu-id="902f6-107">Method</span></span>                                                                                            | <span data-ttu-id="902f6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="902f6-108">Description</span></span>                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="902f6-109">[**AddBezier (D2D1 \_ Bézier \_ Segment&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span><span class="sxs-lookup"><span data-stu-id="902f6-109">[**AddBezier(D2D1\_BEZIER\_SEGMENT&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span></span>  | <span data-ttu-id="902f6-110">Crea una curva Bézier cúbica entre el punto actual y el punto final especificado.</span><span class="sxs-lookup"><span data-stu-id="902f6-110">Creates a cubic Bezier curve between the current point and the specified end point.</span></span><br/> |
| <span data-ttu-id="902f6-111">[**AddBezier ( \_ segmento de BÉZIER D2D1 \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span><span class="sxs-lookup"><span data-stu-id="902f6-111">[**AddBezier(D2D1\_BEZIER\_SEGMENT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span></span> | <span data-ttu-id="902f6-112">Crea una curva Bézier cúbica entre el punto actual y el punto de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="902f6-112">Creates a cubic Bezier curve between the current point and the specified endpoint.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="902f6-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="902f6-113">Examples</span></span>

<span data-ttu-id="902f6-114">En el ejemplo siguiente se crea un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), se recupera un receptor y se usa para definir una forma de reloj de arena.</span><span class="sxs-lookup"><span data-stu-id="902f6-114">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span> <span data-ttu-id="902f6-115">Para obtener el ejemplo completo, vea [Cómo dibujar y rellenar una forma compleja](how-to-draw-and-fill-a-complex-shape.md).</span><span class="sxs-lookup"><span data-stu-id="902f6-115">For the complete example, see [How to Draw and Fill a Complex Shape](how-to-draw-and-fill-a-complex-shape.md).</span></span>


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





## <a name="requirements"></a><span data-ttu-id="902f6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="902f6-116">Requirements</span></span>



| <span data-ttu-id="902f6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="902f6-117">Requirement</span></span> | <span data-ttu-id="902f6-118">Value</span><span class="sxs-lookup"><span data-stu-id="902f6-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="902f6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="902f6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="902f6-120"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="902f6-120"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="902f6-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="902f6-121">Library</span></span><br/> | <dl> <span data-ttu-id="902f6-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="902f6-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="902f6-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="902f6-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="902f6-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="902f6-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="902f6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="902f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="902f6-126">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="902f6-126">**ID2D1GeometrySink**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

<span data-ttu-id="902f6-127">�</span><span class="sxs-lookup"><span data-stu-id="902f6-127">�</span></span>

<span data-ttu-id="902f6-128">�</span><span class="sxs-lookup"><span data-stu-id="902f6-128">�</span></span>
