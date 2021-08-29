---
title: WOM_CLOSE mensaje (Mmsystem.h)
description: El mensaje WOM CLOSE se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se cierra un \_ dispositivo de salida de audio de forma de onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- WOM_CLOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ba0187638ec4bc0406066c9a50ee4ce53ca150e4dabc918a829cfaa08733b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803485"
---
# <a name="wom_close-message"></a>Mensaje WOM \_ CLOSE

El **mensaje WOM \_ CLOSE** se envía a una función de devolución de llamada de salida de audio de forma de onda cuando se cierra un dispositivo de salida de audio de forma de onda. El identificador del dispositivo ya no es válido después de que se haya enviado este mensaje.


```C++
WOM_CLOSE 
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

 

 





