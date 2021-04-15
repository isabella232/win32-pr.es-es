---
description: Notifica a las aplicaciones que se ha producido un evento de administración de energía.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Mensaje de WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545486"
---
# <a name="wm_powerbroadcast-message"></a>Mensaje de POWERBROADCAST de WM \_

Notifica a las aplicaciones que se ha producido un evento de administración de energía.

Una ventana recibe este mensaje a través de su función **WindowProc** .


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

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                          | Significado                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> * * * * <dt>WM \_ POWERBROADCAST *</dt> * * * <dt>536 (0x218)</dt> </dl> | Identificador de mensaje.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

El evento de administración de energía. Este parámetro puede ser uno de los siguientes identificadores de eventos.



| Evento                                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | El estado de la energía ha cambiado.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0X12)</dt> </dl>        | La operación se está reanudando automáticamente desde un estado de baja energía. Este mensaje se envía cada vez que se reanuda el sistema.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0X7)</dt> </dl>                  | La operación se está reanudando desde un estado de baja energía. Este mensaje se envía después de [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) si la entrada del usuario desencadena la reanudación, como presionar una tecla.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | El sistema está suspendiendo la operación.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | Se ha recibido un evento de cambio de configuración de energía. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Datos específicos del evento. Para la mayoría de los eventos, este parámetro está reservado y no se utiliza.

Si el parámetro *wParam* es [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), el parámetro *lParam* es un puntero a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver **true** si procesa este mensaje.

## <a name="remarks"></a>Observaciones

El sistema siempre envía un mensaje [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) cuando se reanuda el sistema. Si el sistema se reanuda en respuesta a la entrada del usuario, como presionar una tecla, el sistema también envía un mensaje de **PBT \_ APMRESUMESUSPEND** después de enviar PBT \_ APMRESUMEAUTOMATIC.

**WM \_** Los mensajes POWERBROADCAST no distinguen entre diferentes Estados de energía baja. Una aplicación solo puede determinar que el sistema está entrando en estado de baja energía o se ha reanudado. no puede determinar el estado de energía específico. El sistema registra los detalles acerca de las transiciones de estado de energía en el registro de eventos del sistema de Windows.

Para evitar que el sistema pase a un estado de baja energía en Windows Vista, una aplicación debe llamar a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para informar al sistema de que está en uso.

Los siguientes mensajes no se admiten en ninguno de los sistemas operativos especificados en la sección de requisitos:

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[\_Mensajes POWERBROADCAST de WM](wm-powerbroadcast-messages.md)
</dt> <dt>

[Mensajes de administración de energía](power-management-messages.md)
</dt> </dl>

 

 




