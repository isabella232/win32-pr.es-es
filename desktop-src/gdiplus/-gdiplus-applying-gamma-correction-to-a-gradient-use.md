---
description: Puede habilitar la corrección gamma para un pincel de degradado pasando TRUE al método PathGradientBrush::SetGammaCorrection de ese pincel.
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Aplicar corrección gamma a un degradado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eae76306e5c68804d76777d9fc80c65d06904702487a8b60f80659b9d16a96ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888545"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Aplicar corrección gamma a un degradado

Puede habilitar la corrección gamma para un pincel de degradado pasando **TRUE** al método [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) de ese pincel. Puede deshabilitar la corrección gamma pasando **FALSE** al **método PathGradientBrush::SetGammaCorrection.** La corrección gamma está deshabilitada de forma predeterminada.

En el ejemplo siguiente se crea un pincel de degradado lineal y se usa ese pincel para rellenar dos rectángulos. El primer rectángulo se rellena sin corrección gamma y el segundo rectángulo se rellena con corrección gamma.


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

![ilustración que muestra dos rectángulos: el relleno coloreado del primero varía en intensidad, el relleno del segundo varía menos](images/gammagradient1.png)

En el ejemplo siguiente se crea un pincel de degradado de trazado basado en un trazado con forma de estrella. El código usa el pincel de degradado de ruta de acceso con la corrección gamma deshabilitada (el valor predeterminado) para rellenar la ruta de acceso. A continuación, el código pasa **TRUE** al [**método PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) para habilitar la corrección gamma para el pincel de degradado de ruta de acceso. La llamada a [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) establece la transformación del mundo de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que la llamada subsiguiente a [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) rellene una estrella que se encuentra a la derecha de la primera estrella.


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

![ilustración de dos inicios de cinco puntos con relleno de degradado de color; el primero tiene áreas oscuras, el segundo no](images/gammagradient2.png)

 

 



