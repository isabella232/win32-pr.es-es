---
title: Obtener acceso a un búfer de e/s de archivos
description: Obtener acceso a un búfer de e/s de archivos
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- e/s de archivos multimedia, acceso a búferes
- e/s de archivos, acceso a búferes
- entrada y salida (e/s), acceso a búferes
- E/s (entrada y salida), tener acceso a los búferes
- obtener acceso a búferes de e/s
- e/s almacenada en búfer
- mmioSetInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676368"
---
# <a name="accessing-a-file-io-buffer"></a>Obtener acceso a un búfer de e/s de archivos

En el ejemplo siguiente se accede directamente a un búfer de e/s para leer datos de un archivo de audio de onda.


```C++
HMMIO    hmmio; 
MMIOINFO mmioinfo; 
DWORD    dwDataSize; 
DWORD    dwCount; 
HPSTR    hptr; 

// Get information about the file I/O buffer. 
if (mmioGetInfo(hmmio, &mmioinfo, 0)) 
{ 
    Error("Failed to get I/O buffer info."); 
    . 
    . 
    . 
    mmioClose(hmmio, 0); 
    return; 
} 
 
// Read the entire file by directly reading the file I/O buffer. 
// When the end of the I/O buffer is reached, advance the buffer. 

for (dwCount = dwDataSize, hptr = lpData; dwCount  0; dwCount--) 
{ 
    // Check to see if the I/O buffer must be advanced. 
    if (mmioinfo.pchNext == mmioinfo.pchEndRead) 
    { 
        if(mmioAdvance(hmmio, &mmioinfo, MMIO_READ)) 
        { 
            Error("Failed to advance buffer."); 
            . 
            . 
            . 
            mmioClose(hmmio, 0); 
            return; 
        } 
    } 
 
    // Get a character from the buffer. 
    *hptr++ = *mmioinfo.pchNext++; 
} 
 
// End direct buffer access and close the file. 
mmioSetInfo(hmmio, &mmioinfo, 0); 
mmioClose(hmmio, 0); 

```



Cuando termine de acceder a un búfer de e/s de archivos, llame a la función [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) , pasando una dirección de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) rellenada por la función [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) . Si ha escrito en el búfer, establezca la \_ marca MMIO Dirty en el miembro **dwFlags** de la estructura **MMIOINFO** antes de llamar a **mmioSetInfo**. De lo contrario, el búfer no se vaciará en el disco.

 

 