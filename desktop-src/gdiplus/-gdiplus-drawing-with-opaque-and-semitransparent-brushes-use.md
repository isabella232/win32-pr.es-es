---
description: Al rellenar una forma, debe pasar la dirección de un objeto Brush a uno de los métodos de relleno de la clase Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Dibujo con pinceles opacos y semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce5bb89c460c9769f805fb33af9eb91e9d8207448e702476aff4d25dec33a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248879"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Dibujo con pinceles opacos y semitransparentes

Al rellenar una forma, debe pasar la dirección de un [**objeto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) a uno de los métodos de relleno de la [**clase Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) El único parámetro del constructor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) es un [**objeto Color.**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) Para rellenar una forma opaca, establezca el componente alfa del color en 255. Para rellenar una forma semitransparente, establezca el componente alfa en cualquier valor entre 1 y 254.

Cuando se rellena una forma semitransparente, el color de la forma se mezcla con los colores del fondo. El componente alfa especifica cómo se mezclan la forma y los colores de fondo; Los valores alfa cercanos a 0 dan más peso a los colores de fondo y los valores alfa cercanos a 255 ponderan más el color de forma.

En el ejemplo siguiente se dibuja una imagen y, a continuación, se rellenan tres puntos suspensivos que se superponen a la imagen. La primera elipse usa un componente alfa de 255, por lo que es opaca. La segunda y tercera elipses usan un componente alfa de 128, por lo que son semitransparentes; puede ver la imagen de fondo a través de las elipses. La llamada a [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) hace que la combinación de la tercera elipse se haga junto con la corrección gamma.


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

![ilustración en la que se muestra una imagen superada por tres puntos suspensivos: uno opaco, otro ligeramente transparente y otro muy transparente](images/compqualellipse.png)

 

 



