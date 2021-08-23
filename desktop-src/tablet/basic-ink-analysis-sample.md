---
description: En el ejemplo Análisis básico de entrada de lápiz se muestra cómo la clase InkAnalyzer divide la entrada de lápiz en varios segmentos de palabra y dibujo. Este ejemplo es una versión actualizada del ejemplo de divisor de lápiz.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Ejemplo básico de análisis de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ab307deac8ac58a741b0c7f332986b09074f4f5c6a8afa53f0156a94916bf16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660835"
---
# <a name="basic-ink-analysis-sample"></a>Ejemplo básico de análisis de entrada de lápiz

En el ejemplo Análisis básico de entrada de lápiz se muestra cómo [la clase InkAnalyzer](/previous-versions/ms583671(v=vs.100)) divide la entrada de lápiz en varios segmentos de palabra y dibujo.

Este ejemplo es una versión actualizada del ejemplo [de divisor de lápiz.](ink-divider-sample.md) Mientras que el ejemplo de divisor de entrada de lápiz usa la [clase Divider,](/previous-versions/ms839398(v=msdn.10)) en este ejemplo se usa la API InkAnalysis más reciente y preferida. InkAnalysis API combina [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) y Divider en una API y amplía la funcionalidad de ambos.

Al actualizar el formulario, el ejemplo dibuja un rectángulo alrededor de cada unidad analizada: palabras, líneas, párrafos, regiones de escritura, dibujos y viñetas. El formulario usa colores diferentes para las distintas unidades. Los rectángulos también se amplían en diferentes cantidades para asegurarse de que ningún otro rectángulo esté oculto por ningún otro.

En la tabla siguiente se especifica el color y la temperatura de cada unidad analizada.



| Unidad analizada             | Color del rectángulo | Rectángulo de rectángulo (píxeles) |
|---------------------------|--------------------|--------------------------------|
| Word<br/>           | Verde<br/>   | 1<br/>                   |
| Línea<br/>           | Fucsia<br/> | 3<br/>                   |
| Paragraph<br/>      | Azul<br/>    | 5<br/>                   |
| Región de escritura<br/> | Amarillo<br/>  | 7<br/>                   |
| Dibujo<br/>        | Rojo<br/>     | 1<br/>                   |
| Bala<br/>         | Naranja<br/>  | 1<br/>                   |



 

Puede borrar trazos en el formulario. En la aplicación de ejemplo, puede alternar entre el modo de entrada manuscrita y el modo de borrado para cambiar la función del lápiz.


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



Al agregar o eliminar trazos, los ejemplos actualiza [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).


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



Tenga en cuenta que, en el menú Modo, Análisis de diseño automático está seleccionado de forma predeterminada. Con esta opción seleccionada, los controladores de eventos [Stroke](/previous-versions/ms835344(v=msdn.10)) y [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) del objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) llaman al método [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) cada vez que se crea o elimina un trazo.

> [!Note]  
> Llamar al método Analyze del [](/previous-versions/ms568971(v=vs.100)) objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) con más de unos cuantos trazos presentes crea un retraso apreciable en una aplicación. Esto se debe a que Analizar es una operación de análisis de entrada de lápiz sincrónica. En la práctica, llame al método Analyze solo cuando necesite el resultado. De lo contrario, use [el método BackgroundAnalyze asincrónico,](/previous-versions/ms568972(v=vs.100)) como se muestra en el ejemplo.

 

## <a name="handling-the-analysis-results"></a>Control de los resultados del análisis

El ejemplo crea dos matrices para contener los distintos rectángulos, ya sea horizontal o girado. Use un rectángulo de selección girado para obtener el ángulo en el que se escribe una línea de palabras. En el ejemplo se muestran las propiedades devueltas por [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) y se muestra el rectángulo de selección o el rectángulo de selección girado (en función de la selección del menú).


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



El analizador calcula [GetRotatedBoundingBox durante](/previous-versions/ms569544(v=vs.100)) el análisis. Puede acceder a la información desde los rectángulos de selección girados en la aplicación por una serie de motivos útiles:

-   Detecte o dibuje los límites de una sola línea, párrafo u otra unidad.
-   Determine el ángulo en el que se escribe una línea o párrafo.
-   Implemente características como la selección de una línea, párrafo u otra unidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reconocimiento básico y análisis de entrada de lápiz](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[Ejemplo de formulario de papel digitalizado](scanned-paper-form-sample.md)
</dt> <dt>

[Ejemplo de divisor de entrada manuscrita](ink-divider-sample.md)
</dt> </dl>

 

