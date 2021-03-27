---
description: Algunos archivos de imagen contienen metadatos que se pueden leer para determinar las características de la imagen.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Leer y escribir metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f599c1134efc8768d0b6ed59deaae8adf9f6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809637"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="779a4-103">Leer y escribir metadatos</span><span class="sxs-lookup"><span data-stu-id="779a4-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="779a4-104">Algunos archivos de imagen contienen metadatos que se pueden leer para determinar las características de la imagen.</span><span class="sxs-lookup"><span data-stu-id="779a4-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="779a4-105">Por ejemplo, una fotografía digital podría contener metadatos que puede leer para determinar la marca y el modelo de la cámara utilizada para capturar la imagen.</span><span class="sxs-lookup"><span data-stu-id="779a4-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="779a4-106">Con GDI+ de Windows, puede leer los metadatos existentes y también puede escribir nuevos metadatos en los archivos de imagen.</span><span class="sxs-lookup"><span data-stu-id="779a4-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="779a4-107">GDI+ proporciona una manera uniforme de almacenar y recuperar metadatos de archivos de imagen en varios formatos.</span><span class="sxs-lookup"><span data-stu-id="779a4-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="779a4-108">En GDI+, una parte de los metadatos se denomina *elemento de propiedad*.</span><span class="sxs-lookup"><span data-stu-id="779a4-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="779a4-109">Puede almacenar y recuperar metadatos mediante una llamada a los métodos **SetPropertyItem** y **GetPropertyItem** de la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , y no tiene que preocuparse de los detalles de cómo un formato de archivo determinado almacena esos metadatos.</span><span class="sxs-lookup"><span data-stu-id="779a4-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="779a4-110">GDI+ actualmente admite metadatos para los formatos de archivo TIFF, JPEG, EXIF y PNG.</span><span class="sxs-lookup"><span data-stu-id="779a4-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="779a4-111">El formato EXIF, que especifica cómo almacenar las imágenes capturadas por cámaras digitales fijas, se basa en los formatos TIFF y JPEG.</span><span class="sxs-lookup"><span data-stu-id="779a4-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="779a4-112">EXIF usa el formato TIFF para datos de píxeles sin comprimir y el formato JPEG para datos de píxeles comprimidos.</span><span class="sxs-lookup"><span data-stu-id="779a4-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="779a4-113">GDI+ define un conjunto de etiquetas de propiedad que identifican los elementos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="779a4-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="779a4-114">Algunas etiquetas son de uso general; es decir, se admiten en todos los formatos de archivo mencionados en el párrafo anterior.</span><span class="sxs-lookup"><span data-stu-id="779a4-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="779a4-115">Otras etiquetas son de propósito especial y solo se aplican a ciertos formatos.</span><span class="sxs-lookup"><span data-stu-id="779a4-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="779a4-116">Si intenta guardar un elemento de propiedad en un archivo que no admite ese elemento de propiedad, GDI+ omite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="779a4-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="779a4-117">Más concretamente, el método [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) devuelve PropertyNotSupported.</span><span class="sxs-lookup"><span data-stu-id="779a4-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="779a4-118">Puede determinar los elementos de propiedad que se almacenan en un archivo de imagen mediante una llamada a [**Image:: GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span><span class="sxs-lookup"><span data-stu-id="779a4-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="779a4-119">Si intenta recuperar un elemento de propiedad que no está en el archivo, GDI+ omite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="779a4-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="779a4-120">Más concretamente, el método [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) devuelve PropertyNotFound.</span><span class="sxs-lookup"><span data-stu-id="779a4-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="779a4-121">Leer metadatos de un archivo</span><span class="sxs-lookup"><span data-stu-id="779a4-121">Reading Metadata from a File</span></span>

<span data-ttu-id="779a4-122">La siguiente aplicación de consola llama al método **GetPropertySize** de un objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para determinar el número de fragmentos de metadatos que se encuentran en el archivo FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="779a4-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   UINT    size = 0;
   UINT    count = 0;
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n", count);
   printf("The total size of the metadata is %d bytes.\n", size);
 
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="779a4-123">El código anterior, junto con un archivo determinado, FakePhoto.jpg, generó el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="779a4-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="779a4-124">GDI+ almacena un elemento individual de metadatos en un objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) .</span><span class="sxs-lookup"><span data-stu-id="779a4-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="779a4-125">Puede llamar al método **GetAllPropertyItems** de la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para recuperar todos los metadatos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="779a4-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="779a4-126">El método **GetAllPropertyItems** devuelve una matriz de objetos **PropertyItem** .</span><span class="sxs-lookup"><span data-stu-id="779a4-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="779a4-127">Antes de llamar a **GetAllPropertyItems**, debe asignar un búfer lo suficientemente grande como para recibir esa matriz.</span><span class="sxs-lookup"><span data-stu-id="779a4-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="779a4-128">Puede llamar al método **GetPropertySize** de la clase **Image** para obtener el tamaño (en bytes) del búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="779a4-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="779a4-129">Un objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) tiene los cuatro miembros públicos siguientes:</span><span class="sxs-lookup"><span data-stu-id="779a4-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            |                                                                                                                                                                                                                                                                                                        |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a4-130">**id**</span><span class="sxs-lookup"><span data-stu-id="779a4-130">**id**</span></span>     | <span data-ttu-id="779a4-131">Etiqueta que identifica el elemento de metadatos.</span><span class="sxs-lookup"><span data-stu-id="779a4-131">A tag that identifies the metadata item.</span></span> <span data-ttu-id="779a4-132">Los valores que se pueden asignar a **ID** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime y like) se definen en Gdiplusimaging. h.</span><span class="sxs-lookup"><span data-stu-id="779a4-132">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="779a4-133">**length**</span><span class="sxs-lookup"><span data-stu-id="779a4-133">**length**</span></span> | <span data-ttu-id="779a4-134">La longitud, en bytes, de la matriz de valores a la que apunta el miembro de datos del **valor** .</span><span class="sxs-lookup"><span data-stu-id="779a4-134">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="779a4-135">Tenga en cuenta que si el miembro de datos **Type** está establecido en PropertyTagTypeASCII, el miembro de datos length es la **longitud** de una cadena de caracteres terminada en null, incluido el terminador null.</span><span class="sxs-lookup"><span data-stu-id="779a4-135">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="779a4-136">**type**</span><span class="sxs-lookup"><span data-stu-id="779a4-136">**type**</span></span>   | <span data-ttu-id="779a4-137">El tipo de datos de los valores de la matriz a la que apunta el miembro de datos del valor.</span><span class="sxs-lookup"><span data-stu-id="779a4-137">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="779a4-138">Las constantes (PropertyTagTypeByte, PropertyTagTypeASCII y like) que representan varios tipos de datos se describen en [**constantes de tipo etiqueta de propiedad de imagen**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="779a4-138">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="779a4-139">**value**</span><span class="sxs-lookup"><span data-stu-id="779a4-139">**value**</span></span>  | <span data-ttu-id="779a4-140">Puntero a una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="779a4-140">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="779a4-141">La siguiente aplicación de consola Lee y muestra los siete fragmentos de metadatos en el archivo FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="779a4-141">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="779a4-142">La función Main se basa en la función auxiliar PropertyTypeFromWORD, que se muestra después de la función main.</span><span class="sxs-lookup"><span data-stu-id="779a4-142">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  size = 0;
   UINT  count = 0;

   #define MAX_PROPTYPE_SIZE 30
   WCHAR strPropertyType[MAX_PROPTYPE_SIZE] = L"";

   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");

   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n\n", count);

   // GetAllPropertyItems returns an array of PropertyItem objects.
   // Allocate a buffer large enough to receive that array.
   PropertyItem* pPropBuffer =(PropertyItem*)malloc(size);

   // Get the array of PropertyItem objects.
   bitmap->GetAllPropertyItems(size, count, pPropBuffer);

   // For each PropertyItem in the array, display the id, type, and length.
   for(UINT j = 0; j < count; ++j)
   {
      // Convert the property type from a WORD to a string.
      PropertyTypeFromWORD(
         pPropBuffer[j].type, strPropertyType, MAX_PROPTYPE_SIZE);

      printf("Property Item %d\n", j);
      printf("  id: 0x%x\n", pPropBuffer[j].id);
      wprintf(L"  type: %s\n", strPropertyType);
      printf("  length: %d bytes\n\n", pPropBuffer[j].length);
   }

   free(pPropBuffer);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
} // main

