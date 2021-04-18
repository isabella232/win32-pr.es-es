---
description: En el ejemplo de análisis de tinta básico se muestra cómo la clase InkAnalyzer divide la tinta en varios segmentos de palabras y de dibujo. Este ejemplo es una versión actualizada del ejemplo de divisor de tinta.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Ejemplo básico de análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94ac73ca9049169c6e406059665a66e8eaa6f3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720306"
---
# <a name="basic-ink-analysis-sample"></a><span data-ttu-id="33217-103">Ejemplo básico de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="33217-103">Basic Ink Analysis Sample</span></span>

<span data-ttu-id="33217-104">En el ejemplo de análisis de tinta básico se muestra cómo la clase [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) divide la tinta en varios segmentos de palabras y de dibujo.</span><span class="sxs-lookup"><span data-stu-id="33217-104">The Basic Ink Analysis sample shows how the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class divides ink into various word and drawing segments.</span></span>

<span data-ttu-id="33217-105">Este ejemplo es una versión actualizada del [ejemplo de divisor de tinta](ink-divider-sample.md).</span><span class="sxs-lookup"><span data-stu-id="33217-105">This sample is an updated version of the [Ink Divider Sample](ink-divider-sample.md).</span></span> <span data-ttu-id="33217-106">Mientras que el ejemplo de divisor de tinta utiliza la clase [divisor](/previous-versions/ms839398(v=msdn.10)) , en este ejemplo se usa la API InkAnalysis más reciente y preferida.</span><span class="sxs-lookup"><span data-stu-id="33217-106">Whereas the Ink Divider Sample uses the [Divider](/previous-versions/ms839398(v=msdn.10)) class, this sample uses the newer and preferred InkAnalysis API.</span></span> <span data-ttu-id="33217-107">La API InkAnalysis combina el [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) y el divisor en una API y expande la funcionalidad de ambos.</span><span class="sxs-lookup"><span data-stu-id="33217-107">The InkAnalysis API combines the [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) and Divider into one API and expands on the functionality of both.</span></span>

<span data-ttu-id="33217-108">Al actualizar el formulario, el ejemplo dibuja un rectángulo alrededor de cada unidad analizada: palabras, líneas, párrafos, regiones de escritura, dibujos y viñetas.</span><span class="sxs-lookup"><span data-stu-id="33217-108">When you update the form, the sample draws a rectangle around each analyzed unit: words, lines, paragraphs, writing regions, drawings and bullets.</span></span> <span data-ttu-id="33217-109">El formulario usa colores diferentes para las distintas unidades.</span><span class="sxs-lookup"><span data-stu-id="33217-109">The form uses different colors for the different units.</span></span> <span data-ttu-id="33217-110">Los rectángulos también se amplían en diferentes cantidades para asegurarse de que ningún rectángulo esté oculto por otros.</span><span class="sxs-lookup"><span data-stu-id="33217-110">The rectangles are also enlarged by different amounts to ensure that no one rectangle is obscured by any others.</span></span>

