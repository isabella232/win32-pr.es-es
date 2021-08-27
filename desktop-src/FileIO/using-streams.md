---
description: Código de ejemplo que muestra cómo usar secuencias básicas del sistema de archivos NTFS.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Uso de Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ebb6e2297c82e8643eb79ce66991b32fdf27e46fc723113a2866c79b2f8377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078395"
---
# <a name="using-streams"></a>Uso de Secuencias

En el ejemplo de este tema se muestra cómo usar secuencias básicas del sistema de archivos NTFS.

En este ejemplo se crea un archivo, denominado "TestFile", con un tamaño de 16 bytes. Sin embargo, el archivo también tiene un tipo de secuencia adicional ::$DATA, denominado "Stream", que agrega 23 bytes adicionales que el sistema operativo no notifica. Por lo tanto, al ver la propiedad file size del archivo, solo verá el tamaño del flujo predeterminado ::$DATA para el archivo.


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



Si escribe **Type TestFile en** un símbolo del sistema, se muestra la siguiente salida:

``` syntax
This is TestFile
```

Sin embargo, si escribe las palabras **Type TestFile:Stream**, se genera el siguiente error:

"La sintaxis de nombre de archivo, nombre de directorio o etiqueta de volumen es incorrecta".

Para ver lo que hay en TestFile:stream, use uno de los siguientes comandos:

**Más < TestFile:Stream**

**Más < TestFile:Stream:$DATA**

El texto mostrado es el siguiente:

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos Secuencias](file-streams.md)
</dt> </dl>

 

 



