---
description: Notifica a las aplicaciones que el sistema se está reanudando desde suspensión o hibernación. Este evento se entrega cada vez que se reanuda el sistema y no indica si un usuario está presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: PBT_APMRESUMEAUTOMATIC evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062844"
---
# <a name="pbt_apmresumeautomatic-event"></a>Evento \_ PBT APMRESUMEAUTOMATIC

Notifica a las aplicaciones que el sistema se está reanudando desde suspensión o hibernación. Este evento se entrega cada vez que se reanuda el sistema y no indica si un usuario está presente.

Una ventana recibe este evento a través [**del mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.

> [!Note]  
> En Windows 10, versión 1507 o posterior, si el sistema se reanuda desde suspensión solo para entrar inmediatamente en hibernación, este evento no se entrega. En este caso, no se envía un mensaje [**WM \_ POWERBROADCAST.**](wm-powerbroadcast.md)

 


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

*Hwnd* 
</dt> <dd>

Identificador a ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador del mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                                   | Significado                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el sistema detecta cualquier actividad de usuario después de difundir PBT \_ APMRESUMEAUTOMATIC, difundirá un evento [ \_ PBT APMRESUMESUSPEND](pbt-apmresumesuspend.md) para que las aplicaciones sepan que pueden reanudar la interacción completa con el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




