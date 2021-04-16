---
title: Abrir un archivo AVI
description: Abrir un archivo AVI
ms.assetid: 322eb45f-7dd3-40f4-b6bf-381021c50397
keywords:
- AVIFileInit función)
- AVIFileOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833219194dc984bbf7bfa3d0415f77c5eed9b43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486799"
---
# <a name="opening-an-avi-file"></a>Abrir un archivo AVI

En el ejemplo siguiente se inicializa la biblioteca AVIFile con la función [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) y se abre un archivo AVI con la función [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) . La función utiliza un controlador de archivos predeterminado.


```C++
// LoadAVIFile - loads AVIFile and opens an AVI file. 
// 
// szfile - filename 
// hwnd - window handle 
// 
VOID LoadAVIFile(LPCSTR szFile, HWND hwnd) 
{ 
    LONG hr; 
    PAVIFILE pfile; 
 
    AVIFileInit();          // opens AVIFile library 
 
    hr = AVIFileOpen(&pfile, szFile, OF_SHARE_DENY_WRITE, 0L); 
    if (hr != 0){ 
        // Handle failure.
        return; 
    } 
 
// 
// Place functions here that interact with the open file. 
// 
 
    AVIFileRelease(pfile);  // closes the file 
    AVIFileExit();          // releases AVIFile library 
} 
 
```



 

 




