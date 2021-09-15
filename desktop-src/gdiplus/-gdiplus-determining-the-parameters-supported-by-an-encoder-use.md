---
description: La clase Image proporciona el método Image::GetEncoderParameterList para que pueda determinar los parámetros admitidos por un codificador de imagen determinado.
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Determinar los parámetros admitidos por un codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570668"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Determinar los parámetros admitidos por un codificador

La [**clase Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona el método [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) para que pueda determinar los parámetros admitidos por un codificador de imagen determinado. El **método Image::GetEncoderParameterList** devuelve una matriz de objetos [**EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) Debe asignar un búfer para recibir esa matriz antes de llamar a **Image::GetEncoderParameterList**. Puede llamar a [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) para determinar el tamaño del búfer necesario.

La siguiente aplicación de consola obtiene la lista de parámetros para el codificador JPEG. La función main se basa en la función auxiliar GetEncoderClsid, que se muestra en [Recuperación](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)del identificador de clase para un codificador .


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

   // Create Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap* bitmap = new Bitmap(1, 1);

   // Get the JPEG encoder CLSID.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // How big (in bytes) is the JPEG encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap->GetEncoderParameterListSize(&encoderClsid);
   printf("The parameter list requires %d bytes.\n", listSize);

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   // Get the parameter list for the JPEG encoder.
   bitmap->GetEncoderParameterList(
      &encoderClsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   free(pEncoderParameters);
   delete(bitmap);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Al ejecutar la aplicación de consola anterior, obtiene una salida similar a la siguiente:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Cada uno de los [**objetos EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) de la matriz tiene los cuatro miembros de datos públicos siguientes:

El código siguiente es una continuación de la aplicación de consola que se muestra en el ejemplo anterior. El código examina el segundo objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) de la matriz devuelta por [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist). El código llama a [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), que es una función del sistema declarada en Objbase.h, para convertir el miembro **Guid** del objeto **EncoderParameter** en una cadena.


```
// Look at the second (index 1) EncoderParameter object in the array.
printf("Parameter[1]\n");

WCHAR strGuid[39];
StringFromGUID2(pEncoderParameters->Parameter[1].Guid, strGuid, 39);
wprintf(L"   The GUID is %s.\n", strGuid);

printf("   The value type is %d.\n", 
   pEncoderParameters->Parameter[1].Type);

printf("   The number of values is %d.\n",
   pEncoderParameters->Parameter[1].NumberOfValues);
```



Este código anterior genera el siguiente resultado:


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



Puede buscar el GUID en Gdiplusimaging.h y averiguar que la categoría de este objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es EncoderQuality. Puede usar esta categoría (EncoderQuality) del parámetro para establecer el nivel de compresión de una imagen JPEG.

En Gdiplusenums.h, la enumeración [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica que el tipo de datos 6 **es ValueLongRange.** Un intervalo largo es un par de **valores ULONG.**

El número de valores es uno, por lo que sabemos que el **miembro Value** del objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es un puntero a una matriz que tiene un elemento . Ese elemento es un par de **valores ULONG.**

El código siguiente es una continuación de la aplicación de consola que se muestra en los dos ejemplos anteriores. El código define un tipo de datos denominado **PLONGRANGE** (puntero a un intervalo largo). Se usa una variable de tipo **PLONGRANGE** para extraer los valores mínimo y máximo que se pueden pasar como una configuración de calidad al codificador JPEG.


```
typedef struct
   {
      long min;
      long max;
   }* PLONGRANGE;

   PLONGRANGE pLongRange = 
      (PLONGRANGE)(pEncoderParameters->Parameter[1].Value);

   printf("   The minimum possible quality value is %d.\n",
      pLongRange->min);

   printf("   The maximum possible quality value is %d.\n",
      pLongRange->max);
```



Este código anterior genera el siguiente resultado:


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



En el ejemplo anterior, el valor devuelto en el objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es un par de valores **ULONG** que indican los valores mínimo y máximo posibles para el parámetro de calidad. En algunos casos, los valores devueltos en un **objeto EncoderParameter** son miembros de la [**enumeración EncoderValue.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) En los temas siguientes se describe la **enumeración EncoderValue** y los métodos para enumerar los posibles valores de parámetro con más detalle:

-   [Usar la enumeración EncoderValue](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Enumeración de parámetros y valores para todos los codificadores](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
