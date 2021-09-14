---
description: Notifica a las aplicaciones que el sistema ha reanudado el funcionamiento.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: PBT_APMRESUMECRITICAL evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062843"
---
# <a name="pbt_apmresumecritical-event"></a>Evento \_ PBT APMRESUMECRITICAL

\[PBT APMRESUMECRITICAL está disponible para su uso en los \_ sistemas operativos especificados en la sección Requisitos. Se quitó la compatibilidad con este evento en Windows Vista. Use [PBT \_ APMRESUMEAUTOMATIC en su](pbt-apmresumeautomatic.md) lugar.\]

Notifica a las aplicaciones que el sistema ha reanudado el funcionamiento. Este evento puede indicar que algunas o todas las aplicaciones no recibieron un evento [ \_ PBT APMSUSPEND.](pbt-apmsuspend.md) Por ejemplo, este evento se puede difundir después de una suspensión crítica causada por una batería con errores.

Una ventana recibe este evento a través del [**mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.


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

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador del mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                              | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Dado que se produce una suspensión crítica sin notificación previa, es posible que los recursos y los datos disponibles anteriormente no estén presentes cuando la aplicación reciba este evento. La aplicación debe intentar restaurar su estado lo mejor que pueda. Mientras se encuentra en una suspensión crítica, el sistema mantiene el estado de la DRAM y los discos duros locales, pero puede que no mantenga conexiones netas. Es posible que una aplicación tenga que tomar medidas con respecto a los archivos que estaban abiertos en la red antes de la suspensión crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                                           |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




