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
# <a name="using-streams"></a><span data-ttu-id="36cca-103">Usar secuencias</span><span class="sxs-lookup"><span data-stu-id="36cca-103">Using Streams</span></span>

<span data-ttu-id="36cca-104">En el ejemplo de este tema se muestra cómo usar secuencias básicas del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="36cca-104">The example in this topic demonstrates how to use basic NTFS file system streams.</span></span>

<span data-ttu-id="36cca-105">En este ejemplo se crea un archivo, denominado "TestFile", con un tamaño de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="36cca-105">This example creates a file, called "TestFile," with a size of 16 bytes.</span></span> <span data-ttu-id="36cca-106">Sin embargo, el archivo también tiene un tipo de flujo adicional:: $DATA, denominado "Stream", que agrega 23 bytes adicionales que el sistema operativo no indica.</span><span class="sxs-lookup"><span data-stu-id="36cca-106">However, the file also has an additional ::$DATA stream type, named "Stream" which adds an additional 23 bytes that is not reported by the operating system.</span></span> <span data-ttu-id="36cca-107">Por lo tanto, al ver la propiedad de tamaño de archivo del archivo, solo verá el tamaño de la secuencia default:: $DATA del archivo.</span><span class="sxs-lookup"><span data-stu-id="36cca-107">Therefore, when you view the file size property for the file, you see only the size of default ::$DATA stream for the file.</span></span>


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



<span data-ttu-id="36cca-108">Si escribe **Type TESTFILE** en un símbolo del sistema, se mostrará el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="36cca-108">If you type **Type TestFile** at a command prompt, it displays the following output:</span></span>

``` syntax
This is TestFile
```

<span data-ttu-id="36cca-109">Sin embargo, si escribe las palabras **Type TESTFILE: Stream**, se genera el siguiente error:</span><span class="sxs-lookup"><span data-stu-id="36cca-109">However, if you type the words **Type TestFile:Stream**, it generates the following error:</span></span>

<span data-ttu-id="36cca-110">"El nombre de archivo, el nombre de directorio o la sintaxis de la etiqueta de volumen son incorrectos".</span><span class="sxs-lookup"><span data-stu-id="36cca-110">"The filename, directory name, or volume label syntax is incorrect."</span></span>

<span data-ttu-id="36cca-111">Para ver lo que hay en TestFile: Stream, use uno de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="36cca-111">To view what is in TestFile:stream, use one of the following commands:</span></span>

<span data-ttu-id="36cca-112">**Más < TestFile: Stream**</span><span class="sxs-lookup"><span data-stu-id="36cca-112">**More < TestFile:Stream**</span></span>

<span data-ttu-id="36cca-113">**Más < TestFile: Stream: $DATA**</span><span class="sxs-lookup"><span data-stu-id="36cca-113">**More < TestFile:Stream:$DATA**</span></span>

<span data-ttu-id="36cca-114">El texto que se muestra es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="36cca-114">The text displayed is as follows:</span></span>

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a><span data-ttu-id="36cca-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36cca-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36cca-116">Secuencias de archivo</span><span class="sxs-lookup"><span data-stu-id="36cca-116">File Streams</span></span>](file-streams.md)
</dt> </dl>

 

 



