---
description: En este ejemplo se muestran dos métodos para buscar la entrada de lápiz, dada una ubicación de pantalla.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Ejemplo de prueba de inyección de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572377"
---
# <a name="ink-hit-test-sample"></a>Ejemplo de prueba de inyección de lápiz

En este ejemplo se muestran dos métodos para buscar la entrada de lápiz, dada una ubicación de pantalla.

En este ejemplo se usan las siguientes características:

-   Uso de un recopilador de entrada de lápiz
-   Realización de una prueba de impacto
-   Buscar el punto más cercano

## <a name="accessing-the-ink-api"></a>Acceso a Ink API

En primer lugar, haga referencia a las clases de Tablet PC, que se encuentran en Windows Vista o Windows KIT de desarrollo de software (SDK) de XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Controlar la carga de formularios y Paint eventos

Controlador de eventos Load del formulario:

-   Crea un [objeto InkCollector,](/previous-versions/ms583683(v=vs.100)) ic, para el formulario.
-   Establece la propiedad [CollectionMode](/previous-versions/ms836497(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para omitir los gestos.
-   Habilita [InkCollector.](/previous-versions/ms583683(v=vs.100))
-   Establece la propiedad [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) en **TRUE.**


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

-   En el modo HitTest, pinta un círculo alrededor del cursor. El lápiz activo se establece en el método handleHitTest de la aplicación.
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



Este ejemplo tiene un algoritmo de repintado muy sencillo. Con su [propiedad AutoRedraw](/previous-versions/ms836495(v=msdn.10)) establecida en **TRUE,** el recopilador de entrada manuscrita se vuelve a dibujar cuando se vuelve a dibujar el formulario. Para simplificar el volver a dibujar el formulario, la aplicación realiza un seguimiento de un cuadro de límite, la variable miembro invalidateRect, para el área donde se agrega la pintura, que se invalida cada vez que se vuelve a dibujar el formulario.

## <a name="handling-menu-events"></a>Controlar eventos de menú

El comando Exit deshabilita [InkCollector antes](/previous-versions/ms583683(v=vs.100)) de salir de la aplicación.

El comando Ink actualiza el modo de aplicación y el estado del menú, habilita el recopilador de lápiz e invalida la región dibujada previamente del formulario.

Los comandos Prueba de acceso y Punto más cercano cambian el cursor, actualizan el modo de aplicación y el estado del menú, deshabilitan el recopilador de lápiz e invalidan la región dibujada previamente del formulario.

El clear! El comando deshabilita [InkCollector](/previous-versions/ms583683(v=vs.100)) al reemplazar la propiedad Ink del objeto [InkCollector](/previous-versions/ms836505(v=msdn.10)) por un nuevo objeto [Ink,](/previous-versions/ms571716(v=vs.100)) genera un evento de comando Ink y fuerza una actualización en el control.

## <a name="handling-mouse-events"></a>Control de eventos del mouse

El [controlador de eventos MouseMove](/previous-versions/ms567617(v=vs.100)) comprueba el modo de aplicación:

-   En el modo ink, no hace nada, lo que permite que el recopilador de lápiz re recolecte la entrada de lápiz con normalidad.
-   En el modo HitTest, envía los argumentos de evento al método handleHitTest de la aplicación.
-   En el modo NearestPoint, envía los argumentos de evento al método handleNearestPoint de la aplicación.

## <a name="performing-a-hit-test"></a>Realización de una prueba de impacto

El método handleHitTest de la aplicación crea dos puntos, la ubicación del cursor y un punto HitSize píxeles alejados del cursor y, a continuación, convierte estos dos puntos de píxeles a coordenadas de espacio de entrada de lápiz.


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



A continuación, el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) usa el método [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para buscar los trazos que están dentro de pt3. X - pt2. X unidades de espacio de entrada de lápiz del cursor, pt2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



A continuación, el método handleHitTest establece el color del lápiz en función de si se encontraron trazos, invalida la región invalidateRect, calcula una nueva región en la que se dibuja el círculo de prueba de impacto y, a continuación, invalida la nueva región.

## <a name="locating-the-nearest-point"></a>Buscar el punto más cercano

El método handleNearestPoint de la aplicación crea dos puntos iguales a la ubicación del cursor, uno de estos puntos, pt, se convierte en espacio de entrada de lápiz y se usa en la llamada al método NearestPoint del objeto [InkCollector.](/previous-versions/ms583683(v=vs.100)) [](/previous-versions/ms836505(v=msdn.10)) El método NearestPoint devuelve el [objeto Stroke](/previous-versions/ms827842(v=msdn.10)) más cercano al punto y establece el parámetro de salida del índice de punto flotante.


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



Si no hay trazos, el método NearestPoint devuelve **NULL** y la ubicación del cursor se usa como punto más cercano. De lo contrario, se calcula la ubicación en el trazo que corresponde al índice de punto flotante.

A continuación, las coordenadas de punto más cercanas se convierten en píxeles desde el espacio de entrada de lápiz. El método handleNearestPoint invalida la región invalidateRect, calcula una nueva región en la que se dibuja la línea hasta el punto más cercano e invalida también la nueva región.

## <a name="closing-the-form"></a>Cerrar el formulario

El método Dispose del formulario elimina el [objeto InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
