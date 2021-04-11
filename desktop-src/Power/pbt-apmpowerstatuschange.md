---
description: Notifica a las aplicaciones un cambio en el estado de energía del equipo, como un conmutador de la alimentación de la batería a/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: Evento PBT_APMPOWERSTATUSCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276832"
---
# <a name="pbt_apmpowerstatuschange-event"></a>\_Evento PBT APMPOWERSTATUSCHANGE

Notifica a las aplicaciones un cambio en el estado de energía del equipo, como un conmutador de la alimentación de la batería a/C. El sistema difunde también este evento cuando la energía de la batería restante queda por debajo del umbral especificado por el usuario o cuando la energía de la batería cambia en un porcentaje especificado.

Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) . Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
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

| Value                                                                                                                                                                                                                                                        | Significado                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**PBT \_ APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt> </dl> | Identificador del evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este evento llamando a la función [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar el estado de energía actual del equipo. En concreto, la aplicación debe comprobar los miembros **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime** y **BatteryLifePercent** de la estructura [**de \_ \_ Estado de energía del sistema**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) en busca de cambios. Este evento puede producirse cuando la duración de la batería cae a menos de 5 minutos, o cuando el porcentaje de la duración de la batería cae por debajo del 10 por ciento, o si la duración de la batería cambia en un 3 por ciento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estado de la alimentación del sistema](system-power-status.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[**Estado de la alimentación del sistema \_ \_**](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




