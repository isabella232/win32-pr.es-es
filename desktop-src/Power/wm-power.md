---
description: Notifica a las aplicaciones que el sistema, normalmente un equipo personal con batería, está a punto de entrar en modo de suspensión.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Mensaje de WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677878"
---
# <a name="wm_power-message"></a>Mensaje de energía de WM \_

Notifica a las aplicaciones que el sistema, normalmente un equipo personal con batería, está a punto de entrar en modo de suspensión.

> [!Note]  
> El mensaje de **\_ energía de WM** está obsoleto. Solo se proporciona para ofrecer compatibilidad con aplicaciones basadas en Windows de 16 bits. Las aplicaciones deben usar el mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .

 

Una ventana recibe este mensaje a través de su función **WindowProc** .


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

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador del mensaje de **\_ energía de WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

La notificación de evento de potencia. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**PWR \_ CRITICALRESUME**</dt> </dl> | Indica que el sistema está reanudando la operación después de entrar en modo suspendido sin difundir primero un mensaje de notificación **PWR \_ SUSPENDREQUEST** a la aplicación. Una aplicación debe realizar las acciones de recuperación necesarias.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**PWR \_ SUSPENDREQUEST**</dt> </dl> | Indica que el sistema está a punto de entrar en modo suspendido.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**PWR \_ SUSPENDRESUME**</dt> </dl>    | Indica que el sistema está reanudando la operación después de haber entrado en modo suspendido normalmente, es decir, el sistema difunde un mensaje de notificación **PWR \_ SUSPENDREQUEST** a la aplicación antes de que se suspendiera el sistema. Una aplicación debe realizar las acciones de recuperación necesarias.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que devuelve una aplicación depende del valor del parámetro *wParam* . Si *wParam* es **PWR \_ SUSPENDREQUEST**, el valor devuelto es **PWR \_ FAIL** para evitar que el sistema entre en estado suspendido; de lo contrario, es **PWR \_ OK**. Si *wParam* es **PWR \_ SUSPENDRESUME** o **PWR \_ CRITICALRESUME**, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Este mensaje solo se difunde a una aplicación que se ejecuta en un sistema que se ajusta a la especificación del sistema básico de entrada y salida (BIOS) de administración avanzada de energía (APM). El controlador de administración de energía emite el mensaje a cada ventana devuelta por la función **EnumWindows** .

El modo suspendido es el estado en el que se produce la mayor cantidad de ahorro de energía, pero se conservan todos los datos y parámetros operativos. Se conserva el contenido de la memoria de acceso aleatorio (RAM), pero es probable que se desactiven muchos dispositivos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




