---
description: Este programa muestra cómo copiar y pegar entradas manuscritas en otra aplicación. También permite al usuario copiar una selección de trazos y pegar el resultado en el objeto de entrada manuscrita existente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Ejemplo de Portapapeles de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541318"
---
# <a name="ink-clipboard-sample"></a>Ejemplo de Portapapeles de lápiz

Este programa muestra cómo copiar y pegar entradas manuscritas en otra aplicación. También permite al usuario copiar una selección de trazos y pegar el resultado en el objeto de entrada manuscrita existente.

Están disponibles los siguientes modos del portapapeles:

-   Formato serializado de tinta (ISF)
-   Metarchivo de 
-   Metarchivo mejorado (EMF)
-   Bitmap
-   Entrada de texto
-   Boceto de tinta

La tinta de texto y el boceto son dos tipos de controles de entrada de lápiz que se usan como texto o dibujo respectivamente. Es posible pegar el ISF, la tinta de texto y el boceto de la tinta en una entrada manuscrita existente.

Además del portapapeles, este ejemplo también muestra cómo seleccionar trazos con la herramienta lazo. El usuario puede Desplace los trazos seleccionados y modificar sus atributos de dibujo. Esta funcionalidad es un subconjunto de la funcionalidad de selección ya proporcionada por el control de superposición de tinta; se implementa aquí con fines ilustrativos.

En este ejemplo se usan las siguientes características:

-   El objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .
-   Compatibilidad con el portapapeles de lápiz.
-   El uso del lazo con el método [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .

En este ejemplo se muestra la representación de la entrada manuscrita, la copia de esa tinta y la posterior pegada en otra aplicación, como Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Recopilación de entradas manuscritas y configuración del formulario

En primer lugar, haga referencia a las interfaces de automatización de Tablet PC, que se instalan con el <entity type="reg"/> Kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



A continuación, el formulario declara algunas constantes y campos que se indican más adelante en este ejemplo.


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



Por último, en el controlador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario, se inicializa el formulario, se crea un objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para el formulario y se habilita el recopilador de tinta.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Control de eventos de menú

Los controladores de eventos del elemento de menú actualizan principalmente el estado del formulario.

El comando CLEAR quita el rectángulo de selección y elimina los trazos del objeto [Ink](/previous-versions/ms583670(v=vs.100)) del recopilador de tinta.

El comando Exit deshabilita el recolector de tinta antes de salir de la aplicación.

El menú Edición habilita los comandos cortar y copiar según el estado de selección del formulario y permite el comando pegar basado en el contenido del portapapeles, determinado mediante el método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) del objeto [Ink](/previous-versions/ms583670(v=vs.100)) .

Los comandos cortar y copiar usan un método auxiliar para copiar la entrada manuscrita en el portapapeles. El comando cortar usa un método auxiliar para eliminar los trazos seleccionados.

El comando pegar comprueba primero el método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) del objeto [Ink](/previous-versions/ms583670(v=vs.100)) para ver si se puede pegar el objeto en el portapapeles. A continuación, el comando pegar calcula la esquina superior izquierda de la región de pegado, convierte las coordenadas de píxeles al espacio de entrada y pega los trazos del portapapeles en el recopilador de tinta. Por último, se actualiza el cuadro de selección.


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



Los comandos SELECT y Ink actualizan el modo de aplicación y los atributos de dibujo predeterminados, borran la selección actual, actualizan el estado del menú y actualizan el formulario. Otros controladores se basan en el estado de la aplicación para realizar la función correcta, ya sea con el lazo o la colocación de la tinta. Además, el comando SELECT agrega los controladores de eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) y [Stroke](/previous-versions/ms567622(v=vs.100)) al recopilador de tinta y el comando de entrada manuscrita quita estos controladores de eventos del recopilador de tinta.

Los formatos que están disponibles en el portapapeles cuando se copian los trazos se muestran en el menú Formato y el usuario selecciona el formato para copiar la tinta de esta lista. Los tipos de formatos disponibles incluyen el formato serializado de tinta (ISF), el metarchivo, el metarchivo mejorado y el mapa de bits. Los formatos de tinta de boceto y de entrada de texto se excluyen mutuamente y dependen de que la tinta se copie en el portapapeles como un objeto OLE.

El menú estilo permite al usuario cambiar las propiedades de color y ancho del lápiz y los trazos seleccionados.

Por ejemplo, el comando rojo establece la propiedad [color](/previous-versions/ms582103(v=vs.100)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) del recopilador de tinta en el color rojo. Dado que no se ha establecido la propiedad [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) del objeto [cursor](/previous-versions/ms552104(v=vs.100)) , cualquier nueva entrada de lápiz que se dibuje en el recolector de tintas heredará del color de dibujo predeterminado. Además, si hay trazos seleccionados actualmente, la propiedad color de los atributos de dibujo de cada trazo también se actualiza.


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



