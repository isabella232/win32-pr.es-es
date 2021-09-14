---
description: Notifica a las aplicaciones un cambio en el estado de energía del equipo, como un cambio de la energía de la batería a A/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: PBT_APMPOWERSTATUSCHANGE evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062848"
---
# <a name="pbt_apmpowerstatuschange-event"></a>Evento \_ PBT APMPOWERSTATUSCHANGE

Notifica a las aplicaciones un cambio en el estado de energía del equipo, como un cambio de la energía de la batería a A/C. El sistema difunde también este evento cuando la energía de la batería restante queda por debajo del umbral especificado por el usuario o cuando la energía de la batería cambia en un porcentaje especificado.

Una ventana recibe este evento a través del [**mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.


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

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador del mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                                        | Significado                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**PBT \_ APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este evento llamando a la [**función GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar el estado de energía actual del equipo. En concreto, la aplicación debe comprobar los miembros **ACLineStatus,** **BatteryFlag,** **BatteryLifeTime** y **BatteryLifePercent** de la estructura [**SYSTEM POWER \_ \_ STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) para ver si hay cambios. Este evento puede producirse cuando la duración de la batería disminuye a menos de 5 minutos, cuando el porcentaje de duración de la batería cae por debajo del 10 % o si la duración de la batería cambia en un 3 %.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estado de energía del sistema](system-power-status.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[**ESTADO \_ DE ENERGÍA DEL \_ SISTEMA**](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




