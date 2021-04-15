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
# <a name="path-geometries-overview"></a><span data-ttu-id="68638-103">Información general sobre las geometrías de ruta</span><span class="sxs-lookup"><span data-stu-id="68638-103">Path Geometries Overview</span></span>

<span data-ttu-id="68638-104">En este tema se describe cómo usar las geometrías de ruta de acceso de Direct2D para crear dibujos complejos.</span><span class="sxs-lookup"><span data-stu-id="68638-104">This topic describes how to use Direct2D path geometries to create complex drawings.</span></span> <span data-ttu-id="68638-105">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="68638-105">It contains the following sections.</span></span>

-   [<span data-ttu-id="68638-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68638-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="68638-107">Geometrías de ruta de acceso en Direct2D</span><span class="sxs-lookup"><span data-stu-id="68638-107">Path Geometries in Direct2D</span></span>](#path-geometries-in-direct2d)
-   [<span data-ttu-id="68638-108">Usar un ID2D1GeometrySink para rellenar una geometría de trazado</span><span class="sxs-lookup"><span data-stu-id="68638-108">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [<span data-ttu-id="68638-109">Ejemplo: crear un dibujo complejo</span><span class="sxs-lookup"><span data-stu-id="68638-109">Example: Create a Complex Drawing</span></span>](#example-create-a-complex-drawing)
    -   [<span data-ttu-id="68638-110">Crear una geometría de trazado para la montaña izquierda</span><span class="sxs-lookup"><span data-stu-id="68638-110">Create a Path Geometry for the Left Mountain</span></span>](#create-a-path-geometry-for-the-left-mountain)
    -   [<span data-ttu-id="68638-111">Crear una geometría de trazado para la montaña derecha</span><span class="sxs-lookup"><span data-stu-id="68638-111">Create a Path Geometry for the Right Mountain</span></span>](#create-a-path-geometry-for-the-right-mountain)
    -   [<span data-ttu-id="68638-112">Crear una geometría de trazado para el sol</span><span class="sxs-lookup"><span data-stu-id="68638-112">Create a Path Geometry for the Sun</span></span>](#create-a-path-geometry-for-the-sun)
    -   [<span data-ttu-id="68638-113">Crear una geometría de trazado para el río</span><span class="sxs-lookup"><span data-stu-id="68638-113">Create a Path Geometry for the River</span></span>](#create-a-path-geometry-for-the-river)
    -   [<span data-ttu-id="68638-114">Representar las geometrías de trazado en la pantalla</span><span class="sxs-lookup"><span data-stu-id="68638-114">Render the Path Geometries onto the Display</span></span>](#render-the-path-geometries-onto-the-display)
-   [<span data-ttu-id="68638-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68638-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="68638-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68638-116">Prerequisites</span></span>

<span data-ttu-id="68638-117">En esta información general se supone que está familiarizado con la creación de aplicaciones básicas de Direct2D, tal como se describe en [creación de una aplicación sencilla de direct2d](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="68638-117">This overview assumes that you are familiar with creating basic Direct2D applications, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span> <span data-ttu-id="68638-118">También se supone que está familiarizado con las características básicas de las geometrías de Direct2D, tal como se describe en la [información general sobre las geometrías](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68638-118">It also assumes that you are familiar with the basic features of Direct2D geometries, as described in the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="path-geometries-in-direct2d"></a><span data-ttu-id="68638-119">Geometrías de ruta de acceso en Direct2D</span><span class="sxs-lookup"><span data-stu-id="68638-119">Path Geometries in Direct2D</span></span>

<span data-ttu-id="68638-120">La interfaz [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) representa las geometrías de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="68638-120">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="68638-121">Para crear una instancia de la geometría de una ruta de acceso, llame al método [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="68638-121">To instantiate a path geometry, call the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span> <span data-ttu-id="68638-122">Estos objetos se pueden usar para describir figuras geométricas complejas que se componen de segmentos como arcos, curvas y líneas.</span><span class="sxs-lookup"><span data-stu-id="68638-122">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="68638-123">Para rellenar una geometría de trazado con figuras y segmentos, llame al método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para recuperar un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) y use los métodos del receptor de Geometry para agregar figuras y segmentos a la geometría del trazado.</span><span class="sxs-lookup"><span data-stu-id="68638-123">To populate a path geometry with figures and segments, call the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) and use the geometry sink's methods to add figures and segments to the path geometry.</span></span>

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a><span data-ttu-id="68638-124">Usar un ID2D1GeometrySink para rellenar una geometría de trazado</span><span class="sxs-lookup"><span data-stu-id="68638-124">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>

<span data-ttu-id="68638-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describe un trazado geométrico que puede contener líneas, arcos, curvas Bézier cúbicas y curvas Bézier cuadráticas.</span><span class="sxs-lookup"><span data-stu-id="68638-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.</span></span>

<span data-ttu-id="68638-126">Un receptor de geometría se compone de una o más figuras.</span><span class="sxs-lookup"><span data-stu-id="68638-126">A geometry sink consists of one or more figures.</span></span> <span data-ttu-id="68638-127">Cada ilustración se compone de uno o varios segmentos de línea, curva o arco.</span><span class="sxs-lookup"><span data-stu-id="68638-127">Each figure is made up of one or more line, curve, or arc segments.</span></span> <span data-ttu-id="68638-128">Para crear una figura, llame al método [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , pase el punto inicial de la figura y, a continuación, use sus métodos Add (como [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) y [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para agregar segmentos).</span><span class="sxs-lookup"><span data-stu-id="68638-128">To create a figure, call the [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) method, passing in the figure's starting point, and then use its Add methods (such as [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) and [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to add segments.</span></span> <span data-ttu-id="68638-129">Cuando haya terminado de agregar segmentos, llame al método [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) .</span><span class="sxs-lookup"><span data-stu-id="68638-129">When you are finished adding segments, call the [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) method.</span></span> <span data-ttu-id="68638-130">Puede repetir esta secuencia para crear más figuras.</span><span class="sxs-lookup"><span data-stu-id="68638-130">You can repeat this sequence to create additional figures.</span></span> <span data-ttu-id="68638-131">Cuando haya terminado de crear las figuras, llame al método [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .</span><span class="sxs-lookup"><span data-stu-id="68638-131">When you are finished creating figures, call the [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) method.</span></span>

## <a name="example-create-a-complex-drawing"></a><span data-ttu-id="68638-132">Ejemplo: crear un dibujo complejo</span><span class="sxs-lookup"><span data-stu-id="68638-132">Example: Create a Complex Drawing</span></span>

<span data-ttu-id="68638-133">En la ilustración siguiente se muestra un dibujo complejo con líneas, arcos y curvas Bézier.</span><span class="sxs-lookup"><span data-stu-id="68638-133">The following illustration shows a complex drawing with lines, arcs, and Bezier curves.</span></span> <span data-ttu-id="68638-134">En el ejemplo de código siguiente se muestra cómo crear el dibujo usando cuatro objetos de geometría de trazado, uno para la montaña izquierda, otro para la montaña derecha, uno para el río y otro para el sol con destellos.</span><span class="sxs-lookup"><span data-stu-id="68638-134">The code example that follows shows how to create the drawing by using four path geometry objects, one for the left mountain, one for the right mountain, one for the river, and one for the sun with flares.</span></span>

![Ilustración de un río, montañas y el sol mediante el uso de geometrías de trazado](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a><span data-ttu-id="68638-136">Crear una geometría de trazado para la montaña izquierda</span><span class="sxs-lookup"><span data-stu-id="68638-136">Create a Path Geometry for the Left Mountain</span></span>

<span data-ttu-id="68638-137">En el ejemplo se crea primero una geometría de trazado para la montaña izquierda, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="68638-137">The example first creates a path geometry for the left mountain as shown in the following illustration.</span></span>

![Muestra un dibujo complejo de un polígono que muestra una montaña.](images/path-geo-leftmnt.png)

<span data-ttu-id="68638-139">Para crear la montaña izquierda, el ejemplo llama al método [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para crear un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span><span class="sxs-lookup"><span data-stu-id="68638-139">To create the left mountain, the example calls the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



<span data-ttu-id="68638-140">A continuación, el ejemplo usa el método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para obtener un receptor de geometría de un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y lo almacena en la variable *pSink* .</span><span class="sxs-lookup"><span data-stu-id="68638-140">The example then uses the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to obtain a geometry sink from an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and stores it in the *pSink* variable.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



<span data-ttu-id="68638-141">A continuación, en el ejemplo se llama a [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), pasando [**D2D1 \_ figura \_ Begin \_ rellenada**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) que indica que esta figura se ha rellenado y, a continuación, llama a [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), pasando una matriz de [**D2D1 \_ Point \_ 2F**](d2d1-point-2f.md) Points, (267, 177), (236, 192), (212, 160), (156, 255) y (346, 255).</span><span class="sxs-lookup"><span data-stu-id="68638-141">The example then calls [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passing in [**D2D1\_FIGURE\_BEGIN\_FILLED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) that indicates this figure is filled, then calls [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passing in an array of [**D2D1\_POINT\_2F**](d2d1-point-2f.md) points, (267, 177), (236, 192), (212, 160), (156, 255) and (346, 255).</span></span>

<span data-ttu-id="68638-142">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="68638-142">The following code shows how to do this.</span></span>


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



### <a name="create-a-path-geometry-for-the-right-mountain"></a><span data-ttu-id="68638-143">Crear una geometría de trazado para la montaña derecha</span><span class="sxs-lookup"><span data-stu-id="68638-143">Create a Path Geometry for the Right Mountain</span></span>

<span data-ttu-id="68638-144">A continuación, en el ejemplo se crea otra geometría de ruta de acceso para la montaña derecha con puntos (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) y (575, 263).</span><span class="sxs-lookup"><span data-stu-id="68638-144">The example then creates another path geometry for the right mountain with points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263), and (575, 263).</span></span> <span data-ttu-id="68638-145">En la ilustración siguiente se muestra cómo se muestra la montaña derecha.</span><span class="sxs-lookup"><span data-stu-id="68638-145">The following illustration shows how the right mountain is displayed.</span></span>

![Ilustración de un polígono que muestra una montaña](images/path-geo-rightmnt.png)

<span data-ttu-id="68638-147">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="68638-147">The following code shows how to do this.</span></span>


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



### <a name="create-a-path-geometry-for-the-sun"></a><span data-ttu-id="68638-148">Crear una geometría de trazado para el sol</span><span class="sxs-lookup"><span data-stu-id="68638-148">Create a Path Geometry for the Sun</span></span>

<span data-ttu-id="68638-149">A continuación, en el ejemplo se rellena otra geometría de ruta de acceso para el sol, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="68638-149">The example then populates another path geometry for the sun as shown in the following illustration.</span></span>

![Ilustración de curvas de arco y Bézier que muestran el sol](images/path-geo-sun.png)

<span data-ttu-id="68638-151">Para ello, la geometría de trazado crea un receptor y agrega una figura para el arco y una figura para cada destello al receptor.</span><span class="sxs-lookup"><span data-stu-id="68638-151">To do this, the path geometry creates a sink, and adds a figure for the arc and a figure for each flare to the sink.</span></span> <span data-ttu-id="68638-152">Al repetir la secuencia de [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), sus métodos Add (como [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) y [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), se agregan varias figuras al receptor.</span><span class="sxs-lookup"><span data-stu-id="68638-152">By repeating the sequence of [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), its Add (such as [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) methods, and [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), multiple figures are added to the sink.</span></span>

<span data-ttu-id="68638-153">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="68638-153">The following code shows how to do this.</span></span>


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



### <a name="create-a-path-geometry-for-the-river"></a><span data-ttu-id="68638-154">Crear una geometría de trazado para el río</span><span class="sxs-lookup"><span data-stu-id="68638-154">Create a Path Geometry for the River</span></span>

<span data-ttu-id="68638-155">A continuación, en el ejemplo se crea otra ruta de acceso geométrica para el río que contiene curvas Bézier.</span><span class="sxs-lookup"><span data-stu-id="68638-155">The example then creates another geometry path for the river that contains Bezier curves.</span></span> <span data-ttu-id="68638-156">En la ilustración siguiente se muestra cómo se muestra el río.</span><span class="sxs-lookup"><span data-stu-id="68638-156">The following illustration shows how the river is displayed.</span></span>

![Ilustración de las curvas de Bézier que muestran un río](images/path-geo-river.png)

<span data-ttu-id="68638-158">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="68638-158">The following code shows how to do this.</span></span>


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



### <a name="render-the-path-geometries-onto-the-display"></a><span data-ttu-id="68638-159">Representar las geometrías de trazado en la pantalla</span><span class="sxs-lookup"><span data-stu-id="68638-159">Render the Path Geometries onto the Display</span></span>

<span data-ttu-id="68638-160">En el código siguiente se muestra cómo representar las geometrías de trazado rellenadas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="68638-160">The following code shows how to render the populated path geometries on the display.</span></span> <span data-ttu-id="68638-161">Primero dibuja y pinta la geometría del sol, después de la geometría de la montaña izquierda, la geometría del río y, por último, la geometría de la montaña derecha.</span><span class="sxs-lookup"><span data-stu-id="68638-161">It first draws and paints the sun geometry, next the left mountain geometry, then the river geometry, and finally the right mountain geometry.</span></span>


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



<span data-ttu-id="68638-162">En el ejemplo completo se genera la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="68638-162">The complete example outputs the following illustration.</span></span>

![Ilustración de un río, montañas y el sol mediante el uso de geometrías de trazado](images/path-geo-mnts.png)

## <a name="related-topics"></a><span data-ttu-id="68638-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68638-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68638-165">Crear una aplicación de Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="68638-165">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="68638-166">Información general sobre las geometrías</span><span class="sxs-lookup"><span data-stu-id="68638-166">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> </dl>

 

 