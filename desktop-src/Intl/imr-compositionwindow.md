---
description: Notifica a una aplicación cuando un IME seleccionado necesita información sobre la ventana de composición. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con los parámetros establecidos como se muestra a continuación.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: Código de notificación de IMR_COMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652677"
---
# <a name="imr_compositionwindow-notification-code"></a>Código de notificación de IMR \_ COMPOSITIONWINDOW

Notifica a una aplicación cuando un IME seleccionado necesita información sobre la ventana de composición. La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con los parámetros establecidos como se muestra a continuación.


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMR \_ COMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a un búfer que contiene una estructura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación rellena la estructura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) . De lo contrario, el comando devuelve 0.

## <a name="remarks"></a>Observaciones

El IME puede enviar este comando a una ventana que haya borrado la \_ marca SHOWUICOMPOSITIONWINDOW de ISC en el controlador de mensajes de [**\_ IME IME \_ SETCONTEXT**](wm-ime-setcontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**\_solicitud de IME de WM \_**](wm-ime-request.md)
</dt> <dt>

[**\_SETCONTEXT IME de WM \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 




