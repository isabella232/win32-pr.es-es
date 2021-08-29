---
description: Notifica a las aplicaciones que se denegó el permiso para suspender el equipo.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: PBT_APMQUERYSUSPENDFAILED evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4151829d2c00fc8d4577fb8a7231111df09eb1326985f274d4dcc9e8986b2b86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143368"
---
# <a name="pbt_apmquerysuspendfailed-event"></a>Evento \_ PBT APMQUERYSUSPENDFAILED

\[PBT APMQUERYSUSPENDFAILED está disponible para su uso en los sistemas operativos especificados \_ en la sección Requisitos. Se quitó la compatibilidad con este evento en Windows Vista. Use [**SetThreadExecutionState en su**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) lugar.\]

Notifica a las aplicaciones que se denegó el permiso para suspender el equipo. Este evento se difunde si alguna aplicación o controlador devolvió **BROADCAST \_ QUERY \_ DENY** a un evento [anterior de \_ PBT APMQUERYSUSPEND.](pbt-apmquerysuspend.md)

Una ventana recibe este evento a través del [**mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
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

| Value                                                                                                                                                                                                                                                          | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Normalmente, las aplicaciones responden a este evento reanudando el funcionamiento normal.

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

[Administración de energía](power-management-portal.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




