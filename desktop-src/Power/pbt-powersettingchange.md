---
description: Evento de cambio de configuración de energía enviado con un mensaje de ventana WM POWERBROADCAST o en una devolución de llamada de notificación \_ HandlerEx para servicios.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: PBT_POWERSETTINGCHANGE evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062834"
---
# <a name="pbt_powersettingchange-event"></a>Evento \_ PBT POWERSETTINGCHANGE

Evento de cambio de configuración de energía enviado con un mensaje de ventana [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) o en una devolución de llamada de notificación [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) para servicios.


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

*Hwnd* 
</dt> <dd>

Identificador a ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador del mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                                        | Significado                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura \_ DE CONFIGURACIÓN DE POWERBROADCAST.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> <dt>

[**CONFIGURACIÓN DE \_ POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

