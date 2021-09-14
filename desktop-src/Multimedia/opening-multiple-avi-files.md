---
title: Abrir varios archivos AVI
description: Abrir varios archivos AVI
ms.assetid: 982bcea1-77b0-4a38-893d-1f506ffb18f5
keywords:
- Función initAVI
- función termAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac540d670b15eaf1befb1d2f253223e3571ecee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173618"
---
# <a name="opening-multiple-avi-files"></a>Abrir varios archivos AVI

Si la aplicación abre varios archivos, debe incluir rutinas como las siguientes funciones simples. La aplicación usaría la función "initAVI" durante su inicialización y la función "termAVI" durante su finalización. Estas funciones simplemente encapsulan [**la función mciSendString.**](/previous-versions//dd757161(v=vs.85))


```C++
// Initialize the MCIAVI driver. This returns TRUE if OK, 
// FALSE on error. 
 
BOOL initAVI(VOID) 
{ 
    // Perform additional initialization before loading first file. 
    return mciSendString("open digitalvideo", NULL, 0, NULL) == 0; 
} 
 
// Close the MCIAVI driver. 
void termAVI(VOID) 
{ 
    mciSendString("close digitalvideo", NULL, 0, NULL); 
} 
```



 

 