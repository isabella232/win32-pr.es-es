---
title: MM_WIM_CLOSE mensaje (Mmsystem.h)
description: El mensaje MM WIM CLOSE se envía a una ventana cuando se cierra un dispositivo \_ de entrada de audio de forma de \_ onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371185"
---
# <a name="mm_wim_close-message"></a>Mensaje \_ MM WIM \_ CLOSE

El **mensaje \_ MM WIM \_ CLOSE** se envía a una ventana cuando se cierra un dispositivo de entrada de audio de forma de onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Controle el dispositivo de entrada de audio de forma de onda que se cerró.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
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

 

 





