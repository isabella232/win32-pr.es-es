---
title: Mensaje de MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: '\_ \_ \_ Un dispositivo de mezclador envía el mensaje de cambio del control mm MIXM para notificar a una aplicación que ha cambiado el estado de un control asociado con una línea de audio. La aplicación debe actualizar su presentación y los valores almacenados en caché para el control especificado.'
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- Mensaje de MM_MIXM_CONTROL_CHANGE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651406"
---
# <a name="mm_mixm_control_change-message"></a>\_Mensaje de \_ cambio del control MIXM mm \_

Un dispositivo de mezclador envía el mensaje de **\_ cambio del \_ control \_ mm MIXM** para notificar a una aplicación que ha cambiado el estado de un control asociado con una línea de audio. La aplicación debe actualizar su presentación y los valores almacenados en caché para el control especificado.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Identificador del dispositivo de mezclador (**HMIXER**) que envió el mensaje de notificación.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*
</dt> <dd>

Identificador del control de mezclador que ha cambiado de estado. Este identificador es el mismo que el miembro **dwControlID** de la estructura **MIXERCONTROL** devuelta por la función **mixerGetLineControls**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una aplicación debe abrir un dispositivo de mezclador y especificar una ventana de devolución de llamada para recibir el mensaje de **\_ cambio del \_ control \_ mm MIXM** .

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

 

 





