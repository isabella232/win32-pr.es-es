---
title: MM_WOM_CLOSE mensaje (Mmsystem.h)
description: El mensaje MM WOM CLOSE se envía a una ventana cuando se cierra un dispositivo \_ de salida de audio de forma de \_ onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- MM_WOM_CLOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371227"
---
# <a name="mm_wom_close-message"></a>Mensaje \_ DE MM WOM \_ CLOSE

El **mensaje \_ MM WOM \_ CLOSE** se envía a una ventana cuando se cierra un dispositivo de salida de audio de forma de onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Controle el dispositivo que se cerró.

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

 

 





