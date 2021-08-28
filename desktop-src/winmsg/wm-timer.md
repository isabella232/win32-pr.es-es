---
description: Se publica en la cola de mensajes del subproceso de instalación cuando expira un temporizador. La función GetMessage o PeekMessage publica el mensaje.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: WM_TIMER mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d770d640b801849eeebe1c4ec86df8c41642c6149b89e00d82261f4e090f56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710035"
---
# <a name="wm_timer-message"></a>Mensaje \_ DE TEMPORIZADOR DE WM

Se publica en la cola de mensajes del subproceso de instalación cuando expira un temporizador. La función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) publica el mensaje.


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Identificador del temporizador.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una función de devolución de llamada definida por la aplicación que se pasó a la [**función SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) cuando se instaló el temporizador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Puede procesar el mensaje proporcionando un caso **DE \_ TEMPORIZADOR DE WM** en el procedimiento de ventana. De lo contrario, [**DispatchMessage llamará**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) a la función de devolución de llamada [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) especificada en la llamada a la [**función SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) usada para instalar el temporizador.

El **mensaje \_ WM TIMER** es un mensaje de prioridad baja. Las [**funciones GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) y [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) publican este mensaje solo cuando no hay ningún otro mensaje de prioridad superior en la cola de mensajes del subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

**Conceptual**
</dt> <dt>

[Timers](timers.md) (Temporizadores)
</dt> </dl>

 

 
