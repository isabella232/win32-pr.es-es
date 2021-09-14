---
title: Cambiar el tamaño del búfer de E/S
description: Cambiar el tamaño del búfer de E/S
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- E/S de archivo multimedia, cambiar el tamaño del búfer
- E/S de archivo, cambiar el tamaño del búfer
- entrada y salida (E/S), cambio del tamaño del búfer
- E/S (entrada y salida), cambiar el tamaño del búfer
- cambiar el tamaño del búfer de E/S
- E/S sin búfer
- E/S en búfer
- Función mmioSetBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266015"
---
# <a name="changing-the-io-buffer-size"></a>Cambiar el tamaño del búfer de E/S

En el ejemplo siguiente se abre un archivo denominado SAMPLE.TXT para E/S sin búfer y, a continuación, se habilita la E/S almacenada en búfer con un búfer interno de 16K mediante la función [**mmioSetBuffer.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)


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



 

 