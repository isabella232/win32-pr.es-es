---
description: Notifica a las aplicaciones que se ha denegado el permiso para suspender el equipo.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Evento PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677897"
---
# <a name="pbt_apmquerysuspendfailed-event"></a>\_Evento PBT APMQUERYSUSPENDFAILED

\[PBT \_ APMQUERYSUSPENDFAILED está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Se ha quitado la compatibilidad con este evento en Windows Vista. Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) en su lugar.\]

Notifica a las aplicaciones que se ha denegado el permiso para suspender el equipo. Este evento se emite si cualquier aplicación o controlador devolvió una **consulta de difusión \_ \_ Deny** a un evento [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) anterior.

Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) . Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.


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

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador de mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                                          | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0X2)</dt> </dl> | Identificador del evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las aplicaciones normalmente responden a este evento reanudando el funcionamiento normal.

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

[Administración de energía](power-management-portal.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




