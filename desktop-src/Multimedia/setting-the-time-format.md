---
title: Establecer el formato de hora
description: Establecer el formato de hora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904551"
---
# <a name="setting-the-time-format"></a>Establecer el formato de hora

Use el mensaje del comando [**\_ set de MCI**](mci-set.md) junto con la estructura de [**parms de MCI \_ set \_**](mci-set-parms.md) para establecer el formato de hora para un dispositivo abierto. Establezca el miembro **dwTimeFormat** en una de las siguientes constantes.



| Constante                   | Formato de hora                                          |
|----------------------------|------------------------------------------------------|
| \_bytes de formato de MCI \_         | Bytes (en archivos con formato PCM modulado de código \[ \] ) |
| formato MCI en \_ \_ milisegundos  | Milisegundos                                         |
| \_formato MCI \_ MSF           | Minuto/segundo/marco                                  |
| \_ejemplos de formato de MCI \_       | Ejemplos                                              |
| \_Formato MCI \_ SMPTE \_ 24     | SMPTE, 24 fotogramas                                      |
| \_Formato MCI \_ SMPTE \_ 25     | SMPTE, 25 fotograma                                      |
| \_Formato MCI \_ SMPTE \_ 30     | SMPTE, 30 fotogramas                                      |
| \_Formato MCI \_ SMPTE \_ 30DROP | SMPTE, 30 fotogramas de colocación                                 |
| \_formato MCI \_ TMSF          | Pista/minuto/segundo/marco                            |
| \_ \_ formato \_ SONGPTR de MCI SEQ  | Puntero de canción MIDI                                    |



 

En el ejemplo siguiente se establece el formato de hora en milisegundos en el dispositivo especificado por la variable wDeviceID con la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 