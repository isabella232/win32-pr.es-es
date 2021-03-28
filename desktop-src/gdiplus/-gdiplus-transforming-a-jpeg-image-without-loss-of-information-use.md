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
# <a name="lossless-transform-of-a-jpeg-image"></a><span data-ttu-id="ccf91-103">Transformación sin pérdida de una imagen JPEG</span><span class="sxs-lookup"><span data-stu-id="ccf91-103">Lossless transform of a JPEG image</span></span>

<span data-ttu-id="ccf91-104">Al comprimir una imagen JPEG, parte de la información de la imagen se pierde.</span><span class="sxs-lookup"><span data-stu-id="ccf91-104">When you compress a JPEG image, some of the information in the image is lost.</span></span> <span data-ttu-id="ccf91-105">Si abre un archivo JPEG, modifica la imagen y la guarda en otro archivo JPEG, se reducirá la calidad.</span><span class="sxs-lookup"><span data-stu-id="ccf91-105">If you open a JPEG file, alter the image, and save it to another JPEG file, the quality will decrease.</span></span> <span data-ttu-id="ccf91-106">Si se repite el proceso muchas veces, verá una degradación sustancial en la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ccf91-106">If you repeat that process many times, you will see a substantial degradation in the image quality.</span></span>

<span data-ttu-id="ccf91-107">Como JPEG es uno de los formatos de imagen más populares en la web, y dado que las personas a menudo desean modificar imágenes JPEG, GDI+ proporciona las siguientes transformaciones que se pueden realizar en imágenes JPEG sin pérdida de información:</span><span class="sxs-lookup"><span data-stu-id="ccf91-107">Because JPEG is one of the most popular image formats on the Web, and because people often like to modify JPEG images, GDI+ provides the following transformations that can be performed on JPEG images without loss of information:</span></span>

-   <span data-ttu-id="ccf91-108">Girar 90 grados</span><span class="sxs-lookup"><span data-stu-id="ccf91-108">Rotate 90 degrees</span></span>
-   <span data-ttu-id="ccf91-109">Girar 180 grados</span><span class="sxs-lookup"><span data-stu-id="ccf91-109">Rotate 180 degrees</span></span>
-   <span data-ttu-id="ccf91-110">Girar 270 grados</span><span class="sxs-lookup"><span data-stu-id="ccf91-110">Rotate 270 degrees</span></span>
-   <span data-ttu-id="ccf91-111">Voltear horizontalmente</span><span class="sxs-lookup"><span data-stu-id="ccf91-111">Flip horizontally</span></span>
-   <span data-ttu-id="ccf91-112">Voltear verticalmente</span><span class="sxs-lookup"><span data-stu-id="ccf91-112">Flip vertically</span></span>

<span data-ttu-id="ccf91-113">Puede aplicar una de las transformaciones que se muestran en la lista anterior al llamar al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de un objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="ccf91-113">You can apply one of the transformations shown in the preceding list when you call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="ccf91-114">Si se cumplen las siguientes condiciones, la transformación continuará sin pérdida de información:</span><span class="sxs-lookup"><span data-stu-id="ccf91-114">If the following conditions are met, then the transformation will proceed without loss of information:</span></span>

-   <span data-ttu-id="ccf91-115">El archivo que se usa para construir el objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) es un archivo JPEG.</span><span class="sxs-lookup"><span data-stu-id="ccf91-115">The file used to construct the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object is a JPEG file.</span></span>
-   <span data-ttu-id="ccf91-116">El ancho y el alto de la imagen son múltiplos de 16.</span><span class="sxs-lookup"><span data-stu-id="ccf91-116">The width and height of the image are both multiples of 16.</span></span>

<span data-ttu-id="ccf91-117">Si el ancho y el alto de la imagen no son múltiplos de 16, GDI+ hará lo mejor para conservar la calidad de la imagen al aplicar una de las transformaciones de giro o de volteo que se muestran en la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="ccf91-117">If the width and height of the image are not both multiples of 16, GDI+ will do its best to preserve the image quality when you apply one of the rotation or flipping transformations shown in the preceding list.</span></span>

<span data-ttu-id="ccf91-118">Para transformar una imagen JPEG, inicialice un objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) y pase la dirección de ese objeto al método [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="ccf91-118">To transform a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="ccf91-119">Inicialice el objeto **EncoderParameters** para que tenga una matriz formada por un objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="ccf91-119">Initialize the **EncoderParameters** object so that it has an array that consists of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="ccf91-120">Inicialice un objeto **EncoderParameter** de modo que su miembro de **valor** apunte a una variable **ULong** que contiene uno de los siguientes elementos de la enumeración [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="ccf91-120">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** variable that holds one of the following elements of the [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>

-   <span data-ttu-id="ccf91-121">EncoderValueTransformRotate90,</span><span class="sxs-lookup"><span data-stu-id="ccf91-121">EncoderValueTransformRotate90,</span></span>
-   <span data-ttu-id="ccf91-122">EncoderValueTransformRotate180,</span><span class="sxs-lookup"><span data-stu-id="ccf91-122">EncoderValueTransformRotate180,</span></span>
-   <span data-ttu-id="ccf91-123">EncoderValueTransformRotate270,</span><span class="sxs-lookup"><span data-stu-id="ccf91-123">EncoderValueTransformRotate270,</span></span>
-   <span data-ttu-id="ccf91-124">EncoderValueTransformFlipHorizontal,</span><span class="sxs-lookup"><span data-stu-id="ccf91-124">EncoderValueTransformFlipHorizontal,</span></span>
-   <span data-ttu-id="ccf91-125">EncoderValueTransformFlipVertical</span><span class="sxs-lookup"><span data-stu-id="ccf91-125">EncoderValueTransformFlipVertical</span></span>

<span data-ttu-id="ccf91-126">Establezca el miembro **GUID** del objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) en EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="ccf91-126">Set the **Guid** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object to EncoderTransformation.</span></span>

<span data-ttu-id="ccf91-127">La siguiente aplicación de consola crea un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de un archivo JPEG y, a continuación, guarda la imagen en un archivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="ccf91-127">The following console application creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then saves the image to a new file.</span></span> <span data-ttu-id="ccf91-128">Durante el proceso de guardar, la imagen se gira 90 grados.</span><span class="sxs-lookup"><span data-stu-id="ccf91-128">During the save process, the image is rotated 90 degrees.</span></span> <span data-ttu-id="ccf91-129">Si el ancho y el alto de la imagen son múltiplos de 16, el proceso de rotación y guardado de la imagen no provoca la pérdida de información.</span><span class="sxs-lookup"><span data-stu-id="ccf91-129">If the width and height of the image are both multiples of 16, the process of rotating and saving the image causes no loss of information.</span></span>

<span data-ttu-id="ccf91-130">La función Main se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="ccf91-130">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
