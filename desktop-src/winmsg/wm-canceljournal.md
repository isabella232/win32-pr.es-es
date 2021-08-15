---
description: Se publica en una aplicación cuando un usuario cancela las actividades de diario de la aplicación. El mensaje se publica con un identificador de ventana NULL.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: WM_CANCELJOURNAL mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8672f86393275c46383c6eb27c7eb1884178b86635ea93bf758de16521e6d2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849341"
---
# <a name="wm_canceljournal-message"></a>Mensaje \_ CANCELJOURNAL de WM

Se publica en una aplicación cuando un usuario cancela las actividades de diario de la aplicación. El mensaje se publica con un **identificador de ventana** NULL.


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **void**

Este mensaje no devuelve un valor. Está pensado para procesarse desde dentro del bucle principal de una aplicación o un procedimiento de enlace [**GetMessage,**](/windows/win32/api/winuser/nf-winuser-getmessage) no desde un procedimiento de ventana.

## <a name="remarks"></a>Comentarios

Los modos de registro y reproducción de diario son modos impuestos en el sistema que permiten a una aplicación registrar o reproducir secuencialmente la entrada del usuario. El sistema entra en estos modos cuando una aplicación instala un procedimiento de enlace [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) [*o JournalPlaybackProc.*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) Cuando el sistema está en cualquiera de estos modos de diario, las aplicaciones deben turnar la lectura de la entrada de la cola de entrada. Si alguna aplicación deja de leer la entrada mientras el sistema está en modo de diario, otras aplicaciones se ven forzadas a esperar.

Para garantizar un sistema sólido, que no puede dejar de responder ninguna aplicación, el sistema cancela automáticamente las actividades de registro en diario cuando un usuario presiona CTRL+ESC o CTRL+ALT+SUPR. A continuación, el sistema desenlaza los procedimientos de enlace de diario y envía un mensaje **\_ CANCELJOURNAL** wm, con un identificador de ventana **NULL,** a la aplicación que establece el enlace de diario.

El **mensaje \_ CANCELJOURNAL de WM** tiene un identificador de ventana **NULL,** por lo que no se puede enviar a un procedimiento de ventana. Hay dos maneras de que una aplicación vea un mensaje **\_ CANCELJOURNAL** de WM: si la aplicación se ejecuta en su propio bucle main, debe capturar el mensaje entre su llamada a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) y su llamada a [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage). Si la aplicación no se ejecuta en su propio bucle main, debe establecer un procedimiento de enlace [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (mediante una llamada a [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) que especifica el tipo de enlace **WH \_ GETMESSAGE)** que busca el mensaje.

Cuando una aplicación ve un mensaje **\_ CANCELJOURNAL** de WM, puede suponer dos cosas: el usuario ha cancelado intencionadamente el registro de diario o el modo de reproducción, y el sistema ya ha desenlazado cualquier registro de diario o procedimientos de enlace de reproducción.

Tenga en cuenta que las combinaciones de teclas mencionadas anteriormente (CTRL+ESC o CTRL+ALT+SUPR) hacen que el sistema cancele el registro en diario. Si alguna aplicación deja de responder, ofrece al usuario un medio de recuperación. El código de clave virtual CANCEL de [**VK \_**](../inputdev/virtual-key-codes.md) (normalmente implementado como combinación de teclas CTRL+BREAK) es lo que una aplicación que está en modo de registro de diario debe observar como una señal de que el usuario desea cancelar la actividad de registro en diario. La diferencia es que la observación de **VK \_ CANCEL** es un comportamiento sugerido para las aplicaciones de diario, mientras que CTRL+ESC o CTRL+ALT+SUPR hacen que el sistema cancele el registro en diario independientemente del comportamiento de una aplicación de diario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Enlaces](hooks.md)
</dt> </dl>

 

 
