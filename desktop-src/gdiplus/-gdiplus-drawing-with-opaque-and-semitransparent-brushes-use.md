---
description: Al rellenar una forma, debe pasar la dirección de un objeto Brush a uno de los métodos Fill de la clase Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Dibujar con pinceles opacos y semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156196"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Dibujar con pinceles opacos y semitransparentes

Al rellenar una forma, debe pasar la dirección de un objeto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) a uno de los métodos Fill de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . El único parámetro del constructor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) es un objeto de [**color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) . Para rellenar una forma opaca, establezca el componente alfa del color en 255. Para rellenar una forma semitransparente, establezca el componente alfa en cualquier valor entre 1 y 254.

Cuando se rellena una forma semitransparente, el color de la forma se mezcla con los colores del fondo. El componente alfa especifica cómo se mezclan los colores de la forma y el fondo; los valores alfa cercanos a 0 dan más peso en los colores de fondo y los valores alfa cercanos a 255 colocan más peso en el color de la forma.

En el ejemplo siguiente se dibuja una imagen y, a continuación, se rellenan tres elipses que se superponen a la imagen. La primera elipse usa un componente alfa de 255, por lo que es opaca. La segunda y tercera elipses usan un componente alfa de 128, por lo que son semitransparentes; puede ver la imagen de fondo a través de las elipses. La llamada a [**Graphics:: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) hace que se realice la combinación de la tercera elipse junto con la corrección gamma.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



En la ilustración siguiente se muestra la salida del código anterior.

![Ilustración en la que se muestra una imagen superpuesta por tres elipses: una opaca, una ligeramente transparente, una muy transparente](images/compqualellipse.png)

 

 



