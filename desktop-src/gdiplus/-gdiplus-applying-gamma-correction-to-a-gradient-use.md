---
description: 'Puede habilitar la corrección gamma para un pincel de degradado pasando TRUE al método PathGradientBrush:: SetGammaCorrection de ese pincel.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Aplicar la corrección gamma a un degradado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156233"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Aplicar la corrección gamma a un degradado

Puede habilitar la corrección gamma para un pincel de degradado pasando **true** al método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) de ese pincel. Puede deshabilitar la corrección gamma pasando **false** al método **PathGradientBrush:: SetGammaCorrection** . La corrección gamma está deshabilitada de forma predeterminada.

En el ejemplo siguiente se crea un pincel de degradado lineal y se utiliza ese pincel para rellenar dos rectángulos. El primer rectángulo se rellena sin corrección gamma y el segundo rectángulo se rellena con la corrección gamma.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



En la ilustración siguiente se muestran los dos rectángulos rellenos. El rectángulo superior, que no tiene corrección gamma, aparece oscuro en el centro. El rectángulo inferior, que tiene corrección gamma, parece tener una intensidad más uniforme.

![Ilustración que muestra dos rectángulos: el relleno en color de la primera varía en intensidad, el relleno del segundo varía menos](images/gammagradient1.png)

En el ejemplo siguiente se crea un pincel de degradado de trazado basado en un trazado en forma de estrella. El código usa el pincel de degradado de trazado con la corrección gamma deshabilitada (valor predeterminado) para rellenar la ruta de acceso. Después, el código pasa **true** al método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) para habilitar la corrección gamma del pincel de degradado de trazado. La llamada a [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) establece la transformación universal de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) de modo que la siguiente llamada a [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) llene una estrella situada a la derecha de la primera estrella.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



En la ilustración siguiente se muestra la salida del código anterior. La estrella de la derecha tiene corrección gamma. Tenga en cuenta que la estrella de la izquierda, que no tiene corrección gamma, tiene áreas que aparecen oscuras.

![la ilustración de la señal de 2 5 comienza con un relleno de degradado de color; el primero tiene áreas oscuras, la segunda no](images/gammagradient2.png)

 

 



