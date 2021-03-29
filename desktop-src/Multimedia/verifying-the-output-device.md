---
title: Comprobando el dispositivo de salida
description: Comprobando el dispositivo de salida
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- Comando estado de MCI_
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1774eb3df2a45f98558862a15349007cd299d142
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994344"
---
# <a name="verifying-the-output-device"></a><span data-ttu-id="ebe80-104">Comprobando el dispositivo de salida</span><span class="sxs-lookup"><span data-stu-id="ebe80-104">Verifying the Output Device</span></span>

<span data-ttu-id="ebe80-105">Después de abrir Sequencer, debe comprobar si el asignador de MIDI estaba disponible y seleccionado como dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="ebe80-105">After opening the sequencer, you should check whether the MIDI mapper was available and selected as the output device.</span></span> <span data-ttu-id="ebe80-106">En el ejemplo siguiente se usa el comando [**MCI \_ status**](mci-status.md) para comprobar que el asignador MIDI es el dispositivo de salida para el secuenciador MCI.</span><span class="sxs-lookup"><span data-stu-id="ebe80-106">The following example uses the [**MCI\_ STATUS**](mci-status.md) command to verify that the MIDI mapper is the output device for the MCI sequencer.</span></span>


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



 

 




