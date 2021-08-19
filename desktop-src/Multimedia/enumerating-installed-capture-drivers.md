---
title: Enumerar los controladores de captura instalados
description: Enumerar los controladores de captura instalados
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- Función capGetDriverDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8fe85103259354bcc3b42834ecaff03d660eb408cda8191e5e0abea7393d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988664"
---
# <a name="enumerating-installed-capture-drivers"></a>Enumerar los controladores de captura instalados

En el ejemplo siguiente se usa [**la función capGetDriverDescription para**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) obtener los nombres y las versiones de los controladores de captura instalados.


```C++
char szDeviceName[80];
char szDeviceVersion[80];

for (wIndex = 0; wIndex < 10; wIndex++) 
{
    if (capGetDriverDescription(
            wIndex, 
            szDeviceName, 
            sizeof (szDeviceName), 
            szDeviceVersion, 
            sizeof (szDeviceVersion)
        )) 
    {
        // Append name to list of installed capture drivers
        // and then let the user select a driver to use.
    }
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




