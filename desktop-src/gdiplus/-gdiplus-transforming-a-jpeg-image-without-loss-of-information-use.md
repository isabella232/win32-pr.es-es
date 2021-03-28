---
title: Transformación sin pérdida de una imagen JPEG
description: Al comprimir una imagen JPEG, parte de la información de la imagen se pierde.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984431"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>Transformación sin pérdida de una imagen JPEG

Al comprimir una imagen JPEG, parte de la información de la imagen se pierde. Si abre un archivo JPEG, modifica la imagen y la guarda en otro archivo JPEG, se reducirá la calidad. Si se repite el proceso muchas veces, verá una degradación sustancial en la calidad de la imagen.

Como JPEG es uno de los formatos de imagen más populares en la web, y dado que las personas a menudo desean modificar imágenes JPEG, GDI+ proporciona las siguientes transformaciones que se pueden realizar en imágenes JPEG sin pérdida de información:

-   Girar 90 grados
-   Girar 180 grados
-   Girar 270 grados
-   Voltear horizontalmente
-   Voltear verticalmente

Puede aplicar una de las transformaciones que se muestran en la lista anterior al llamar al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de un objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Si se cumplen las siguientes condiciones, la transformación continuará sin pérdida de información:

-   El archivo que se usa para construir el objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) es un archivo JPEG.
-   El ancho y el alto de la imagen son múltiplos de 16.

Si el ancho y el alto de la imagen no son múltiplos de 16, GDI+ hará lo mejor para conservar la calidad de la imagen al aplicar una de las transformaciones de giro o de volteo que se muestran en la lista anterior.

Para transformar una imagen JPEG, inicialice un objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) y pase la dirección de ese objeto al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Inicialice el objeto **EncoderParameters** para que tenga una matriz formada por un objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Inicialice un objeto **EncoderParameter** de modo que su miembro de **valor** apunte a una variable **ULong** que contiene uno de los siguientes elementos de la enumeración [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   EncoderValueTransformFlipHorizontal,
-   EncoderValueTransformFlipVertical

Establezca el miembro **GUID** del objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) en EncoderTransformation.

La siguiente aplicación de consola crea un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de un archivo JPEG y, a continuación, guarda la imagen en un archivo nuevo. Durante el proceso de guardar, la imagen se gira 90 grados. Si el ancho y el alto de la imagen son múltiplos de 16, el proceso de rotación y guardado de la imagen no provoca la pérdida de información.

La función Main se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



 

 
