---
title: Abrir secuencias en un archivo AVI y cerrar el archivo
description: Abrir secuencias en un archivo AVI y cerrar el archivo
ms.assetid: 3c6afa04-3d95-48cd-b468-7167bac07d46
keywords:
- AVIFileGetStream función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca06378862ec543e9da8f671eca50841c85d744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268600"
---
# <a name="opening-streams-in-an-avi-file-and-closing-the-file"></a>Abrir secuencias en un archivo AVI y cerrar el archivo

En el siguiente ejemplo se abren todas las secuencias en un archivo AVI mediante la función [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) . Si se produce un error, se cierra el archivo.


```C++
// InsertAVIFile - opens the streams in an AVI file. 
// 
// pfile - file-interface pointer from AVIFileOpen 
// 
// Global variables 
// gcpavi - count of the number of streams in an AVI file 
// gapavi[] = array of stream-interface pointers 
 
void InsertAVIFile(PAVIFILE pfile, HWND hwnd, LPSTR lpszFile) 
{ 
    int    i; 
    gcpavi = 0; 
 
    // Open the streams until a stream is not available. 
    for (i = gcpavi; i < MAXNUMSTREAMS; i++) { 
        gapavi[i] = NULL; 
        if (AVIFileGetStream(pfile, &gapavi[i], 0L, i - gcpavi) 
            != AVIERR_OK) 
        break; 
 
    if (gapavi[i] == NULL) 
        break; 
    } 
    // Display error message-stream not found. 
    if (gcpavi == i) 
    { 
        // Handle failure.
        if (pfile) // If file is open, close it 
            AVIFileRelease(pfile); 
        return; 
    } 
    else { 
        gcpavi = i - 1; 
    } 
 
//  . 
//  . Place functions to process data here. 
//  . 
} 
 
```



 

 




