---
description: 'Esta aplicación se basa en el ejemplo de colección de lápiz mediante la demostración de la eliminación de trazos de lápiz. El ejemplo proporciona al usuario un menú que tiene cuatro modos entre los que elegir: habilitado para lápiz, borrado en cúsp, borrado en intersecciones y borrado de trazos.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Ejemplo de borrado de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572380"
---
# <a name="ink-erasing-sample"></a>Ejemplo de borrado de lápiz

Esta aplicación se basa en el ejemplo de [colección de](ink-collection-sample.md) lápiz mediante la demostración de la eliminación de trazos de lápiz. El ejemplo proporciona al usuario un menú que tiene cuatro modos entre los que elegir: habilitado para lápiz, borrado en cúsp, borrado en intersecciones y borrado de trazos.

En el modo habilitado para lápiz, el [objeto InkCollector](/previous-versions/ms836493(v=msdn.10)) recopila la entrada de lápiz como se muestra en [Ink Collection Sample](ink-collection-sample.md).

En un modo de borrado, se borran los segmentos de trazos de entrada de lápiz existentes que el usuario toca con el cursor. Además, las intersecciones o cúsps se pueden marcar con un círculo rojo.

Las partes más interesantes de este ejemplo se encuentran en el controlador de eventos del formulario y en las funciones de borrado a las que se llama desde el controlador `InkErase` `OnPaint` de eventos del `OnMouseMove` formulario.

## <a name="circling-the-cusps-and-intersections"></a>Circular las cúsps y las intersecciones

El controlador de eventos del formulario pinta primero los trazos y, en función del modo de aplicación, puede buscar y marcar todas las cúsps o intersecciones con un círculo rojo `OnPaint` pequeño. Un cusp marca el punto en el que un trazo cambia de dirección repentinamente. Una intersección marca un punto en el que un trazo forma una intersección con sí mismo u otro trazo.

El [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) evento se produce cada vez que se vuelve a dibujar un control.

> [!Note]  
> El ejemplo obliga al formulario a volver a dibujarse cada vez que se borra un trazo, o cuando cambia el modo de aplicación, mediante el [método Refresh del](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) formulario.

 


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



En , el código recorre en iteración cada cúsp en cada trazo `PaintCusps` y dibuja un círculo rojo a su alrededor. La propiedad [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del trazo devuelve los índices de los puntos dentro de un cúsps que corresponden a cusps. Además, tenga en cuenta el método [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) del objeto [Renderer,](/previous-versions/ms828481(v=msdn.10)) que convierte el punto en coordenadas relevantes para el método DrawObjectpse.


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



En , el código recorre en iteración cada trazo para encontrar sus intersecciones con todo el `PaintIntersections` conjunto de trazos. Tenga en cuenta que al método [FindIntersections](/previous-versions/ms827856(v=msdn.10)) del trazo se le pasa una colección [Strokes](/previous-versions/ms827799(v=msdn.10)) y devuelve una matriz de valores de índice de punto flotante que representan las intersecciones. A continuación, el código calcula una coordenada X-Y para cada intersección y dibuja un círculo rojo a su alrededor.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Control de un lápiz que tiene dos extremos

Se definen tres controladores de eventos para el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) para los eventos [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)) [y Stroke.](/previous-versions/ms567622(v=vs.100)) Cada controlador de eventos comprueba [la propiedad](/previous-versions/ms839521(v=msdn.10)) [Inverted](/previous-versions/ms839525(v=msdn.10)) del objeto Cursor para ver qué extremo del lápiz se está utilizando. Cuando se invierte el lápiz:

-   El `myInkCollector_CursorDown` método hace que el trazo sea transparente.
-   El `myInkCollector_NewPackets` método borra los trazos.
-   El `myInkCollector_Stroke` método cancela el evento. [Los eventos NewPackets](/previous-versions/ms567621(v=vs.100)) se generan antes del [evento Stroke.](/previous-versions/ms567622(v=vs.100))

## <a name="tracking-the-cursor"></a>Seguimiento del cursor

Tanto si el usuario usa un lápiz como un mouse, se generan eventos [MouseMove.](/previous-versions/ms567617(v=vs.100)) El controlador de eventos MouseMove comprueba primero si el modo actual es un modo de borrado y si se presiona algún botón del mouse, y omite el evento si estos estados no están presentes. A continuación, el controlador de eventos convierte las coordenadas [](/previous-versions/ms828481(v=msdn.10)) de píxel del cursor en coordenadas de espacio de entrada de lápiz mediante el método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) del objeto representador y llama a uno de los métodos de borrado del código en función del modo de borrado actual.

## <a name="erasing-strokes"></a>Borrar trazos

El método toma la ubicación del cursor en el espacio de entrada de lápiz y genera una `EraseStrokes` colección de trazos que se encuentran dentro de las `HitTestRadius` unidades. El `currentStroke` parámetro especifica un objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) que no se debe eliminar. A continuación, se elimina la colección de trazos del recopilador y se vuelve a dibujar el formulario.


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



## <a name="erasing-at-intersections"></a>Borrado en intersecciones

El método recorre en iteración cada trazo que se encuentra dentro del radio de prueba y genera una matriz de intersecciones entre ese trazo y todos los demás `EraseAtIntersections` trazos de la colección. Si no se encuentra ninguna intersección, se elimina todo el trazo; De lo contrario, se encuentra el punto más cercano del trazo al punto de prueba y, a partir de ahí, se encuentran las intersecciones a ambos lados del punto, que describen el segmento que se va a quitar.

El [método Split](/previous-versions/ms827842(v=msdn.10)) del objeto [Stroke](/previous-versions/ms828477(v=msdn.10)) se usa para separar el segmento del resto del trazo y, a continuación, se elimina el segmento, dejando intacto el resto del trazo. Al igual que `EraseStrokes` en , el formulario se vuelve a dibujar antes de que el método vuelva.


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



## <a name="erasing-at-cusps"></a>Borrado en cusps

Para cada trazo que se encuentra dentro del radio de prueba, el método recupera la matriz de cúsps del método `EraseAtCusps` [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) del objeto [Stroke.](/previous-versions/ms827842(v=msdn.10)) Cada extremo del trazo también es un cúsp, por lo que si el trazo solo tiene dos cúsps, se elimina todo el trazo; De lo contrario, se encuentra el punto más cercano del trazo al punto de prueba y, a partir de ahí, se encuentran las intersecciones a ambos lados del punto, que describen el segmento que se va a quitar.

El [método Split](/previous-versions/ms827842(v=msdn.10)) del objeto [Stroke](/previous-versions/ms828477(v=msdn.10)) se usa para separar el segmento del resto del trazo y, a continuación, se elimina el segmento, dejando intacto el resto del trazo. Al igual que `EraseStrokes` en , el formulario se vuelve a dibujar antes de que el método vuelva.


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



## <a name="closing-the-form"></a>Cerrar el formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario elimina el [objeto InkCollector,](/previous-versions/ms836493(v=msdn.10)) `myInkCollector` .

 

 
