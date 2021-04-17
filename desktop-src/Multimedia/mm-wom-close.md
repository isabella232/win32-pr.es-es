---
title: Mensaje de MM_WOM_CLOSE (mmsystem. h)
description: El \_ mensaje de cierre mm WOM \_ se envía a una ventana cuando se cierra un dispositivo de salida de audio de forma de onda. El identificador de dispositivo ya no es válido después de enviar este mensaje.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- Mensaje de MM_WOM_CLOSE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686254"
---
# <a name="mm_wom_close-message"></a>Mensaje de cierre de MM \_ WOM \_

El mensaje de **\_ \_ cierre mm WOM** se envía a una ventana cuando se cierra un dispositivo de salida de audio de forma de onda. El identificador de dispositivo ya no es válido después de enviar este mensaje.


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Identificador del dispositivo que se cerró.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
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

 

 





