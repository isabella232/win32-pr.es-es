---
description: En este programa de ejemplo se muestra cómo acercar y desplazar la entrada de lápiz.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Ejemplo de zoom de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d786fe502e1510a44df39049e845f05694a1befae0d4a21bcfa2ba2bd2b19b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939445"
---
# <a name="ink-zoom-sample"></a>Ejemplo de zoom de lápiz

En este programa de ejemplo se muestra cómo acercar y desplazar la entrada de lápiz. En concreto, permite al usuario acercar y alejar la entrada de lápiz en incrementos. También muestra cómo acercar una región determinada mediante un rectángulo de zoom. Por último, en este ejemplo se muestra cómo recopilar la entrada de lápiz en diferentes relaciones de zoom y cómo configurar el desplazamiento dentro del área de dibujo con zoom.

En el ejemplo, las [transformaciones de](/previous-versions/ms828481(v=msdn.10)) objetos y vistas del objeto representador se usan para realizar zoom y desplazamiento. La transformación de vista se aplica a los puntos y el ancho del lápiz. La transformación de objetos solo se aplica a los puntos. El usuario puede controlar qué transformación se usa cambiando el elemento Ancho del lápiz de escala en el menú Modo.

> [!Note]  
> Es problemático realizar algunas llamadas COM en determinados métodos de interfaz [**(InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) y [**InkRenderer.SetObjectTransform,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)por ejemplo) cuando se ha enviado un mensaje. Cuando los mensajes se envían, deben estar en la cola de mensajes POST. Para solucionar este escenario, pruebe si está controlando un mensaje de POST mediante una llamada a [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) y POST, si el mensaje se envió.

 

En este ejemplo se usan las siguientes características:

-   El [objeto InkCollector](/previous-versions/ms583683(v=vs.100))
-   Método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) del objeto [Renderer](/previous-versions/ms828481(v=msdn.10))
-   Método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) del objeto [Renderer](/previous-versions/ms828481(v=msdn.10))

## <a name="initializing-the-form"></a>Inicializar el formulario

En primer lugar, el ejemplo hace referencia a las interfaces de automatización de Tablet PC, que se proporcionan en Windows Vista o Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



El ejemplo declara un [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` y algunos miembros privados para ayudar con el escalado.


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



A continuación, el ejemplo crea y habilita [InkCollector en](/previous-versions/ms583683(v=vs.100)) el controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario. Además, se [establece la](/previous-versions/ms837941(v=msdn.10)) propiedad Width de la [propiedad DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto InkCollector. Por último, se definen los intervalos de la barra de desplazamiento y se llama al `UpdateZoomAndScroll` método de la aplicación.


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a>Actualizar los valores de zoom y desplazamiento

El área de dibujo del recopilador de lápiz se ve afectada por muchos eventos. En el `UpdateZoomAndScroll` método , se usa una matriz de transformación para escalar y traducir el recopilador de entrada de lápiz dentro de la ventana.

> [!Note]  
> El método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) del objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) aplica la transformación tanto a los trazos como al ancho del lápiz, mientras que el [método SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) solo aplica la transformación a los trazos.

 

Por último, se llama al `UpdateScrollBars` método de la aplicación y se fuerza la actualización del formulario.


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a>Administración de las barras de desplazamiento

El método configura las barras de desplazamiento para que funcionen correctamente con el tamaño de la ventana actual, la configuración de zoom y la ubicación de desplazamiento dentro `UpdateScrollBars` de [InkCollector](/previous-versions/ms583683(v=vs.100)). Este método calcula los valores de cambio grande y pequeño para las barras de desplazamiento vertical y horizontal. También calcula el valor actual de las barras de desplazamiento y si deben estar visibles. El método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) del objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) controla la conversión de píxeles al espacio de coordenadas zoomed y tiene en cuenta cualquier escalado y desplazamiento que se aplica a través de la vista y las transformaciones de objetos.


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a>Acercar a un rectángulo

Los `pnlDrawingArea` controladores de eventos del panel administran el dibujo del rectángulo en la ventana. Si el comando Zoom To Rect está activado en el menú Modo, el controlador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) llama al método de la `ZoomToRectangle` aplicación. El método calcula el ancho y el alto del rectángulo, comprueba las condiciones de límite, actualiza los valores de la barra de desplazamiento y el factor de escala y, a continuación, llama al método de la aplicación para aplicar la `ZoomToRectangle` `UpdateZoomAndScroll` nueva configuración.

## <a name="closing-the-form"></a>Cerrar el formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario elimina el [objeto InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