<span data-ttu-id="33217-111">En la tabla siguiente se especifica el color y la ampliación de cada unidad analizada.</span><span class="sxs-lookup"><span data-stu-id="33217-111">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="33217-112">Unidad analizada</span><span class="sxs-lookup"><span data-stu-id="33217-112">Analyzed unit</span></span>             | <span data-ttu-id="33217-113">Color del rectángulo</span><span class="sxs-lookup"><span data-stu-id="33217-113">Color of rectangle</span></span> | <span data-ttu-id="33217-114">Ampliación de rectángulo (píxeles)</span><span class="sxs-lookup"><span data-stu-id="33217-114">Rectangle enlargement (pixels)</span></span> |
|---------------------------|--------------------|--------------------------------|
| <span data-ttu-id="33217-115">Word</span><span class="sxs-lookup"><span data-stu-id="33217-115">Word</span></span><br/>           | <span data-ttu-id="33217-116">Verde</span><span class="sxs-lookup"><span data-stu-id="33217-116">Green</span></span><br/>   | <span data-ttu-id="33217-117">1</span><span class="sxs-lookup"><span data-stu-id="33217-117">1</span></span><br/>                   |
| <span data-ttu-id="33217-118">Línea</span><span class="sxs-lookup"><span data-stu-id="33217-118">Line</span></span><br/>           | <span data-ttu-id="33217-119">Fucsia</span><span class="sxs-lookup"><span data-stu-id="33217-119">Magenta</span></span><br/> | <span data-ttu-id="33217-120">3</span><span class="sxs-lookup"><span data-stu-id="33217-120">3</span></span><br/>                   |
| <span data-ttu-id="33217-121">Paragraph</span><span class="sxs-lookup"><span data-stu-id="33217-121">Paragraph</span></span><br/>      | <span data-ttu-id="33217-122">Azul</span><span class="sxs-lookup"><span data-stu-id="33217-122">Blue</span></span><br/>    | <span data-ttu-id="33217-123">5</span><span class="sxs-lookup"><span data-stu-id="33217-123">5</span></span><br/>                   |
| <span data-ttu-id="33217-124">Región de escritura</span><span class="sxs-lookup"><span data-stu-id="33217-124">Writing region</span></span><br/> | <span data-ttu-id="33217-125">Amarillo</span><span class="sxs-lookup"><span data-stu-id="33217-125">Yellow</span></span><br/>  | <span data-ttu-id="33217-126">7</span><span class="sxs-lookup"><span data-stu-id="33217-126">7</span></span><br/>                   |
| <span data-ttu-id="33217-127">Dibujo</span><span class="sxs-lookup"><span data-stu-id="33217-127">Drawing</span></span><br/>        | <span data-ttu-id="33217-128">Rojo</span><span class="sxs-lookup"><span data-stu-id="33217-128">Red</span></span><br/>     | <span data-ttu-id="33217-129">1</span><span class="sxs-lookup"><span data-stu-id="33217-129">1</span></span><br/>                   |
| <span data-ttu-id="33217-130">Viñeta</span><span class="sxs-lookup"><span data-stu-id="33217-130">Bullet</span></span><br/>         | <span data-ttu-id="33217-131">Naranja</span><span class="sxs-lookup"><span data-stu-id="33217-131">Orange</span></span><br/>  | <span data-ttu-id="33217-132">1</span><span class="sxs-lookup"><span data-stu-id="33217-132">1</span></span><br/>                   |



 

<span data-ttu-id="33217-133">Puede borrar trazos en el formulario.</span><span class="sxs-lookup"><span data-stu-id="33217-133">You can erase strokes in the form.</span></span> <span data-ttu-id="33217-134">En la aplicación de ejemplo, puede alternar entre el modo de lápiz y de borrado para cambiar la función del lápiz.</span><span class="sxs-lookup"><span data-stu-id="33217-134">In the sample application, you can toggle between Ink and Erase mode to change the function of the pen.</span></span>


```C++
        private void miInk_Click(object sender, System.EventArgs e)
        {
            // Turn on the inking mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Ink;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = true;
            miErase.Checked = false;

            // Update the UI
            this.Refresh();
        }

        private void miErase_Click(object sender, System.EventArgs e)
        {
            // Turn on the ink deletion mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Delete;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = false;
            miErase.Checked = true;

            // Update the UI
            this.Refresh();
        }
```



<span data-ttu-id="33217-135">Cuando se agregan o eliminan trazos, los ejemplos actualizan el [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="33217-135">When you add or delete strokes, the samples updates the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span></span>


```C++
        private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
        {
            // Filter out the eraser stroke.
            if (InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
            {

                // Add the new stroke to the InkAnalyzer's stroke collection
                myInkAnalyzer.AddStroke(e.Stroke);

                if (miAutomaticLayoutAnalysis.Checked)
                {
                    // Invoke an analysis operation on the background thread
                    myInkAnalyzer.BackgroundAnalyze();
                }
            }
        }

        void myInkOverlay_StrokeDeleting(object sender, InkOverlayStrokesDeletingEventArgs e)
        {
            // Remove the strokes to be deleted from the InkAnalyzer's stroke collection
            myInkAnalyzer.RemoveStrokes(e.StrokesToDelete);

            // If automatic layout analysis is turned on, analyze the ink on the background thread
            if ( miAutomaticLayoutAnalysis.Checked )
            {
                // Invoke an analysis operation on the background thread
                myInkAnalyzer.BackgroundAnalyze ( );
            }
        }
```



<span data-ttu-id="33217-136">Tenga en cuenta que en el menú modo, el análisis de diseño automático está activado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="33217-136">Notice that in the Mode menu, Automatic Layout Analysis is on by default.</span></span> <span data-ttu-id="33217-137">Con esta opción seleccionada, los controladores de eventos [Stroke](/previous-versions/ms835344(v=msdn.10)) y [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) del objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) llaman al método [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) cada vez que se crea o se elimina un trazo.</span><span class="sxs-lookup"><span data-stu-id="33217-137">With this option selected, the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Stroke](/previous-versions/ms835344(v=msdn.10)) and [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) event handlers call the [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method every time a stroke is created or deleted.</span></span>

> [!Note]  
> <span data-ttu-id="33217-138">Si se llama al método [Analyze](/previous-versions/ms568971(v=vs.100)) del objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) con más de unos pocos trazos, se crea un retraso perceptible en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="33217-138">Calling the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object's [Analyze](/previous-versions/ms568971(v=vs.100)) method with more than a few strokes present creates a noticeable delay in an application.</span></span> <span data-ttu-id="33217-139">Esto se debe a que ANALYZE es una operación sincrónica de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="33217-139">This is because Analyze is a synchronous ink analysis operation.</span></span> <span data-ttu-id="33217-140">En la práctica, llame al método Analyze solo cuando necesite el resultado.</span><span class="sxs-lookup"><span data-stu-id="33217-140">In practice, call the Analyze method only when you need the result.</span></span> <span data-ttu-id="33217-141">De lo contrario, use el método [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) asincrónico, como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="33217-141">Otherwise use the asynchronous [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method, as shown in the sample.</span></span>

 

