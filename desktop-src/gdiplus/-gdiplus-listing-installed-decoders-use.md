---
description: Windows GDI+ proporciona la función GetImageDecoders para que pueda determinar qué descodificadores de imágenes están disponibles en el equipo.
ms.assetid: 793e23de-d959-4feb-8bf6-647a455c85ae
title: Enumerar descodificadores instalados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a20a4e8ac88fa884483ebeaf6592b8085fde807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985158"
---
# <a name="listing-installed-decoders"></a><span data-ttu-id="28e83-103">Enumerar descodificadores instalados</span><span class="sxs-lookup"><span data-stu-id="28e83-103">Listing Installed Decoders</span></span>

<span data-ttu-id="28e83-104">Windows GDI+ proporciona la función [**GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) para que pueda determinar qué descodificadores de imágenes están disponibles en el equipo.</span><span class="sxs-lookup"><span data-stu-id="28e83-104">Windows GDI+ provides the [**GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) function so that you can determine which image decoders are available on your computer.</span></span> <span data-ttu-id="28e83-105">**GetImageDecoders** devuelve una matriz de objetos [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="28e83-105">**GetImageDecoders** returns an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="28e83-106">Antes de llamar a **GetImageDecoders**, debe asignar un búfer lo suficientemente grande como para recibir esa matriz.</span><span class="sxs-lookup"><span data-stu-id="28e83-106">Before you call **GetImageDecoders**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="28e83-107">Puede llamar a [**GetImageDecodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) para determinar el tamaño del búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="28e83-107">You can call [**GetImageDecodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="28e83-108">La siguiente aplicación de consola muestra los descodificadores de imágenes disponibles:</span><span class="sxs-lookup"><span data-stu-id="28e83-108">The following console application lists the available image decoders:</span></span>


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



<span data-ttu-id="28e83-109">Al ejecutar la aplicación de consola anterior, la salida será similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="28e83-109">When you run the preceding console application, the output will be similar to the following:</span></span>


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



 

 
