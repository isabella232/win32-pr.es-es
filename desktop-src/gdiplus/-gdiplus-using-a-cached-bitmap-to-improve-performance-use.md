---
description: Los objetos Image y Bitmap almacenan imágenes en un formato independiente del dispositivo.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Uso de un mapa de bits almacenado en caché para mejorar el rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997453"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a><span data-ttu-id="25217-103">Uso de un mapa de bits almacenado en caché para mejorar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="25217-103">Using a Cached Bitmap to Improve Performance</span></span>

<span data-ttu-id="25217-104">Los objetos [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) almacenan imágenes en un formato independiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25217-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) objects store images in a device-independent format.</span></span> <span data-ttu-id="25217-105">Un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) almacena una imagen en el formato del dispositivo de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="25217-105">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object stores an image in the format of the current display device.</span></span> <span data-ttu-id="25217-106">La representación de una imagen almacenada en un objeto **CachedBitmap** es rápida porque ningún tiempo de procesamiento se dedica a convertir la imagen al formato requerido por el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="25217-106">Rendering an image stored in a **CachedBitmap** object is fast because no processing time is spent converting the image to the format required by the display device.</span></span>

<span data-ttu-id="25217-107">En el ejemplo siguiente se crea un objeto [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) a partir del archivo Texture.jpg.</span><span class="sxs-lookup"><span data-stu-id="25217-107">The following example creates a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object and a [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object from the file Texture.jpg.</span></span> <span data-ttu-id="25217-108">El **mapa de bits** y **CachedBitmap** se dibujan cada 30.000 veces.</span><span class="sxs-lookup"><span data-stu-id="25217-108">The **Bitmap** and the **CachedBitmap** are each drawn 30,000 times.</span></span> <span data-ttu-id="25217-109">Si ejecuta el código, verá que las imágenes **CachedBitmap** se dibujan mucho más rápido que las imágenes de **mapa de bits** .</span><span class="sxs-lookup"><span data-stu-id="25217-109">If you run the code, you will see that the **CachedBitmap** images are drawn substantially faster than the **Bitmap** images.</span></span>


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> <span data-ttu-id="25217-110">Un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) coincide con el formato del dispositivo de pantalla en el momento en que se construyó el objeto **CachedBitmap** .</span><span class="sxs-lookup"><span data-stu-id="25217-110">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object matches the format of the display device at the time the **CachedBitmap** object was constructed.</span></span> <span data-ttu-id="25217-111">Si el usuario del programa cambia la configuración de pantalla, el código debe construir un nuevo objeto **CachedBitmap** .</span><span class="sxs-lookup"><span data-stu-id="25217-111">If the user of your program changes the display settings, your code should construct a new **CachedBitmap** object.</span></span> <span data-ttu-id="25217-112">El método **DrawImage** producirá un error si se le pasa un objeto **CachedBitmap** que se creó antes de un cambio en el formato de presentación.</span><span class="sxs-lookup"><span data-stu-id="25217-112">The **DrawImage** method will fail if you pass it a **CachedBitmap** object that was created prior to a change in the display format.</span></span>

 

 

 



