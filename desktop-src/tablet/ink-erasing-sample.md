---
description: 'Esta aplicación se basa en el ejemplo de colección de entradas de lápiz mostrando la eliminación de trazos de tinta. En el ejemplo se proporciona al usuario un menú que tiene cuatro modos de elegir: habilitada para tinta, borrado en cúspide, borrado en intersecciones y borrado de trazos.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Ejemplo de borrado de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540414"
---
# <a name="ink-erasing-sample"></a>Ejemplo de borrado de tinta

Esta aplicación se basa en el ejemplo de [colección de entradas de lápiz](ink-collection-sample.md) mostrando la eliminación de trazos de tinta. En el ejemplo se proporciona al usuario un menú que tiene cuatro modos de elegir: habilitada para tinta, borrado en cúspide, borrado en intersecciones y borrado de trazos.

En el modo de entrada de lápiz, el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) recopila entradas de lápiz, tal como se muestra en el [ejemplo de colección de tinta](ink-collection-sample.md).

En un modo de borrado, se borran los segmentos de trazos de tinta existentes que el usuario toca con el cursor. Además, las cresta o las intersecciones se pueden marcar con un círculo rojo.

Las partes más interesantes de este ejemplo se encuentran en el `InkErase` controlador de eventos del formulario `OnPaint` y en las funciones de borrado a las que se llama desde el controlador de eventos del formulario `OnMouseMove` .

## <a name="circling-the-cusps-and-intersections"></a>Rodear las elevaciones y las intersecciones

El controlador de `OnPaint` eventos del formulario pinta primero los trazos y, según el modo de aplicación, puede buscar y marcar todas las crestas o intersecciones con un pequeño círculo rojo. Un cúspide marca el punto en el que un trazo cambia de dirección de repente. Una intersección marca un punto en el que un trazo se cruza con él mismo u otro trazo.

El evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) se produce cada vez que se vuelve a dibujar un control.

> [!Note]  
> El ejemplo obliga al formulario a dibujarse a sí mismo cada vez que se borra un trazo, o cuando el modo de aplicación cambia, utilizando el método [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del formulario.

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



En `PaintCusps` , el código recorre en iteración cada cúspide en cada trazo y dibuja un círculo rojo alrededor de él. La propiedad [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del trazo devuelve los índices de los puntos dentro de un Stoke que corresponden a las crestas. Además, tenga en cuenta el método [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) del objeto [representador](/previous-versions/ms828481(v=msdn.10)) , que convierte el punto en coordenadas relevantes para el método DrawEllipse.


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



En `PaintIntersections` , el código recorre en iteración cada trazo para buscar sus intersecciones con todo el conjunto de trazos. Observe que se pasa al método [FindIntersections](/previous-versions/ms827856(v=msdn.10)) del trazo una colección [Strokes](/previous-versions/ms827799(v=msdn.10)) y se devuelve una matriz de valores de índice de punto flotante que representan las intersecciones. Después, el código calcula una coordenada X-Y para cada intersección y dibuja un círculo rojo alrededor de ella.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Controlar un lápiz que tiene dos extremos

Se definen tres controladores de eventos para el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) para los eventos [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))y [Stroke](/previous-versions/ms567622(v=vs.100)) . Cada controlador de eventos comprueba la propiedad [invertida](/previous-versions/ms839525(v=msdn.10)) del objeto [cursor](/previous-versions/ms839521(v=msdn.10)) para ver el final del lápiz que se está usando. Cuando se invierte el lápiz:

-   El `myInkCollector_CursorDown` método hace que el trazo sea transparente.
-   El `myInkCollector_NewPackets` método borra los trazos.
-   El `myInkCollector_Stroke` método cancela el evento. Los eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) se generan antes del evento [Stroke](/previous-versions/ms567622(v=vs.100)) .

## <a name="tracking-the-cursor"></a>Seguimiento del cursor

Si el usuario usa un lápiz o un mouse, se generan eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) . El controlador de eventos MouseMove primero comprueba para determinar si el modo actual es un modo de borrado y si se presiona cualquier botón del mouse, y omite el evento si estos Estados no están presentes. A continuación, el controlador de eventos convierte las coordenadas de píxel del cursor en coordenadas de espacio de la entrada de lápiz mediante el método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) del objeto de [representador](/previous-versions/ms828481(v=msdn.10)) y llama a uno de los métodos de borrado del código según el modo de borrado actual.

## <a name="erasing-strokes"></a>Borrar trazos

El `EraseStrokes` método toma la ubicación del cursor en el espacio de entrada y genera una colección de trazos que se encuentran en `HitTestRadius` unidades. El `currentStroke` parámetro especifica un objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) que no se debe eliminar. A continuación, se elimina la colección Strokes del recopilador y se vuelve a dibujar el formulario.


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a>Borrar en intersecciones

El `EraseAtIntersections` método recorre en iteración cada trazo que se encuentra dentro del radio de prueba y genera una matriz de intersecciones entre ese trazo y todos los demás trazos de la colección. Si no se encuentra ninguna intersección, se elimina todo el trazo; de lo contrario, se ubica el punto más cercano del trazo al punto de prueba y, a partir de ese momento, se encuentran las intersecciones de cada lado del punto, que describen el segmento que se va a quitar.

El método [Split](/previous-versions/ms828477(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) se usa para separar el segmento del resto del trazo y, a continuación, se elimina el segmento, lo que deja intacto el resto del trazo. Como en `EraseStrokes` , el formulario se vuelve a dibujar antes de que el método devuelva.


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a>Borrar en crestas

Para cada trazo que se encuentra dentro del radio de prueba, el `EraseAtCusps` método recupera la matriz de cresta del método [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) . Cada extremo del trazo también es una cúspide, por lo que si el trazo solo tiene dos elevaciones, se elimina todo el trazo; de lo contrario, se ubica el punto más cercano del trazo al punto de prueba y, a partir de ese momento, se encuentran las intersecciones de cada lado del punto, que describen el segmento que se va a quitar.

El método [Split](/previous-versions/ms828477(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) se usa para separar el segmento del resto del trazo y, a continuación, se elimina el segmento, lo que deja intacto el resto del trazo. Como en `EraseStrokes` , el formulario se vuelve a dibujar antes de que el método devuelva.


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a>Cierre del formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
