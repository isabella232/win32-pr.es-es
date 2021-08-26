---
description: Una de las propiedades de la clase Graphics es la región de recorte. Todo el dibujo realizado por un objeto Graphics determinado está restringido a la región de recorte de ese objeto Graphics. Puede establecer la región de recorte llamando al método SetClip.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Recorte con una región
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2569350dd0d25066c42fc8ee102cad76e8e77c425bd075122da2179dd3249c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943905"
---
# <a name="clipping-with-a-region"></a>Recorte con una región

Una de las propiedades de la clase [**Graphics es**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) la región de recorte. Todo el dibujo realizado por un objeto **Graphics** determinado está restringido a la región de recorte de ese **objeto Graphics.** Puede establecer la región de recorte llamando al **método SetClip.**

En el ejemplo siguiente se crea una ruta de acceso que consta de un único polígono. A continuación, el código crea una región basada en esa ruta de acceso. La dirección de la región se pasa al **método SetClip** de un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y, a continuación, se dibujan dos cadenas.


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



En la ilustración siguiente se muestran las cadenas recortadas.

![ilustración que muestra partes de dos oraciones que aparecen dentro de una forma de cuatro lados](images/clip1.png)

 

 



