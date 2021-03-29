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
# <a name="using-the-encodervalue-enumeration"></a><span data-ttu-id="a4891-103">Usar la enumeración EncoderValue</span><span class="sxs-lookup"><span data-stu-id="a4891-103">Using the EncoderValue Enumeration</span></span>

<span data-ttu-id="a4891-104">Un codificador determinado admite determinadas categorías de parámetros y, para cada una de esas categorías, ese codificador permite determinados valores.</span><span class="sxs-lookup"><span data-stu-id="a4891-104">A given encoder supports certain parameter categories, and for each of those categories, that encoder allows certain values.</span></span> <span data-ttu-id="a4891-105">Por ejemplo, el codificador JPEG admite la categoría de parámetro EncoderValueQuality y los valores de parámetro permitidos son los enteros del 0 al 100.</span><span class="sxs-lookup"><span data-stu-id="a4891-105">For example, the JPEG encoder supports the EncoderValueQuality parameter category, and the allowable parameter values are the integers 0 through 100.</span></span> <span data-ttu-id="a4891-106">Algunos de los valores de parámetro permitidos son los mismos en varios codificadores.</span><span class="sxs-lookup"><span data-stu-id="a4891-106">Some of the allowable parameter values are the same across several encoders.</span></span> <span data-ttu-id="a4891-107">Estos valores estándar se definen en la enumeración [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) en Gdiplusenums. h:</span><span class="sxs-lookup"><span data-stu-id="a4891-107">These standard values are defined in the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration in Gdiplusenums.h:</span></span>


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



<span data-ttu-id="a4891-108">Una de las categorías de parámetros que admite el codificador JPEG es la categoría EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="a4891-108">One of the parameter categories supported by the JPEG encoder is the EncoderTransformation category.</span></span> <span data-ttu-id="a4891-109">Mediante el examen de la enumeración [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) , puede especular (y sería correcto) que la categoría EncoderTransformation permite los cinco valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="a4891-109">By examining the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration, you might speculate (and you would be correct) that the EncoderTransformation category allows the following five values:</span></span>


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



<span data-ttu-id="a4891-110">La siguiente aplicación de consola comprueba que el codificador JPEG admite la categoría de parámetro EncoderTransformation y que hay cinco valores permitidos para este tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="a4891-110">The following console application verifies that the JPEG encoder supports the EncoderTransformation parameter category and that there are five allowable values for such a parameter.</span></span> <span data-ttu-id="a4891-111">La función Main se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="a4891-111">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="a4891-112">Al ejecutar la aplicación de consola anterior, obtendrá una salida similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="a4891-112">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



<span data-ttu-id="a4891-113">Puede buscar el GUID en Gdiplusimaging. h y averiguar que la categoría de este objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="a4891-113">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderTransformation.</span></span> <span data-ttu-id="a4891-114">En Gdiplusenums. h, la enumeración [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica que el tipo de datos 4 es ValueLong (entero sin signo de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="a4891-114">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 4 is ValueLong (32-bit unsigned integer).</span></span> <span data-ttu-id="a4891-115">El número de valores es cinco, por lo que sabemos que el miembro de **valor** del objeto **EncoderParameter** es un puntero a una matriz de cinco valores **ULong** .</span><span class="sxs-lookup"><span data-stu-id="a4891-115">The number of values is five, so we know that the **Value** member of the **EncoderParameter** object is a pointer to an array of five **ULONG** values.</span></span>

<span data-ttu-id="a4891-116">El código siguiente es una continuación de la aplicación de consola que se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="a4891-116">The following code is a continuation of the console application that is shown in the preceding example.</span></span> <span data-ttu-id="a4891-117">El código muestra los valores permitidos para un parámetro EncoderTransformation:</span><span class="sxs-lookup"><span data-stu-id="a4891-117">The code lists the allowable values for an EncoderTransformation parameter:</span></span>


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



<span data-ttu-id="a4891-118">Este código anterior genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="a4891-118">The preceding code produces the following output:</span></span>


```
The allowable values are  13  14  15  16  17
```



<span data-ttu-id="a4891-119">Los valores permitidos (13, 14, 15, 16 y 17) se corresponden con los siguientes miembros de la enumeración [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="a4891-119">The allowable values (13, 14, 15, 16, and 17) correspond to the following members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
