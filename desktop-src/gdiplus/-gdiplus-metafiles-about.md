---
description: Windows GDI+ proporciona la clase Metafile para que pueda grabar y mostrar metarchivos.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metaarchivos (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360280"
---
# <a name="metafiles-gdi"></a>Metaarchivos (GDI+)

Windows GDI+ proporciona la clase Metafile para que pueda grabar y mostrar [**metarchivos**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Un metarchivo, también denominado imagen vectorial, es una imagen que se almacena como una secuencia de comandos y valores de dibujo. Los comandos y la configuración registrados en un objeto de **metarchivo** se pueden almacenar en memoria o guardar en un archivo o una secuencia.

GDI+ puede mostrar los metaarchivos que se han almacenado en los formatos siguientes:

-   Formato WMF (WMF)
-   Metarchivo mejorado (EMF)
-   EMF +

GDI+ puede grabar metaarchivos en los formatos EMF y EMF +, pero no en formato WMF.

EMF + es una extensión de EMF que permite almacenar registros GDI+. Hay dos variaciones en el formato EMF +: EMF + only y EMF + dual. Los metaarchivos EMF + Only solo contienen registros GDI+. Estos metaarchivos se pueden mostrar en GDI+, pero no en Windows Interfaz de dispositivo gráfico (GDI). Los metaarchivos EMF + dual contienen registros GDI+ y GDI. Cada registro de GDI+ de un metarchivo EMF + dual se empareja con un registro GDI alternativo. Estos metaarchivos se pueden mostrar en GDI+ o en GDI.

En el ejemplo siguiente se registra una configuración y un comando de dibujo en un archivo de disco. Tenga en cuenta que en el ejemplo se crea un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y que el constructor del objeto **Graphics** recibe la dirección de un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) como argumento.


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



Como se muestra en el ejemplo anterior, la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) es la clave para registrar instrucciones y configuraciones en un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Cualquier llamada realizada a un método de un objeto **Graphics** se puede grabar en un objeto de **metarchivo** . Del mismo modo, puede establecer cualquier propiedad de un objeto **Graphics** y grabar esa configuración en un objeto de **metarchivo** . La grabación finaliza cuando el objeto **Graphics** se elimina o sale del ámbito.

En el ejemplo siguiente se muestra el metarchivo creado en el ejemplo anterior. El metarchivo se muestra con la esquina superior izquierda en (100, 100).


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



En el ejemplo siguiente se registran varios valores de propiedades (región de recorte, transformación universal y modo de suavizado) en un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Después, el código registra varias instrucciones de dibujo. Las instrucciones y la configuración se guardan en un archivo de disco.


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



En el ejemplo siguiente se muestra la imagen de metarchivo creada en el ejemplo anterior.


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



En la ilustración siguiente se muestra la salida del código anterior. Observe el suavizado de contorno, la región de recorte elíptica y la rotación de 30 grados.

![captura de pantalla de una ventana que contiene una elipse rellena con líneas que se originan en un punto fuera de la elipse](images/aboutgdip05-art00.png)

 

 



