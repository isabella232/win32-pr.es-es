---
description: Notifica a una aplicación cuando un IME seleccionado necesita información sobre la ventana de composición. La aplicación recibe este comando a través del mensaje WM \_ IME \_ REQUEST con parámetros establecidos como se muestra a continuación.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: IMR_COMPOSITIONWINDOW de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5f1f45652a2f58386a50284e3bf2cfec182c6f4ad89641dcc27a63cf12b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810058"
---
# <a name="imr_compositionwindow-notification-code"></a>Código de notificación de IMR \_ COMPOSITIONWINDOW

Notifica a una aplicación cuando un IME seleccionado necesita información sobre la ventana de composición. La aplicación recibe este comando a través del mensaje [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con parámetros establecidos como se muestra a continuación.


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMR \_ COMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a un búfer que contiene una [**estructura COMPOSITIONFORM.**](/windows/win32/api/imm/ns-imm-compositionform)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación rellena la [**estructura COMPOSITIONFORM.**](/windows/win32/api/imm/ns-imm-compositionform) De lo contrario, el comando devuelve 0.

## <a name="remarks"></a>Comentarios

El IME puede enviar este comando a una ventana que ha borrado la marca SHOWUICOMPOSITIONWINDOW de ISC en el controlador de mensajes SETCONTEXT de \_ [**WM \_ IME. \_**](wm-ime-setcontext.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del Administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**SOLICITUD \_ DE WM IME \_**](wm-ime-request.md)
</dt> <dt>

[**SETCONTEXT \_ de WM IME \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 




