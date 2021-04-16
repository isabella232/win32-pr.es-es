---
description: Este programa de ejemplo muestra cómo hacer zoom y desplazar la entrada manuscrita.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Ejemplo de zoom de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540406"
---
# <a name="ink-zoom-sample"></a>Ejemplo de zoom de tinta

Este programa de ejemplo muestra cómo hacer zoom y desplazar la entrada manuscrita. En concreto, permite al usuario acercar y alejar la entrada de lápiz en incrementos. También muestra cómo hacer zoom en una región determinada mediante un rectángulo de zoom. Por último, en este ejemplo se muestra cómo recopilar la entrada de lápiz con distintas proporciones de zoom y cómo configurar el desplazamiento dentro del área de dibujo ampliada.

En el ejemplo, las transformaciones vista y objeto del objeto [representador](/previous-versions/ms828481(v=msdn.10)) se utilizan para realizar el zoom y el desplazamiento. La transformación de la vista se aplica a los puntos y al ancho del lápiz. La transformación de objeto solo se aplica a los puntos. El usuario puede controlar qué transformación se usa cambiando el elemento ancho del lápiz de escala en el menú modo.

> [!Note]  
> Es problemático realizar algunas llamadas COM en determinados métodos de interfaz ([**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) y [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), por ejemplo) cuando se ha enviado un mensaje. Cuando se envían mensajes, deben calcularse en la cola de mensajes posteriores. Para abordar este escenario, pruebe si está controlando un mensaje desde POST llamando a [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) y envíe el mensaje a sí mismo si se ha enviado el mensaje.

 

En este ejemplo se usan las siguientes características:

-   El objeto [InkCollector](/previous-versions/ms583683(v=vs.100))
-   El método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10))
-   El método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10))

## <a name="initializing-the-form"></a>Inicializar el formulario

En primer lugar, el ejemplo hace referencia a las interfaces de automatización de Tablet PC que se proporcionan en el kit de desarrollo de software (SDK) de Windows Vista o Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



En el ejemplo se declara un [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` , y algunos miembros privados para ayudar con el escalado.


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



A continuación, el ejemplo crea y habilita [InkCollector](/previous-versions/ms583683(v=vs.100)) en el controlador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario. Además, la propiedad [ancho](/previous-versions/ms837941(v=msdn.10)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto InkCollector está establecida. Por último, se definen los intervalos de la barra de desplazamiento y se llama al método de la aplicación `UpdateZoomAndScroll` .


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

Muchos eventos afectan al área de dibujo del recopilador de tinta. En el `UpdateZoomAndScroll` método, una matriz de transformación se usa para escalar y trasladar el recolector de tinta dentro de la ventana.

> [!Note]  
> El método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10)) aplica la transformación a los trazos y al ancho del lápiz, mientras que el método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) solo aplica la transformación a los trazos.

 

Por último, se llama al método de la aplicación `UpdateScrollBars` y se fuerza la actualización del formulario.


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



## <a name="managing-the-scroll-bars"></a>Administrar las barras de desplazamiento

El `UpdateScrollBars` método configura las barras de desplazamiento para que funcionen correctamente con el tamaño de la ventana actual, la configuración del zoom y la ubicación de desplazamiento en [InkCollector](/previous-versions/ms583683(v=vs.100)). Este método calcula el cambio grande y los valores pequeños para las barras de desplazamiento vertical y horizontal. También calcula el valor actual de las barras de desplazamiento y si deben ser visibles. El método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) del objeto de [representador](/previous-versions/ms828481(v=msdn.10)) controla la conversión de píxeles al espacio de coordenadas y a las cuentas de zoom para cualquier ajuste de escala y desplazamiento que se aplique a través de las transformaciones de objeto y vista.


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



## <a name="zooming-to-a-rectangle"></a>Acercar un rectángulo

Los `pnlDrawingArea` controladores de eventos de panel administran el dibujo del rectángulo en la ventana. Si el comando zoom to Rect está activado en el menú modo, el controlador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) llama al método de la aplicación `ZoomToRectangle` . El `ZoomToRectangle` método calcula el ancho y el alto del rectángulo, comprueba las condiciones de límite, actualiza los valores de la barra de desplazamiento y el factor de escala y, a continuación, llama al método de la aplicación `UpdateZoomAndScroll` para aplicar la nueva configuración.

## <a name="closing-the-form"></a>Cierre del formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
