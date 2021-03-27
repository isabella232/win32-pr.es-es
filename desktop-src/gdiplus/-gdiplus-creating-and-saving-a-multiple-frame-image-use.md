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
# <a name="creating-and-saving-a-multiple-frame-image"></a><span data-ttu-id="83aa6-103">Creación y almacenamiento de una imagen de trama múltiple</span><span class="sxs-lookup"><span data-stu-id="83aa6-103">Creating and Saving a Multiple-Frame Image</span></span>

<span data-ttu-id="83aa6-104">Con determinados formatos de archivo, puede guardar varias imágenes (fotogramas) en un solo archivo.</span><span class="sxs-lookup"><span data-stu-id="83aa6-104">With certain file formats, you can save multiple images (frames) to a single file.</span></span> <span data-ttu-id="83aa6-105">Por ejemplo, puede guardar varias páginas en un solo archivo TIFF.</span><span class="sxs-lookup"><span data-stu-id="83aa6-105">For example, you can save several pages to a single TIFF file.</span></span> <span data-ttu-id="83aa6-106">Para guardar la primera página, llame al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="83aa6-106">To save the first page, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="83aa6-107">Para guardar las páginas siguientes, llame al método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) de la clase **Image** .</span><span class="sxs-lookup"><span data-stu-id="83aa6-107">To save subsequent pages, call the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **Image** class.</span></span>

> [!Note]  
> <span data-ttu-id="83aa6-108">No se puede usar [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) para agregar fotogramas a un archivo GIF animado.</span><span class="sxs-lookup"><span data-stu-id="83aa6-108">You cannot use [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) to add frames to an animated gif file.</span></span>

 

<span data-ttu-id="83aa6-109">La siguiente aplicación de consola crea un archivo TIFF con cuatro páginas.</span><span class="sxs-lookup"><span data-stu-id="83aa6-109">The following console application creates a TIFF file with four pages.</span></span> <span data-ttu-id="83aa6-110">Las imágenes que se convierten en las páginas del archivo TIFF proceden de cuatro archivos de disco: Shapes.bmp, Cereal.gif, Iron.jpg y House.png.</span><span class="sxs-lookup"><span data-stu-id="83aa6-110">The images that become the pages of the TIFF file come from four disk files: Shapes.bmp, Cereal.gif, Iron.jpg, and House.png.</span></span> <span data-ttu-id="83aa6-111">Code First construye cuatro objetos [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : **multi**, **página2**, **PAGE3** y **page4**.</span><span class="sxs-lookup"><span data-stu-id="83aa6-111">The code first constructs four [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects: **multi**, **page2**, **page3**, and **page4**.</span></span> <span data-ttu-id="83aa6-112">Al principio, **multi** solo contiene la imagen de Shapes.bmp, pero finalmente contiene las cuatro imágenes.</span><span class="sxs-lookup"><span data-stu-id="83aa6-112">At first, **multi** contains only the image from Shapes.bmp, but eventually it contains all four images.</span></span> <span data-ttu-id="83aa6-113">A medida que las páginas individuales se agregan al objeto de **varias**  **imágenes** , también se agregan al archivo de disco multiframe. tif.</span><span class="sxs-lookup"><span data-stu-id="83aa6-113">As the individual pages are added to the **multi**  **Image** object, they are also added to the disk file Multiframe.tif.</span></span>

<span data-ttu-id="83aa6-114">Tenga en cuenta que el código llama a [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (no a [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) para guardar la primera página.</span><span class="sxs-lookup"><span data-stu-id="83aa6-114">Note that the code calls [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) to save the first page.</span></span> <span data-ttu-id="83aa6-115">El primer argumento que se pasa al método Save es el nombre del archivo de disco que finalmente contendrá varios fotogramas.</span><span class="sxs-lookup"><span data-stu-id="83aa6-115">The first argument passed to the Save method is the name of the disk file that will eventually contain several frames.</span></span> <span data-ttu-id="83aa6-116">El segundo argumento que se pasa al método Save especifica el codificador que se utilizará para convertir los datos del objeto de **varias**  [**imágenes**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) en el formato (en este caso, TIFF) que requiere el archivo de disco.</span><span class="sxs-lookup"><span data-stu-id="83aa6-116">The second argument passed to the Save method specifies the encoder that will be used to convert the data in the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object to the format (in this case TIFF) required by the disk file.</span></span> <span data-ttu-id="83aa6-117">El mismo codificador se usa automáticamente en todas las llamadas subsiguientes al método SaveAdd del objeto de **varias**  **imágenes** .</span><span class="sxs-lookup"><span data-stu-id="83aa6-117">That same encoder is used automatically by all subsequent calls to the SaveAdd method of the **multi**  **Image** object.</span></span>

<span data-ttu-id="83aa6-118">El tercer argumento que se pasa al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) es la dirección de un objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) .</span><span class="sxs-lookup"><span data-stu-id="83aa6-118">The third argument passed to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method is the address of an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object.</span></span> <span data-ttu-id="83aa6-119">El objeto **EncoderParameters** tiene una matriz que contiene un único objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="83aa6-119">The **EncoderParameters** object has an array that contains a single [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="83aa6-120">El miembro **GUID** de ese objeto **EncoderParameter** se establece en EncoderSaveFlag.</span><span class="sxs-lookup"><span data-stu-id="83aa6-120">The **Guid** member of that **EncoderParameter** object is set to EncoderSaveFlag.</span></span> <span data-ttu-id="83aa6-121">El miembro **Value** del objeto **EncoderParameter** apunta a un **ULong** que contiene el valor EncoderValueMultiFrame.</span><span class="sxs-lookup"><span data-stu-id="83aa6-121">The **Value** member of the **EncoderParameter** object points to a **ULONG** that contains the value EncoderValueMultiFrame.</span></span>

<span data-ttu-id="83aa6-122">El código guarda las páginas segunda, tercera y cuarta llamando al método [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) del objeto de **varias**  [**imágenes**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="83aa6-122">The code saves the second, third, and fourth pages by calling the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="83aa6-123">El primer argumento que se pasa al método SaveAdd es la dirección de un objeto de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="83aa6-123">The first argument passed to the SaveAdd method is the address of an **Image** object.</span></span> <span data-ttu-id="83aa6-124">La imagen de ese objeto de **imagen** se agrega al objeto de **varias**  **imágenes** y también se agrega al archivo de disco multiframe. tif.</span><span class="sxs-lookup"><span data-stu-id="83aa6-124">The image in that **Image** object is added to the **multi**  **Image** object and is also added to the Multiframe.tif disk file.</span></span> <span data-ttu-id="83aa6-125">El segundo argumento que se pasa al método SaveAdd es la dirección del mismo objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que usó el método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) .</span><span class="sxs-lookup"><span data-stu-id="83aa6-125">The second argument passed to the SaveAdd method is the address of the same [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that was used by the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method.</span></span> <span data-ttu-id="83aa6-126">La diferencia es que el **ULong** al que apunta el miembro de **valor** contiene ahora el valor EncoderValueFrameDimensionPage.</span><span class="sxs-lookup"><span data-stu-id="83aa6-126">The difference is that the **ULONG** pointed to by the **Value** member now contains the value EncoderValueFrameDimensionPage.</span></span>

<span data-ttu-id="83aa6-127">La función Main se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="83aa6-127">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
