---
title: Mensaje de WM_COMMAND (Winuser. h)
description: Se envía cuando el usuario selecciona un elemento de comando de un menú, cuando un control envía un mensaje de notificación a su ventana primaria o cuando se traduce una pulsación de tecla de aceleración.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709018"
---
# <a name="wm_command-message"></a>Mensaje de comando de WM \_

Se envía cuando el usuario selecciona un elemento de comando de un menú, cuando un control envía un mensaje de notificación a su ventana primaria o cuando se traduce una pulsación de tecla de aceleración.


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Para obtener una descripción de este parámetro, vea la sección Comentarios.

</dd> <dt>

*lParam* 
</dt> <dd>

Para obtener una descripción de este parámetro, vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="example"></a>Ejemplo

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
Ejemplo tomado de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples) en github.


## <a name="remarks"></a>Observaciones

El uso de los parámetros *wParam* e *lParam* se resume aquí.



| Origen del mensaje | wParam (palabra alta)                | wParam (palabra baja)                | lParam                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| Menú           | 0                                 | Identificador de menú (IDM \_ \* )        | 0                            |
| Acelerador    | 1                                 | Identificador de acelerador (IDM \_ \* ) | 0                            |
| Control        | Código de notificación definido por el control | Identificador de control               | Identificador de la ventana de control |



 

### <a name="menus"></a>Menús

Si una aplicación habilita un separador de menús, el sistema envía un mensaje de **\_ comando de WM** con la palabra baja del parámetro *wParam* establecida en cero cuando el usuario selecciona el separador.

Si se define un menú con un valor [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) de **mns \_ NOTIFYBYPOS**, se envía [**WM \_ MENUCOMMAND**](wm-menucommand.md) en lugar del **\_ comando WM**.

### <a name="accelerators"></a>Aceleradores

Las pulsaciones de teclas de aceleración que seleccionan elementos en el menú ventana se traducen en mensajes [**\_ SYSCOMMAND de WM**](wm-syscommand.md) .

Si se produce una pulsación de tecla de aceleración que corresponde a un elemento de menú cuando se minimiza la ventana que posee el menú, no se envía ningún mensaje de **\_ comando de WM** . Sin embargo, si se produce una pulsación de tecla de aceleración que no coincide con ninguno de los elementos del menú de la ventana o en el menú ventana, se envía un mensaje de **\_ comando de WM** , incluso si la ventana está minimizada.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

