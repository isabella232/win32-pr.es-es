---
title: Usar la marca de MCI_NOTIFY
description: Uso de la \_ marca de notificación de MCI
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- MCI_NOTIFY marca
- Comando MCI_PLAY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903245"
---
# <a name="using-the-mci_notify-flag"></a>Uso de la \_ marca de notificación de MCI

En el ejemplo siguiente se muestra cómo \_ se usa la marca de notificación de MCI con el comando de [**\_ reproducción de MCI**](mci-play.md) . El identificador del procedimiento de ventana que procesará el mensaje [**mm \_ MCINOTIFY**](mm-mcinotify.md) se especifica en *hWnd*.


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




