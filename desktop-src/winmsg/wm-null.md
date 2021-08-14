---
description: No realiza ninguna operación. Una aplicación envía el mensaje WM \_ NULL si desea publicar un mensaje que la ventana de destinatario omitirá.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: WM_NULL mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ade89ee83a7d0d0b9d012248da729facbd07d269387a86cd4dfac873b76be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199951"
---
# <a name="wm_null-message"></a>Mensaje NULL de WM \_

No realiza ninguna operación. Una aplicación envía el **mensaje WM \_ NULL** si desea publicar un mensaje que la ventana de destinatario omitirá.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NULL                         0x0000
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

Tipo: **LRESULT**

Una aplicación devuelve cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Por ejemplo, si una aplicación ha instalado un enlace **WH \_ GETMESSAGE** y desea evitar que se procese un mensaje, la función de devolución de llamada [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) puede cambiar el número de mensaje a **WM \_ NULL** para que el destinatario lo ignore.

Como otro ejemplo, una aplicación puede comprobar si una ventana responde a los mensajes mediante el envío del **mensaje WM \_ NULL** con la [**función SendMessageTimeout.**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Visión general](windows.md)
</dt> </dl>

 

 
