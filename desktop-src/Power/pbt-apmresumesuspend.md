---
description: Notifica a las aplicaciones que el sistema ha reanudado el funcionamiento después de suspenderse.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: PBT_APMRESUMESUSPEND evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062836"
---
# <a name="pbt_apmresumesuspend-event"></a>Evento \_ PBT APMRESUMESUSPEND

Notifica a las aplicaciones que el sistema ha reanudado el funcionamiento después de suspenderse.

Una ventana recibe este evento a través del [**mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
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

| Value                                                                                                                                                                                                                                           | Significado                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación solo puede recibir este evento si recibió el evento [ \_ PBT APMSUSPEND](pbt-apmsuspend.md) antes de que se suspendiera el equipo. De lo contrario, la aplicación recibirá un evento [ \_ PBT APMRESUMECRITICAL.](pbt-apmresumecritical.md)

Si el sistema se reactiva debido a la actividad del usuario (por ejemplo, al presionar el botón de encendido) o si el sistema detecta la interacción del usuario en la consola física (como la entrada del mouse o el teclado) después de activarse desatendidamente, el sistema difunde primero el evento [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) y luego difunde el evento \_ PBT APMRESUMESUSPEND. Además, el sistema activa la pantalla. La aplicación debe volver a abrir los archivos que cerró cuando el sistema entró en suspensión y prepararse para la entrada del usuario.

Si el sistema se reactiva debido a una señal de reactivación externa (reactivación remota), el sistema solo difunde el evento [ \_ PBT APMRESUMEAUTOMATIC.](pbt-apmresumeautomatic.md) No se envía el evento \_ PBT APMRESUMESUSPEND.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




