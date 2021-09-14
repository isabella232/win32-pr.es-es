---
description: Este ejemplo se basa en el ejemplo de colección ink. Muestra cómo usar el objeto Divider para analizar la entrada de lápiz.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Ejemplo de divisor de entrada manuscrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a272d6a5530938e6fecfeefc9f46ffdd0835d045
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247785"
---
# <a name="ink-divider-sample"></a>Ejemplo de divisor de entrada manuscrita

Este ejemplo se basa en el ejemplo [de colección de lápiz](ink-collection-sample.md). Muestra cómo usar el objeto [Divider](/previous-versions/ms839398(v=msdn.10)) para analizar la entrada de lápiz.

Para obtener información conceptual detallada sobre [el divisor](/previous-versions/ms839398(v=msdn.10)), vea El [objeto divisor](the-divider-object.md).

Cuando se actualiza el formulario, el ejemplo dibuja un rectángulo delimitador alrededor de cada unidad analizada, dividido en palabras, líneas, párrafos y dibujos. Además de usar colores diferentes, estos rectángulos se amplían en diferentes cantidades para asegurarse de que ninguno de los rectángulos esté oculto por otros. En la tabla siguiente se especifica el color y la temperatura de cada unidad analizada.



| unidad analizada        | Color              | Píxeles de aumento |
|----------------------|--------------------|-------------------|
| Word<br/>      | Verde<br/>   | 1<br/>      |
| Línea<br/>      | Fucsia<br/> | 3<br/>      |
| Paragraph<br/> | Azul<br/>    | 5<br/>      |
| Dibujo<br/>   | Rojo<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>Configuración del formulario

Cuando se carga el formulario, [se crea un](/previous-versions/ms839398(v=msdn.10)) objeto Divider. Se crea un objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) y se asocia a un panel en el formulario. A continuación, los controladores de eventos se adjuntan al objeto InkOverlay para realizar un seguimiento de cuándo se agregan y eliminan trazos. A continuación, si hay reconocedores disponibles, se asigna un objeto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) para el reconocedor predeterminado al divisor. A continuación, se establece la propiedad [LineHeight](/previous-versions/ms839409(v=msdn.10)) del objeto Divider y la colección [Strokes](/previous-versions/ms827799(v=msdn.10)) del objeto InkOverlay se asigna al divisor. Por último, el objeto InkOverlay está habilitado.


```C++
// Create the ink overlay and associate it with the form
myInkOverlay = new Microsoft.Ink.InkOverlay(DrawArea.Handle);

// Set the erasing mode to stroke erase.
myInkOverlay.EraserMode = InkOverlayEraserMode.StrokeErase;

// Hook event handler for the Stroke event to myInkOverlay_Stroke.
// This is necessary since the application needs to pass the strokes 
// to the ink divider.
myInkOverlay.Stroke += new InkCollectorStrokeEventHandler(myInkOverlay_Stroke); 

// Hook the event handler for StrokeDeleting event to myInkOverlay_StrokeDeleting.
// This is necessary as the application needs to remove the strokes from 
// ink divider object as well.
myInkOverlay.StrokesDeleting += new InkOverlayStrokesDeletingEventHandler(myInkOverlay_StrokeDeleting);

// Hook the event handler for StrokeDeleted event to myInkOverlay_StrokeDeleted.
// This is necessary to update the layout analysis result when automatic layout analysis
// option is selected.
myInkOverlay.StrokesDeleted += new InkOverlayStrokesDeletedEventHandler(myInkOverlay_StrokeDeleted);

// Create the ink divider object
myInkDivider = new Divider();

// Add a default recognizer context to the divider object
// without adding the recognizer context, the divider would
// not use a recognizer to do its word segmentation and would
// have less accurate results.
// Adding the recognizer context slows down the call to 
// myInkDivider.Divide though.
// It is possible that there is no recognizer installed on the
// machine for this language. In that case the divider does
// not use a recognizer to improve its accuracy.
// Get the default recognizer if any
try
{
    Recognizers recognizers = new Recognizers();
     myInkDivider.RecognizerContext = recognizers.GetDefaultRecognizer().CreateRecognizerContext();
}
catch (InvalidOperationException)
{
     //We are in the case where no default recognizers can be found
}

    // The LineHeight property helps the InkDivider distinguish between 
    // drawing and handwriting. The value should be the expected height 
    // of the user's handwriting in ink space units (0.01mm).
    // Here we set the LineHeight to 840, which is about 1/3 of an inch.
    myInkDivider.LineHeight = 840;

// Assign ink overlay's strokes collection to the ink divider
// This strokes collection is updated in the event handler
myInkDivider.Strokes = myInkOverlay.Ink.Strokes;

// Enable ink collection
myInkOverlay.Enabled = true;
```



La colección [Strokes](/previous-versions/ms839422(v=msdn.10)) del objeto [Divider](/previous-versions/ms839398(v=msdn.10)) debe mantenerse sincronizada con la colección [Strokes](/previous-versions/ms827799(v=msdn.10)) del objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (a la que se accede a través de la propiedad Ink del objeto Ink del [objeto](/previous-versions/ms833110(v=msdn.10)) Ink). Para asegurarse de que esto sucede, el controlador de eventos [Stroke](/previous-versions/ms835344(v=msdn.10)) para el objeto InkOverlay se escribe como se muestra a continuación. Tenga en cuenta que el controlador de eventos comprueba primero si [EditingMode](/previous-versions/ms833105(v=msdn.10)) está establecido en **Ink** para filtrar los trazos del borrador. Si el usuario ha solicitado el análisis de diseño automático, la aplicación llama al método DivideInk del formulario y actualiza el área de dibujo.


