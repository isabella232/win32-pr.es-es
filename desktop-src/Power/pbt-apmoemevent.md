---
description: Notifica a las aplicaciones que el BIOS de APM ha señalado un evento oem de APM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: PBT_APMOEMEVENT evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92feb840e69c3a7e560d7bc71a0a5e4746ae5677920010f0251a1b951ddb8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961664"
---
# <a name="pbt_apmoemevent-event"></a>Evento \_ PBT APMOEMEVENT

\[PBT \_ APMOEMEVENT está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. Se quitó la compatibilidad con este evento en Windows Vista.\]

Notifica a las aplicaciones que el BIOS de APM ha señalado un evento oem de APM.

Una ventana recibe este evento a través del [**mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
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

| Value                                                                                                                                                                                                                             | Significado                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <dt>**PBT \_ APMOEMEVENT**</dt> <dt>11 (0xB)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Código de evento definido por el OEM que señalaba el BIOS de APM del sistema. Los códigos de evento oem están en el intervalo de 0200h - 02FFh.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Dado que no todas las implementaciones del BIOS de APM proporcionan notificaciones de eventos de OEM, es posible que este evento nunca se difunda en algunos equipos.

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

 

 




