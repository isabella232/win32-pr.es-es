---
description: La clase Metafile, que hereda de la clase Image, permite registrar una secuencia de comandos de dibujo.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Grabación de metarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047cdce842a9b44096ebd0f866e1b1551a5f951e138557062dff5e8f8d54f3ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014785"
---
# <a name="recording-metafiles"></a>Grabación de metarchivos

La [**clase Metafile,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) que hereda de la [**clase Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) permite registrar una secuencia de comandos de dibujo. Los comandos registrados se pueden almacenar en memoria, guardarse en un archivo o guardarse en una secuencia. Los metarchivos pueden contener gráficos vectoriales, imágenes de trama y texto.

En el ejemplo siguiente se crea un [**objeto Metafile.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) El código usa el **objeto Metafile** para registrar una secuencia de comandos gráficos y, a continuación, guarda los comandos registrados en un archivo denominado SampleMetafile.emf. Tenga en cuenta que el constructor **metarchivo** recibe un identificador de contexto de dispositivo y el constructor [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recibe la dirección del **objeto Metafile.** La grabación se detiene (y los comandos grabados se guardan en el archivo) cuando el **objeto Graphics** sale del ámbito. Las dos últimas líneas de código muestran el metarchivo creando un nuevo objeto **Graphics** y pasando la dirección del objeto **Metarchivo** al método **DrawImage** de ese **objeto Graphics.** Tenga en cuenta que el código usa el mismo **objeto metarchivo** para registrar y mostrar (reproducir) el metarchivo.


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> Para registrar un metarchivo, debe construir un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un [**objeto Metarchivo.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) La grabación del metarchivo finaliza cuando ese **objeto Graphics** se elimina o sale del ámbito.

 

Un metarchivo contiene su propio estado gráfico, que se define mediante el [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) que se usa para registrar el metarchivo. Todas las propiedades del objeto **Graphics** (región de recorte, transformación del mundo, modo de suavizado y similares) que establezca al grabar el metarchivo se almacenarán en el metarchivo. Al mostrar el metarchivo, el dibujo se realizará según esas propiedades almacenadas.

En el ejemplo siguiente, suponga que el modo de suavizado se estableció en SmoothingModeNormal durante la grabación del metarchivo. Aunque el modo de suavizado del objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usado para la reproducción se establece en SmoothingModeHighQuality, el metarchivo se reproducirá según la configuración SmoothingModeNormal. Es el modo de suavizado establecido durante la grabación lo que es importante, no el modo de suavizado establecido antes de la reproducción.


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



