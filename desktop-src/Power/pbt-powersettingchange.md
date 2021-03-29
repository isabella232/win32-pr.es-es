---
description: Evento de cambio de configuración de energía enviado con un mensaje de ventana de POWERBROADCAST de WM \_ o en una devolución de llamada de notificación de HandlerEx para servicios.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: Evento PBT_POWERSETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909686"
---
# <a name="pbt_powersettingchange-event"></a>\_Evento PBT POWERSETTINGCHANGE

Evento de cambio de configuración de energía enviado con un mensaje de ventana de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) o en una devolución de llamada de notificación de [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) para servicios.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
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
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt> </dl> | Identificador del evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> <dt>

[**configuración de POWERBROADCAST \_**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

