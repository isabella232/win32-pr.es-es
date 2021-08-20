---
title: WOM_DONE mensaje (Mmsystem.h)
description: El mensaje WOM DONE se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se devuelve el búfer de salida dado \_ a la aplicación.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE mensaje Windows Multimedia
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
ms.openlocfilehash: 0f8e54fe6f8f79c9fe5885861dbda758a663ca49b38ed559b06ba59627768055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134820"
---
# <a name="wom_done-message"></a>Mensaje DE WOM \_ DONE

El **mensaje WOM \_ DONE** se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se devuelve el búfer de salida dado a la aplicación. Los búferes se devuelven a la aplicación cuando se han reproducido, o como resultado de una llamada a la [**función waveOutReset.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntero a una [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Audio de forma de onda](waveform-audio.md)
</dt> <dt>

[Mensajes de forma de onda](waveform-messages.md)
</dt> </dl>

 

