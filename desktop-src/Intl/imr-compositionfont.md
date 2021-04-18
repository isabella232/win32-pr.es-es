---
description: Notifica a una aplicación cuando un IME seleccionado necesita información sobre la fuente utilizada por la ventana de composición. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con parámetros, como se muestra a continuación.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: Código de notificación de IMR_COMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687457"
---
# <a name="imr_compositionfont-notification-code"></a>Código de notificación de IMR \_ COMPOSITIONFONT

Notifica a una aplicación cuando un IME seleccionado necesita información sobre la fuente utilizada por la ventana de composición. La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con parámetros, como se muestra a continuación.


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMR \_ COMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a un búfer que contiene una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . La aplicación rellena los valores de la ventana de composición actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación rellena la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . De lo contrario, el comando devuelve 0.

## <a name="remarks"></a>Observaciones

El IME puede enviar este comando a una ventana que borró la \_ marca SHOWUICOMPOSITIONWINDOW de ISC en el controlador de mensajes de [**\_ IME \_ de WM**](wm-ime-setcontext.md) .

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

[**\_solicitud de IME de WM \_**](wm-ime-request.md)
</dt> <dt>

[**\_SETCONTEXT IME de WM \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 
