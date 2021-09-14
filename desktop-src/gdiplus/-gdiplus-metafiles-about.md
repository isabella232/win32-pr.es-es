---
description: Windows GDI+ proporciona la clase Metafile para que pueda registrar y mostrar metarchivos.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metarchivos (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072420"
---
# <a name="metafiles-gdi"></a>Metarchivos (GDI+)

Windows GDI+ proporciona la [**clase Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) para que pueda registrar y mostrar metarchivos. Un metarchivo, también denominado imagen vectorial, es una imagen que se almacena como una secuencia de comandos y configuraciones de dibujo. Los comandos y la configuración registrados en un objeto **metarchivo** se pueden almacenar en memoria o guardarse en un archivo o secuencia.

GDI+ pueden mostrar metarchivos que se han almacenado en los siguientes formatos:

-   Windows Formato de metarchivo (WMF)
-   Metarchivo mejorado (EMF)
-   EMF+

GDI+ puede registrar metarchivos en los formatos EMF y EMF+, pero no en el formato WMF.

EMF+ es una extensión de EMF que permite almacenar GDI+ registros. Hay dos variaciones en el formato EMF+: EMF+ Only y EMF+ Dual. EMF+ Solo los metarchivos contienen GDI+ registros. Estos metarchivos se pueden mostrar mediante GDI+, pero no Windows Interfaz de dispositivo gráfico (GDI). Los metarchivos duales de EMF+ contienen GDI+ y GDI. Cada GDI+ registro de un metarchivo dual emf+ se empareja con un registro GDI alternativo. Estos metarchivos se pueden mostrar mediante GDI+ o GDI.

En el ejemplo siguiente se registra una configuración y un comando de dibujo en un archivo de disco. Tenga en cuenta que en el ejemplo se crea un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y que el constructor del objeto **Graphics** recibe la dirección de un objeto [**Metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) como argumento.


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



Como se muestra en el ejemplo anterior, la [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) es la clave para grabar instrucciones y configuraciones en un [**objeto Metarchivo.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) Cualquier llamada realizada a un método de un **objeto Graphics** se puede registrar en un **objeto Metarchivo.** Del mismo modo, puede establecer cualquier propiedad de un objeto **Graphics** y registrar esa configuración en un **objeto Metarchivo.** La grabación finaliza cuando se elimina **el objeto Graphics** o se sale del ámbito.

En el ejemplo siguiente se muestra el metarchivo creado en el ejemplo anterior. El metarchivo se muestra con la esquina superior izquierda en (100, 100).


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



En el ejemplo siguiente se registra varias configuraciones de propiedades (región de recorte, transformación del mundo y modo de suavizado) en un [**objeto Metarchivo.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) A continuación, el código registra varias instrucciones de dibujo. Las instrucciones y la configuración se guardan en un archivo de disco.


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

 

 



