---
description: La clase Metafile, que hereda de la clase Image, permite grabar una secuencia de comandos de dibujo.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Grabar metaarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984439"
---
# <a name="recording-metafiles"></a>Grabar metaarchivos

La clase [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que hereda de la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , permite grabar una secuencia de comandos de dibujo. Los comandos grabados se pueden almacenar en memoria, guardar en un archivo o guardar en una secuencia. Los metaarchivos pueden contener gráficos vectoriales, imágenes de trama y texto.

En el ejemplo siguiente se crea un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . El código usa el objeto de **metarchivo** para registrar una secuencia de comandos de gráficos y, a continuación, guarda los comandos grabados en un archivo denominado SampleMetafile. EMF. Tenga en cuenta que el constructor de **metarchivo** recibe un identificador de contexto de dispositivo y el constructor de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recibe la dirección del objeto de **metarchivo** . La grabación se detiene (y los comandos grabados se guardan en el archivo) cuando el objeto **gráfico** sale del ámbito. Las dos últimas líneas de código muestran el metarchivo creando un nuevo objeto **Graphics** y pasando la dirección del objeto de **metarchivo** al método **DrawImage** de ese objeto **Graphics** . Tenga en cuenta que el código utiliza el mismo objeto de **metarchivo** para grabar y mostrar (reproducir) el metarchivo.


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
> Para grabar un metarchivo, debe construir un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . La grabación del metarchivo finaliza cuando ese objeto **gráfico** se elimina o sale del ámbito.

 

Un metarchivo contiene su propio estado de gráficos, que se define mediante el objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) que se usa para grabar el metarchivo. Cualquier propiedad del objeto **Graphics** (la región de recorte, la transformación universal, el modo de suavizado y el parecido) que establezca al grabar el metarchivo se almacenará en el metarchivo. Al mostrar el metarchivo, el dibujo se realizará según las propiedades almacenadas.

En el ejemplo siguiente, supongamos que el modo de suavizado se estableció en SmoothingModeNormal durante la grabación del metarchivo. Aunque el modo de suavizado del objeto de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) que se usa para la reproducción está establecido en SmoothingModeHighQuality, el metarchivo se reproducirá según la configuración de SmoothingModeNormal. Es el modo de suavizado establecido durante la grabación que es importante, no el modo de suavizado establecido antes de la reproducción.


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



