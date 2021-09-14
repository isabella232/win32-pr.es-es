---
description: Algunos archivos de imagen contienen metadatos que puede leer para determinar las características de la imagen.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Leer y escribir metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4ea0a8f389f31870b31a0b15480815bdd7cf1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252609"
---
# <a name="reading-and-writing-metadata"></a>Leer y escribir metadatos

Algunos archivos de imagen contienen metadatos que puede leer para determinar las características de la imagen. Por ejemplo, una fotografía digital podría contener metadatos que puede leer para determinar la marca y el modelo de la cámara que se usa para capturar la imagen. Con Windows GDI+, puede leer los metadatos existentes y también puede escribir nuevos metadatos en archivos de imagen.

GDI+ proporciona una manera uniforme de almacenar y recuperar metadatos de archivos de imagen en varios formatos. En GDI+, un fragmento de metadatos se denomina elemento *de propiedad*. Puede almacenar y recuperar metadatos llamando a los métodos **SetPropertyItem** y **GetPropertyItem** de la clase [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y no tiene que preocuparse por los detalles de cómo un formato de archivo determinado almacena los metadatos.

GDI+ actualmente admite metadatos para los formatos de archivo TIFF, JPEG, Exif y PNG. El formato Exif, que especifica cómo almacenar imágenes capturadas por cámaras digitales, se basa en los formatos TIFF y JPEG. Por ejemplo, usa el formato TIFF para los datos de píxeles sin comprimir y el formato JPEG para los datos de píxeles comprimidos.

GDI+ define un conjunto de etiquetas de propiedad que identifican los elementos de propiedad. Ciertas etiquetas son de uso general; Es decir, son compatibles con todos los formatos de archivo mencionados en el párrafo anterior. Otras etiquetas son de uso especial y solo se aplican a determinados formatos. Si intenta guardar un elemento de propiedad en un archivo que no admite ese elemento de propiedad, GDI+ omite la solicitud. Más concretamente, el [**método Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) devuelve PropertyNotSupported.

Puede determinar los elementos de propiedad almacenados en un archivo de imagen llamando a [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist). Si intenta recuperar un elemento de propiedad que no está en el archivo, GDI+ omite la solicitud. Más concretamente, el [**método Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) devuelve PropertyNotFound.

## <a name="reading-metadata-from-a-file"></a>Leer metadatos de un archivo

La siguiente aplicación de consola llama al **método GetPropertySize** de un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para determinar cuántos fragmentos de metadatos hay en el archivo FakePhoto.jpg.


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



El código anterior, junto con un archivo determinado, FakePhoto.jpg, generaba la siguiente salida:


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



GDI+ almacena un fragmento individual de metadatos en un [**objeto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) Puede llamar al método **GetAllPropertyItems** de la [**clase Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para recuperar todos los metadatos de un archivo. El **método GetAllPropertyItems** devuelve una matriz de **objetos PropertyItem.** Antes de llamar **a GetAllPropertyItems**, debe asignar un búfer lo suficientemente grande como para recibir esa matriz. Puede llamar al **método GetPropertySize** de la **clase Image** para obtener el tamaño (en bytes) del búfer necesario.

Un [**objeto PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) tiene los cuatro miembros públicos siguientes:



|            | Descripción                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **id**     | Etiqueta que identifica el elemento de metadatos. Los valores que se pueden asignar a **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime y otros) se definen en Gdiplusimaging.h.                                                                                           |
| **length** | Longitud, en bytes, de la matriz de valores a la que apunta el **miembro de** datos value. Tenga en  cuenta que si el miembro de datos de tipo se  establece en PropertyTagTypeASCII, el miembro de datos length es la longitud de una cadena de caracteres terminada en NULL, incluido el terminador NULL.                        |
| **type**   | Tipo de datos de los valores de la matriz a los que apunta el miembro de datos value. Las constantes (PropertyTagTypeByte, PropertyTagTypeASCII y otros) que representan varios tipos de datos se describen en Constantes de tipo de etiqueta de [**propiedad de imagen**](-gdiplus-constant-image-property-tag-type-constants.md). |
| **value**  | Puntero a una matriz de valores.                                                                                                                                                                                                                                                                       |



 

La siguiente aplicación de consola lee y muestra los siete fragmentos de metadatos en el archivo FakePhoto.jpg. La función main se basa en la función auxiliar PropertyTypeFromWORD, que se muestra después de la función main.


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



La aplicación de consola anterior genera la siguiente salida:


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



La salida anterior muestra un número de identificador hexadecimal para cada elemento de propiedad. Puede buscar esos números de identificador en Constantes de [etiqueta de](-gdiplus-constant-image-property-tag-constants.md) propiedad de imagen y averiguar que representan las siguientes etiquetas de propiedad.



| Valor hexadecimal                                                                                                       | Etiqueta de propiedad                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0320 0x010f<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | PropertyTagImageTitle PropertyTagEquipMake<br/>  PropertyTagEquipModel<br/>  PropertyTagExifDTOriginal<br/>  PropertyTagExifExposureTime<br/>  PropertyTagLuminanceTable<br/>  PropertyTagChrominanceTable<br/> |



 

El segundo elemento de propiedad (índice 1) de la lista tiene **el** identificador PropertyTagEquipMake y **el** tipo PropertyTagTypeASCII. En el ejemplo siguiente, que es una continuación de la aplicación de consola anterior, se muestra el valor de ese elemento de propiedad:


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



La línea de código anterior genera la siguiente salida:


```
The equipment make is Northwind Traders.
```



El quinto elemento de propiedad (índice 4) de la lista tiene **el** identificador PropertyTagExifExposureTime y **el** tipo PropertyTagTypeRational. Ese tipo de datos (PropertyTagTypeRational) es un par de **LONG** s. En el ejemplo siguiente, que es una continuación de la aplicación de consola anterior, se muestran esos dos **valores LONG** como una fracción. Esa fracción, 1/125, es el tiempo de exposición medido en segundos.


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



Este código anterior genera el siguiente resultado:


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>Escribir metadatos en un archivo

Para escribir un elemento de metadatos en un objeto [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) inicialice un objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) y, a continuación, pase la dirección de ese objeto **PropertyItem** al **método SetPropertyItem** del **objeto Image.**

La siguiente aplicación de consola escribe un elemento (el título de la imagen) de los metadatos en un objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y, a continuación, guarda la imagen en el archivo de FakePhoto2.jpg. La función principal se basa en la función auxiliar GetEncoderClsid, que se muestra en el tema [Recuperación](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)del identificador de clase para un codificador .


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



 

 
