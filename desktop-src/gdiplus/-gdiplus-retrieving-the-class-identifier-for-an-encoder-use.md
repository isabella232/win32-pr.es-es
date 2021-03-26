---
description: La función GetEncoderClsid en el ejemplo siguiente recibe el tipo MIME de un codificador y devuelve el identificador de clase (CLSID) de ese codificador.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Recuperar el identificador de clase para un codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03193bfa9f2e86e92f66a649280828f12d4807c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985134"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a><span data-ttu-id="4edc9-103">Recuperar el identificador de clase para un codificador</span><span class="sxs-lookup"><span data-stu-id="4edc9-103">Retrieving the Class Identifier for an Encoder</span></span>

<span data-ttu-id="4edc9-104">La función GetEncoderClsid en el ejemplo siguiente recibe el tipo MIME de un codificador y devuelve el identificador de clase (**CLSID**) de ese codificador.</span><span class="sxs-lookup"><span data-stu-id="4edc9-104">The function GetEncoderClsid in the following example receives the MIME type of an encoder and returns the class identifier (**CLSID**) of that encoder.</span></span> <span data-ttu-id="4edc9-105">Los tipos MIME de los codificadores integrados en GDI+ de Windows son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4edc9-105">The MIME types of the encoders built into Windows GDI+ are as follows:</span></span>

-   <span data-ttu-id="4edc9-106">image/bmp</span><span class="sxs-lookup"><span data-stu-id="4edc9-106">image/bmp</span></span>
-   <span data-ttu-id="4edc9-107">image/jpeg</span><span class="sxs-lookup"><span data-stu-id="4edc9-107">image/jpeg</span></span>
-   <span data-ttu-id="4edc9-108">image/gif</span><span class="sxs-lookup"><span data-stu-id="4edc9-108">image/gif</span></span>
-   <span data-ttu-id="4edc9-109">image/tiff</span><span class="sxs-lookup"><span data-stu-id="4edc9-109">image/tiff</span></span>
-   <span data-ttu-id="4edc9-110">image/png</span><span class="sxs-lookup"><span data-stu-id="4edc9-110">image/png</span></span>

<span data-ttu-id="4edc9-111">La función llama a [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) para obtener una matriz de objetos [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="4edc9-111">The function calls [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) to get an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="4edc9-112">Si uno de los objetos **ImageCodecInfo** de la matriz representa el codificador solicitado, la función devuelve el índice del objeto **ImageCodecInfo** y copia el **CLSID** en la variable a la que apunta **pClsid**.</span><span class="sxs-lookup"><span data-stu-id="4edc9-112">If one of the **ImageCodecInfo** objects in that array represents the requested encoder, the function returns the index of the **ImageCodecInfo** object and copies the **CLSID** into the variable pointed to by **pClsid**.</span></span> <span data-ttu-id="4edc9-113">Si se produce un error en la función, devuelve – 1.</span><span class="sxs-lookup"><span data-stu-id="4edc9-113">If the function fails, it returns –1.</span></span>


```
int GetEncoderClsid(const WCHAR* format, CLSID* pClsid)
{
   UINT  num = 0;          // number of image encoders
   UINT  size = 0;         // size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo = NULL;

   GetImageEncodersSize(&num, &size);
   if(size == 0)
      return -1;  // Failure

   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));
   if(pImageCodecInfo == NULL)
      return -1;  // Failure

   GetImageEncoders(num, size, pImageCodecInfo);

   for(UINT j = 0; j < num; ++j)
   {
      if( wcscmp(pImageCodecInfo[j].MimeType, format) == 0 )
      {
         *pClsid = pImageCodecInfo[j].Clsid;
         free(pImageCodecInfo);
         return j;  // Success
      }    
   }

   free(pImageCodecInfo);
   return -1;  // Failure
}
```



<span data-ttu-id="4edc9-114">La siguiente aplicación de consola llama a la función GetEncoderClsid para determinar el **CLSID** del codificador PNG:</span><span class="sxs-lookup"><span data-stu-id="4edc9-114">The following console application calls the GetEncoderClsid function to determine the **CLSID** of the PNG encoder:</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

#include "GdiplusHelperFunctions.h"

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID  encoderClsid;
   INT    result;
   WCHAR  strGuid[39];

   result = GetEncoderClsid(L"image/png", &encoderClsid);

   if(result < 0)
   {
      printf("The PNG encoder is not installed.\n");
   }
   else
   {
      StringFromGUID2(encoderClsid, strGuid, 39);
      printf("An ImageCodecInfo object representing the PNG encoder\n");
      printf("was found at position %d in the array.\n", result);
      wprintf(L"The CLSID of the PNG encoder is %s.\n", strGuid);
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="4edc9-115">Al ejecutar la aplicación de consola anterior, obtendrá una salida similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="4edc9-115">When you run the preceding console application, you get an output similar to the following:</span></span>


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
