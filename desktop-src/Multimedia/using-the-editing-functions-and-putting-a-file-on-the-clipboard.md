---
title: Usar las funciones de edición y colocar un archivo en el portapapeles
description: Usar las funciones de edición y colocar un archivo en el portapapeles
ms.assetid: 2c69e44a-5f45-45e7-bbad-c593359943a0
keywords:
- EditStreamClone función)
- EditStreamCopy función)
- EditStreamCut función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533f2165afdb3173ea0f8c603764f25d0fa625fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994027"
---
# <a name="using-the-editing-functions-and-putting-a-file-on-the-clipboard"></a>Usar las funciones de edición y colocar un archivo en el portapapeles

En el ejemplo siguiente se recortan, copian o eliminan segmentos de una matriz de secuencias. Los flujos de corte y copiados se combinan en un archivo nuevo y se colocan en el portapapeles. Entre las funciones que se usan se incluyen [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone), [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)y [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut).


```C++
// Global variables 
// gcpavi - count of streams in an AVI file 
// gapavi[] - array of stream-interface pointers, used as data source 
// gapaviSel[] - stream-interface pointers of edited streams 
// galSelStart[] - edit starting point in each stream 
// galSelLen[] - length of edit to make in each stream 
// gapaviTemp[] - array of stream-interface pointers put on clipboard 
// 
// Comment: 
//     The editable streams in gapaviSel have been 
//     initialized with CreateEditableStream. 
 
case MENU_CUT: 
case MENU_COPY: 
case MENU_DELETE: 
{ 
    PAVIFILE pf; 
    int      i; 
 
    // Walk list of selections and make streams out of each section. 
    gcpaviSel = 0;  // index counter for destination streams 
    for (i = 0; i < gcpavi; i++) { 
        if (galSelStart[i] != -1) { 
            if (wParam == MENU_COPY) 
                EditStreamCopy(gapavi[i], &galSelStart[i], 
                &galSelLen[i], &gapaviSel[gcpaviSel++]); 
            else { 
                EditStreamCut(gapavi[i], &galSelStart[i], 
                &galSelLen[i], &gapaviSel[gcpaviSel++]); 
            } 
        } 
    } 
 
. 
. 
. 
    // Put on the clipboard if segment is not deleted. 
    if (gcpaviSel && wParam != MENU_DELETE) { 
        PAVISTREAM   gapaviTemp[MAXNUMSTREAMS]; 
        int i; 
 
        // Clone the edited streams, so that if the user does 
        // more editing, the clipboard won't change. 
        for (i = 0; i < gcpaviSel; i++) { 
            gapaviTemp[i] = NULL; 
            EditStreamClone(gapaviSel[i], &gapaviTemp[i]); 
            // 
            // Place error check here. 
            // 
        } 
 
        // Create a file from the streams and put on clipboard. 
        AVIMakeFileFromStreams(&pf, gcpaviSel, gapaviTemp); 
        AVIPutFileOnClipboard(pf); 
 
        // Release clone streams. 
        for (i = 0; i < gcpaviSel; i++) { 
            AVIStreamRelease(gapaviTemp[i]); 
        } 
 
        // Release file put on clipboard. 
        AVIFileRelease(pf); 
    } 
 
    // Release streams created. 
    for (i = 0; i < gcpaviSel; i++) 
        AVIStreamRelease(gapaviSel[i]); 
} 
 
```



 

 




