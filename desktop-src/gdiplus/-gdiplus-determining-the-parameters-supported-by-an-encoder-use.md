---
description: 'La clase Image proporciona el método Image:: GetEncoderParameterList para que pueda determinar los parámetros admitidos por un codificador de imágenes determinado.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Determinar los parámetros admitidos por un codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997508"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="aa12f-103">Determinar los parámetros admitidos por un codificador</span><span class="sxs-lookup"><span data-stu-id="aa12f-103">Determining the Parameters Supported by an Encoder</span></span>

<span data-ttu-id="aa12f-104">La clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona el método [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) para que pueda determinar los parámetros admitidos por un codificador de imágenes determinado.</span><span class="sxs-lookup"><span data-stu-id="aa12f-104">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method so that you can determine the parameters that are supported by a given image encoder.</span></span> <span data-ttu-id="aa12f-105">El método **Image:: GetEncoderParameterList** devuelve una matriz de objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="aa12f-105">The **Image::GetEncoderParameterList** method returns an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="aa12f-106">Debe asignar un búfer para recibir esa matriz antes de llamar a **Image:: GetEncoderParameterList**.</span><span class="sxs-lookup"><span data-stu-id="aa12f-106">You must allocate a buffer to receive that array before you call **Image::GetEncoderParameterList**.</span></span> <span data-ttu-id="aa12f-107">Puede llamar a [**Image:: GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) para determinar el tamaño del búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="aa12f-107">You can call [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="aa12f-108">La siguiente aplicación de consola obtiene la lista de parámetros para el codificador JPEG.</span><span class="sxs-lookup"><span data-stu-id="aa12f-108">The following console application obtains the parameter list for the JPEG encoder.</span></span> <span data-ttu-id="aa12f-109">La función Main se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="aa12f-109">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="aa12f-110">Al ejecutar la aplicación de consola anterior, obtendrá una salida similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="aa12f-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



<span data-ttu-id="aa12f-111">Cada uno de los objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) de la matriz tiene los cuatro miembros de datos públicos siguientes:</span><span class="sxs-lookup"><span data-stu-id="aa12f-111">Each of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects in the array has the following four public data members:</span></span>

<span data-ttu-id="aa12f-112">El código siguiente es una continuación de la aplicación de consola que se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="aa12f-112">The following code is a continuation of the console application shown in the preceding example.</span></span> <span data-ttu-id="aa12f-113">El código examina el segundo objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) de la matriz devuelta por [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span><span class="sxs-lookup"><span data-stu-id="aa12f-113">The code looks at the second [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object in the array returned by [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span></span> <span data-ttu-id="aa12f-114">El código llama a [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), que es una función del sistema declarada en Objbase. h, para convertir el miembro **GUID** del objeto **EncoderParameter** en una cadena.</span><span class="sxs-lookup"><span data-stu-id="aa12f-114">The code calls [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), which is a system function declared in Objbase.h, to convert the **Guid** member of the **EncoderParameter** object to a string.</span></span>


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



<span data-ttu-id="aa12f-115">Este código anterior genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="aa12f-115">The preceding code produces the following output:</span></span>


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



<span data-ttu-id="aa12f-116">Puede buscar el GUID en Gdiplusimaging. h y averiguar que la categoría de este objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es EncoderQuality.</span><span class="sxs-lookup"><span data-stu-id="aa12f-116">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderQuality.</span></span> <span data-ttu-id="aa12f-117">Puede usar esta categoría (EncoderQuality) de parámetro para establecer el nivel de compresión de una imagen JPEG.</span><span class="sxs-lookup"><span data-stu-id="aa12f-117">You can use this category (EncoderQuality) of parameter to set the compression level of a JPEG image.</span></span>

<span data-ttu-id="aa12f-118">En Gdiplusenums. h, la enumeración [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica que el tipo de datos 6 es **ValueLongRange**.</span><span class="sxs-lookup"><span data-stu-id="aa12f-118">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 6 is **ValueLongRange**.</span></span> <span data-ttu-id="aa12f-119">Un intervalo largo es un par de valores **ULong** .</span><span class="sxs-lookup"><span data-stu-id="aa12f-119">A long range is a pair of **ULONG** values.</span></span>

<span data-ttu-id="aa12f-120">El número de valores es uno, por lo que sabemos que el miembro de **valor** del objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es un puntero a una matriz que tiene un elemento.</span><span class="sxs-lookup"><span data-stu-id="aa12f-120">The number of values is one, so we know that the **Value** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pointer to an array that has one element.</span></span> <span data-ttu-id="aa12f-121">Un elemento es un par de valores **ULong** .</span><span class="sxs-lookup"><span data-stu-id="aa12f-121">That one element is a pair of **ULONG** values.</span></span>

<span data-ttu-id="aa12f-122">El código siguiente es una continuación de la aplicación de consola que se muestra en los dos ejemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="aa12f-122">The following code is a continuation of the console application that is shown in the preceding two examples.</span></span> <span data-ttu-id="aa12f-123">El código define un tipo de datos denominado **PLONGRANGE** (puntero a un intervalo largo).</span><span class="sxs-lookup"><span data-stu-id="aa12f-123">The code defines a data type called **PLONGRANGE** (pointer to a long range).</span></span> <span data-ttu-id="aa12f-124">Una variable de tipo **PLONGRANGE** se usa para extraer los valores mínimo y máximo que se pueden pasar como una configuración de calidad al codificador JPEG.</span><span class="sxs-lookup"><span data-stu-id="aa12f-124">A variable of type **PLONGRANGE** is used to extract the minimum and maximum values that can be passed as a quality setting to the JPEG encoder.</span></span>


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



<span data-ttu-id="aa12f-125">Este código anterior genera el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="aa12f-125">The preceding code produces the following output:</span></span>


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



<span data-ttu-id="aa12f-126">En el ejemplo anterior, el valor devuelto en el objeto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) es un par de valores **ULong** que indican los valores máximo y mínimo posibles para el parámetro Quality.</span><span class="sxs-lookup"><span data-stu-id="aa12f-126">In the preceding example, the value returned in the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pair of **ULONG** values that indicate the minimum and maximum possible values for the quality parameter.</span></span> <span data-ttu-id="aa12f-127">En algunos casos, los valores devueltos en un objeto **EncoderParameter** son miembros de la enumeración [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) .</span><span class="sxs-lookup"><span data-stu-id="aa12f-127">In some cases, the values returned in an **EncoderParameter** object are members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="aa12f-128">En los temas siguientes se describe la enumeración y los métodos de **EncoderValue** para enumerar posibles valores de parámetros con más detalle:</span><span class="sxs-lookup"><span data-stu-id="aa12f-128">The following topics discuss the **EncoderValue** enumeration and methods for listing possible parameter values in more detail:</span></span>

-   [<span data-ttu-id="aa12f-129">Usar la enumeración EncoderValue</span><span class="sxs-lookup"><span data-stu-id="aa12f-129">Using the EncoderValue Enumeration</span></span>](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [<span data-ttu-id="aa12f-130">Enumerar los parámetros y los valores de todos los codificadores</span><span class="sxs-lookup"><span data-stu-id="aa12f-130">Listing Parameters and Values for All Encoders</span></span>](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
