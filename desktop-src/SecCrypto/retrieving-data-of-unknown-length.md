---
description: Muchas funciones devuelven una cantidad potencialmente grande de datos a una dirección proporcionada como uno de los parámetros por la aplicación.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Recuperar datos de longitud desconocida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a71a30e935dd20bee6cce8f6dbc00a3b61478a90f4ea2139d7daaddc6894da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975019"
---
# <a name="retrieving-data-of-unknown-length"></a>Recuperar datos de longitud desconocida

Muchas funciones devuelven una cantidad potencialmente grande de datos a una dirección proporcionada como uno de los parámetros por la aplicación. En todos estos casos, la operación se realiza de forma similar, si no idéntica. El parámetro que apunta a la ubicación de los datos devueltos usará la convención de notación donde pb o pv son los dos primeros caracteres del nombre del parámetro. Otro parámetro tendrá byte como los tres primeros caracteres del nombre del parámetro. Este parámetro representa el tamaño, en bytes, de los datos que se devolverán a la ubicación pb o pv. Por ejemplo, considere la siguiente especificación de función:

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

En este ejemplo, *pbData* es un puntero a la ubicación donde se devolverán los datos y *byteData* es el tamaño, en bytes, de los datos devueltos.

> [!Note]  
> A veces, el parámetro complementario al parámetro pvc puede llevar un prefijo ligeramente diferente, como p o pv. Además, para los parámetros complementarios que usan la combinación de prefijos pwsz y pcch, el parámetro pcch es el recuento, en caracteres [*(Unicode*](../secgloss/u-gly.md) o [*ASCII,*](../secgloss/a-gly.md)según corresponda), de los datos devueltos.

 

Si el búfer especificado por el parámetro *pbData* no es lo suficientemente grande como para contener los datos devueltos, la función establece el código ERROR MORE DATA (que se puede ver llamando a la función \_ \_ [**GetLastError)**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) y almacena el tamaño de búfer necesario, en bytes, en la variable a la que apunta *byteData.*

Si **null** es la entrada para *pbData* y *byteData* no es **NULL,** no se devuelve ningún error y la función devuelve el tamaño, en bytes, del búfer de memoria necesario en la variable a la que *apunta byteData*. Esto permite a una aplicación determinar el tamaño y la mejor manera de asignar un búfer para los datos devueltos.

> [!Note]  
> Cuando se introduce **NULL** para *pbData* a fin de determinar el tamaño necesario para asegurarse de que los datos devueltos se ajusten al búfer especificado, es posible que la segunda llamada a la función que rellena el búfer con los datos deseados no use todo el búfer. Después de la segunda llamada, el tamaño real de los datos devueltos se encuentra en *kbData*. Use este tamaño al procesar los datos.

 

En el ejemplo siguiente se muestra cómo se pueden implementar los parámetros de entrada y salida para este propósito.


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



 

 