## <a name="handling-the-analysis-results"></a><span data-ttu-id="33217-142">Controlar los resultados del análisis</span><span class="sxs-lookup"><span data-stu-id="33217-142">Handling the Analysis Results</span></span>

<span data-ttu-id="33217-143">En el ejemplo se crean dos matrices para contener los distintos rectángulos, ya sea horizontal o girado.</span><span class="sxs-lookup"><span data-stu-id="33217-143">The sample creates two arrays to hold the various rectangles, either horizontal or rotated.</span></span> <span data-ttu-id="33217-144">Use un cuadro de límite girado para obtener el ángulo en el que se escribe una línea de palabras.</span><span class="sxs-lookup"><span data-stu-id="33217-144">Use a rotated bounding box to get the angle on which a line of words is written.</span></span> <span data-ttu-id="33217-145">En el ejemplo se muestran las propiedades devueltas por [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) y se muestra el cuadro de límite o el cuadro de límite girado (dependiendo de la selección del menú).</span><span class="sxs-lookup"><span data-stu-id="33217-145">The sample shows the properties returned by the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) and displays the bounding box or the rotated bounding box (depending on the menu selection).</span></span>


```C++
      private Rectangle[] GetHorizontalBBoxes(Guid nodeType, int inflate)
        {
            // Declare the array of rectangles to hold the result
            Rectangle[] analysisRects;

            // Get the division units from the division result of division type
            ContextNodeCollection nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // If there is at least one unit, we construct the rectangles
            if ((null != nodes) && (0 < nodes.Count))
            {
                // We need to convert rectangles from ink units to
                // pixel units. For that, we need Graphics object
                // to pass to InkRenderer.InkSpaceToPixel method
                using (Graphics g = drawArea.CreateGraphics())
                {
                    // Construct the rectangles
                    analysisRects = new Rectangle[nodes.Count];

                    // InkRenderer.InkSpaceToPixel takes Point as parameter. 
                    // Create two Point objects to point to (Top, Left) and
                    // (Width, Height) properties of rectangle. (Width, Height)
                    // is used instead of (Right, Bottom) because (Right, Bottom)
                    // are read-only properties on Rectangle
                    Point ptLocation = new Point();
                    Point ptSize = new Point();

                    // Index into the bounding boxes
                    int i = 0;

                    // Iterate through the collection of division units to obtain the bounding boxes
                    foreach (ContextNode node in nodes)
                    {
                        // Get the bounding box of the strokes of the division unit
                        analysisRects[i] = node.Location.GetBounds();

                        // The bounding box is in ink space unit. Convert them into pixel unit. 
                        ptLocation = analysisRects[i].Location;
                        ptSize.X = analysisRects[i].Width;
                        ptSize.Y = analysisRects[i].Height;

                        // Convert the Location from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptLocation);

                        // Convert the Size from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptSize);

                        // Assign the result back to the corresponding properties
                        analysisRects[i].Location = ptLocation;
                        analysisRects[i].Width = ptSize.X;
                        analysisRects[i].Height = ptSize.Y;

                        // Inflate the rectangle by inflate pixels in both directions
                        analysisRects[i].Inflate(inflate, inflate);

                        // Increment the index
                        ++i;
                    }

                } // Relinquish the Graphics object
            }
            else
            {
                // Otherwise we return null
                analysisRects = null;
            }

            // Return the Rectangle[] object
            return analysisRects;
        }

        private System.Collections.ArrayList GetRotatedBBoxes(Guid nodeType, int inflate)
        {
            //Find the correct collection of results nodes.
            ContextNodeCollection Nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // Declare the array list to hold the results; 
            // This array represents the four points of a rectangle, with the first point
            // copied again to complete the cycle of points.

            ArrayList polygonPoints = new ArrayList(Nodes.Count);

            // Cycle through each results node, get and convert the
            // rotated bounding box points
            foreach (ContextNode node in Nodes)
            {
                //Declare the point array
                Point[] rotatedBoundingBox = null;

                //Switch on the type of ContextNode to cast into the
                //appropriate type.  This is required to access the 
                //type specific property "RotatedBoundingBox" which
                //is not found on all ContextNode types.
                if (nodeType == ContextNodeType.InkWord)
                {
                    rotatedBoundingBox = ((InkWordNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Line)
                {
                    rotatedBoundingBox = ((LineNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Paragraph)
                {
                    rotatedBoundingBox = ((ParagraphNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.WritingRegion ||
                         nodeType == ContextNodeType.InkDrawing ||
                         nodeType == ContextNodeType.InkBullet )
                {

                    // Rotated Bounding Boxes are not a supported option for 
                    // Writing Regions or Drawings.  We return the axis aligned 
                    // bounding box instead
                    Rectangle rect = node.Location.GetBounds();

                    // We need to create a looped list of 4 points to be consistent
                    // with the way InkAnalysis represents rotated bounding boxes.  
                    rotatedBoundingBox = new Point[4];

                    rotatedBoundingBox[0] = new Point(rect.X, rect.Y);
                    rotatedBoundingBox[1] = new Point(rect.Right, rect.Y);
                    rotatedBoundingBox[2] = new Point(rect.Right, rect.Bottom);
                    rotatedBoundingBox[3] = new Point(rect.X, rect.Bottom);

                }


                if (null != rotatedBoundingBox)
                {
                    // We need to convert rectangles from ink units to
                    // pixel units. For that, we need Graphics object
                    // to pass to InkRenderer.InkSpaceToPixel method
                    using (Graphics g = drawArea.CreateGraphics())
                    {
                        // convert each of the points from ink space to pixel space
                        for (int i = 0; i < rotatedBoundingBox.Length; i++)
                        {
                            myInkOverlay.Renderer.InkSpaceToPixel(g, ref rotatedBoundingBox[i]);
                        }

                        //inflate the points by calling helper method
                        InflateHelperMethod(ref rotatedBoundingBox, inflate);

                        // increment the node portion of the polygonPoints array
                        polygonPoints.Add(rotatedBoundingBox);
                    }
                }
            }
            //Return the results
            return polygonPoints;
        }
```