// Helper function
HRESULT PropertyTypeFromWORD(WORD index, WCHAR* string, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* propertyTypes[] = {
      L"Nothing",                   // 0
      L"PropertyTagTypeByte",       // 1
      L"PropertyTagTypeASCII",      // 2
      L"PropertyTagTypeShort",      // 3
      L"PropertyTagTypeLong",       // 4
      L"PropertyTagTypeRational",   // 5
      L"Nothing",                   // 6
      L"PropertyTagTypeUndefined",  // 7
      L"Nothing",                   // 8
      L"PropertyTagTypeSLONG",      // 9
      L"PropertyTagTypeSRational"}; // 10

   hr = StringCchCopyW(string, maxChars, propertyTypes[index]);
   return hr;
}
```



<span data-ttu-id="779a4-143">La aplicación de consola anterior genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="779a4-143">The preceding console application produces the following output:</span></span>


```
Property Item 0
  id: 0x320
  type: PropertyTagTypeASCII
  length: 16 bytes
Property Item 1
  id: 0x10f
  type: PropertyTagTypeASCII
  length: 17 bytes
Property Item 2
  id: 0x110
  type: PropertyTagTypeASCII
  length: 7 bytes
Property Item 3
  id: 0x9003
  type: PropertyTagTypeASCII
  length: 20 bytes
