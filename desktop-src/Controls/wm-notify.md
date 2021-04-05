---
title: Mensaje de WM_NOTIFY (Winuser. h)
description: Lo envía un control común a su ventana primaria cuando se ha producido un evento o el control requiere cierta información.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- WM_NOTIFY controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996635"
---
# <a name="wm_notify-message"></a>Mensaje de notificación de WM \_

Lo envía un control común a su ventana primaria cuando se ha producido un evento o el control requiere cierta información.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control común que envía el mensaje. No se garantiza que este identificador sea único. Una aplicación debe usar el miembro **hwndFrom** o **idFrom** de la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (pasada como el parámetro *lParam* ) para identificar el control.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene el código de notificación e información adicional. En algunos mensajes de notificación, este parámetro apunta a una estructura más grande que tiene la estructura **NMHDR** como primer miembro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto se omite excepto para los mensajes de notificación que especifican lo contrario.

## <a name="remarks"></a>Observaciones

El destino del mensaje debe ser el **hWnd** del elemento primario del control. Este valor se puede obtener mediante [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), tal como se muestra en el ejemplo siguiente, donde *m \_ controlHwnd* es el **hWnd** del propio control.


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



Algunas notificaciones, principalmente las que han estado en la API durante mucho tiempo, se envían como mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) . Para obtener más información, consulte [control de mensajes](control-messages.md).

Si el controlador de mensajes está en un procedimiento de cuadro de diálogo, debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT para establecer un valor devuelto.

En Windows Vista y sistemas posteriores, no se puede enviar el mensaje de **\_ notificación de WM** entre procesos.

Muchas notificaciones están disponibles en los formatos ANSI y Unicode. La ventana que envía el mensaje de **\_ notificación de WM** usa el mensaje de [**\_ NOTIFYFORMAT de WM**](wm-notifyformat.md) para determinar qué formato se debe usar. Consulte **WM \_ NOTIFYFORMAT** para más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NOTIFYFORMAT de WM \_**](wm-notifyformat.md)
</dt> </dl>

 