<span data-ttu-id="33217-146">El analizador calcula [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) durante el análisis.</span><span class="sxs-lookup"><span data-stu-id="33217-146">The parser calculates [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) during analysis.</span></span> <span data-ttu-id="33217-147">Puede tener acceso a la información de los cuadros de límite girados en la aplicación por una serie de motivos útiles:</span><span class="sxs-lookup"><span data-stu-id="33217-147">You can access the information from the rotated bounding boxes in your application for a number of useful reasons:</span></span>

-   <span data-ttu-id="33217-148">Detectar o dibujar los límites de una sola línea, párrafo u otra unidad.</span><span class="sxs-lookup"><span data-stu-id="33217-148">Detect or draw the bounds of a single line, paragraph, or other unit.</span></span>
-   <span data-ttu-id="33217-149">Determine el ángulo en el que se escribe una línea o un párrafo.</span><span class="sxs-lookup"><span data-stu-id="33217-149">Determine the angle at which a line or paragraph is written.</span></span>
-   <span data-ttu-id="33217-150">Implementar características como la selección de una línea, un párrafo u otra unidad.</span><span class="sxs-lookup"><span data-stu-id="33217-150">Implement features such as selection for a line, paragraph, or other unit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33217-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33217-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33217-152">Reconocimiento básico y análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="33217-152">Basic Recognition and Ink Analysis</span></span>](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[<span data-ttu-id="33217-153">Ejemplo de formulario de papel digitalizado</span><span class="sxs-lookup"><span data-stu-id="33217-153">Scanned Paper Form Sample</span></span>](scanned-paper-form-sample.md)
</dt> <dt>

[<span data-ttu-id="33217-154">Ejemplo de divisor de tinta</span><span class="sxs-lookup"><span data-stu-id="33217-154">Ink Divider Sample</span></span>](ink-divider-sample.md)
</dt> </dl>

 

