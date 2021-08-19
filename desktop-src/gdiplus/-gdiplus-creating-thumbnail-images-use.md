---
description: Una imagen en miniatura es una versión pequeña de una imagen. Puede crear una imagen en miniatura llamando al método GetThumbnailImage de un objeto Image.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Creación de imágenes en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d44fec3220bef7a6691d3852d16f90e9cf43635c99f69bba16f3b569ebabc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696316"
---
# <a name="creating-thumbnail-images"></a>Creación de imágenes en miniatura

Una imagen en miniatura es una versión pequeña de una imagen. Puede crear una imagen en miniatura llamando al **método GetThumbnailImage** de un [**objeto Image.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)

En el ejemplo siguiente se crea un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Compass.bmp. La imagen original tiene un ancho de 640 píxeles y un alto de 479 píxeles. El código crea una imagen en miniatura que tiene un ancho de 100 píxeles y un alto de 100 píxeles.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



En la ilustración siguiente se muestra la imagen en miniatura.

![ilustración de un pequeño gráfico que muestra una brújula](images/thumbnail1.png)

 

 



