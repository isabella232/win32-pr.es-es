---
title: Abrir un dispositivo simple mediante el nombre del dispositivo
description: Abrir un dispositivo simple mediante el nombre del dispositivo
ms.assetid: 9e116499-2094-40e1-b2bc-3e3b8281a472
keywords:
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f84a852a18da3edb4431308259bacf38623bce3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371720"
---
# <a name="opening-a-simple-device-by-using-the-device-name"></a>Abrir un dispositivo simple mediante el nombre del dispositivo

En el ejemplo siguiente se abre un dispositivo de audio de CD especificando el nombre del dispositivo mediante la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a CD audio device by specifying the device name.

mciOpenParms.lpstrDeviceType = "cdaudio";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN, MCI_OPEN_TYPE,
    (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 