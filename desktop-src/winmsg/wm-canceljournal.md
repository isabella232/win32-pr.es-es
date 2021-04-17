---
description: Se envía a una aplicación cuando un usuario cancela las actividades de registro en diario de la aplicación. El mensaje se envía con un identificador de ventana nulo.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Mensaje de WM_CANCELJOURNAL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706677"
---
# <a name="wm_canceljournal-message"></a>Mensaje de CANCELJOURNAL de WM \_

Se envía a una aplicación cuando un usuario cancela las actividades de registro en diario de la aplicación. El mensaje se envía con un identificador de ventana **nulo** .


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

Este mensaje no devuelve ningún valor. Está pensada para ser procesada desde el bucle principal de una aplicación o un procedimiento de enlace [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , no desde un procedimiento de ventana.

## <a name="remarks"></a>Observaciones

Los modos de reproducción y registro del diario son modos impuestos en el sistema que permiten a una aplicación grabar o reproducir de forma secuencial datos proporcionados por el usuario. El sistema entra en estos modos cuando una aplicación instala un procedimiento de enlace [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) o [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) . Cuando el sistema se encuentra en cualquiera de estos modos de registro en diario, las aplicaciones deben realizar la lectura de la entrada de la cola de entrada. Si una aplicación deja de leer la entrada mientras el sistema está en un modo de registro en diario, se fuerza a otras aplicaciones a esperar.

Para garantizar un sistema sólido, uno que no puede dejar de responder a ninguna aplicación, el sistema cancela automáticamente las actividades de registro en diario cuando un usuario presiona CTRL + ESC o CTRL + ALT + SUPR. Después, el sistema desenlaza los procedimientos de enlace de registro en diario y envía un mensaje de **WM \_ CANCELJOURNAL** , con un identificador de ventana **nulo** , a la aplicación que establece el enlace de registro en diario.

El mensaje de **\_ CANCELJOURNAL de WM** tiene un identificador de ventana **nulo** , por lo que no se puede enviar a un procedimiento de ventana. Hay dos maneras de que una aplicación vea un mensaje **de \_ CANCELJOURNAL de WM** : Si la aplicación se ejecuta en su propio bucle principal, debe detectar el mensaje entre su llamada a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) y su llamada a [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage). Si la aplicación no se ejecuta en su propio bucle principal, debe establecer un procedimiento de enlace [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (a través de una llamada a [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) que especifique el tipo de enlace de **\_ GETMESSAGE** ) que inspecciona el mensaje.

Cuando una aplicación ve un mensaje de **\_ CANCELJOURNAL de WM** , puede suponer dos cosas: el usuario canceló intencionadamente el registro del diario o el modo de reproducción, y el sistema ya ha desenlazado los procedimientos de registro del diario o del enlace de reproducción.

Tenga en cuenta que las combinaciones de teclas mencionadas anteriormente (CTRL + ESC o CTRL + ALT + Supr) hacen que el sistema cancele el registro en diario. Si una aplicación deja de responder, proporciona al usuario un medio de recuperación. El código de la clave virtual de [**\_ cancelación de VK**](../inputdev/virtual-key-codes.md) (normalmente implementado como combinación de teclas Ctrl + Inter) es lo que una aplicación que está en modo de registro de diario debe supervisar como una señal de que el usuario desea cancelar la actividad de diario. La diferencia es que supervisar la **\_ cancelación de VK** es un comportamiento sugerido para las aplicaciones de registro en diario, mientras que Ctrl + ESC o Ctrl + Alt + Supr hacen que el sistema cancele el registro en diario, independientemente del comportamiento de la aplicación de registro en diario.

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

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Vista**
</dt> <dt>

[Enlaces](hooks.md)
</dt> </dl>

 

 
