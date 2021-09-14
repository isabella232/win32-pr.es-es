---
title: WM_NOTIFY mensaje (Winuser.h)
description: Enviado por un control común a su ventana primaria cuando se ha producido un evento o el control requiere cierta información.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- WM_NOTIFY controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165197"
---
# <a name="wm_notify-message"></a>Mensaje \_ WM NOTIFY

Enviado por un control común a su ventana primaria cuando se ha producido un evento o el control requiere cierta información.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control común que envía el mensaje. No se garantiza que este identificador sea único. Una aplicación debe usar el **miembro hwndFrom** o **idFrom** de la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (pasado como parámetro *lParam)* para identificar el control.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene el código de notificación y la información adicional. Para algunos mensajes de notificación, este parámetro apunta a una estructura mayor que tiene la estructura **NMHDR** como su primer miembro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto se omite, excepto para los mensajes de notificación que especifican lo contrario.

## <a name="remarks"></a>Observaciones

El destino del mensaje debe ser el **HWND** del elemento primario del control. Este valor se puede obtener mediante [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), como se muestra en el ejemplo siguiente, donde *m \_ controlHwnd* es el **HWND** del propio control.


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



Las aplicaciones controlan el mensaje en el procedimiento de ventana de la ventana primaria, como se muestra en el ejemplo siguiente, que controla el mensaje de notificación enviado por el control personalizado en el ejemplo anterior.


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



Algunas notificaciones, principalmente las que han estado en la API durante mucho tiempo, se envían como [**mensajes \_ WM COMMAND.**](/windows/desktop/menurc/wm-command) Para obtener más información, vea [Controlar mensajes](control-messages.md).

Si el controlador de mensajes está en un procedimiento de cuadro de diálogo, debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con MSGRESULT de DWL para \_ establecer un valor devuelto.

Para Windows Vista y sistemas posteriores, el **mensaje \_ WM NOTIFY** no se puede enviar entre procesos.

Muchas notificaciones están disponibles en formato ANSI y Unicode. La ventana que envía el **mensaje \_ WM NOTIFY** usa el mensaje [**\_ NOTIFYFORMAT de WM**](wm-notifyformat.md) para determinar qué formato se debe usar. Consulte **WM \_ NOTIFYFORMAT para** obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**WM \_ NOTIFYFORMAT**](wm-notifyformat.md)
</dt> </dl>

 

