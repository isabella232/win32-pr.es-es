---
title: Dibujar y rellenar una forma básica
description: En este tema se describe cómo dibujar una forma básica.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 93d8f3a3ddeb06c9168971789dff3ac8c9222d22
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827004"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="04280-103">Dibujar y rellenar una forma básica</span><span class="sxs-lookup"><span data-stu-id="04280-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="04280-104">En este tema se describe cómo dibujar una forma básica.</span><span class="sxs-lookup"><span data-stu-id="04280-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="04280-105">La [**interfaz ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) proporciona métodos para delinear y rellenar elipses, rectángulos y líneas.</span><span class="sxs-lookup"><span data-stu-id="04280-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="04280-106">En los ejemplos siguientes se muestra cómo crear y dibujar una elipse.</span><span class="sxs-lookup"><span data-stu-id="04280-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="04280-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="04280-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="04280-108">Dibujar el contorno de una elipse con un trazo sólido</span><span class="sxs-lookup"><span data-stu-id="04280-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="04280-109">Dibujar una elipse con un trazo discontinuo</span><span class="sxs-lookup"><span data-stu-id="04280-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="04280-110">Dibujar y rellenar una elipse</span><span class="sxs-lookup"><span data-stu-id="04280-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="04280-111">Dibujar formas más complejas</span><span class="sxs-lookup"><span data-stu-id="04280-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="04280-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04280-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="04280-113">Dibujar el contorno de una elipse con un trazo sólido</span><span class="sxs-lookup"><span data-stu-id="04280-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="04280-114">Para dibujar el contorno de una elipse, defina un pincel (por [**ejemplo, ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o [**ID2D1LinearGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)para pintar el contorno y una [**\_ elipse D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) para describir la posición y las dimensiones de la elipse y, a continuación, pasar estos objetos al método [**ID2D1RenderTarget::D raw Insertpse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="04280-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="04280-115">En el ejemplo siguiente se crea un pincel de color sólido negro y se almacena en el miembro de clase m \_ spBlackBrush.</span><span class="sxs-lookup"><span data-stu-id="04280-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="04280-116">En el ejemplo siguiente se define [**una \_ elipse D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) y se usa con el pincel definido en el ejemplo anterior para dibujar el contorno de una elipse.</span><span class="sxs-lookup"><span data-stu-id="04280-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="04280-117">En este ejemplo se genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="04280-117">This example produces the output shown in the following illustration.</span></span>

![ilustración de una elipse con un trazo sólido](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="04280-119">Dibujar una elipse con un trazo discontinuo</span><span class="sxs-lookup"><span data-stu-id="04280-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="04280-120">En el ejemplo anterior se usó un trazo sin formato.</span><span class="sxs-lookup"><span data-stu-id="04280-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="04280-121">Puede modificar el aspecto de un trazo de varias maneras mediante la creación de [**un ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span><span class="sxs-lookup"><span data-stu-id="04280-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="04280-122">**ID2D1StrokeStyle** permite especificar la forma al principio y al final de un trazo, si tiene un patrón de guion, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="04280-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="04280-123">En el ejemplo siguiente se **crea un id2D1StrokeStyle** que describe un trazo discontinuo.</span><span class="sxs-lookup"><span data-stu-id="04280-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="04280-124">En este ejemplo se usa un patrón de guion predefinido, [**D2D1 \_ DASH STYLE DASH DOT \_ \_ \_ \_ DOT,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)pero también puede especificar el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="04280-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



<span data-ttu-id="04280-125">En el ejemplo siguiente se usa el estilo de trazo con el [**método DrawVelopse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="04280-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="04280-126">En este ejemplo se genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="04280-126">This example produces the output shown in the following illustration.</span></span>

![ilustración de una elipse con un trazo discontinuo](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="04280-128">Dibujar y rellenar una elipse</span><span class="sxs-lookup"><span data-stu-id="04280-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="04280-129">Para pintar el interior de una elipse, use el [**método FillVelopse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="04280-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="04280-130">En el ejemplo siguiente se usa [**el método DrawVelopse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) para esquematear la elipse y, a continuación, se usa el **método FillVelopse** para pintar su interior.</span><span class="sxs-lookup"><span data-stu-id="04280-130">The following example uses the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="04280-131">En este ejemplo se genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="04280-131">This example produces the output shown in the following illustration.</span></span>

![ilustración de una elipse con un trazo discontinuo y, a continuación, rellena con un color gris sólido](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="04280-133">En el ejemplo siguiente se rellena primero la elipse y, a continuación, se dibuja su contorno.</span><span class="sxs-lookup"><span data-stu-id="04280-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="04280-134">En este ejemplo se genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="04280-134">This example produces the output shown in the following illustration.</span></span>

![ilustración de una elipse rellena con un color gris sólido y, a continuación, con un trazo discontinuo](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="04280-136">En estos ejemplos se ha omitido el código.</span><span class="sxs-lookup"><span data-stu-id="04280-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="04280-137">Dibujar formas más complejas</span><span class="sxs-lookup"><span data-stu-id="04280-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="04280-138">Para dibujar formas más complejas, defina objetos ID2D1Geometry y úsenlos con los métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) [**y FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)</span><span class="sxs-lookup"><span data-stu-id="04280-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="04280-139">Para obtener más información, vea Información general [sobre geometrías.](direct2d-geometries-overview.md)</span><span class="sxs-lookup"><span data-stu-id="04280-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04280-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04280-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04280-141">Información general sobre las geometrías</span><span class="sxs-lookup"><span data-stu-id="04280-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="04280-142">Información general sobre los pinceles</span><span class="sxs-lookup"><span data-stu-id="04280-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 
