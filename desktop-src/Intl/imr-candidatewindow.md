---
description: Notfies una aplicación cuando un IME seleccionado necesita información sobre la ventana candidata. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: Código de notificación de IMR_CANDIDATEWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667157"
---
# <a name="imr_candidatewindow-notification-code"></a>Código de notificación de IMR \_ CANDIDATEWINDOW

Notfies una aplicación cuando un IME seleccionado necesita información sobre la ventana candidata. La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMR \_ CANDIDATEWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a un búfer que contiene una estructura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . Su miembro **dwIndex** contiene el índice de la ventana candidata a la que se hace referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación rellena la estructura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . De lo contrario, el comando devuelve 0.

## <a name="remarks"></a>Observaciones

El IME puede enviar este comando a una ventana que haya borrado la \_ marca SHOWUICANDIDATEWINDOW de ISC en el controlador de mensajes de [**\_ IME IME \_ SETCONTEXT**](wm-ime-setcontext.md) .

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**\_solicitud de IME de WM \_**](wm-ime-request.md)
</dt> <dt>

[**\_SETCONTEXT IME de WM \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 




