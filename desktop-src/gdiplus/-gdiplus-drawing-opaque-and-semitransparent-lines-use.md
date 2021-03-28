---
description: Al dibujar una línea, debe pasar la dirección de un objeto Pen al método DrawLine de la clase Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Dibujo de líneas opacas y semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557437"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>Dibujo de líneas opacas y semitransparentes

Al dibujar una línea, debe pasar la dirección de un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) al método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Uno de los parámetros del constructor **Pen** es un objeto de [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Para dibujar una línea opaca, establezca el componente alfa del color en 255. Para dibujar una línea semitransparente, establezca el componente alfa en cualquier valor entre 1 y 254.

Cuando se dibuja una línea semitransparente sobre un fondo, el color de la línea se mezcla con los colores del fondo. El componente alfa especifica cómo se mezclan los colores de línea y de fondo; los valores alfa cercanos a 0 dan más peso en los colores de fondo y los valores alfa cercanos a 255 colocan más peso en el color de línea.

En el ejemplo siguiente se dibuja una imagen y, a continuación, se dibujan tres líneas que usan la imagen como fondo. La primera línea usa un componente alfa de 255, por lo que es opaca. La segunda y tercera líneas usan un componente alfa de 128, por lo que son semitransparentes; puede ver la imagen de fondo a través de las líneas. La llamada a [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) hace que la combinación de la tercera línea se realice junto con la corrección gamma.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



En la ilustración siguiente se muestra la salida del código anterior.

![Ilustración en la que se muestra una imagen superpuesta por tres líneas anchas: una opaca, una ligeramente transparente y una muy transparente](images/compqualline.png)

 

 



