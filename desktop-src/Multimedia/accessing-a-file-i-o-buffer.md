---
title: Acceso a un búfer de E/S de archivo
description: Acceso a un búfer de E/S de archivo
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- E/S de archivos multimedia, acceso a búferes
- E/S de archivo, acceso a búferes
- entrada y salida (E/S), acceso a búferes
- E/S (entrada y salida), acceso a búferes
- acceso a búferes de E/S
- E/S en búfer
- Función mmioSetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371798"
---
# <a name="accessing-a-file-io-buffer"></a>Acceso a un búfer de E/S de archivo

En el ejemplo siguiente se accede a un búfer de E/S directamente para leer datos de un archivo de audio de forma de onda.


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



Cuando termine de acceder a un búfer de E/S de archivo, llame a la función [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) y pase una dirección de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) rellenada por la [**función mmioGetInfo.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) Si escribió en el búfer, establezca la marca MMIO DIRTY en el miembro dwFlags de la estructura MMIOINFO antes de llamar \_ a  **mmioSetInfo**.  De lo contrario, el búfer no se vaciará en el disco.

 

 