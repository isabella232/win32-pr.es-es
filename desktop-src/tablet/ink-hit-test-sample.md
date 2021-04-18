---
description: En este ejemplo se muestran dos métodos para buscar la tinta, dada una ubicación de pantalla.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Ejemplo de prueba de posicionamiento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715084"
---
# <a name="ink-hit-test-sample"></a>Ejemplo de prueba de posicionamiento de tinta

En este ejemplo se muestran dos métodos para buscar la tinta, dada una ubicación de pantalla.

En este ejemplo se usan las siguientes características:

-   Usar un recolector de tinta
-   Realización de una prueba de posicionamiento
-   Buscar el punto más cercano

## <a name="accessing-the-ink-api"></a>Acceso a la API de entrada manuscrita

En primer lugar, haga referencia a las clases de Tablet PC, que se encuentran en el kit de desarrollo de software (SDK) de Windows Vista o Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Controlar los eventos de carga y de dibujo del formulario

El controlador de eventos de carga del formulario:

-   Crea un objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, para el formulario.
-   Establece la propiedad [si CollectionMode es](/previous-versions/ms836497(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para omitir los gestos.
-   Habilita [InkCollector](/previous-versions/ms583683(v=vs.100)).
-   Establece la propiedad [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) en **true**.


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



El controlador de eventos Paint del formulario comprueba el modo de aplicación:

-   En el modo HitTest, pinta un círculo alrededor del cursor. La plumilla activa se establece en el método handleHitTest de la aplicación.
-   En el modo NearestPoint, pinta una línea roja entre el cursor y el punto más cercano al cursor. El punto más cercano se calcula en el método handleNearestPoint de la aplicación.


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



Este ejemplo tiene un algoritmo Repaint muy sencillo. Con su propiedad [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) establecida en **true**, el recopilador de tinta se vuelve a dibujar cuando se vuelve a dibujar el formulario. Para simplificar la redibujo del formulario, la aplicación realiza un seguimiento de un cuadro de límite, la variable miembro invalidateRect, para el área en la que se agrega Paint, que se invalida cada vez que se vuelve a dibujar el formulario.

## <a name="handling-menu-events"></a>Control de eventos de menú

El comando Exit deshabilita [InkCollector](/previous-versions/ms583683(v=vs.100)) antes de salir de la aplicación.

El comando de entrada manuscrita actualiza el modo de aplicación y el estado del menú, habilita el recopilador de tinta y invalida la región que se ha pintado previamente del formulario.

Los comandos de la prueba de posicionamiento y del punto más cercano cambian el cursor, actualizan el modo de aplicación y el estado del menú, deshabilitan el recopilador de tinta e invalidan la región dibujada anteriormente del formulario.

¡ Desactive! el comando deshabilita [InkCollector](/previous-versions/ms583683(v=vs.100)) mientras se reemplaza la propiedad de [entrada manuscrita](/previous-versions/ms836505(v=msdn.10)) del objeto InkCollector con un nuevo objeto de [entrada manuscrita](/previous-versions/ms571716(v=vs.100)) , genera un evento de comando de entrada manuscrita y fuerza una actualización en el control.

## <a name="handling-mouse-events"></a>Controlar eventos del mouse

El controlador de eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) comprueba el modo de aplicación:

-   En el modo de tinta, no hace nada, lo que permite que el recolector de tintas recopile normalmente la tinta.
-   En el modo HitTest, envía los argumentos de evento al método handleHitTest de la aplicación.
-   En el modo NearestPoint, envía los argumentos de evento al método handleNearestPoint de la aplicación.

## <a name="performing-a-hit-test"></a>Realización de una prueba de posicionamiento

El método handleHitTest de la aplicación crea dos puntos, la ubicación del cursor y un punto alcanza los píxeles distantes del cursor y, a continuación, convierte estos dos puntos de píxeles en coordenadas del espacio de la tinta.


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



A continuación, el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) usa el método [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para buscar los trazos que se encuentran dentro de PT3. X-PT2. X las unidades de espacio de la tinta del cursor, PT2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



A continuación, el método handleHitTest establece el color de la pluma en función de si se han encontrado trazos, invalida la región invalidateRect, calcula una nueva región en la que se dibuja el círculo de la prueba de posicionamiento y, a continuación, invalida la nueva región.

## <a name="locating-the-nearest-point"></a>Buscar el punto más cercano

El método handleNearestPoint de la aplicación crea dos puntos iguales a la ubicación del cursor, uno de estos puntos, PT, se convierte en el espacio de la tinta y se usa en la llamada al método NearestPoint del objeto de [entrada de lápiz](/previous-versions/ms836505(v=msdn.10)) de [InkCollector](/previous-versions/ms583683(v=vs.100)). El método NearestPoint devuelve el objeto de [trazo](/previous-versions/ms827842(v=msdn.10)) más cercano al punto y establece el parámetro de salida de índice de punto flotante.


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



Si no hay trazos presentes, el método NearestPoint devuelve **null** y la ubicación del cursor se usa como el punto más cercano. De lo contrario, se calcula la ubicación en el trazo que corresponde al índice de punto flotante.

A continuación, las coordenadas de punto más cercanas se convierten a píxeles desde el espacio de tinta, el método handleNearestPoint invalida la región invalidateRect, calcula una nueva región en la que se dibuja la línea en el punto más cercano e invalida también la nueva región.

## <a name="closing-the-form"></a>Cierre del formulario

El método Dispose del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
