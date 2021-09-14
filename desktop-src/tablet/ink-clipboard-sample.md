---
description: En este programa se muestra cómo copiar y pegar la entrada de lápiz en otra aplicación. También permite al usuario copiar una selección de trazos y pegar el resultado en el objeto ink existente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Ejemplo del Portapapeles de Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262407"
---
# <a name="ink-clipboard-sample"></a>Ejemplo del Portapapeles de Ink

En este programa se muestra cómo copiar y pegar la entrada de lápiz en otra aplicación. También permite al usuario copiar una selección de trazos y pegar el resultado en el objeto ink existente.

Están disponibles los siguientes modos del Portapapeles:

-   Formato serializado de entrada de lápiz (ISF)
-   Metarchivo de 
-   Metarchivo mejorado (EMF)
-   Bitmap
-   Entrada manuscrita de texto
-   Sketch Ink

La entrada manuscrita de texto y la entrada de lápiz de boceto son dos tipos de controles de entrada de lápiz que se usan como texto o dibujo, respectivamente. Es posible pegar ISF, la entrada de lápiz de texto y la entrada de lápiz de boceto en la entrada de lápiz existente.

Además del Portapapeles, en este ejemplo también se muestra cómo seleccionar trazos con la herramienta de pestañas. El usuario puede mover los trazos seleccionados y modificar sus atributos de dibujo. Esta funcionalidad es un subconjunto de la funcionalidad de selección que ya proporciona el control de superposición de lápiz; se implementa aquí con fines ilustrativos.

En este ejemplo se usan las siguientes características:

-   Objeto [InkCollector.](/previous-versions/ms583683(v=vs.100))
-   Compatibilidad con el Portapapeles de ink.
-   El uso del lasso con el [método Microsoft.Ink.Ink.HitTest.](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90))

En este ejemplo se muestra la representación de la entrada de lápiz, la copia y la posterior pega en otra aplicación, como Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Recopilar entrada de lápiz y configurar el formulario

En primer lugar, haga referencia a las interfaces de Automatización de Tablet PC, que se instalan con el Kit de desarrollo de software (SDK) de Microsoft Windows <entity type="reg"/> XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



A continuación, el formulario declara algunas constantes y campos que se anotan más adelante en este ejemplo.


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



Por último, en el controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario, se inicializa el formulario, se crea un objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para el formulario y se habilita el recopilador de lápiz.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Controlar eventos de menú

Los controladores de eventos del elemento de menú actualizan principalmente el estado del formulario.

El comando Borrar quita el rectángulo de selección y elimina los trazos del objeto Ink del recopilador [de](/previous-versions/ms583670(v=vs.100)) lápiz.

El comando Salir deshabilita el recopilador de entrada de lápiz antes de salir de la aplicación.

El menú Editar habilita los comandos Cortar y Copiar en función del estado de selección del formulario y habilita el comando Pegar en función del contenido del Portapapeles, determinado mediante el método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) del objeto [Ink.](/previous-versions/ms583670(v=vs.100))

Los comandos Cortar y Copiar usan un método auxiliar para copiar la entrada de lápiz en el Portapapeles. El comando Cortar usa un método auxiliar para eliminar los trazos seleccionados.

El comando Pegar comprueba primero el método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) del objeto [Ink](/previous-versions/ms583670(v=vs.100)) para ver si se puede pegar el objeto en el Portapapeles. A continuación, el comando Pegar calcula la esquina superior izquierda de la región de pegado, convierte las coordenadas de píxeles en espacio de entrada de lápiz y pega los trazos del Portapapeles en el recopilador de lápiz. Por último, se actualiza el cuadro de selección.


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



Los comandos Select y Ink actualizan el modo de aplicación y los atributos de dibujo predeterminados, borran la selección actual, actualizan el estado del menú y actualizan el formulario. Otros controladores se basan en el estado de la aplicación para realizar la función correcta, ya sea mediante el uso de la entrada de lápiz o la colocación de la entrada de lápiz. Además, el comando Select agrega los controladores de eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) y [Stroke](/previous-versions/ms567622(v=vs.100)) al recopilador de lápiz y el comando Ink quita estos controladores de eventos del recopilador de lápiz.

Los formatos que están disponibles en el Portapapeles cuando se copian trazos aparecen en el menú Formato y el usuario selecciona el formato para copiar la entrada de lápiz de esta lista. Los tipos de formatos disponibles incluyen Ink Serialized Format (ISF), metarchivo, metarchivo mejorado y mapa de bits. Los formatos de entrada manuscrita de boceto y entrada de lápiz de texto son mutuamente excluyentes y se basan en la entrada de lápiz que se copia en el Portapapeles como un objeto OLE.

El menú Estilo permite al usuario cambiar las propiedades de color y ancho del lápiz y los trazos seleccionados.

