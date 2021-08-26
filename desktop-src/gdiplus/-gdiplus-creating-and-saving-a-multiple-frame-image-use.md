---
description: Con determinados formatos de archivo, puede guardar varias imágenes (fotogramas) en un único archivo.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Creación y almacenamiento de una imagen de trama múltiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd99bc2d5f21c143b66ccc201f9a96a93f3437516a6fd1cdd03e521a00ceb59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115125"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Creación y almacenamiento de una imagen de trama múltiple

Con determinados formatos de archivo, puede guardar varias imágenes (fotogramas) en un único archivo. Por ejemplo, puede guardar varias páginas en un único archivo TIFF. Para guardar la primera página, llame al [método Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la [**clase Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Para guardar las páginas posteriores, llame [al método SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) de la **clase Image.**

> [!Note]  
> No puede usar [SaveAdd para](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) agregar fotogramas a un archivo gif animado.

 

La siguiente aplicación de consola crea un archivo TIFF con cuatro páginas. Las imágenes que se convierten en páginas del archivo TIFF proceden de cuatro archivos de disco: Shapes.bmp, Cereal.gif, Iron.jpg y House.png. El código construye primero cuatro objetos [**Image:**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) **multi**, **page2,** **page3** y **page4.** Al principio, **multi** contiene solo la imagen de Shapes.bmp, pero finalmente contiene las cuatro imágenes. A medida que las páginas individuales se agregan al objeto **de**  **varias** imágenes, también se agregan al archivo de disco Multiframe.tif.

Tenga en cuenta que el código [llama a Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (no a [SaveAdd)](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))para guardar la primera página. El primer argumento pasado al método Save es el nombre del archivo de disco que con el tiempo contendrá varios fotogramas. El segundo argumento pasado al método Save especifica el codificador que se usará para convertir los datos del objeto **multi**  [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) al formato (en este caso TIFF) requerido por el archivo de disco. Todas las llamadas posteriores al método SaveAdd del **objeto multi** Image usan automáticamente ese **mismo** codificador.  

El tercer argumento pasado al [método Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) es la dirección de un [**objeto EncoderParameters.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) El **objeto EncoderParameters** tiene una matriz que contiene un único [**objeto EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) El **miembro GUID** de ese objeto **EncoderParameter** se establece en EncoderSaveFlag. El **miembro Value** del objeto **EncoderParameter** apunta a **un ULONG** que contiene el valor EncoderValueMultiFrame.

El código guarda la segunda, tercera y cuarta página llamando al [método SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) del **objeto multi**[**Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)   El primer argumento pasado al método SaveAdd es la dirección de un **objeto Image.** La imagen de ese **objeto Image** se agrega al objeto **de** imagen múltiple y también se agrega al archivo de disco Multiframe.tif.   El segundo argumento pasado al método SaveAdd es la dirección del mismo objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que usó [el método Save.](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) La diferencia es que el **ULONG** al que apunta el **miembro Value** ahora contiene el valor EncoderValueFrameDimensionPage.

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

   EncoderParameters encoderParameters;
   ULONG             parameterValue;
   Status            stat;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create four image objects.
   Image* multi = new Image(L"Shapes.bmp");
   Image* page2 = new Image(L"Cereal.gif");
   Image* page3 = new Image(L"Iron.jpg");
   Image* page4 = new Image(L"House.png");

   // Save the first page (frame).
   parameterValue = EncoderValueMultiFrame;
   stat = multi->Save(L"MultiFrame.tif", &encoderClsid, &encoderParameters);
   if(stat == Ok)
      printf("Page 1 saved successfully.\n");

   // Save the second page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page2, &encoderParameters);
   if(stat == Ok)
      printf("Page 2 saved successfully.\n");

   // Save the third page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page3, &encoderParameters);
   if(stat == Ok)
      printf("Page 3 saved successfully.\n");

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page4, &encoderParameters);
   if(stat == Ok)
      printf("Page 4 saved successfully.\n");

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   stat = multi->SaveAdd(&encoderParameters);
   if(stat == Ok)
      printf("File closed successfully.\n");

   delete multi;
   delete page2;
   delete page3;
   delete page4;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
