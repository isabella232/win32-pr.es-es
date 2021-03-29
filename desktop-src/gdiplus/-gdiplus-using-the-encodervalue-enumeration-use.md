---
description: Un codificador determinado admite determinadas categorías de parámetros y, para cada una de esas categorías, ese codificador permite determinados valores.
ms.assetid: cb9552e9-e807-4b07-b315-4550762e7026
title: Usar la enumeración EncoderValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755248150e81f963ea1c5c597ab04649c342944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985111"
---
# <a name="using-the-encodervalue-enumeration"></a>Usar la enumeración EncoderValue

Un codificador determinado admite determinadas categorías de parámetros y, para cada una de esas categorías, ese codificador permite determinados valores. Por ejemplo, el codificador JPEG admite la categoría de parámetro EncoderValueQuality y los valores de parámetro permitidos son los enteros del 0 al 100. Algunos de los valores de parámetro permitidos son los mismos en varios codificadores. Estos valores estándar se definen en la enumeración [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) en Gdiplusenums. h:


```
enum EncoderValue
{
   EncoderValueColorTypeCMYK,             // 0
   EncoderValueColorTypeYCCK,             // 1
   EncoderValueCompressionLZW,            // 2
   EncoderValueCompressionCCITT3,         // 3
   EncoderValueCompressionCCITT4,         // 4
   EncoderValueCompressionRle,            // 5
   EncoderValueCompressionNone,           // 6
   EncoderValueScanMethodInterlaced,      // 7
   EncoderValueScanMethodNonInterlaced,   // 8
   EncoderValueVersionGif87,              // 9
   EncoderValueVersionGif89,              // 10
   EncoderValueRenderProgressive,         // 11
   EncoderValueRenderNonProgressive,      // 12
   EncoderValueTransformRotate90,         // 13
   EncoderValueTransformRotate180,        // 14
   EncoderValueTransformRotate270,        // 15
   EncoderValueTransformFlipHorizontal,   // 16
   EncoderValueTransformFlipVertical,     // 17
   EncoderValueMultiFrame,                // 18
   EncoderValueLastFrame,                 // 19
   EncoderValueFlush,                     // 20
   EncoderValueFrameDimensionTime,        // 21
   EncoderValueFrameDimensionResolution,  // 22
   EncoderValueFrameDimensionPage         // 23
};
```



Una de las categorías de parámetros que admite el codificador JPEG es la categoría EncoderTransformation. Mediante el examen de la enumeración [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) , puede especular (y sería correcto) que la categoría EncoderTransformation permite los cinco valores siguientes:


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



La siguiente aplicación de consola comprueba que el codificador JPEG admite la categoría de parámetro EncoderTransformation y que hay cinco valores permitidos para este tipo de parámetro. La función Main se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);
INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   // Create a Bitmap (inherited from Image) object so that we can call
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
   // Look at the first (index 0) EncoderParameter object in the array.
   printf("Parameter[0]\n");
   WCHAR strGuid[39];
   StringFromGUID2(pEncoderParameters->Parameter[0].Guid, strGuid, 39);
   wprintf(L"   The guid is %s.\n", strGuid);
   printf("   The data type is %d.\n", 
      pEncoderParameters->Parameter[0].Type);
   printf("   The number of values is %d.\n",
      pEncoderParameters->Parameter[0].NumberOfValues);
   free(pEncoderParameters);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Al ejecutar la aplicación de consola anterior, obtendrá una salida similar a la siguiente:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



Puede buscar el GUID en Gdiplusimaging. h y averiguar que la categoría de este objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es EncoderTransformation. En Gdiplusenums. h, la enumeración [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica que el tipo de datos 4 es ValueLong (entero sin signo de 32 bits). El número de valores es cinco, por lo que sabemos que el miembro de **valor** del objeto **EncoderParameter** es un puntero a una matriz de cinco valores **ULong** .

El código siguiente es una continuación de la aplicación de consola que se muestra en el ejemplo anterior. El código muestra los valores permitidos para un parámetro EncoderTransformation:


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



Este código anterior genera el siguiente resultado:


```
The allowable values are  13  14  15  16  17
```



Los valores permitidos (13, 14, 15, 16 y 17) se corresponden con los siguientes miembros de la enumeración [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
