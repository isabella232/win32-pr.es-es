---
title: MM_MIXM_CONTROL_CHANGE mensaje (Mmsystem.h)
description: Un dispositivo mezclador envía el mensaje MM MIXM CONTROL CHANGE para notificar a una aplicación que el estado de un control asociado a una línea \_ \_ de audio ha \_ cambiado. La aplicación debe actualizar sus valores de visualización y almacenados en caché para el control especificado.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE mensaje Windows Multimedia
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
ms.openlocfilehash: 44305a5a441e4d12a1b3f43029ae3a41f7642c13b15a50f74a1acab158c2ed58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807185"
---
# <a name="mm_mixm_control_change-message"></a>Mensaje \_ MM MIXM \_ CONTROL \_ CHANGE

Un dispositivo mezclador envía el mensaje **MM \_ MIXM \_ CONTROL \_ CHANGE** para notificar a una aplicación que el estado de un control asociado a una línea de audio ha cambiado. La aplicación debe actualizar sus valores de visualización y almacenados en caché para el control especificado.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Identificador del dispositivo mezclador **(H MIXER)** que envió el mensaje de notificación.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*
</dt> <dd>

Identificador de control del control mezclador que ha cambiado de estado. Este identificador es el mismo que el **miembro dwControlID** de la estructura **MIXERCONTROL** devuelta por la **función mixerGetLineControls.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una aplicación debe abrir un dispositivo mezclador y especificar una ventana de devolución de llamada para recibir el **mensaje MM \_ MIXM CONTROL \_ \_ CHANGE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mezcladores de audio](audio-mixers.md)
</dt> <dt>

[Mensajes de Mixer audio](audio-mixer-messages.md)
</dt> </dl>

 

 





