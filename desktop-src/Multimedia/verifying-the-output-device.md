---
title: Comprobación del dispositivo de salida
description: Comprobación del dispositivo de salida
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- MCI_ comando STATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1774eb3df2a45f98558862a15349007cd299d142
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371762"
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



 

 




