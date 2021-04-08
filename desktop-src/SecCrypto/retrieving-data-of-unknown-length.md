---
description: Muchas funciones devuelven una cantidad de datos potencialmente grande a una dirección proporcionada como uno de los parámetros por la aplicación.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Recuperación de datos de longitud desconocida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30620018f3c4871bd27299c3dd21ae42936c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908597"
---
# <a name="retrieving-data-of-unknown-length"></a><span data-ttu-id="744ab-103">Recuperación de datos de longitud desconocida</span><span class="sxs-lookup"><span data-stu-id="744ab-103">Retrieving Data of Unknown Length</span></span>

<span data-ttu-id="744ab-104">Muchas funciones devuelven una cantidad de datos potencialmente grande a una dirección proporcionada como uno de los parámetros por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="744ab-104">Many functions return a potentially large amount of data to an address provided as one of the parameters by the application.</span></span> <span data-ttu-id="744ab-105">En todos estos casos, la operación se realiza de manera similar, si no es idéntica.</span><span class="sxs-lookup"><span data-stu-id="744ab-105">In all these cases, the operation is performed in a similar, if not identical, fashion.</span></span> <span data-ttu-id="744ab-106">El parámetro que apunta a la ubicación de los datos devueltos usará la Convención de notación en la que PB o PV son los dos primeros caracteres del nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="744ab-106">The parameter that points to the location of the returned data will use the notation convention where pb or pv are the first two characters of the parameter name.</span></span> <span data-ttu-id="744ab-107">Otro parámetro tendrá PCB como los tres primeros caracteres del nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="744ab-107">Another parameter will have pcb as the first three characters of the parameter name.</span></span> <span data-ttu-id="744ab-108">Este parámetro representa el tamaño, en bytes, de los datos que se devolverán a la ubicación PB o PV.</span><span class="sxs-lookup"><span data-stu-id="744ab-108">This parameter represents the size, in bytes, of the data that will be returned to the pb or pv location.</span></span> <span data-ttu-id="744ab-109">Por ejemplo, considere la siguiente especificación de función:</span><span class="sxs-lookup"><span data-stu-id="744ab-109">For example, consider the following function specification:</span></span>

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

<span data-ttu-id="744ab-110">En este ejemplo, *pbData* es un puntero a la ubicación donde se devolverán los datos y *pcbData* es el tamaño, en bytes, de los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="744ab-110">In this example, *pbData* is a pointer to the location where the data will be returned, and *pcbData* is the size, in bytes, of the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="744ab-111">A veces, el parámetro complementario del parámetro PCB puede llevar un prefijo ligeramente diferente, como p o PV.</span><span class="sxs-lookup"><span data-stu-id="744ab-111">The companion parameter to the pcb parameter may sometimes carry a slightly different prefix, such as p or pv.</span></span> <span data-ttu-id="744ab-112">Además, para los parámetros complementarios que usan la combinación de prefijos pwsz y PCCh, el parámetro PCCh es el recuento, en caracteres ([*Unicode*](../secgloss/u-gly.md) o [*ASCII*](../secgloss/a-gly.md), según corresponda), de los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="744ab-112">Also, for companion parameters using the combination of prefixes pwsz and pcch, the pcch parameter is the count, in characters ([*Unicode*](../secgloss/u-gly.md) or [*ASCII*](../secgloss/a-gly.md), as applicable), of the returned data.</span></span>

 

<span data-ttu-id="744ab-113">Si el búfer especificado por el parámetro *pbData* no es lo suficientemente grande como para contener los datos devueltos, la función establece el error \_ más código de \_ datos (que se puede ver mediante una llamada a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) y almacena el tamaño de búfer necesario, en bytes, en la variable a la que apunta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="744ab-113">If the buffer specified by the *pbData* parameter is not large enough to hold the returned data, the function sets the ERROR\_MORE\_DATA code (which can be seen by calling the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function) and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*.</span></span>

<span data-ttu-id="744ab-114">Si **null** es INPUT para *pbData* y *pcbData* no es **null**, no se devuelve ningún error y la función devuelve el tamaño, en bytes, del búfer de memoria necesario en la variable a la que apunta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="744ab-114">If **NULL** is input for *pbData* and *pcbData* is not **NULL**, no error is returned, and the function returns the size, in bytes, of the needed memory buffer in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="744ab-115">Esto permite que una aplicación determine el tamaño de y la mejor manera de asignar un búfer para los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="744ab-115">This lets an application determine the size of, and the best way to allocate, a buffer for the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="744ab-116">Cuando se especifica **null como valor** de *pbData* para determinar el tamaño necesario para asegurarse de que los datos devueltos caben en el búfer especificado, es posible que la segunda llamada a la función que rellena el búfer con los datos deseados no use todo el búfer.</span><span class="sxs-lookup"><span data-stu-id="744ab-116">When **NULL** is input for *pbData* to determine the size needed to ensure that the returned data fits in the specified buffer, the second call to the function which populates the buffer with the desired data may not use the whole buffer.</span></span> <span data-ttu-id="744ab-117">Después de la segunda llamada, el tamaño real de los datos devueltos se encuentra en *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="744ab-117">After the second call, the actual size of the data returned is contained in *pcbData*.</span></span> <span data-ttu-id="744ab-118">Use este tamaño al procesar los datos.</span><span class="sxs-lookup"><span data-stu-id="744ab-118">Use this size when processing the data.</span></span>

 

<span data-ttu-id="744ab-119">En el ejemplo siguiente se muestra cómo se pueden implementar los parámetros de entrada y salida para este fin.</span><span class="sxs-lookup"><span data-stu-id="744ab-119">The following example shows how input and output parameters might be implemented for this purpose.</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(char *s);

void main()
{

// Set up SomeFunction variables.
PCCRL_CONTEXT pCrlContext; // Initialized elsewhere.
DWORD dwPropId;            // Initialized elsewhere.
DWORD cbData;
BYTE  *pbData;

// Call SomeFunction to set cbData, the size of 
// the buffer needed for pbData.
if(SomeFunction(
     pCrlContext, 
     dwPropId, 
     NULL, 
     &cbData))
{
       printf("The function succeeded.\n");
}
else
{

// The function call failed. Handle the error.
       MyHandleError("Function call failed.");
}

// The call succeeded; the size for the needed buffer, in bytes, 
// now resides in cbData.

// Malloc memory for the size of the message.
if(pbData = (BYTE*)malloc(cbData))
{
   printf("Memory has been allocated.\n");
}
else
{

   // The allocation failed. Write an error message and exit.
   MyHandleError("Malloc operation failed. ");
}

// The space for the buffer has been allocated.
// Call SomeFunction to fill the buffer with the data.
if(SomeFunction(
      pCrlContext, 
      dwPropId, 
      pbData, 
      &cbData))
{
       printf("The function succeeded.\n");
}
else
{

   // The second function call failed. Handle the error.
   MyHandleError("The second call to the function failed.");
}

// The function succeeded; the data is now in the buffer
// pointed to by pbData. Note that cbData is
// updated with the actual size of the data returned. Use this size 
// to process bytes of pbData.

// When you have finished using the allocated memory, free it.
free(pbData);

} // End of main

//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.
void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
}
```



 

 
