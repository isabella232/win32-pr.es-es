---
description: Algunos archivos de imagen contienen metadatos que puede leer para determinar las características de la imagen.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Leer y escribir metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4ea0a8f389f31870b31a0b15480815bdd7cf1f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118300"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="39e2d-103">Leer y escribir metadatos</span><span class="sxs-lookup"><span data-stu-id="39e2d-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="39e2d-104">Algunos archivos de imagen contienen metadatos que puede leer para determinar las características de la imagen.</span><span class="sxs-lookup"><span data-stu-id="39e2d-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="39e2d-105">Por ejemplo, una fotografía digital puede contener metadatos que puede leer para determinar la marca y el modelo de la cámara que se usa para capturar la imagen.</span><span class="sxs-lookup"><span data-stu-id="39e2d-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="39e2d-106">Con Windows GDI+, puede leer los metadatos existentes y también puede escribir nuevos metadatos en archivos de imagen.</span><span class="sxs-lookup"><span data-stu-id="39e2d-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="39e2d-107">GDI+ proporciona una manera uniforme de almacenar y recuperar metadatos de archivos de imagen en varios formatos.</span><span class="sxs-lookup"><span data-stu-id="39e2d-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="39e2d-108">En GDI+, un fragmento de metadatos se denomina elemento *de propiedad*.</span><span class="sxs-lookup"><span data-stu-id="39e2d-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="39e2d-109">Puede almacenar y recuperar metadatos llamando a los métodos **SetPropertyItem** y **GetPropertyItem** de la clase [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y no tiene que preocuparse por los detalles de cómo un formato de archivo determinado almacena los metadatos.</span><span class="sxs-lookup"><span data-stu-id="39e2d-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="39e2d-110">GDI+ admite actualmente metadatos para los formatos de archivo TIFF, JPEG, Exif y PNG.</span><span class="sxs-lookup"><span data-stu-id="39e2d-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="39e2d-111">El formato Exif, que especifica cómo almacenar imágenes capturadas por cámaras digitales, se basa en los formatos TIFF y JPEG.</span><span class="sxs-lookup"><span data-stu-id="39e2d-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="39e2d-112">Por ejemplo, usa el formato TIFF para los datos de píxeles sin comprimir y el formato JPEG para los datos de píxeles comprimidos.</span><span class="sxs-lookup"><span data-stu-id="39e2d-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="39e2d-113">GDI+ define un conjunto de etiquetas de propiedad que identifican los elementos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="39e2d-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="39e2d-114">Ciertas etiquetas son de uso general; Es decir, son compatibles con todos los formatos de archivo mencionados en el párrafo anterior.</span><span class="sxs-lookup"><span data-stu-id="39e2d-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="39e2d-115">Otras etiquetas son de uso especial y solo se aplican a determinados formatos.</span><span class="sxs-lookup"><span data-stu-id="39e2d-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="39e2d-116">Si intenta guardar un elemento de propiedad en un archivo que no admite ese elemento de propiedad, GDI+ omite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39e2d-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="39e2d-117">Más concretamente, el [**método Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) devuelve PropertyNotSupported.</span><span class="sxs-lookup"><span data-stu-id="39e2d-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="39e2d-118">Puede determinar los elementos de propiedad almacenados en un archivo de imagen llamando a [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span><span class="sxs-lookup"><span data-stu-id="39e2d-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="39e2d-119">Si intenta recuperar un elemento de propiedad que no está en el archivo, GDI+ omite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39e2d-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="39e2d-120">Más concretamente, el [**método Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) devuelve PropertyNotFound.</span><span class="sxs-lookup"><span data-stu-id="39e2d-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="39e2d-121">Leer metadatos de un archivo</span><span class="sxs-lookup"><span data-stu-id="39e2d-121">Reading Metadata from a File</span></span>

<span data-ttu-id="39e2d-122">La siguiente aplicación de consola llama al **método GetPropertySize** de un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para determinar cuántos fragmentos de metadatos hay en el archivo FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="39e2d-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


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



