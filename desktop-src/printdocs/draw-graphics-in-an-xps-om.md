---
description: En esta página se describe cómo dibujar gráficos en un OM XPS.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Dibujar gráficos en un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabbf8cfb821c80dfff43e2e7844331c8920f726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716027"
---
# <a name="draw-graphics-in-an-xps-om"></a><span data-ttu-id="858f6-103">Dibujar gráficos en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-103">Draw Graphics in an XPS OM</span></span>

<span data-ttu-id="858f6-104">En esta página se describe cómo dibujar gráficos en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="858f6-104">This page describes how to draw graphics in an XPS OM.</span></span>

<span data-ttu-id="858f6-105">Para dibujar gráficos basados en vectores en una página, cree una instancia de una interfaz [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) , rellénelo con el contenido deseado y agréguelo a la lista de objetos visuales de la página o Canvas.</span><span class="sxs-lookup"><span data-stu-id="858f6-105">To draw vector-based graphics in a page, instantiate an [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface, populate it with the desired content, and add it to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="858f6-106">Una interfaz **IXpsOMPath** contiene propiedades de una forma basada en vectores como el contorno, el color de relleno, el estilo de línea y el color de línea.</span><span class="sxs-lookup"><span data-stu-id="858f6-106">An **IXpsOMPath** interface contains such properties of a vector-based shape as the outline, fill color, line style, and line color.</span></span> <span data-ttu-id="858f6-107">La forma de la ruta de acceso se especifica mediante una interfaz [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) , que contiene una colección de interfaces [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) y, opcionalmente, una interfaz [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) .</span><span class="sxs-lookup"><span data-stu-id="858f6-107">The path's shape is specified by an [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface, which contains a collection of [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interfaces and, optionally, an [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) interface.</span></span> <span data-ttu-id="858f6-108">Puede usar cualquier interfaz que herede de la interfaz [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) para rellenar el perímetro de la ruta de acceso y el interior de la forma que describe la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="858f6-108">You can use any interface that inherits from the [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) interface to fill the perimeter of the path and the interior of the shape that is described by the path.</span></span>

<span data-ttu-id="858f6-109">Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="858f6-109">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="858f6-110">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="858f6-110">Code Example</span></span>

<span data-ttu-id="858f6-111">En el ejemplo de código siguiente se crea una ruta de acceso simple que describe un rectángulo que se rellena con un solo color.</span><span class="sxs-lookup"><span data-stu-id="858f6-111">The following code example creates a simple path that describes a rectangle that is filled with a single color.</span></span>

### <a name="create-the-stroke-and-the-fill-brushes"></a><span data-ttu-id="858f6-112">Crear el trazo y los pinceles de relleno</span><span class="sxs-lookup"><span data-stu-id="858f6-112">Create the stroke and the fill brushes</span></span>

<span data-ttu-id="858f6-113">En la primera sección del ejemplo de código se crea el [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) que se usará para rellenar el objeto de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="858f6-113">The first section of the code example creates the [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) that will be used to fill the path object.</span></span>


```C++
    HRESULT               hr = S_OK;

    XPS_COLOR             xpsColor;
    IXpsOMSolidColorBrush *xpsFillBrush = NULL;
    IXpsOMSolidColorBrush *xpsStrokeBrush = NULL;

    // Set the fill brush color to RED.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColor,
        NULL,          // color profile resource
        &xpsFillBrush);
    // The color profile resource parameter is NULL because
    //  this color type does not use a color profile resource.

    // Set the stroke brush color to BLACK.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0x00;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
            &xpsColor,
            NULL, // This color type does not use a color profile resource.
            &xpsStrokeBrush);

    // The brushes are released below after they have been used.
```



### <a name="define-the-shape"></a><span data-ttu-id="858f6-114">Definir la forma</span><span class="sxs-lookup"><span data-stu-id="858f6-114">Define the shape</span></span>

<span data-ttu-id="858f6-115">En la segunda sección del ejemplo de código se crea la interfaz [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) .</span><span class="sxs-lookup"><span data-stu-id="858f6-115">The second section of the code example creates the [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface.</span></span> <span data-ttu-id="858f6-116">Después crea la interfaz [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) que especifica la forma de la figura y agrega la figura a la interfaz **IXpsOMGeometry** .</span><span class="sxs-lookup"><span data-stu-id="858f6-116">It then creates the [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interface that specifies the figure's shape, and adds the figure to the **IXpsOMGeometry** interface.</span></span> <span data-ttu-id="858f6-117">En el ejemplo se crea un rectángulo especificado por *Rect*.</span><span class="sxs-lookup"><span data-stu-id="858f6-117">The example creates a rectangle that is specified by *rect*.</span></span> <span data-ttu-id="858f6-118">Los segmentos deben definirse solo para tres de los cuatro lados del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="858f6-118">Segments must be defined for only three of the four sides of the rectangle.</span></span> <span data-ttu-id="858f6-119">El perímetro de la forma, en este caso, el rectángulo comienza en el punto inicial y se extiende según se define en los segmentos de la figura Geometry.</span><span class="sxs-lookup"><span data-stu-id="858f6-119">The perimeter of the shape, the rectangle in this case, starts from the start point and extends as defined by the segments of the geometry figure.</span></span> <span data-ttu-id="858f6-120">Al establecer la propiedad **IsClosed** en **true** , se indica que el rectángulo se cierra agregando un segmento adicional que conecta el final del último segmento al punto inicial.</span><span class="sxs-lookup"><span data-stu-id="858f6-120">Setting the **IsClosed** property to **TRUE** indicates that the rectangle is closed by adding one additional segment that connects the end of the last segment to the start point.</span></span>


```C++
    // rect is initialized outside of the sample and 
    //  contains the coordinates of the rectangular geometry to create.
    XPS_RECT                            rect = {0,0,100,100};       

    HRESULT                             hr = S_OK;
    IXpsOMGeometryFigure                *rectFigure;
    IXpsOMGeometry                      *imageRectGeometry;
    IXpsOMGeometryFigureCollection      *geomFigureCollection;

    // Define the start point and create an empty figure.
    XPS_POINT                           startPoint = {rect.x, rect.y};
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    // Define the segments of the geometry figure.
    //  First, define the type of each segment.
    XPS_SEGMENT_TYPE segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE,  // each segment is a straight line
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // Define the x and y coordinates of each corner of the figure
    //  the start point has already been defined so only the 
    //  remaining three corners need to be defined.
    FLOAT segmentData[6] = {
        rect.x,                (rect.y + rect.height),
        (rect.x + rect.width), (rect.y + rect.height), 
        (rect.x + rect.width), rect.y 
    };

    // Describe if the segments are stroked (that is if the segment lines
    //  should be drawn as a line).
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE // Yes, draw each of the segment lines.
    };

    // Add the segment data to the figure.
    hr = rectFigure->SetSegments(
                        3, 
                        6, 
                        segmentTypes, 
                        segmentData, 
                        segmentStrokes);

    // Set the closed and filled properties of the figure.
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
 
    // Create the geometry object.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    
    // Get a pointer to the figure collection interface of the geometry...
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );

    // ...and then add the figure created above to this geometry.
    hr = geomFigureCollection->Append( rectFigure );
    // If not needed for anything else, release the rectangle figure.
    rectFigure->Release();

    // when done adding figures, release the figure collection. 
    geomFigureCollection->Release();

    //  When done with the geometry object, release the object.
    // imageRectGeometry->Release();
    //  In this case, imageRectGeometry is used in the next sample
    //  so the geometry object is not released, yet.
    
```



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a><span data-ttu-id="858f6-121">Crear la ruta de acceso y agregarla a la colección visual</span><span class="sxs-lookup"><span data-stu-id="858f6-121">Create the path and add it to the visual collection</span></span>

<span data-ttu-id="858f6-122">La sección final de este ejemplo de código crea y configura el objeto de ruta de acceso y, a continuación, lo agrega a la lista de objetos visuales de la página.</span><span class="sxs-lookup"><span data-stu-id="858f6-122">The final section of this code example creates and configures the path object, then adds it to the page's list of visual objects.</span></span>


```C++
    HRESULT                    hr = S_OK;
    // The page interface pointer is initialized outside of this sample.
    IXpsOMPath                *rectPath = NULL;
    IXpsOMVisualCollection    *pageVisuals = NULL;

    // Create the new path object.
    hr = xpsFactory->CreatePath( &rectPath );

    // Add the geometry to the path.
    //  imageRectGeometry is initialized outside of this example.
    hr = rectPath->SetGeometryLocal( imageRectGeometry );

    // Set the short description of the path to provide
    //  a textual description of the object for accessibility.
    hr = rectPath->SetAccessibilityShortDescription( L"Red Rectangle" );
    
    // Set the fill and stroke brushes to use the brushes 
    //  created in the first section.
    hr = rectPath->SetFillBrushLocal( xpsFillBrush );
    hr = rectPath->SetStrokeBrushLocal( xpsStrokeBrush);

    // Get the visual collection of this page and add this path to it.
    hr = xpsPage->GetVisuals( &pageVisuals );
    hr = pageVisuals->Append( rectPath );
    // If not needed for anything else, release the rectangle path.
    rectPath->Release();
    
    // When done with the visual collection, release it.
    pageVisuals->Release();

    // When finished with the brushes, release the interface pointers.
    if (NULL != xpsFillBrush) xpsFillBrush->Release();
    if (NULL != xpsStrokeBrush) xpsStrokeBrush->Release();

    // When done with the geometry interface, release it.
    imageRectGeometry->Release();

    // When done with the path interface, release it.
    rectPath->Release();

```



## <a name="best-practices"></a><span data-ttu-id="858f6-123">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="858f6-123">Best Practices</span></span>

<span data-ttu-id="858f6-124">Agregue una descripción textual de la forma especificada por la interfaz [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) .</span><span class="sxs-lookup"><span data-stu-id="858f6-124">Add a textual description of the shape that is specified by the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface.</span></span> <span data-ttu-id="858f6-125">Para beneficiarse de los usuarios con discapacidad visual, use los métodos [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) y [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) para proporcionar contenido textual para características de soporte técnico de accesibilidad, como lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="858f6-125">For the benefit of visually impaired users, use the [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) and [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) methods to provide textual content for accessibility support features, such as screen readers.</span></span>

## <a name="additional-information"></a><span data-ttu-id="858f6-126">Información adicional</span><span class="sxs-lookup"><span data-stu-id="858f6-126">Additional Information</span></span>

<span data-ttu-id="858f6-127">En el ejemplo de código de esta página se usa una interfaz [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) como pincel de relleno y pincel de trazo para la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="858f6-127">The code example on this page uses an [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) interface as the fill brush and stroke brush for the path.</span></span> <span data-ttu-id="858f6-128">Además de la interfaz **IXpsOMSolidColorBrush** , puede utilizar una interfaz [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)o [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) .</span><span class="sxs-lookup"><span data-stu-id="858f6-128">In addition to the **IXpsOMSolidColorBrush** interface, you can use an [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush), or [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) interface.</span></span>

<span data-ttu-id="858f6-129">El trazo es la línea que se puede dibujar alrededor del perímetro de la ilustración.</span><span class="sxs-lookup"><span data-stu-id="858f6-129">The stroke is the line that can be drawn around the perimeter of the figure.</span></span> <span data-ttu-id="858f6-130">La [especificación de papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) admite muchos estilos de línea de trazo diferentes.</span><span class="sxs-lookup"><span data-stu-id="858f6-130">The [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supports many different stroke line styles.</span></span> <span data-ttu-id="858f6-131">Para especificar el estilo de línea del trazo, establezca las propiedades del trazo con los siguientes métodos de la interfaz [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) :</span><span class="sxs-lookup"><span data-stu-id="858f6-131">To specify the stroke line style, set the stroke properties with the following methods of the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface:</span></span>

-   <span data-ttu-id="858f6-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) o [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) para establecer el pincel de trazo</span><span class="sxs-lookup"><span data-stu-id="858f6-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) or [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) to set the stroke brush</span></span>
-   <span data-ttu-id="858f6-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) para obtener la colección de guiones de trazo que describe los trazos</span><span class="sxs-lookup"><span data-stu-id="858f6-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) to get the stroke dash collection that describes the strokes</span></span>
-   <span data-ttu-id="858f6-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) y [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) para describir el aspecto de un trazo discontinuo</span><span class="sxs-lookup"><span data-stu-id="858f6-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to and [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) to describe the appearance of a dashed stroke</span></span>
-   <span data-ttu-id="858f6-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) y [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) para definir el estilo de finalización de línea</span><span class="sxs-lookup"><span data-stu-id="858f6-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) and [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) to define the line termination style</span></span>
-   <span data-ttu-id="858f6-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) y [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) para describir cómo se unen los segmentos</span><span class="sxs-lookup"><span data-stu-id="858f6-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) and [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) to describe how the segments are joined</span></span>
-   <span data-ttu-id="858f6-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) para establecer el grosor del trazo</span><span class="sxs-lookup"><span data-stu-id="858f6-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) to set the stroke thickness</span></span>

## <a name="related-topics"></a><span data-ttu-id="858f6-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="858f6-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="858f6-139">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="858f6-139">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="858f6-140">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-140">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="858f6-141">Escribir texto en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-141">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="858f6-142">Colocar imágenes en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-142">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="858f6-143">Escribir un OM XPS en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-143">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="858f6-144">Imprimir un OM XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-144">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="858f6-145">**Se usa en esta página**</span><span class="sxs-lookup"><span data-stu-id="858f6-145">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="858f6-146">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="858f6-146">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="858f6-147">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="858f6-147">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="858f6-148">**IXpsOMGeometryFigure**</span><span class="sxs-lookup"><span data-stu-id="858f6-148">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="858f6-149">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="858f6-149">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="858f6-150">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="858f6-150">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="858f6-151">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="858f6-151">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="858f6-152">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="858f6-152">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="858f6-153">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="858f6-153">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="858f6-154">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="858f6-154">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="858f6-155">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="858f6-155">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="858f6-156">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-156">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="858f6-157">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="858f6-157">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="858f6-158">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="858f6-158">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
