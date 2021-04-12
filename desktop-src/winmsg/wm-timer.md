---
description: Se envía a la cola de mensajes del subproceso de instalación cuando expira un temporizador. El mensaje se expone mediante la función GetMessage o PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Mensaje de WM_TIMER (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278318"
---
# <a name="wm_timer-message"></a>\_Mensaje del temporizador de WM

Se envía a la cola de mensajes del subproceso de instalación cuando expira un temporizador. El mensaje se expone mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Identificador del temporizador.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una función de devolución de llamada definida por la aplicación que se pasó a la función [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) cuando se instaló el temporizador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Puede procesar el mensaje proporcionando un caso de **\_ temporizador de WM** en el procedimiento de ventana. De lo contrario, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) llamará a la función de devolución de llamada [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) especificada en la llamada a la función [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) que se usa para instalar el temporizador.

El mensaje del **\_ temporizador de WM** es un mensaje de prioridad baja. Las funciones [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) y [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) exponen este mensaje solo cuando no hay otros mensajes de prioridad más alta en la cola de mensajes del subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Vista**
</dt> <dt>

[Timers](timers.md) (Temporizadores)
</dt> </dl>

 

 
