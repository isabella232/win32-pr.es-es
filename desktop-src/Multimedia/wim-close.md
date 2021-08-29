---
title: WIM_CLOSE mensaje (Mmsystem.h)
description: El mensaje CLOSE de WIM se envía a la función de devolución de llamada de entrada de audio de forma de onda dada cuando se cierra un dispositivo de entrada de \_ audio de forma de onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- WIM_CLOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488ef0d8a6a0d36852faa93397f853efb4f76f41761b6f38dd544ddcbc398ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803895"
---
# <a name="wim_close-message"></a>Mensaje \_ DE WIM CLOSE

El **mensaje CLOSE \_ de WIM** se envía a la función de devolución de llamada de entrada de audio de forma de onda dada cuando se cierra un dispositivo de entrada de audio de forma de onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Reservado; debe ser cero.

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

 

 





