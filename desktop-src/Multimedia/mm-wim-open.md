---
title: MM_WIM_OPEN mensaje (Mmsystem.h)
description: El mensaje MM WIM OPEN se envía a una ventana cuando se abre un dispositivo de entrada de \_ audio de forma de \_ onda.
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- MM_WIM_OPEN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc5271f4e2a49b762273b241133ea5c5826ebf1861ba9fe5eb4cf7832b164fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065445"
---
# <a name="mm_wim_open-message"></a>Mensaje \_ MM WIM \_ OPEN

El **mensaje \_ MM WIM \_ OPEN** se envía a una ventana cuando se abre un dispositivo de entrada de audio de forma de onda.


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Controle el dispositivo que se abrió.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





