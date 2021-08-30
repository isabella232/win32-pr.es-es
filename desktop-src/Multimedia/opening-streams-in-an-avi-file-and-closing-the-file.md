---
title: Abrir Secuencias en un archivo AVI y cerrar el archivo
description: Abrir Secuencias en un archivo AVI y cerrar el archivo
ms.assetid: 3c6afa04-3d95-48cd-b468-7167bac07d46
keywords:
- Función AVIFileGetStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634d1e21bc324c85636bd607e14669d3577b2b4b0b3296881af62baefb0b0db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038305"
---
# <a name="opening-streams-in-an-avi-file-and-closing-the-file"></a>Abrir Secuencias en un archivo AVI y cerrar el archivo

En el ejemplo siguiente se abren todas las secuencias de un archivo AVI mediante la [**función AVIFileGetStream.**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) Si se produce un error, el archivo se cierra.


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



 

 