```C++
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e )
{
    // Filter out the eraser stroke.
    if(InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
    {
        // Add the new stroke to the ink divider's strokes collection
        myInkDivider.Strokes.Add(e.Stroke);
        
        if(miAutomaticLayoutAnalysis.Checked)
        {
            // Call DivideInk
            DivideInk();

            // Repaint the screen to reflect the change
            DrawArea.Refresh();
        }
    }
}
```



## <a name="dividing-the-ink"></a>Dividir la entrada de lápiz

Cuando el usuario hace clic en Dividir en el menú Archivo, se llama al método [Divide](/previous-versions/ms839461(v=msdn.10)) en el [objeto Divider.](/previous-versions/ms839398(v=msdn.10)) Se usa el reconocedor predeterminado, si está disponible.


```C++
DivisionResult divResult = myInkDivider.Divide();
```



El objeto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) resultante, al que hace referencia la variable `divResult` , se pasa a una función de utilidad, `getUnitBBBoxes()` . La función de utilidad devuelve una matriz de rectángulos para cualquier tipo de división que se solicite: segmentos, líneas, párrafos o dibujos.


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



Por último, el panel de formulario se ve obligado a volver a dibujar para que aparezcan los rectángulos delimitadores.


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>Resultados del análisis de entrada de lápiz

En la función de utilidad , el [objeto DivisionResult](/previous-versions/ms839371(v=msdn.10)) se consulta para sus resultados mediante el método [ResultByType,](/previous-versions/ms839388(v=msdn.10)) en función del tipo de división solicitado por el autor de la llamada. El método ResultByType devuelve una [colección DivisionUnits.](/previous-versions/ms837954(v=msdn.10)) Cada [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) de la colección representa un dibujo, un único segmento de reconocimiento de escritura a mano, una línea de escritura a mano o un bloque de escritura a mano, en función de lo que se especificó cuando se llamó a la función de utilidad.


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



Si hay al menos una [Unidad de división](/previous-versions/ms837976(v=msdn.10)), se crea una matriz de rectángulos que contiene un rectángulo delimitador por unidad. (Los rectángulos se inflan por diferentes cantidades para cada tipo de unidad, que se mantienen en la variable de inflado, para evitar la superposición).


```C++
// If there is at least one unit, we construct the rectangles
if((null != units) && (0 < units.Count))
{
    // We need to convert rectangles from ink units to
    // pixel units. For that, we need Graphics object
    // to pass to InkRenderer.InkSpaceToPixel method
    using (Graphics g = DrawArea.CreateGraphics())
    {

    // InkSpace to Pixel Space conversion setup done here. 
    // Not shown for brevity.

        // Iterate through the collection of division units to obtain the bounding boxes
        foreach(DivisionUnit unit in units)
        {
            // Get the bounding box of the strokes of the division unit
            divRects[i] = unit.Strokes.GetBoundingBox();

            // Div unit rect Ink space to Pixel space conversion done here. 
            // Not shown for brevity.

            // Inflate the rectangle by inflate pixels in both directions
            divRects[i].Inflate(inflate, inflate);

            // Increment the index
            ++i;
        }

    } // Relinquish the Graphics object
}
```



## <a name="redrawing-the-form"></a>Volver a dibujar el formulario

Cuando se fuerza el nuevo dibujo anterior, el código siguiente se ejecuta para pintar los rectángulos delimitadores de cada [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) en el formulario alrededor de la entrada de lápiz.


```C++
private void DrawArea_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
        {
            // Create the Pen used to draw bounding boxes.
            // First set of bounding boxes drawn here are 
            // the bounding boxes of paragraphs.
            // These boxes are drawn with Blue pen.
            Pen penBox = new Pen(Color.Blue, 2);

            // First, draw the bounding boxes for Paragraphs
            if(null != myParagraphBoundingBoxes)
            {
                // Draw bounding boxes for Paragraphs
                e.Graphics.DrawRectangles(penBox, myParagraphBoundingBoxes);
            }

            // Next, draw the bounding boxes for Lines
            if(null != myLineBoundingBoxes)
            {
                // Color is Magenta pen
                penBox.Color = Color.Magenta;
                // Draw the bounding boxes for Lines
                e.Graphics.DrawRectangles(penBox, myLineBoundingBoxes);
            }
            
            // Then, draw the bounding boxes for Words
            if(null != myWordBoundingBoxes)
            {
                // Color is Green
                penBox.Color = Color.Green;
                // Draw bounding boxes for Words
                e.Graphics.DrawRectangles(penBox, myWordBoundingBoxes);
            }
            
            // Finally, draw the boxes for Drawings
            if(null != myDrawingBoundingBoxes)
            {
                // Color is Red pen
                penBox.Color = Color.Red;
                // Draw bounding boxes for Drawings
                e.Graphics.DrawRectangles(penBox, myDrawingBoundingBoxes);
            }
        }
```



## <a name="closing-the-form"></a>Cerrar el formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario elimina los objetos [InkOverlay,](/previous-versions/ms833057(v=msdn.10)) [Divider,](/previous-versions/ms839398(v=msdn.10)) [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) y la [colección Strokes](/previous-versions/ms827799(v=msdn.10)) usada en el ejemplo.

 

