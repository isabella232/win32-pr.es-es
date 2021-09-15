---
title: Abrir un archivo AVI
description: Abrir un archivo AVI
ms.assetid: 322eb45f-7dd3-40f4-b6bf-381021c50397
keywords:
- Función AVIFileInit
- Función AVIFileOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833219194dc984bbf7bfa3d0415f77c5eed9b43b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476779"
---
# <a name="opening-an-avi-file"></a>Abrir un archivo AVI

En el ejemplo siguiente se inicializa la biblioteca AVIFile mediante la [**función AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) y se abre un archivo AVI mediante la [**función AVIFileOpen.**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) La función usa un controlador de archivos predeterminado.


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



 

 




