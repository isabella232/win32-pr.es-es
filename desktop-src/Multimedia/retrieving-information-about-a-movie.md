---
title: Recuperar información sobre una película
description: Recuperar información sobre una película
ms.assetid: 678272e0-67fe-4ec1-88a8-924a773445a7
keywords:
- mciSendCommand función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fb56164a9dc440240f12c16b9adff1210db71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358821"
---
# <a name="retrieving-information-about-a-movie"></a>Recuperar información sobre una película

En el ejemplo siguiente se establece el formato de hora en los fotogramas y se obtiene la posición actual si el dispositivo se está reproduciendo con la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
MCI_DGV_SET_PARMS mciSet; 
MCI_DGV_STATUS_PARMS mciStatus; 
 
// Put in frame mode. 
mciSet.dwTimeFormat = MCI_FORMAT_FRAMES; 
mciSendCommand(wDeviceID, MCI_SET, 
    MCI_SET_TIME_FORMAT, 
    (DWORD)(LPSTR)&mciSet); 
 
mciStatus.dwItem = MCI_STATUS_MODE; 
mciSendCommand(wDeviceID, MCI_STATUS, 
    MCI_STATUS_ITEM, 
    (DWORD)(LPSTR)&mciStatus); 
 
// If device is playing, get the position. 
if (mciStatus.dwReturn == MCI_MODE_PLAY)
{ 
    mciStatus.dwItem = MCI_STATUS_POSITION; 
    mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM, 
        (DWORD)(LPSTR)&mciStatus); 
 
    // Update the position from mciStatus.dwReturn. 
} 
```



 

 