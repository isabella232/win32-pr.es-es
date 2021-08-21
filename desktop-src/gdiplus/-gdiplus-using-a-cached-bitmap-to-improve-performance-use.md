---
description: Los objetos Image y Bitmap almacenan imágenes en un formato independiente del dispositivo.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Usar un mapa de bits almacenado en caché para mejorar el rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ffee17a2c8d564a38235cc83d204eacc9b4edf2e8070cb5971d55f1f991169f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036333"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Usar un mapa de bits almacenado en caché para mejorar el rendimiento

[**Los objetos Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**y Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) almacenan imágenes en un formato independiente del dispositivo. Un [**objeto CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) almacena una imagen en el formato del dispositivo de visualización actual. La representación de una imagen almacenada en un objeto **CachedBitmap** es rápida porque no se dedica ningún tiempo de procesamiento a convertir la imagen al formato requerido por el dispositivo para mostrar.

En el ejemplo siguiente se crea [**un objeto Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) a partir del archivo Texture.jpg. Bitmap **y** **CachedBitmap** se dibujan 30 000 veces cada uno. Si ejecuta el código, verá que las imágenes **cachedBitmap** se dibujan mucho más rápido que las imágenes **de mapa de** bits.


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
> Un [**objeto CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) coincide con el formato del dispositivo de presentación en el momento en que se construyó el objeto **CachedBitmap.** Si el usuario del programa cambia la configuración de presentación, el código debe construir un nuevo objeto **CachedBitmap.** El **método DrawImage** producirá un error si se pasa un objeto **CachedBitmap** que se creó antes de un cambio en el formato de presentación.

 

 

 



