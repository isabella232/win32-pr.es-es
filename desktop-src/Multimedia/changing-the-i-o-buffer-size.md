---
title: Cambiar el tamaño del búfer de e/s
description: Cambiar el tamaño del búfer de e/s
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- e/s de archivos multimedia, cambiar el tamaño del búfer
- e/s de archivos, cambiar el tamaño del búfer
- entrada y salida (e/s), cambiar el tamaño del búfer
- E/s (entrada y salida), cambiar el tamaño del búfer
- cambiar el tamaño del búfer de e/s
- e/s no almacenada en búfer
- e/s almacenada en búfer
- mmioSetBuffer función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077759"
---
# <a name="changing-the-io-buffer-size"></a>Cambiar el tamaño del búfer de e/s

En el ejemplo siguiente se abre un archivo denominado SAMPLE.TXT para la e/s no almacenada en búfer y, a continuación, se habilita la e/s del búfer con un búfer interno de 16 KB mediante la función [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("SAMPLE.TXT", NULL, MMIO_READ)) != NULL) 
{ 
    // File opened successfully; request an I/O buffer. 
    if (mmioSetBuffer(hFile, NULL, 16384L, 0)) 
        // Buffer cannot be allocated. 
    else 
        // Buffer allocated successfully. 
} 
else 
    // File cannot be opened. 
```



 

 