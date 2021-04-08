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
# <a name="retrieving-data-of-unknown-length"></a>Recuperación de datos de longitud desconocida

Muchas funciones devuelven una cantidad de datos potencialmente grande a una dirección proporcionada como uno de los parámetros por la aplicación. En todos estos casos, la operación se realiza de manera similar, si no es idéntica. El parámetro que apunta a la ubicación de los datos devueltos usará la Convención de notación en la que PB o PV son los dos primeros caracteres del nombre del parámetro. Otro parámetro tendrá PCB como los tres primeros caracteres del nombre del parámetro. Este parámetro representa el tamaño, en bytes, de los datos que se devolverán a la ubicación PB o PV. Por ejemplo, considere la siguiente especificación de función:

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

En este ejemplo, *pbData* es un puntero a la ubicación donde se devolverán los datos y *pcbData* es el tamaño, en bytes, de los datos devueltos.

> [!Note]  
> A veces, el parámetro complementario del parámetro PCB puede llevar un prefijo ligeramente diferente, como p o PV. Además, para los parámetros complementarios que usan la combinación de prefijos pwsz y PCCh, el parámetro PCCh es el recuento, en caracteres ([*Unicode*](../secgloss/u-gly.md) o [*ASCII*](../secgloss/a-gly.md), según corresponda), de los datos devueltos.

 

Si el búfer especificado por el parámetro *pbData* no es lo suficientemente grande como para contener los datos devueltos, la función establece el error \_ más código de \_ datos (que se puede ver mediante una llamada a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) y almacena el tamaño de búfer necesario, en bytes, en la variable a la que apunta *pcbData*.

Si **null** es INPUT para *pbData* y *pcbData* no es **null**, no se devuelve ningún error y la función devuelve el tamaño, en bytes, del búfer de memoria necesario en la variable a la que apunta *pcbData*. Esto permite que una aplicación determine el tamaño de y la mejor manera de asignar un búfer para los datos devueltos.

> [!Note]  
> Cuando se especifica **null como valor** de *pbData* para determinar el tamaño necesario para asegurarse de que los datos devueltos caben en el búfer especificado, es posible que la segunda llamada a la función que rellena el búfer con los datos deseados no use todo el búfer. Después de la segunda llamada, el tamaño real de los datos devueltos se encuentra en *pcbData*. Use este tamaño al procesar los datos.

 

En el ejemplo siguiente se muestra cómo se pueden implementar los parámetros de entrada y salida para este fin.


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



 

 
