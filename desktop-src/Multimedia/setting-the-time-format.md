---
title: Establecer el formato de hora
description: Establecer el formato de hora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eb5a9194f3f2598cd8f88fbefb3ea741f51eb9c25210deb6db69c54259e189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370894"
---
# <a name="setting-the-time-format"></a>Establecer el formato de hora

Use el [**mensaje de comando \_ MCI SET**](mci-set.md) junto con la estructura [**\_ MCI SET \_ PARMS**](mci-set-parms.md) para establecer el formato de hora de un dispositivo abierto. Establezca el **miembro dwTimeFormat** en una de las siguientes constantes.



| Constante                   | Formato de hora                                          |
|----------------------------|------------------------------------------------------|
| BYTES DE FORMATO MCI \_ \_         | Bytes (en archivos de formato PCM modular de código de \[ \] pulso) |
| MILISEGUNDOS DE FORMATO MCI \_ \_  | Milisegundos                                         |
| MCI \_ FORMAT \_ MSF           | Minuto/segundo/fotograma                                  |
| EJEMPLOS DE FORMATO \_ MCI \_       | Ejemplos                                              |
| MCI \_ FORMAT \_ SMPTE \_ 24     | SMPTE, 24 fotogramas                                      |
| FORMATO MCI \_ \_ SMPTE \_ 25     | SMPTE, 25 fotogramas                                      |
| FORMATO MCI \_ \_ SMPTE \_ 30     | SMPTE, 30 fotogramas                                      |
| FORMATO MCI \_ \_ SMPTE \_ 30DROP | SMPTE, 30 fotogramas                                 |
| \_TMSF CON \_ FORMATO MCI          | Seguimiento/minuto/segundo/fotograma                            |
| FORMATO MCI \_ SEQ \_ \_ SONGPTR  | Puntero de canción DE MES                                    |



 

En el ejemplo siguiente se establece el formato de hora en milisegundos en el dispositivo especificado por la variable wDeviceID mediante la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


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



 

 