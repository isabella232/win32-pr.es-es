---
title: Transformación sin pérdida de una imagen JPEG
description: Al comprimir una imagen JPEG, se pierde parte de la información de la imagen.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67152084f95220db3fe7afecfa4be07b366a92b31eb713ec192a2805ecb42ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977295"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>Transformación sin pérdida de una imagen JPEG

Al comprimir una imagen JPEG, se pierde parte de la información de la imagen. Si abre un archivo JPEG, modifica la imagen y la guarda en otro archivo JPEG, la calidad disminuirá. Si repite ese proceso muchas veces, verá una degradación sustancial en la calidad de la imagen.

Dado que JPEG es uno de los formatos de imagen más populares en la Web, y dado que a los usuarios les suele gustar modificar imágenes JPEG, GDI+ proporciona las siguientes transformaciones que se pueden realizar en imágenes JPEG sin pérdida de información:

-   Girar 90 grados
-   Girar 180° grados
-   Girar 270° grados
-   Voltear horizontalmente
-   Voltear verticalmente

Puede aplicar una de las transformaciones que se muestran en la lista anterior al llamar al [método Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de un [**objeto Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Si se cumplen las condiciones siguientes, la transformación continuará sin pérdida de información:

-   El archivo utilizado para construir el [**objeto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) es un archivo JPEG.
-   El ancho y alto de la imagen son múltiplo de 16.

Si el ancho y el alto de la imagen no son múltiplos de 16, GDI+ hará todo lo posible para conservar la calidad de la imagen al aplicar una de las transformaciones de giro o volteo que se muestran en la lista anterior.

Para transformar una imagen JPEG, inicialice un objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) y pase la dirección de ese objeto al [método Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la [**clase Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Inicialice **el objeto EncoderParameters** para que tenga una matriz que consta de un [**objeto EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) Inicialice ese objeto **EncoderParameter** para que su miembro **Value** apunta a una variable **ULONG** que contiene uno de los siguientes elementos de la [**enumeración EncoderValue:**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue)

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   EncoderValueTransformFlipHorizontal,
-   EncoderValueTransformFlipVertical

Establezca el **miembro Guid** del [**objeto EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) en EncoderTransformation.

La siguiente aplicación de consola crea un [**objeto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de un archivo JPEG y, a continuación, guarda la imagen en un archivo nuevo. Durante el proceso de guardado, la imagen gira 90 grados. Si el ancho y el alto de la imagen son múltiplo de 16, el proceso de rotación y guardado de la imagen no produce pérdida de información.

La función main se basa en la función auxiliar GetEncoderClsid, que se muestra en [Recuperación](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)del identificador de clase para un codificador .


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
