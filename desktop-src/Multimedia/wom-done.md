---
title: Mensaje de WOM_DONE (mmsystem. h)
description: El \_ mensaje WOM done se envía a una función de devolución de llamada de salida de audio de forma de onda cuando el búfer de salida especificado se devuelve a la aplicación.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- Mensaje de WOM_DONE de Windows multimedia
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149966"
---
# <a name="wom_done-message"></a>Mensaje de WOM \_ Done

El mensaje **WOM \_ Done** se envía a una función de devolución de llamada de salida de audio de forma de onda cuando el búfer de salida especificado se devuelve a la aplicación. Los búferes se devuelven a la aplicación cuando se han reproducido o como resultado de una llamada a la función [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Audio de onda](waveform-audio.md)
</dt> <dt>

[Mensajes de onda](waveform-messages.md)
</dt> </dl>

 

