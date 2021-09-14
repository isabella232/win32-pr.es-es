---
description: Notifica a las aplicaciones que se ha producido un evento de administración de energía.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: WM_POWERBROADCAST mensaje (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169110"
---
# <a name="wm_powerbroadcast-message"></a>Mensaje \_ DE WM POWERBROADCAST

Notifica a las aplicaciones que se ha producido un evento de administración de energía.

Una ventana recibe este mensaje a través de su **función WindowProc.**


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>
  
*uMsg*
</dt> <dd> 

| Value                                                                                                                                                                                                                                          | Significado                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>*:WM \_ POWERBROADCAST**</dt> <dt>536 (0x218)</dt> </dl> | Identificador del mensaje.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

Evento de administración de energía. Este parámetro puede ser uno de los siguientes identificadores de evento.



| Evento                                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | El estado de energía ha cambiado.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | La operación se reanuda automáticamente desde un estado de bajo consumo. Este mensaje se envía cada vez que se reanuda el sistema.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | La operación se reanuda desde un estado de bajo consumo. Este mensaje se envía después de [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) si la reanudación se desencadena mediante la entrada del usuario, como presionar una tecla.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | El sistema suspende la operación.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | Se ha recibido un evento de cambio de configuración de energía. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Datos específicos del evento. Para la mayoría de los eventos, este parámetro está reservado y no se usa.

Si el *parámetro wParam* es [PBT \_ POWERSETTINGCHANGE,](pbt-powersettingchange.md)el parámetro *lParam* es un puntero a una [**estructura SETTING DE POWERBROADCAST. \_**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver **TRUE** si procesa este mensaje.

## <a name="remarks"></a>Observaciones

El sistema siempre envía un mensaje [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) cada vez que se reanuda el sistema. Si el sistema se reanuda en respuesta a la entrada del usuario, como presionar una tecla, el sistema también envía un mensaje **\_ PBT APMRESUMESUSPEND** después de enviar PBT \_ APMRESUMEAUTOMATIC.

**WM \_ Los mensajes POWERBROADCAST** no distinguen entre distintos estados de bajo consumo. Una aplicación solo puede determinar que el sistema entra o se ha reanudado desde un estado de bajo consumo. no puede determinar el estado de energía específico. El sistema registra detalles sobre las transiciones de estado de energía en el Windows de eventos del sistema.

Para evitar que el sistema haga la transición a un estado de bajo consumo en Windows Vista, una aplicación debe llamar a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para informar al sistema de que está en uso.

Los mensajes siguientes no se admiten en ninguno de los sistemas operativos especificados en la sección Requisitos:

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes \_ DE WM POWERBROADCAST](wm-powerbroadcast-messages.md)
</dt> <dt>

[Mensajes de administración de energía](power-management-messages.md)
</dt> </dl>

 

 




