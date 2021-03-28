---
description: La clase Image proporciona métodos básicos para cargar y mostrar imágenes de trama e imágenes vectoriales. La clase Metafile, que hereda de la clase Image, proporciona métodos más especializados para grabar, mostrar y examinar imágenes vectoriales.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Cargar y mostrar metaarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082104"
---
# <a name="loading-and-displaying-metafiles"></a>Cargar y mostrar metaarchivos

La clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona métodos básicos para cargar y mostrar imágenes de trama e imágenes vectoriales. La clase [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que hereda de la clase **Image** , proporciona métodos más especializados para grabar, mostrar y examinar imágenes vectoriales.

Para mostrar una imagen vectorial (metarchivo) en la pantalla, necesita un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Pase el nombre de un archivo (o un puntero a un flujo) a un constructor de **imagen** . Después de crear un objeto de **imagen** , pase la dirección de ese objeto de **imagen** al método **DrawImage** de un objeto **Graphics** .

En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de un archivo EMF (metarchivo mejorado) y, a continuación, se dibuja la imagen con la esquina superior izquierda en (60, 10):


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



En la ilustración siguiente se muestra la imagen dibujada en la ubicación especificada.

![captura de pantalla de una ventana que contiene una imagen y especifica el punto de origen](images/imageposition2.png)

 

 



