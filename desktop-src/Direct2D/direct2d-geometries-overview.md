---
title: 'Información general sobre las geometrías '
description: Describe los aspectos básicos de las geometrías de Direct2D, los objetos que se pueden usar para representar, manipular y analizar formas.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Información general sobre las geometrías de Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797079"
---
# <a name="geometries-overview"></a><span data-ttu-id="2d75e-104">Información general sobre las geometrías </span><span class="sxs-lookup"><span data-stu-id="2d75e-104">Geometries overview</span></span>

<span data-ttu-id="2d75e-105">En esta información general se describe cómo crear y usar objetos [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para definir y manipular figuras 2D.</span><span class="sxs-lookup"><span data-stu-id="2d75e-105">This overview describes how to create and use [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) objects to define and manipulate 2D figures.</span></span> <span data-ttu-id="2d75e-106">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="2d75e-106">It contains the following sections.</span></span>

## <a name="what-is-a-direct2d-geometry"></a><span data-ttu-id="2d75e-107">¿Qué es una geometría de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="2d75e-107">What is a Direct2D geometry?</span></span>

<span data-ttu-id="2d75e-108">Una geometría de Direct2D es un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-108">A Direct2D geometry is an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object.</span></span> <span data-ttu-id="2d75e-109">Este objeto puede ser una geometría simple ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)o [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), una geometría de trazado ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) o una geometría compuesta ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) y [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="2d75e-109">This object can be a simple geometry ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), or [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), a path geometry ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)), or a composite geometry ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) and [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span></span>

<span data-ttu-id="2d75e-110">Las geometrías de Direct2D permiten describir figuras bidimensionales y ofrecer muchos usos, como definir regiones de prueba de posicionamiento, regiones de recorte e incluso rutas de animación.</span><span class="sxs-lookup"><span data-stu-id="2d75e-110">Direct2D geometries enable you to describe two-dimensional figures and offer many uses, such as defining hit-test regions, clip regions, and even animation paths.</span></span>

<span data-ttu-id="2d75e-111">Las geometrías de Direct2D son recursos inmutables y independientes del dispositivo creados por [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="2d75e-111">Direct2D geometries are immutable and device-independent resources created by [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span> <span data-ttu-id="2d75e-112">Por lo general, debe crear geometrías una vez y mantenerlas mientras dure la aplicación, o hasta que tengan que cambiarse.</span><span class="sxs-lookup"><span data-stu-id="2d75e-112">Generally, you should create geometries one time and keep them for the life of the application, or until they have to be changed.</span></span> <span data-ttu-id="2d75e-113">Para obtener más información sobre los recursos independientes del dispositivo y dependientes del dispositivo, consulte la [información general](resources-and-resource-domains.md)sobre los recursos.</span><span class="sxs-lookup"><span data-stu-id="2d75e-113">For more information about device-independent and device-dependent resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="2d75e-114">En las secciones siguientes se describen los diferentes tipos de geometrías.</span><span class="sxs-lookup"><span data-stu-id="2d75e-114">The following sections describe the different kinds of geometries.</span></span>

## <a name="simple-geometries"></a><span data-ttu-id="2d75e-115">Geometrías simples</span><span class="sxs-lookup"><span data-stu-id="2d75e-115">Simple geometries</span></span>

<span data-ttu-id="2d75e-116">Las geometrías simples incluyen objetos [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)y [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , y se pueden usar para crear figuras geométricas básicas, como rectángulos, rectángulos redondeados, círculos y elipses.</span><span class="sxs-lookup"><span data-stu-id="2d75e-116">Simple geometries include [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), and [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects, and can be used to create basic geometric figures, such as rectangles, rounded rectangles, circles, and ellipses.</span></span>

<span data-ttu-id="2d75e-117">Para crear una geometría simple, use uno de los métodos [**ID2D1Factory:: create<*GeometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-117">To create a simple geometry, use one of the [**ID2D1Factory::Create<*geometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) methods.</span></span> <span data-ttu-id="2d75e-118">Estos métodos crean un objeto del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="2d75e-118">These methods create an object of the specified type.</span></span> <span data-ttu-id="2d75e-119">Por ejemplo, para crear un rectángulo, llame a [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), que devuelve un objeto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ; para crear un rectángulo redondeado, llame a [**ID2D1Factory:: CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), que devuelve un objeto [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) , etc.</span><span class="sxs-lookup"><span data-stu-id="2d75e-119">For example, to create a rectangle, call [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), which returns an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object; to create a rounded rectangle, call [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), which returns an [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) object, and so on.</span></span>

<span data-ttu-id="2d75e-120">En el ejemplo de código siguiente se llama al método [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , pasando una estructura de elipse con el *Centro* establecido en (100, 100), *x-RADIUS* a 100 e y *-RADIUS* a 50.</span><span class="sxs-lookup"><span data-stu-id="2d75e-120">The following code example calls the [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) method, passing in an ellipse structure with the *center* set to (100, 100), *x-radius* to 100, and *y-radius* to 50.</span></span> <span data-ttu-id="2d75e-121">A continuación, llama a [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), pasando la geometría de la elipse devuelta, un puntero a un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)negro y un ancho del trazo de 5.</span><span class="sxs-lookup"><span data-stu-id="2d75e-121">Then, it calls [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passing in the returned ellipse geometry, a pointer to a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), and a stroke width of 5.</span></span> <span data-ttu-id="2d75e-122">En la ilustración siguiente se muestra el resultado del ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="2d75e-122">The following illustration shows the output from the code example.</span></span>

![Ilustración de una elipse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



<span data-ttu-id="2d75e-124">Para dibujar el contorno de cualquier geometría, use el método [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-124">To draw the outline of any geometry, use the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method.</span></span> <span data-ttu-id="2d75e-125">Para pintar su interior, use el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-125">To paint its interior, use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

## <a name="path-geometries"></a><span data-ttu-id="2d75e-126">Geometrías de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="2d75e-126">Path geometries</span></span>

<span data-ttu-id="2d75e-127">La interfaz [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) representa las geometrías de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="2d75e-127">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="2d75e-128">Estos objetos se pueden usar para describir figuras geométricas complejas que se componen de segmentos como arcos, curvas y líneas.</span><span class="sxs-lookup"><span data-stu-id="2d75e-128">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="2d75e-129">En la ilustración siguiente se muestra un dibujo creado con la geometría de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="2d75e-129">The following illustration shows a drawing created by using path geometry.</span></span>

![Ilustración de un río, montañas y el sol](images/path-geo-mnts.png)

<span data-ttu-id="2d75e-131">Para obtener más información y ejemplos, vea [información general sobre las geometrías de ruta de acceso](path-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2d75e-131">For more information and examples, see the [Path Geometries Overview](path-geometries-overview.md).</span></span>

## <a name="composite-geometries"></a><span data-ttu-id="2d75e-132">Geometrías compuestas</span><span class="sxs-lookup"><span data-stu-id="2d75e-132">Composite geometries</span></span>

<span data-ttu-id="2d75e-133">Una geometría compuesta es una geometría agrupada o combinada con otro objeto Geometry o con una transformación.</span><span class="sxs-lookup"><span data-stu-id="2d75e-133">A composite geometry is a geometry grouped or combined with another geometry object, or with a transform.</span></span> <span data-ttu-id="2d75e-134">Las geometrías compuestas incluyen objetos [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) y [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-134">Composite geometries include [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) and [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) objects.</span></span>

### <a name="geometry-groups"></a><span data-ttu-id="2d75e-135">Grupos de geometría</span><span class="sxs-lookup"><span data-stu-id="2d75e-135">Geometry groups</span></span>

<span data-ttu-id="2d75e-136">Los grupos de geometría son una manera cómoda de agrupar varias geometrías al mismo tiempo, por lo que todas las figuras de varias geometrías distintas se concatenan en una.</span><span class="sxs-lookup"><span data-stu-id="2d75e-136">Geometry groups are a convenient way to group several geometries at the same time so all figures of several distinct geometries are concatenated into one.</span></span> <span data-ttu-id="2d75e-137">Para crear un [**objeto ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , llame al método [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) en el objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , pasando el *fillMode* con los valores posibles del [**modo de relleno D2D1 \_ \_ \_ alternativo**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternativo) y del **\_ \_ modo de relleno \_ D2D1**, una matriz de objetos Geometry para agregar al grupo Geometry y el número de elementos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="2d75e-137">To create a [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) object, call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in the *fillMode* with possible values of [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) and **D2D1\_FILL\_MODE\_WINDING**, an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>

<span data-ttu-id="2d75e-138">En el ejemplo de código siguiente se declara primero una matriz de objetos Geometry.</span><span class="sxs-lookup"><span data-stu-id="2d75e-138">The following code example first declares an array of geometry objects.</span></span> <span data-ttu-id="2d75e-139">Estos objetos son cuatro círculos concéntricos que tienen los radios siguientes: 25, 50, 75 y 100.</span><span class="sxs-lookup"><span data-stu-id="2d75e-139">These objects are four concentric circles that have the following radii: 25, 50, 75, and 100.</span></span> <span data-ttu-id="2d75e-140">Después, llame a [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) en el objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , pasando el [**modo de relleno D2D1 \_ \_ \_ alternativo**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), una matriz de objetos Geometry que se van a agregar al grupo Geometry y el número de elementos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="2d75e-140">Then call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>


```C++
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
```

<span data-ttu-id="2d75e-141">En la ilustración siguiente se muestran los resultados de la representación de las dos geometrías de grupo del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2d75e-141">The following illustration shows the results of rendering the two group geometries from the example.</span></span>

![Ilustración de dos conjuntos de cuatro círculos concéntricos, uno con anillos alternados y otro con todos los anillos rellenos](images/create-geometry-group.png)

### <a name="transformed-geometries"></a><span data-ttu-id="2d75e-143">Geometrías transformadas</span><span class="sxs-lookup"><span data-stu-id="2d75e-143">Transformed geometries</span></span>

<span data-ttu-id="2d75e-144">Hay varias maneras de transformar una geometría.</span><span class="sxs-lookup"><span data-stu-id="2d75e-144">There are multiple ways to transform a geometry.</span></span> <span data-ttu-id="2d75e-145">Puede usar el método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) de un destino de representación para transformar todo lo que dibuja el destino de representación, o puede asociar una transformación directamente a una geometría mediante el método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) para crear un [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d75e-145">You can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of a render target to transform everything that the render target draws, or you can associate a transform directly with a geometry by using the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) method to create an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span></span>

<span data-ttu-id="2d75e-146">El método que debe usar depende del efecto que desee.</span><span class="sxs-lookup"><span data-stu-id="2d75e-146">The method that you should use depends on the effect that you want.</span></span> <span data-ttu-id="2d75e-147">Cuando se usa el destino de representación para transformar y después representar una geometría, la transformación afecta a todo lo relacionado con la geometría, incluido el ancho de cualquier trazo que se haya aplicado.</span><span class="sxs-lookup"><span data-stu-id="2d75e-147">When you use the render target to transform and then render a geometry, the transform affects everything about the geometry, including the width of any stroke that you have applied.</span></span> <span data-ttu-id="2d75e-148">Por otro lado, cuando se usa un [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), la transformación solo afecta a las coordenadas que describen la forma.</span><span class="sxs-lookup"><span data-stu-id="2d75e-148">On the other hand, when you use an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), the transform affects only the coordinates that describe the shape.</span></span> <span data-ttu-id="2d75e-149">La transformación no afectará al grosor del trazo cuando se dibuje la geometría.</span><span class="sxs-lookup"><span data-stu-id="2d75e-149">The transformation will not affect the stroke thickness when the geometry is drawn.</span></span>

> [!Note]  
> <span data-ttu-id="2d75e-150">A partir de Windows 8, la transformación del mundo no afectará al grosor del trazo de los trazos con el [**\_ tipo de transformación trazo D2D1 \_ \_ \_ fijo**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)o el [**tipo de \_ transformación trazo D2D1 \_ \_ \_ fino**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span><span class="sxs-lookup"><span data-stu-id="2d75e-150">Starting with Windows 8 the world transform will not affect the stroke thickness of strokes with [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span> <span data-ttu-id="2d75e-151">Debe usar estos tipos de transformación para obtener trazos independientes de transformación.</span><span class="sxs-lookup"><span data-stu-id="2d75e-151">You should use these transform types to achieve transform independent strokes</span></span>

 

<span data-ttu-id="2d75e-152">En el ejemplo siguiente se crea una [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)y, a continuación, se dibuja sin transformarla.</span><span class="sxs-lookup"><span data-stu-id="2d75e-152">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), then draws it without transforming it.</span></span> <span data-ttu-id="2d75e-153">Genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="2d75e-153">It produces the output shown in the following illustration.</span></span>

![Ilustración de un rectángulo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="2d75e-155">En el ejemplo siguiente se usa el destino de representación para escalar la geometría en un factor de 3 y, a continuación, se dibuja.</span><span class="sxs-lookup"><span data-stu-id="2d75e-155">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="2d75e-156">En la ilustración siguiente se muestra el resultado de dibujar el rectángulo sin la transformación y con la transformación.</span><span class="sxs-lookup"><span data-stu-id="2d75e-156">The following illustration shows the result of drawing the rectangle without the transform and with the transform.</span></span> <span data-ttu-id="2d75e-157">Observe que el trazo es más grueso después de la transformación, aunque el grosor del trazo sea 1.</span><span class="sxs-lookup"><span data-stu-id="2d75e-157">Notice that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con un trazo más grueso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="2d75e-159">En el ejemplo siguiente se usa el método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) para escalar la geometría en un factor de 3 y, a continuación, se dibuja.</span><span class="sxs-lookup"><span data-stu-id="2d75e-159">The next example uses the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="2d75e-160">Genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="2d75e-160">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="2d75e-161">Observe que, aunque el rectángulo es mayor, su trazo no ha aumentado.</span><span class="sxs-lookup"><span data-stu-id="2d75e-161">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con el mismo grosor de trazo](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a><span data-ttu-id="2d75e-163">Geometrías como máscaras</span><span class="sxs-lookup"><span data-stu-id="2d75e-163">Geometries as masks</span></span>

<span data-ttu-id="2d75e-164">Puede usar un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) como máscara geométrica al llamar al método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-164">You can use an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object as a geometric mask when you call the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="2d75e-165">La máscara geométrica especifica el área de la capa que se compone en el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="2d75e-165">The geometric mask specifies the area of the layer that is composited into the render target.</span></span> <span data-ttu-id="2d75e-166">Para obtener más información, consulte la sección máscaras geométricas de la [información general sobre capas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2d75e-166">For more information, see the Geometric Masks section of the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="geometric-operations"></a><span data-ttu-id="2d75e-167">Operaciones geométricas</span><span class="sxs-lookup"><span data-stu-id="2d75e-167">Geometric operations</span></span>

<span data-ttu-id="2d75e-168">La interfaz [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) proporciona varias operaciones geométricas que puede usar para manipular y medir figuras geométricas.</span><span class="sxs-lookup"><span data-stu-id="2d75e-168">The [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) interface provides several geometric operations that you can use to manipulate and measure geometric figures.</span></span> <span data-ttu-id="2d75e-169">Por ejemplo, puede usarlos para calcular y devolver sus límites, comparar para ver cómo una geometría está relacionada espacialmente con otra (útil para la prueba de posicionamiento), calcular las áreas y longitudes, etc.</span><span class="sxs-lookup"><span data-stu-id="2d75e-169">For example, you can use them to calculate and return their bounds, compare to see how one geometry is spatially related to another (useful for hit testing), calculate the areas and lengths, and more.</span></span> <span data-ttu-id="2d75e-170">En la tabla siguiente se describen las operaciones geométricas comunes.</span><span class="sxs-lookup"><span data-stu-id="2d75e-170">The following table describes the common geometric operations.</span></span>



| <span data-ttu-id="2d75e-171">Operación</span><span class="sxs-lookup"><span data-stu-id="2d75e-171">Operation</span></span>                                                   | <span data-ttu-id="2d75e-172">Método</span><span class="sxs-lookup"><span data-stu-id="2d75e-172">Method</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d75e-173">Combinar</span><span class="sxs-lookup"><span data-stu-id="2d75e-173">Combine</span></span>                                                     | [<span data-ttu-id="2d75e-174">**CombineWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="2d75e-174">**CombineWithGeometry**</span></span>](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| <span data-ttu-id="2d75e-175">Límites/límites ampliados/recuperar límites, actualización de región sucia</span><span class="sxs-lookup"><span data-stu-id="2d75e-175">Bounds/ Widened Bounds/Retrieve Bounds, Dirty Region update</span></span> | <span data-ttu-id="2d75e-176">[**Wide**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span><span class="sxs-lookup"><span data-stu-id="2d75e-176">[**Widen**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span></span>                             |
| <span data-ttu-id="2d75e-177">Pruebas de posicionamiento</span><span class="sxs-lookup"><span data-stu-id="2d75e-177">Hit Testing</span></span>                                                 | <span data-ttu-id="2d75e-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span><span class="sxs-lookup"><span data-stu-id="2d75e-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span></span>                                             |
| <span data-ttu-id="2d75e-179">Carrera</span><span class="sxs-lookup"><span data-stu-id="2d75e-179">Stroke</span></span>                                                      | [<span data-ttu-id="2d75e-180">**StrokeContainsPoint**</span><span class="sxs-lookup"><span data-stu-id="2d75e-180">**StrokeContainsPoint**</span></span>](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| <span data-ttu-id="2d75e-181">De comparación</span><span class="sxs-lookup"><span data-stu-id="2d75e-181">Comparison</span></span>                                                  | [<span data-ttu-id="2d75e-182">**CompareWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="2d75e-182">**CompareWithGeometry**</span></span>](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| <span data-ttu-id="2d75e-183">Simplificación (quita arcos y curvas Bézier cuadráticas)</span><span class="sxs-lookup"><span data-stu-id="2d75e-183">Simplification (removes arcs and quadratic Bezier curves)</span></span>   | [<span data-ttu-id="2d75e-184">**Simplificar**</span><span class="sxs-lookup"><span data-stu-id="2d75e-184">**Simplify**</span></span>](id2d1geometry-simplify.md)                                                                                                                                 |
| <span data-ttu-id="2d75e-185">Teselación</span><span class="sxs-lookup"><span data-stu-id="2d75e-185">Tessellation</span></span>                                                | [<span data-ttu-id="2d75e-186">**Dividirlas**</span><span class="sxs-lookup"><span data-stu-id="2d75e-186">**Tessellate**</span></span>](id2d1geometry-tessellate.md)                                                                                                                             |
| <span data-ttu-id="2d75e-187">Esquema (quitar intersección)</span><span class="sxs-lookup"><span data-stu-id="2d75e-187">Outline (remove intersection)</span></span>                               | [<span data-ttu-id="2d75e-188">**Esquema**</span><span class="sxs-lookup"><span data-stu-id="2d75e-188">**Outline**</span></span>](id2d1geometry-outline.md)                                                                                                                                   |
| <span data-ttu-id="2d75e-189">Calcular el área o la longitud de una geometría</span><span class="sxs-lookup"><span data-stu-id="2d75e-189">Calculate the area or length of a geometry</span></span>                  | <span data-ttu-id="2d75e-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span><span class="sxs-lookup"><span data-stu-id="2d75e-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span></span> |



 

> [!Note]  
> <span data-ttu-id="2d75e-191">A partir de Windows 8, puede usar el método [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) en [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) para calcular el área o la longitud de una geometría.</span><span class="sxs-lookup"><span data-stu-id="2d75e-191">Starting in Windows 8, you can use the [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) method on the [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) to calculate the area or length of a geometry.</span></span>

 

### <a name="combining-geometries"></a><span data-ttu-id="2d75e-192">Combinar geometrías</span><span class="sxs-lookup"><span data-stu-id="2d75e-192">Combining geometries</span></span>

<span data-ttu-id="2d75e-193">Para combinar una geometría con otra, llame al método [**ID2D1Geometry:: CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-193">To combine one geometry with another, call the [**ID2D1Geometry::CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) method.</span></span> <span data-ttu-id="2d75e-194">Al combinar las geometrías, se especifica una de las cuatro maneras de realizar la operación de combinación: [**D2D1 \_ combine \_ Mode \_ Union**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Unión), [**D2D1 \_ combine \_ Mode \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**D2D1 \_ combine \_ Mode \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) y [**D2D1 \_ combine \_ Mode \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Exclude).</span><span class="sxs-lookup"><span data-stu-id="2d75e-194">When you combine the geometries, you specify one of the four ways to perform the combine operation: [**D2D1\_COMBINE\_MODE\_UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1\_COMBINE\_MODE\_INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1\_COMBINE\_MODE\_XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor), and [**D2D1\_COMBINE\_MODE\_EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude).</span></span> <span data-ttu-id="2d75e-195">En el ejemplo de código siguiente se muestran dos círculos que se combinan mediante el modo de combinación Union, donde el primer círculo tiene el punto central de (75, 75) y el radio de 50, y el segundo círculo tiene el punto central de (125, 75) y el radio de 50.</span><span class="sxs-lookup"><span data-stu-id="2d75e-195">The following code example shows two circles that are combined by using the union combine mode, where the first circle has the center point of (75, 75) and the radius of 50, and the second circle has the center point of (125, 75) and the radius of 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



<span data-ttu-id="2d75e-196">En la ilustración siguiente se muestran dos círculos combinados con un modo de combinación de Union.</span><span class="sxs-lookup"><span data-stu-id="2d75e-196">The following illustration shows two circles combined with a combine mode of union.</span></span>

![Ilustración de dos círculos superpuestos combinados en una Unión](images/combine-mode-union.png)

<span data-ttu-id="2d75e-198">Para ver las ilustraciones de todos los modos de combinación, consulte la [**\_ \_ enumeración del modo de combinación de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span><span class="sxs-lookup"><span data-stu-id="2d75e-198">For illustrations of all the combine modes, see the [**D2D1\_COMBINE\_MODE enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span></span>

### <a name="widen"></a><span data-ttu-id="2d75e-199">Ancha</span><span class="sxs-lookup"><span data-stu-id="2d75e-199">Widen</span></span>

<span data-ttu-id="2d75e-200">El método [**Wide**](id2d1geometry-widen.md) genera una nueva geometría cuyo relleno es equivalente a contornear la geometría existente y, a continuación, escribe el resultado en el objeto [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) especificado.</span><span class="sxs-lookup"><span data-stu-id="2d75e-200">The [**Widen**](id2d1geometry-widen.md) method generates a new geometry whose fill is equivalent to stroking the existing geometry, and then writes the result to the specified [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span> <span data-ttu-id="2d75e-201">En el ejemplo de código siguiente se llama a [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) en el objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-201">The following code example calls [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) on the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object.</span></span> <span data-ttu-id="2d75e-202">Si **Open** se realiza correctamente, llama a **Widening** en el objeto Geometry.</span><span class="sxs-lookup"><span data-stu-id="2d75e-202">If **Open** succeeds, it calls **Widen** on the geometry object.</span></span>


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a><span data-ttu-id="2d75e-203">Dividirlas</span><span class="sxs-lookup"><span data-stu-id="2d75e-203">Tessellate</span></span>

<span data-ttu-id="2d75e-204">El método [**dividirlas**](id2d1geometry-tessellate.md) crea un conjunto de triángulos de rebobinado en el sentido de las agujas del reloj que cubren la geometría después de que se transforme utilizando la matriz especificada y plana con la tolerancia especificada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-204">The [**Tessellate**](id2d1geometry-tessellate.md) method creates a set of clockwise-wound triangles that cover the geometry after it is transformed by using the specified matrix and flattened by using the specified tolerance.</span></span> <span data-ttu-id="2d75e-205">En el ejemplo de código siguiente se usa **dividirlas** para crear una lista de triángulos que representan *pPathGeometry*.</span><span class="sxs-lookup"><span data-stu-id="2d75e-205">The following code example uses **Tessellate** to create a list of triangles that represent *pPathGeometry*.</span></span> <span data-ttu-id="2d75e-206">Los triángulos se almacenan en un [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pmesh* y, a continuación, se transfieren a un miembro de clase, *m \_ pStrokeMesh*, para su uso posterior al representarse.</span><span class="sxs-lookup"><span data-stu-id="2d75e-206">The triangles are stored in an [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, then transferred to a class member, *m\_pStrokeMesh*, for later use when rendering.</span></span>


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a><span data-ttu-id="2d75e-207">FillContainsPoint y StrokeContainsPoint</span><span class="sxs-lookup"><span data-stu-id="2d75e-207">FillContainsPoint and StrokeContainsPoint</span></span>

<span data-ttu-id="2d75e-208">El método [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indica si el área rellenada por la geometría contiene el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="2d75e-208">The [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) method indicates whether the area filled by the geometry contains the specified point.</span></span> <span data-ttu-id="2d75e-209">Puede utilizar este método para realizar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="2d75e-209">You can use this method to do hit testing.</span></span> <span data-ttu-id="2d75e-210">En el ejemplo de código siguiente se llama a **FillContainsPoint** en un objeto [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , pasando un punto en (0,0) y una matriz de [**identidad**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .</span><span class="sxs-lookup"><span data-stu-id="2d75e-210">The following code example calls **FillContainsPoint** on an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) object, passing in a point at (0,0) and an [**Identity**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) matrix.</span></span>


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



<span data-ttu-id="2d75e-211">El método [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) determina si el trazo de la geometría contiene el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="2d75e-211">The [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) method determines whether the geometry's stroke contains the specified point.</span></span> <span data-ttu-id="2d75e-212">Puede utilizar este método para realizar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="2d75e-212">You can use this method to do hit testing.</span></span> <span data-ttu-id="2d75e-213">En el ejemplo de código siguiente se usa **StrokeContainsPoint**.</span><span class="sxs-lookup"><span data-stu-id="2d75e-213">The following code example uses **StrokeContainsPoint**.</span></span>


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a><span data-ttu-id="2d75e-214">Simplificación de </span><span class="sxs-lookup"><span data-stu-id="2d75e-214">Simplify</span></span>

<span data-ttu-id="2d75e-215">El método [**simplificar**](id2d1geometry-simplify.md) quita los arcos y las curvas Bézier cuadráticas de una geometría especificada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-215">The [**Simplify**](id2d1geometry-simplify.md) method removes arcs and quadratic Bezier curves from a specified geometry.</span></span> <span data-ttu-id="2d75e-216">Por lo tanto, la geometría resultante contiene solo líneas y, opcionalmente, curvas Bézier cúbicas.</span><span class="sxs-lookup"><span data-stu-id="2d75e-216">So, the resulting geometry contains only lines and, optionally, cubic Bezier curves.</span></span> <span data-ttu-id="2d75e-217">En el ejemplo de código siguiente se usa la **simplificación** para transformar una geometría con curvas Bézier en una geometría que solo contiene segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="2d75e-217">The following code example uses **Simplify** to transform a geometry with Bezier curves into a geometry that contains only line segments.</span></span>


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a><span data-ttu-id="2d75e-218">ComputeLength y ComputeArea</span><span class="sxs-lookup"><span data-stu-id="2d75e-218">ComputeLength and ComputeArea</span></span>

<span data-ttu-id="2d75e-219">El método [**ComputeLength**](id2d1geometry-computelength.md) calcula la longitud de la geometría especificada si cada segmento se desscribió en una línea.</span><span class="sxs-lookup"><span data-stu-id="2d75e-219">The [**ComputeLength**](id2d1geometry-computelength.md) method calculates the length of the specified geometry if each segment were unrolled into a line.</span></span> <span data-ttu-id="2d75e-220">Esto incluye el segmento de cierre implícito si la geometría está cerrada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-220">This includes the implicit closing segment if the geometry is closed.</span></span> <span data-ttu-id="2d75e-221">En el ejemplo de código siguiente se usa **ComputeLength** para calcular la longitud de un círculo especificado (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="2d75e-221">The following code example uses **ComputeLength** to compute the length of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



<span data-ttu-id="2d75e-222">El método [**ComputeArea**](id2d1geometry-computearea.md) calcula el área de la geometría especificada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-222">The [**ComputeArea**](id2d1geometry-computearea.md) method calculates the area of the specified geometry.</span></span> <span data-ttu-id="2d75e-223">En el ejemplo de código siguiente se usa **ComputeArea** para calcular el área de un círculo especificado (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="2d75e-223">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a><span data-ttu-id="2d75e-224">CompareWithGeometry</span><span class="sxs-lookup"><span data-stu-id="2d75e-224">CompareWithGeometry</span></span>

<span data-ttu-id="2d75e-225">El método [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) describe la intersección entre la geometría que llama a este método y la geometría especificada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-225">The [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) method describes the intersection between the geometry that calls this method and the specified geometry.</span></span> <span data-ttu-id="2d75e-226">Entre los valores posibles para la intersección se incluye la [**\_ relación de geometría \_ \_ D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disunion), la **relación de \_ geometría D2D1 \_ \_ está \_ contenida** (está contenida), la **relación de geometría de D2D1 \_ \_ \_ contiene** (Contains) y la coincidencia de la **relación de geometría de D2D1 \_ \_ \_** (superposición).</span><span class="sxs-lookup"><span data-stu-id="2d75e-226">The possible values for intersection include [**D2D1\_GEOMETRY\_RELATION\_DISJOINT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjoint), **D2D1\_GEOMETRY\_RELATION\_IS\_CONTAINED** (is contained), **D2D1\_GEOMETRY\_RELATION\_CONTAINS** (contains), and **D2D1\_GEOMETRY\_RELATION\_OVERLAP** (overlap).</span></span> <span data-ttu-id="2d75e-227">"disunion" significa que dos rellenos de geometría no forman una intersección.</span><span class="sxs-lookup"><span data-stu-id="2d75e-227">"disjoint" means that two geometry fills do not intersect at all.</span></span> <span data-ttu-id="2d75e-228">"está contenido" significa que la geometría está totalmente contenida en la geometría especificada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-228">"is contained" means that the geometry is completely contained by the specified geometry.</span></span> <span data-ttu-id="2d75e-229">"Contains" significa que la geometría contiene por completo la geometría especificada y "superposición" significa que las dos geometrías se superponen, pero ninguna contiene por completo.</span><span class="sxs-lookup"><span data-stu-id="2d75e-229">"contains" means that the geometry completely contains the specified geometry, and "overlap" means the two geometries overlap but neither completely contains the other.</span></span>

<span data-ttu-id="2d75e-230">En el ejemplo de código siguiente se muestra cómo comparar dos círculos que tienen el mismo radio de 50 pero que están desplazados por 50.</span><span class="sxs-lookup"><span data-stu-id="2d75e-230">The following code example shows how to compare two circles that have the same radius of 50 but are offset by 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a><span data-ttu-id="2d75e-231">Esquema</span><span class="sxs-lookup"><span data-stu-id="2d75e-231">Outline</span></span>

<span data-ttu-id="2d75e-232">El método de [**contorno**](id2d1geometry-outline.md) calcula el contorno de la geometría (una versión de la geometría en la que ninguna figura cruza o cualquier otra figura) y escribe el resultado en un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="2d75e-232">The [**Outline**](id2d1geometry-outline.md) method computes the outline of the geometry (a version of the geometry in which no figure crosses itself or any other figure) and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="2d75e-233">En el ejemplo de código siguiente se usa **Outline** para construir una geometría equivalente sin ninguna de las intersecciones.</span><span class="sxs-lookup"><span data-stu-id="2d75e-233">The following code example uses **Outline** to construct an equivalent geometry without any self-intersections.</span></span> <span data-ttu-id="2d75e-234">Usa la tolerancia de acoplamiento predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-234">It uses the default flattening tolerance.</span></span>


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a><span data-ttu-id="2d75e-235">GetBounds y GetWidenedBounds</span><span class="sxs-lookup"><span data-stu-id="2d75e-235">GetBounds and GetWidenedBounds</span></span>

<span data-ttu-id="2d75e-236">El método [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) recupera los límites de la geometría.</span><span class="sxs-lookup"><span data-stu-id="2d75e-236">The [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) method retrieves the bounds of the geometry.</span></span> <span data-ttu-id="2d75e-237">En el ejemplo de código siguiente se usa **GetBounds** para recuperar los límites de un círculo especificado (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="2d75e-237">The following code example uses **GetBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



<span data-ttu-id="2d75e-238">El método [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) recupera los límites de la geometría después de que se amplíe según el ancho del trazo y el estilo especificados y transformados por la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="2d75e-238">The [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) method retrieves the bounds of the geometry after it is widened by the specified stroke width and style and transformed by the specified matrix.</span></span> <span data-ttu-id="2d75e-239">En el ejemplo de código siguiente se usa **GetWidenedBounds** para recuperar los límites de un círculo especificado (**m \_ pCircleGeometry1**) después de que se amplíe según el ancho del trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="2d75e-239">The following code example uses **GetWidenedBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**) after it is widened by the specified stroke width.</span></span>


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a><span data-ttu-id="2d75e-240">ComputePointAtLength</span><span class="sxs-lookup"><span data-stu-id="2d75e-240">ComputePointAtLength</span></span>

<span data-ttu-id="2d75e-241">El método [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcula el vector de punto y tangente a la distancia especificada a lo largo de la geometría.</span><span class="sxs-lookup"><span data-stu-id="2d75e-241">The [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) method calculates the point and tangent vector at the specified distance along the geometry.</span></span> <span data-ttu-id="2d75e-242">En el ejemplo de código siguiente se usa **ComputePointAtLength**.</span><span class="sxs-lookup"><span data-stu-id="2d75e-242">The following code example uses **ComputePointAtLength**.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a><span data-ttu-id="2d75e-243">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d75e-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d75e-244">Información general sobre las geometrías de ruta</span><span class="sxs-lookup"><span data-stu-id="2d75e-244">Path Geometries Overview</span></span>](path-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="2d75e-245">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="2d75e-245">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 