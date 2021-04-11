---
description: No realiza ninguna operación. Una aplicación envía el mensaje de WM \_ null si desea publicar un mensaje que la ventana de destinatario omitirá.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Mensaje de WM_NULL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276849"
---
# <a name="wm_null-message"></a>\_Mensaje null de WM

No realiza ninguna operación. Una aplicación envía el mensaje de **WM \_ null** si desea publicar un mensaje que la ventana de destinatario omitirá.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Por ejemplo, si una aplicación ha instalado un enlace **qu \_ GETMESSAGE** y desea evitar que se procese un mensaje, la función de devolución de llamada [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) puede cambiar el número de mensaje a **WM \_ null** para que el destinatario lo ignore.

Otro ejemplo: una aplicación puede comprobar si una ventana responde a los mensajes enviando el mensaje de **WM \_ null** con la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Windows](windows.md)
</dt> </dl>

 

 
