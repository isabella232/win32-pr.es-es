---
title: Comprobación del dispositivo de salida
description: Comprobación del dispositivo de salida
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- MCI_ comando STATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b02c014b374f83b3de5df90fd7de1952f65acd99b13f5075a59bc95d40e6380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781661"
---
# <a name="verifying-the-output-device"></a>Comprobación del dispositivo de salida

Después de abrir el secuenciador, debe comprobar si el asignador de MIDI estaba disponible y seleccionado como dispositivo de salida. En el ejemplo siguiente se usa el [**comando MCI \_ STATUS**](mci-status.md) para comprobar que el asignador de MIDI es el dispositivo de salida del secuenciador MCI.


```C++
UINT wDeviceID;      // valid MCI sequencer ID
DWORD dwReturn;
MCI_STATUS_PARMS mciStatusParms;

// Make sure the opened device is the MIDI mapper.

mciStatusParms.dwItem = MCI_SEQ_STATUS_PORT;

if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM,
    (DWORD)(LPVOID) &mciStatusParms))
{
    
    // Error sending MCI_STATUS command. 
    
    return;
}
if (LOWORD(mciStatusParms.dwReturn) == MIDI_MAPPER)
{
    
    // The MIDI mapper is the output device. 
    
}
Else
{
    
    // The MIDI mapper is not the output device. 
    
} 
```



 

 




