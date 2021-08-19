---
title: Abrir un dispositivo simple mediante el nombre del dispositivo
description: Abrir un dispositivo simple mediante el nombre del dispositivo
ms.assetid: 9e116499-2094-40e1-b2bc-3e3b8281a472
keywords:
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d186451717a056188d6fc990188c7e73fcf34cf1339b0787f7cec6e7573557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802332"
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



 

 