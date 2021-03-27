---
description: Con determinados formatos de archivo, puede guardar varias imágenes (fotogramas) en un solo archivo.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Creación y almacenamiento de una imagen de trama múltiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156201"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Creación y almacenamiento de una imagen de trama múltiple

Con determinados formatos de archivo, puede guardar varias imágenes (fotogramas) en un solo archivo. Por ejemplo, puede guardar varias páginas en un solo archivo TIFF. Para guardar la primera página, llame al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Para guardar las páginas siguientes, llame al método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) de la clase **Image** .

> [!Note]  
> No se puede usar [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) para agregar fotogramas a un archivo GIF animado.

 

La siguiente aplicación de consola crea un archivo TIFF con cuatro páginas. Las imágenes que se convierten en las páginas del archivo TIFF proceden de cuatro archivos de disco: Shapes.bmp, Cereal.gif, Iron.jpg y House.png. Code First construye cuatro objetos [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : **multi**, **página2**, **PAGE3** y **page4**. Al principio, **multi** solo contiene la imagen de Shapes.bmp, pero finalmente contiene las cuatro imágenes. A medida que las páginas individuales se agregan al objeto de **varias**  **imágenes** , también se agregan al archivo de disco multiframe. tif.

Tenga en cuenta que el código llama a [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (no a [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) para guardar la primera página. El primer argumento que se pasa al método Save es el nombre del archivo de disco que finalmente contendrá varios fotogramas. El segundo argumento que se pasa al método Save especifica el codificador que se utilizará para convertir los datos del objeto de **varias**  [**imágenes**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) en el formato (en este caso, TIFF) que requiere el archivo de disco. El mismo codificador se usa automáticamente en todas las llamadas subsiguientes al método SaveAdd del objeto de **varias**  **imágenes** .

El tercer argumento que se pasa al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) es la dirección de un objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) . El objeto **EncoderParameters** tiene una matriz que contiene un único objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . El miembro **GUID** de ese objeto **EncoderParameter** se establece en EncoderSaveFlag. El miembro **Value** del objeto **EncoderParameter** apunta a un **ULong** que contiene el valor EncoderValueMultiFrame.

El código guarda las páginas segunda, tercera y cuarta llamando al método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) del objeto de **varias**  [**imágenes**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . El primer argumento que se pasa al método SaveAdd es la dirección de un objeto de **imagen** . La imagen de ese objeto de **imagen** se agrega al objeto de **varias**  **imágenes** y también se agrega al archivo de disco multiframe. tif. El segundo argumento que se pasa al método SaveAdd es la dirección del mismo objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que usó el método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) . La diferencia es que el **ULong** al que apunta el miembro de **valor** contiene ahora el valor EncoderValueFrameDimensionPage.

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



 

 
