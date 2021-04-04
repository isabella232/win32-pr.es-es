---
description: Código de ejemplo que muestra cómo usar secuencias básicas del sistema de archivos NTFS.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Usar secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc73a3524d45eeead4cd6c0d508925e6caa5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278174"
---
# <a name="using-streams"></a>Usar secuencias

En el ejemplo de este tema se muestra cómo usar secuencias básicas del sistema de archivos NTFS.

En este ejemplo se crea un archivo, denominado "TestFile", con un tamaño de 16 bytes. Sin embargo, el archivo también tiene un tipo de flujo adicional:: $DATA, denominado "Stream", que agrega 23 bytes adicionales que el sistema operativo no indica. Por lo tanto, al ver la propiedad de tamaño de archivo del archivo, solo verá el tamaño de la secuencia default:: $DATA del archivo.


```C++
#include <windows.h>
#include <stdio.h>

void main( )
 {
  HANDLE hFile, hStream;
  DWORD dwRet;

  hFile = CreateFile( TEXT("TestFile"), // Filename
                      GENERIC_WRITE,    // Desired access
                      FILE_SHARE_WRITE, // Share flags
                      NULL,             // Security Attributes
                      OPEN_ALWAYS,      // Creation Disposition
                      0,                // Flags and Attributes
                      NULL );           // OVERLAPPED pointer
  if( hFile == INVALID_HANDLE_VALUE )
   {
    printf( "Cannot open TestFile\n" );
    return;
   }
  else
   {
    WriteFile( hFile,              // Handle
               "This is TestFile", // Data to be written
               16,                 // Size of data, in bytes
               &dwRet,             // Number of bytes written
               NULL );             // OVERLAPPED pointer
    CloseHandle( hFile );
    hFile = INVALID_HANDLE_VALUE;
   }

  hStream = CreateFile( TEXT("TestFile:Stream"), // Filename
                        GENERIC_WRITE,           // Desired access
                        FILE_SHARE_WRITE,        // Share flags
                        NULL,                    // Security Attributes
                        OPEN_ALWAYS,             // Creation Disposition
                        0,                       // Flags and Attributes
                        NULL );                  // OVERLAPPED pointer
  if( hStream == INVALID_HANDLE_VALUE )
    printf( "Cannot open TestFile:Stream\n" );
  else
   {
    WriteFile( hStream,                   // Handle
               "This is TestFile:Stream", // Data to be written
               23,                        // Size of data
               &dwRet,                    // Number of bytes written
               NULL);                     // OVERLAPPED pointer
    CloseHandle( hStream );
    hStream = INVALID_HANDLE_VALUE;
   }
}
```



Si escribe **Type TESTFILE** en un símbolo del sistema, se mostrará el siguiente resultado:

``` syntax
This is TestFile
```

Sin embargo, si escribe las palabras **Type TESTFILE: Stream**, se genera el siguiente error:

"El nombre de archivo, el nombre de directorio o la sintaxis de la etiqueta de volumen son incorrectos".

Para ver lo que hay en TestFile: Stream, use uno de los siguientes comandos:

**Más < TestFile: Stream**

**Más < TestFile: Stream: $DATA**

El texto que se muestra es el siguiente:

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencias de archivo](file-streams.md)
</dt> </dl>

 

 



