---
description: No realiza ninguna operación. Una aplicación envía el mensaje \_ WM NULL si desea publicar un mensaje que la ventana del destinatario omitirá.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: WM_NULL mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267183"
---
# <a name="wm_null-message"></a>Mensaje NULL de WM \_

No realiza ninguna operación. Una aplicación envía el **mensaje \_ WM NULL** si desea publicar un mensaje que la ventana del destinatario omitirá.

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

## <a name="remarks"></a>Observaciones

Por ejemplo, si una aplicación ha instalado un enlace **\_ GETMESSAGE de WH** y desea evitar que se procese un mensaje, la función de devolución de llamada [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) puede cambiar el número de mensaje a **WM \_ NULL** para que el destinatario lo ignore.

Como otro ejemplo, una aplicación puede comprobar si una ventana responde a los mensajes mediante el envío del **mensaje WM \_ NULL** con [**la función SendMessageTimeout.**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Visión general](windows.md)
</dt> </dl>

 

 
