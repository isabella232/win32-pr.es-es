---
description: Windows GDI+ proporciona la función GetImageDecoders para que pueda determinar qué descodificadores de imagen están disponibles en el equipo.
ms.assetid: 793e23de-d959-4feb-8bf6-647a455c85ae
title: Enumeración de descodificadores instalados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a20a4e8ac88fa884483ebeaf6592b8085fde807
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072427"
---
# <a name="listing-installed-decoders"></a>Enumeración de descodificadores instalados

Windows GDI+ proporciona la [**función GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) para que pueda determinar qué descodificadores de imagen están disponibles en el equipo. **GetImageDecoders devuelve** una matriz de [**objetos ImageCodecInfo.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) Antes de llamar **a GetImageDecoders,** debe asignar un búfer lo suficientemente grande como para recibir esa matriz. Puede llamar a [**GetImageDecodersSize para**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) determinar el tamaño del búfer necesario.

En la siguiente aplicación de consola se enumeran los descodificadores de imagen disponibles:


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

   UINT  num;        // number of image decoders
   UINT  size;       // size, in bytes, of the image decoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many decoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageDecodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageDecoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageDecoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageDecoders(num, size, pImageCodecInfo);

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
image/x-emf
image/x-wmf
image/tiff
image/png
image/x-icon
```



 

 