Property Item 4
  id: 0x829a
  type: PropertyTagTypeRational
  length: 8 bytes
Property Item 5
  id: 0x5090
  type: PropertyTagTypeShort
  length: 128 bytes
Property Item 6
  id: 0x5091
  type: PropertyTagTypeShort
  length: 128 bytes
```



<span data-ttu-id="779a4-144">La salida anterior muestra un número de Identificador hexadecimal para cada elemento de propiedad.</span><span class="sxs-lookup"><span data-stu-id="779a4-144">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="779a4-145">Puede buscar esos números de identificador en [constantes de etiqueta de propiedad de imagen](-gdiplus-constant-image-property-tag-constants.md) y averiguar que representan las siguientes etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="779a4-145">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="779a4-146">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="779a4-146">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="779a4-147">Etiqueta de propiedad</span><span class="sxs-lookup"><span data-stu-id="779a4-147">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a4-148">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="779a4-148">0x0320 0x010f</span></span><br/>  <span data-ttu-id="779a4-149">0x0110</span><span class="sxs-lookup"><span data-stu-id="779a4-149">0x0110</span></span><br/>  <span data-ttu-id="779a4-150">0x9003</span><span class="sxs-lookup"><span data-stu-id="779a4-150">0x9003</span></span><br/>  <span data-ttu-id="779a4-151">0x829a</span><span class="sxs-lookup"><span data-stu-id="779a4-151">0x829a</span></span><br/>  <span data-ttu-id="779a4-152">0x5090</span><span class="sxs-lookup"><span data-stu-id="779a4-152">0x5090</span></span><br/>  <span data-ttu-id="779a4-153">0x5091</span><span class="sxs-lookup"><span data-stu-id="779a4-153">0x5091</span></span><br/> | <span data-ttu-id="779a4-154">PropertyTagImageTitle PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="779a4-154">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="779a4-155">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="779a4-155">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="779a4-156">PropertyTagExifDTOriginal</span><span class="sxs-lookup"><span data-stu-id="779a4-156">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="779a4-157">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="779a4-157">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="779a4-158">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="779a4-158">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="779a4-159">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="779a4-159">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="779a4-160">El segundo elemento de propiedad (Índice 1) de la lista tiene el **identificador** PropertyTagEquipMake y el **tipo** PropertyTagTypeASCII.</span><span class="sxs-lookup"><span data-stu-id="779a4-160">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="779a4-161">En el ejemplo siguiente, que es una continuación de la aplicación de consola anterior, se muestra el valor de ese elemento de propiedad:</span><span class="sxs-lookup"><span data-stu-id="779a4-161">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="779a4-162">La línea de código anterior genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="779a4-162">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="779a4-163">El quinto elemento de propiedad (índice 4) de la lista tiene el **identificador** PropertyTagExifExposureTime y el **tipo** PropertyTagTypeRational.</span><span class="sxs-lookup"><span data-stu-id="779a4-163">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="779a4-164">Ese tipo de datos (PropertyTagTypeRational) es un par de **Long** s.</span><span class="sxs-lookup"><span data-stu-id="779a4-164">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="779a4-165">En el ejemplo siguiente, que es una continuación de la aplicación de consola anterior, se muestran los dos valores **Long** como fracción.</span><span class="sxs-lookup"><span data-stu-id="779a4-165">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="779a4-166">Esa fracción, 1/125, es el tiempo de exposición medido en segundos.</span><span class="sxs-lookup"><span data-stu-id="779a4-166">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="779a4-167">Este código anterior genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="779a4-167">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="779a4-168">Escribir metadatos en un archivo</span><span class="sxs-lookup"><span data-stu-id="779a4-168">Writing Metadata to a File</span></span>

<span data-ttu-id="779a4-169">Para escribir un elemento de metadatos en un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , inicialice un objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) y, a continuación, pase la dirección de ese objeto **PropertyItem** al método **SetPropertyItem** del objeto de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="779a4-169">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="779a4-170">La siguiente aplicación de consola escribe un elemento (el título de la imagen) de los metadatos en un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y, a continuación, guarda la imagen en el archivo de disco FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="779a4-170">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="779a4-171">La función Main se basa en la función auxiliar GetEncoderClsid, que se muestra en el tema [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="779a4-171">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   Status stat;
   CLSID  clsid;
   char   propertyValue[] = "Fake Photograph";
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   PropertyItem* propertyItem = new PropertyItem;
   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &clsid);
   propertyItem->id = PropertyTagImageTitle;
   propertyItem->length = 16;  // string length including NULL terminator
   propertyItem->type = PropertyTagTypeASCII; 
   propertyItem->value = propertyValue;
   bitmap->SetPropertyItem(propertyItem);
   stat = bitmap->Save(L"FakePhoto2.jpg", &clsid, NULL);
   if(stat == Ok)
      printf("FakePhoto2.jpg saved successfully.\n");
   
   delete propertyItem;
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
