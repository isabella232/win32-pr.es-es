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
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Uso de un mapa de bits almacenado en caché para mejorar el rendimiento

Los objetos [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) almacenan imágenes en un formato independiente del dispositivo. Un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) almacena una imagen en el formato del dispositivo de pantalla actual. La representación de una imagen almacenada en un objeto **CachedBitmap** es rápida porque ningún tiempo de procesamiento se dedica a convertir la imagen al formato requerido por el dispositivo de pantalla.

En el ejemplo siguiente se crea un objeto [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) a partir del archivo Texture.jpg. El **mapa de bits** y **CachedBitmap** se dibujan cada 30.000 veces. Si ejecuta el código, verá que las imágenes **CachedBitmap** se dibujan mucho más rápido que las imágenes de **mapa de bits** .


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
> Un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) coincide con el formato del dispositivo de pantalla en el momento en que se construyó el objeto **CachedBitmap** . Si el usuario del programa cambia la configuración de pantalla, el código debe construir un nuevo objeto **CachedBitmap** . El método **DrawImage** producirá un error si se le pasa un objeto **CachedBitmap** que se creó antes de un cambio en el formato de presentación.

 

 

 



