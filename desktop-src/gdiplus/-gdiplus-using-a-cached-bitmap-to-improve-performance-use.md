---
description: Los objetos Image y Bitmap almacenan imágenes en un formato independiente del dispositivo.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Usar un mapa de bits almacenado en caché para mejorar el rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580465"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Usar un mapa de bits almacenado en caché para mejorar el rendimiento

[**Los objetos Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**y Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) almacenan imágenes en un formato independiente del dispositivo. Un [**objeto CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) almacena una imagen en el formato del dispositivo de visualización actual. La representación de una imagen almacenada en un objeto **CachedBitmap** es rápida porque no se dedica ningún tiempo de procesamiento a convertir la imagen al formato requerido por el dispositivo para mostrar.

En el ejemplo siguiente se crea [**un objeto Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) a partir del archivo Texture.jpg. Bitmap **y** **CachedBitmap** se dibujan 30 000 veces. Si ejecuta el código, verá que las imágenes **cachedBitmap** se dibujan mucho más rápido que las imágenes **de mapa de** bits.


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
> Un [**objeto CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) coincide con el formato del dispositivo para mostrar en el momento en que se construyó el objeto **CachedBitmap.** Si el usuario del programa cambia la configuración de presentación, el código debe construir un nuevo objeto **CachedBitmap.** Se producirá un error en el método **DrawImage** si se le pasa un objeto **CachedBitmap** que se creó antes de un cambio en el formato de presentación.

 

 

 