<span data-ttu-id="39e2d-123">El código anterior, junto con un archivo determinado, FakePhoto.jpg generaba la salida siguiente:</span><span class="sxs-lookup"><span data-stu-id="39e2d-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="39e2d-124">GDI+ almacena un fragmento individual de metadatos en un [**objeto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)</span><span class="sxs-lookup"><span data-stu-id="39e2d-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="39e2d-125">Puede llamar al método **GetAllPropertyItems** de la [**clase Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para recuperar todos los metadatos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="39e2d-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="39e2d-126">El **método GetAllPropertyItems** devuelve una matriz de **objetos PropertyItem.**</span><span class="sxs-lookup"><span data-stu-id="39e2d-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="39e2d-127">Antes de llamar **a GetAllPropertyItems**, debe asignar un búfer lo suficientemente grande como para recibir esa matriz.</span><span class="sxs-lookup"><span data-stu-id="39e2d-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="39e2d-128">Puede llamar al **método GetPropertySize** de la **clase Image** para obtener el tamaño (en bytes) del búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="39e2d-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="39e2d-129">Un [**objeto PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) tiene los cuatro miembros públicos siguientes:</span><span class="sxs-lookup"><span data-stu-id="39e2d-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            | <span data-ttu-id="39e2d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="39e2d-130">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e2d-131">**id**</span><span class="sxs-lookup"><span data-stu-id="39e2d-131">**id**</span></span>     | <span data-ttu-id="39e2d-132">Etiqueta que identifica el elemento de metadatos.</span><span class="sxs-lookup"><span data-stu-id="39e2d-132">A tag that identifies the metadata item.</span></span> <span data-ttu-id="39e2d-133">Los valores que se pueden asignar a **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime y otros) se definen en Gdiplusimaging.h.</span><span class="sxs-lookup"><span data-stu-id="39e2d-133">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="39e2d-134">**length**</span><span class="sxs-lookup"><span data-stu-id="39e2d-134">**length**</span></span> | <span data-ttu-id="39e2d-135">Longitud, en bytes, de la matriz de valores a la que apunta el **miembro de** datos value.</span><span class="sxs-lookup"><span data-stu-id="39e2d-135">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="39e2d-136">Tenga en  cuenta que si el miembro de datos de tipo se  establece en PropertyTagTypeASCII, el miembro de datos length es la longitud de una cadena de caracteres terminada en NULL, incluido el terminador NULL.</span><span class="sxs-lookup"><span data-stu-id="39e2d-136">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="39e2d-137">**type**</span><span class="sxs-lookup"><span data-stu-id="39e2d-137">**type**</span></span>   | <span data-ttu-id="39e2d-138">Tipo de datos de los valores de la matriz a los que apunta el miembro de datos value.</span><span class="sxs-lookup"><span data-stu-id="39e2d-138">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="39e2d-139">Las constantes (PropertyTagTypeByte, PropertyTagTypeASCII y otros tipos de datos) que representan varios tipos de datos se describen en Constantes de tipo de etiqueta de [**propiedad de imagen**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="39e2d-139">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="39e2d-140">**value**</span><span class="sxs-lookup"><span data-stu-id="39e2d-140">**value**</span></span>  | <span data-ttu-id="39e2d-141">Puntero a una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="39e2d-141">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="39e2d-142">La siguiente aplicación de consola lee y muestra los siete fragmentos de metadatos en el archivo FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="39e2d-142">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="39e2d-143">La función main se basa en la función auxiliar PropertyTypeFromWORD, que se muestra después de la función principal.</span><span class="sxs-lookup"><span data-stu-id="39e2d-143">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


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



<span data-ttu-id="39e2d-144">La aplicación de consola anterior genera la siguiente salida:</span><span class="sxs-lookup"><span data-stu-id="39e2d-144">The preceding console application produces the following output:</span></span>


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



<span data-ttu-id="39e2d-145">La salida anterior muestra un número de identificador hexadecimal para cada elemento de propiedad.</span><span class="sxs-lookup"><span data-stu-id="39e2d-145">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="39e2d-146">Puede buscar esos números de identificador en Constantes de [etiqueta de](-gdiplus-constant-image-property-tag-constants.md) propiedad de imagen y averiguar que representan las siguientes etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="39e2d-146">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="39e2d-147">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="39e2d-147">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="39e2d-148">Etiqueta de propiedad</span><span class="sxs-lookup"><span data-stu-id="39e2d-148">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e2d-149">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="39e2d-149">0x0320 0x010f</span></span><br/>  <span data-ttu-id="39e2d-150">0x0110</span><span class="sxs-lookup"><span data-stu-id="39e2d-150">0x0110</span></span><br/>  <span data-ttu-id="39e2d-151">0x9003</span><span class="sxs-lookup"><span data-stu-id="39e2d-151">0x9003</span></span><br/>  <span data-ttu-id="39e2d-152">0x829a</span><span class="sxs-lookup"><span data-stu-id="39e2d-152">0x829a</span></span><br/>  <span data-ttu-id="39e2d-153">0x5090</span><span class="sxs-lookup"><span data-stu-id="39e2d-153">0x5090</span></span><br/>  <span data-ttu-id="39e2d-154">0x5091</span><span class="sxs-lookup"><span data-stu-id="39e2d-154">0x5091</span></span><br/> | <span data-ttu-id="39e2d-155">PropertyTagImageTitle PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="39e2d-155">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="39e2d-156">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="39e2d-156">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="39e2d-157">PropertyTagExifDTOriginal</span><span class="sxs-lookup"><span data-stu-id="39e2d-157">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="39e2d-158">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="39e2d-158">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="39e2d-159">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="39e2d-159">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="39e2d-160">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="39e2d-160">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="39e2d-161">El segundo elemento de propiedad (índice 1) de la lista tiene **el** identificador PropertyTagEquipMake y **el** tipo PropertyTagTypeASCII.</span><span class="sxs-lookup"><span data-stu-id="39e2d-161">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="39e2d-162">En el ejemplo siguiente, que es una continuación de la aplicación de consola anterior, se muestra el valor de ese elemento de propiedad:</span><span class="sxs-lookup"><span data-stu-id="39e2d-162">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="39e2d-163">La línea de código anterior genera la siguiente salida:</span><span class="sxs-lookup"><span data-stu-id="39e2d-163">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="39e2d-164">El quinto elemento de propiedad (índice 4) de la lista tiene **el** identificador PropertyTagExifExposureTime y **el** tipo PropertyTagTypeRational.</span><span class="sxs-lookup"><span data-stu-id="39e2d-164">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="39e2d-165">Ese tipo de datos (PropertyTagTypeRational) es un par de **LONG** s.</span><span class="sxs-lookup"><span data-stu-id="39e2d-165">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="39e2d-166">En el ejemplo siguiente, que es una continuación de la aplicación de consola anterior, se muestran esos dos **valores LONG** como una fracción.</span><span class="sxs-lookup"><span data-stu-id="39e2d-166">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="39e2d-167">Esa fracción, 1/125, es el tiempo de exposición medido en segundos.</span><span class="sxs-lookup"><span data-stu-id="39e2d-167">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="39e2d-168">Este código anterior genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="39e2d-168">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="39e2d-169">Escribir metadatos en un archivo</span><span class="sxs-lookup"><span data-stu-id="39e2d-169">Writing Metadata to a File</span></span>

<span data-ttu-id="39e2d-170">Para escribir un elemento de metadatos en un objeto [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) inicialice un objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) y, a continuación, pase la dirección de ese objeto **PropertyItem** al **método SetPropertyItem** del **objeto Image.**</span><span class="sxs-lookup"><span data-stu-id="39e2d-170">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="39e2d-171">La siguiente aplicación de consola escribe un elemento (el título de la imagen) de los metadatos en un objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y, a continuación, guarda la imagen en el archivo de disco FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="39e2d-171">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="39e2d-172">La función principal se basa en la función auxiliar GetEncoderClsid, que se muestra en el tema [Recuperación](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)del identificador de clase para un codificador .</span><span class="sxs-lookup"><span data-stu-id="39e2d-172">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
