---
description: Notifica a las aplicaciones que el sistema se está reanudando de la suspensión o hibernación. Este evento se entrega cada vez que el sistema se reanuda y no indica si un usuario está presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Evento PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909689"
---
# <a name="pbt_apmresumeautomatic-event"></a>\_Evento PBT APMRESUMEAUTOMATIC

Notifica a las aplicaciones que el sistema se está reanudando de la suspensión o hibernación. Este evento se entrega cada vez que el sistema se reanuda y no indica si un usuario está presente.

Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) . Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.

> [!Note]  
> En los sistemas Windows 10, versión 1507 o posterior, si el sistema se está reanudando de la suspensión solo para entrar inmediatamente en hibernación, este evento no se entrega. En este caso, no se envía un mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador de mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                                   | Significado                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0X12)</dt> </dl> | Identificador del evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el sistema detecta cualquier actividad de usuario después de difundir PBT \_ APMRESUMEAUTOMATIC, difundirá un [evento \_ APMRESUMESUSPEND de PBT](pbt-apmresumesuspend.md) para que las aplicaciones sepan que pueden reanudar la interacción completa con el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)
</dt> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




