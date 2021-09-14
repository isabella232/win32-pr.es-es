---
title: Uso de la MCI_NOTIFY de datos
description: Uso de la marca \_ MCI NOTIFY
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- MCI_NOTIFY marca
- MCI_PLAY comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245738"
---
# <a name="using-the-mci_notify-flag"></a>Uso de la marca \_ MCI NOTIFY

En el ejemplo siguiente se muestra cómo se usa la marca \_ MCI NOTIFY con el [**comando MCI \_ PLAY.**](mci-play.md) El identificador del procedimiento de ventana que procesará el [**mensaje \_ MM MXIATIFY**](mm-mcinotify.md) se especifica en *hwnd*.


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




