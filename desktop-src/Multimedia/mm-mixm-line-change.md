---
title: Mensaje de MM_MIXM_LINE_CHANGE (mmsystem. h)
description: '\_ \_ \_ Un dispositivo de mezclador envía el mensaje de cambio de línea mm MIXM para notificar a una aplicación que ha cambiado el estado de una línea de audio en el dispositivo especificado. La aplicación debe actualizar su presentación y los valores almacenados en caché para la línea de audio especificada.'
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- Mensaje de MM_MIXM_LINE_CHANGE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686090"
---
# <a name="mm_mixm_line_change-message"></a>\_Mensaje de \_ cambio de línea mm MIXM \_

Un dispositivo de mezclador envía el mensaje de **\_ cambio de \_ línea \_ mm MIXM** para notificar a una aplicación que ha cambiado el estado de una línea de audio en el dispositivo especificado. La aplicación debe actualizar su presentación y los valores almacenados en caché para la línea de audio especificada.


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Identificador del dispositivo de mezclador que envió el mensaje de notificación.

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*
</dt> <dd>

Identificador de línea de la línea de audio que ha cambiado de estado. Este identificador es el mismo que el miembro **dwLineID** de la estructura **MIXERLINE** devuelta por la función **mixerGetLineInfo**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una aplicación debe abrir un dispositivo de mezclador y especificar una ventana de devolución de llamada para recibir el mensaje de **\_ cambio de \_ línea \_ mm MIXM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mezcladores de audio](audio-mixers.md)
</dt> <dt>

[Mensajes de mezclador de audio](audio-mixer-messages.md)
</dt> </dl>

 

 





