---
title: Mensaje de WIM_OPEN (mmsystem. h)
description: El \_ mensaje abierto Wim se envía a una función de devolución de llamada de entrada de audio de forma de onda cuando se abre un dispositivo de entrada de audio de forma de onda.
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- Mensaje de WIM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c1661482149c90cf3f2bd6b10620cb32f380be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996949"
---
# <a name="wim_open-message"></a>\_Mensaje abierto Wim

El **mensaje \_ abierto Wim** se envía a una función de devolución de llamada de entrada de audio de forma de onda cuando se abre un dispositivo de entrada de audio de forma de onda.


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Sector debe ser cero.

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

 

 





