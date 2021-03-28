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
# <a name="creating-thumbnail-images"></a><span data-ttu-id="0bebf-104">Crear imágenes en miniatura</span><span class="sxs-lookup"><span data-stu-id="0bebf-104">Creating Thumbnail Images</span></span>

<span data-ttu-id="0bebf-105">Una imagen en miniatura es una versión pequeña de una imagen.</span><span class="sxs-lookup"><span data-stu-id="0bebf-105">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="0bebf-106">Puede crear una imagen en miniatura mediante una llamada al método **GetThumbnailImage** de un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="0bebf-106">You can create a thumbnail image by calling the **GetThumbnailImage** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span>

<span data-ttu-id="0bebf-107">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Compass.bmp.</span><span class="sxs-lookup"><span data-stu-id="0bebf-107">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Compass.bmp.</span></span> <span data-ttu-id="0bebf-108">La imagen original tiene un ancho de 640 píxeles y un alto de 479 píxeles.</span><span class="sxs-lookup"><span data-stu-id="0bebf-108">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="0bebf-109">El código crea una imagen en miniatura con un ancho de 100 píxeles y un alto de 100 píxeles.</span><span class="sxs-lookup"><span data-stu-id="0bebf-109">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



<span data-ttu-id="0bebf-110">En la ilustración siguiente se muestra la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="0bebf-110">The following illustration shows the thumbnail image.</span></span>

![Ilustración de un gráfico pequeño que muestra una brújula](images/thumbnail1.png)

 

 



