---
description: Notifica a las aplicaciones que el sistema ha reanudado la operación.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Evento PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667206"
---
# <a name="pbt_apmresumecritical-event"></a>\_Evento PBT APMRESUMECRITICAL

\[PBT \_ APMRESUMECRITICAL está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Se ha quitado la compatibilidad con este evento en Windows Vista. Use [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) en su lugar.\]

Notifica a las aplicaciones que el sistema ha reanudado la operación. Este evento puede indicar que algunas o todas las aplicaciones no han recibido un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) . Por ejemplo, este evento se puede difundir después de una suspensión crítica causada por una batería con error.

Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) . Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
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

| Value                                                                                                                                                                                                                                              | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt> </dl> | Identificador del evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Dado que se produce una suspensión crítica sin notificación previa, es posible que los recursos y los datos disponibles anteriormente no estén presentes cuando la aplicación reciba este evento. La aplicación debe intentar restaurar su estado lo mejor que pueda. Mientras se encuentra en una suspensión crítica, el sistema mantiene el estado de la DRAM y los discos duros locales, pero es posible que no mantenga conexiones netas. Es posible que una aplicación tenga que tomar medidas en relación con los archivos que estaban abiertos en la red antes de la suspensión crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                                           |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




