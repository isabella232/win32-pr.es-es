---
description: Una imagen en miniatura es una versión pequeña de una imagen. Puede crear una imagen en miniatura mediante una llamada al método GetThumbnailImage de un objeto de imagen.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Crear imágenes en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552178"
---
# <a name="creating-thumbnail-images"></a>Crear imágenes en miniatura

Una imagen en miniatura es una versión pequeña de una imagen. Puede crear una imagen en miniatura mediante una llamada al método **GetThumbnailImage** de un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .

En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Compass.bmp. La imagen original tiene un ancho de 640 píxeles y un alto de 479 píxeles. El código crea una imagen en miniatura con un ancho de 100 píxeles y un alto de 100 píxeles.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



En la ilustración siguiente se muestra la imagen en miniatura.

![Ilustración de un gráfico pequeño que muestra una brújula](images/thumbnail1.png)

 

 



