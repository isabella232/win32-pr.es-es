---
description: GDI+ proporciona la función GetImageEncoders para que pueda determinar qué codificadores de imágenes están disponibles en el equipo.
ms.assetid: a261cf61-b853-4208-984b-0d5040eb1667
title: Enumeración de codificadores instalados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310e9d366cdacde019373724f2b9feb3b94aef8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063443"
---
# <a name="listing-installed-encoders"></a>Enumeración de codificadores instalados

GDI+ proporciona la [**función GetImageEncoders para**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) que pueda determinar qué codificadores de imágenes están disponibles en el equipo. **GetImageEncoders devuelve** una matriz de [**objetos ImageCodecInfo.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) Antes de llamar **a GetImageEncoders,** debe asignar un búfer lo suficientemente grande como para recibir esa matriz. Puede llamar a [**GetImageEncodersSize para**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) determinar el tamaño del búfer necesario.

En la siguiente aplicación de consola se enumeran los codificadores de imagen disponibles:


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // number of image encoders
   UINT  size;       // size, in bytes, of the image encoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);

   // Display the graphics file format (MimeType)
   // for each ImageCodecInfo object.
   for(UINT j = 0; j < num; ++j)
   { 
      wprintf(L"%s\n", pImageCodecInfo[j].MimeType);   
   }

   free(pImageCodecInfo);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Al ejecutar la aplicación de consola anterior, la salida será similar a la siguiente:


```
image/bmp
image/jpeg
image/gif
image/tiff
image/png
```



 

 
