---
description: Notifica a las aplicaciones que el sistema, normalmente un equipo personal con batería, está a punto de entrar en modo suspendido.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: WM_POWER mensaje (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169121"
---
# <a name="wm_power-message"></a>Mensaje \_ DE WM POWER

Notifica a las aplicaciones que el sistema, normalmente un equipo personal con batería, está a punto de entrar en modo suspendido.

> [!Note]  
> El **mensaje WM \_ POWER** está obsoleto. Solo se proporciona por compatibilidad con aplicaciones basadas en Windows bits. Las aplicaciones deben usar el [**\_ mensaje WM POWERBROADCAST.**](wm-powerbroadcast.md)

 

Una ventana recibe este mensaje a través de su **función WindowProc.**


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador a ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador **del mensaje DE WM \_ POWER.**

</dd> <dt>

*wParam* 
</dt> <dd>

La notificación de eventos de energía. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**PWR \_ CRITICALRESUME**</dt> </dl> | Indica que el sistema está reanudando la operación después de entrar en modo suspendido sin difundir primero un mensaje de notificación **\_ SUSPENDREQUEST** de PWR a la aplicación. Una aplicación debe realizar las acciones de recuperación necesarias.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**PWR \_ SUSPENDREQUEST**</dt> </dl> | Indica que el sistema está a punto de entrar en modo suspendido.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**PWR \_ SUSPENDRESUME**</dt> </dl>    | Indica que el sistema está reanudando la operación después de haber entrado en modo suspendido normalmente, es decir, el sistema difunde un mensaje de notificación **\_ SUSPENDREQUEST** de PWR a la aplicación antes de que se suspendiera el sistema. Una aplicación debe realizar las acciones de recuperación necesarias.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que devuelve una aplicación depende del valor del *parámetro wParam.* Si *wParam* es **PWR \_ SUSPENDREQUEST**, el valor devuelto es **PWR \_ FAIL** para evitar que el sistema entre en el estado suspendido; de lo contrario, **es PWR \_ OK**. Si *wParam es* **PWR \_ SUSPENDRESUME** o **PWR \_ CRITICALRESUME,** el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Este mensaje solo se difunde a una aplicación que se ejecuta en un sistema que se ajusta a la especificación del sistema básico de entrada y salida (BIOS) de Advanced Power Management (APM). El controlador de administración de energía difunde el mensaje a cada ventana devuelta por la **función EnumWindows.**

El modo suspendido es el estado en el que se produce la mayor cantidad de ahorro de energía, pero se conservan todos los datos y parámetros operativos. El contenido de la memoria de acceso aleatorio (RAM) se conserva, pero es probable que muchos dispositivos se apaguen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