## <a name="handling-mouse-events"></a>Controlar eventos del mouse

El controlador de eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) comprueba el modo de aplicación. Si el modo es MoveInk y un botón del mouse está inactivo, el controlador mueve los trazos usando el método move de la colección [Strokes](/previous-versions/ms552701(v=vs.100)) y actualiza el cuadro de selección. De lo contrario, el controlador comprueba para determinar si el rectángulo de selección contiene el cursor, habilita la recopilación de entradas de lápiz en consecuencia y también establece el cursor según corresponda.

El controlador de eventos [MouseDown](/previous-versions/ms567616(v=vs.100)) comprueba la configuración del cursor. Si el cursor se establece en [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), el controlador establece el modo de aplicación en MoveInk y registra la ubicación del cursor. De lo contrario, si hay una selección actual, desactívela.

El controlador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) comprueba el modo de aplicación. Si el modo es MoveInk, el controlador establece el modo de aplicación basado en el estado de activación del comando SELECT.

El evento [NewPackets](/previous-versions/ms567621(v=vs.100)) se desencadena en el modo de selección cuando el recopilador de tinta recibe nuevos datos de paquete. Si la aplicación está en modo de selección, es necesario interceptar los nuevos paquetes y usarlos para dibujar el lazo de selección.

La coordenada de cada paquete se convierte en píxeles, se restringe al área de dibujo y se agrega a la colección de puntos del lazo. A continuación, se llama a un método auxiliar para dibujar el lazo en el formulario.

## <a name="handling-a-new-stroke"></a>Controlar un nuevo trazo

El evento [Stroke](/previous-versions/ms567622(v=vs.100)) se desencadena en el modo de selección cuando se dibuja un nuevo trazo. Si la aplicación está en modo de selección, este trazo corresponde al lazo y es necesario actualizar la información de los trazos seleccionados.

El controlador cancela el evento [Stroke](/previous-versions/ms567622(v=vs.100)) , comprueba si hay más de dos puntos de lazo, copia la colección Points en una matriz de objetos [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) y convierte las coordenadas de los puntos de la matriz de píxeles a espacio de entrada manuscrita. A continuación, el controlador usa el método [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) del objeto de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) para obtener los trazos seleccionados por los puntos de lazo y actualiza el estado de selección del formulario. Por último, el trazo que provocó el evento se quita de la colección de trazos seleccionados, se vacía la colección de puntos de lazo y un método auxiliar dibuja el rectángulo de selección.


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



## <a name="copying-ink-to-the-clipboard"></a>Copiar la entrada manuscrita en el portapapeles

El método auxiliar CopyInkToClipboard crea un valor de [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) , comprueba el estado del menú Formato para actualizar los formatos que se van a colocar en el portapapeles y usa el método [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) del objeto de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) para copiar los trazos en el portapapeles.


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

El método auxiliar SetSelection actualiza el selectedStrokes archivado y si la colección es **null** o está **vacía**, el rectángulo de selección se establece en el rectángulo vacío. Si la colección de [trazos](/previous-versions/ms552701(v=vs.100)) seleccionada no está vacía, el método SetSelection realiza los siguientes pasos:

-   Determina el rectángulo delimitador mediante el método [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) de la colección Strokes.
-   Convierte las coordenadas del rectángulo del espacio de entrada en píxeles
-   Aumenta el rectángulo para proporcionar un espacio visual entre él y los trazos seleccionados.
-   Crea controladores de selección para el cuadro de selección actual.

Por último, el método SetSelection establece la visibilidad de los controladores de selección y establece la propiedad [AutoRedraw](/previous-versions/ms571706(v=vs.100)) del recopilador de tinta en **false**, si se seleccionan los trazos.


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



## <a name="drawing-the-lasso"></a>Dibujo del lazo

El lazo se dibuja como una serie de puntos abiertos que siguen la ruta de acceso del trazo de lazo y una línea de conector discontinua entre los dos extremos. El evento [NewPackets](/previous-versions/ms567621(v=vs.100)) se genera cuando se dibuja el lazo y el controlador de eventos pasa la información del trazo al método DrawLasso.

El método auxiliar DrawLasso quita primero la línea del conector anterior y, a continuación, recorre en iteración los puntos del trazo. A continuación, DrawLasso calcula dónde se colocan los puntos a lo largo del trazo y los dibuja. Por último, dibuja una nueva línea de conector.

## <a name="closing-the-form"></a>Cierre del formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) , myInkCollector.

 

 
