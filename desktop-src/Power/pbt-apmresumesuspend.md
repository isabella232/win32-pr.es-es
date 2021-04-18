---
description: Notifica a las aplicaciones que el sistema ha reanudado la operación después de suspenderse.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Evento PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667205"
---
# <a name="pbt_apmresumesuspend-event"></a>\_Evento PBT APMRESUMESUSPEND

Notifica a las aplicaciones que el sistema ha reanudado la operación después de suspenderse.

Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) . Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.


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

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador de mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                           | Significado                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0X7)</dt> </dl> | Identificador del evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación puede recibir este evento solo si recibió el evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de que se suspendiera el equipo. De lo contrario, la aplicación recibirá un evento [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .

Si el sistema se reactiva debido a la actividad del usuario (por ejemplo, al presionar el botón de encendido) o si el sistema detecta la interacción del usuario en la consola física (por ejemplo, la entrada del mouse o del teclado) después de activar desatendido, el sistema emite primero el evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) y, a continuación, difunde el \_ evento APMRESUMESUSPEND de PBT. Además, el sistema activa la pantalla. La aplicación debe volver a abrir los archivos que cerró cuando el sistema entró en suspensión y prepararse para los datos proporcionados por el usuario.

Si el sistema se reactiva debido a una señal de reactivación externa (reactivación remota), el sistema difundirá solo el evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) . \_No se envía el evento PBT APMRESUMESUSPEND.

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

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md)
</dt> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




