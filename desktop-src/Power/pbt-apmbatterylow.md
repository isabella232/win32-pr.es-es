---
description: Notifica a las aplicaciones que la energía de la batería es baja.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: PBT_APMBATTERYLOW evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc8f6d42d00ee1a4b92d7a977668b1161e1f91270e8d55c46d724f73ec105a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961775"
---
# <a name="pbt_apmbatterylow-event"></a>Evento \_ PBT APMBATTERYLOW

\[PBT \_ APMBATTERYLOW está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. Se quitó la compatibilidad con este evento en Windows Vista. Use [PBT \_ APMPOWERSTATUSCHANGE en](pbt-apmpowerstatuschange.md) su lugar.\]

Notifica a las aplicaciones que la energía de la batería es baja.

Una ventana recibe este evento a través del [**mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
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

| Value                                                                                                                                                                                                                                  | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado, debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este evento se difunde cuando el BIOS de APM de un sistema señala una notificación de bajo consumo de batería de APM. Dado que algunas implementaciones de BIOS de APM no proporcionan notificaciones cuando las baterías están bajas, es posible que este evento nunca se difunda en algunos equipos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                                           |
| Header<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