Por ejemplo, el comando Rojo establece la [propiedad Color](/previous-versions/ms582103(v=vs.100)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) del recopilador de lápiz en el color rojo. Dado que no se ha establecido la propiedad [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) del [objeto Cursor,](/previous-versions/ms552104(v=vs.100)) cualquier nueva entrada de lápiz dibujada en el recopilador de lápiz hereda el color de dibujo predeterminado. Además, si hay algún trazo seleccionado actualmente, también se actualiza la propiedad Color de los atributos de dibujo de cada trazo.


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a>Control de eventos del mouse

El [controlador de eventos MouseMove](/previous-versions/ms567617(v=vs.100)) comprueba el modo de aplicación. Si el modo es MoveInk y un botón del mouse está apagado, el controlador mueve los trazos mediante el método Move de la colección [Strokes](/previous-versions/ms552701(v=vs.100)) y actualiza el cuadro de selección. De lo contrario, el controlador comprueba si el rectángulo de selección contiene el cursor, habilita la recopilación de lápiz en consecuencia y también establece el cursor en consecuencia.

El [controlador de eventos MouseDown](/previous-versions/ms567616(v=vs.100)) comprueba la configuración del cursor. Si el cursor se establece en [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), el controlador establece el modo de aplicación en MoveInk y registra la ubicación del cursor. De lo contrario, si hay una selección actual, descálala.

El [controlador de eventos MouseUp](/previous-versions/ms567618(v=vs.100)) comprueba el modo de aplicación. Si el modo es MoveInk, el controlador establece el modo de aplicación en función del estado activado del comando Select.

El [evento NewPackets](/previous-versions/ms567621(v=vs.100)) se genera en modo de selección cuando el recopilador de entrada manuscrita recibe nuevos datos de paquetes. Si la aplicación está en modo de selección, es necesario interceptar los nuevos paquetes y usarlos para dibujar el lasso de selección.

La coordenada de cada paquete se convierte en píxeles, se restringe al área de dibujo y se agrega a la colección de puntos del lasso. A continuación, se llama a un método auxiliar para dibujar el lasso en el formulario.

## <a name="handling-a-new-stroke"></a>Controlar un nuevo trazo

El [evento Stroke](/previous-versions/ms567622(v=vs.100)) se genera en el modo de selección cuando se dibuja un nuevo trazo. Si la aplicación está en modo de selección, este trazo corresponde al lasso y es necesario actualizar la información de los trazos seleccionados.

El controlador cancela el evento [Stroke,](/previous-versions/ms567622(v=vs.100)) comprueba más de dos puntos de lasso, copia la colección Points en una matriz de objetos [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) y convierte las coordenadas de los puntos de la matriz de píxeles al espacio de entrada de lápiz. A continuación, el controlador usa el método [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) del objeto [Ink](/previous-versions/ms583670(v=vs.100)) para obtener los trazos seleccionados por los puntos de lasso y actualiza el estado de selección del formulario. Por último, el trazo que ha producido el evento se quita de la colección de trazos seleccionados, la colección de puntos de lasso se vacía y un método auxiliar dibuja el rectángulo de selección.


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a>Copiar entrada de lápiz en el Portapapeles

El método auxiliar CopyInkToClipboard crea un valor [InkClipboardFormats,](/previous-versions/ms583681(v=vs.100)) comprueba el estado del menú Formato para actualizar los formatos que se colocarán en el Portapapeles y usa el método [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) del objeto [Ink](/previous-versions/ms583670(v=vs.100)) para copiar los trazos en el Portapapeles.


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a>Actualizar una selección

El método auxiliar SetSelection actualiza el archivo selectedStrokes y, si la colección es **NULL** o **EMPTY,** el rectángulo de selección se establece en el rectángulo vacío. Si la colección [Strokes seleccionada](/previous-versions/ms552701(v=vs.100)) no está vacía, el método SetSelection realiza los pasos siguientes:

-   Determina el rectángulo delimitador mediante el método [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) de la colección strokes.
-   Convierte las coordenadas del rectángulo del espacio de entrada de lápiz en píxeles.
-   Infla el rectángulo para proporcionar algo de espacio visual entre él y los trazos seleccionados.
-   Crea identificadores de selección para el cuadro de selección actual.

Por último, el método SetSelection establece la visibilidad de los identificadores de selección y establece la propiedad [AutoRedraw](/previous-versions/ms571706(v=vs.100)) del recopilador de lápiz en **FALSE** si se seleccionan trazos.


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a>Dibujar el lasso

El lasso se dibuja como una serie de puntos abiertos que siguen la ruta de acceso del trazo de lasso y una línea de conector discontinua entre los dos extremos. El [evento NewPackets](/previous-versions/ms567621(v=vs.100)) se genera a medida que se dibuja el lasso y el controlador de eventos pasa la información del trazo al método DrawLasso.

El método auxiliar DrawLasso quita primero la línea del conector anterior y, a continuación, recorre en iteración los puntos del trazo. A continuación, DrawLasso calcula dónde colocar los puntos a lo largo del trazo y los dibuja. Por último, dibuja una nueva línea de conector.

## <a name="closing-the-form"></a>Cerrar el formulario

El método [Dispose del formulario](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) elimina el [objeto InkCollector,](/previous-versions/ms583683(v=vs.100)) myInkCollector.

 

 
