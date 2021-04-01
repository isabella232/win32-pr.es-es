---
title: Mensaje de WM_CTLCOLORSTATIC (Winuser. h)
description: Un control estático o un control de edición que sea de solo lectura o deshabilitado, envía el \_ mensaje de CTLCOLORSTATIC de WM a su ventana primaria cuando el control está a punto de dibujarse.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802174"
---
# <a name="wm_ctlcolorstatic-message"></a>Mensaje de CTLCOLORSTATIC de WM \_

Un control estático o un control de edición que sea de solo lectura o deshabilitado, envía el mensaje de **\_ CTLCOLORSTATIC de WM** a su ventana primaria cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer los colores de primer plano y de fondo del texto del control estático.

Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto de dispositivo para la ventana de control estática.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control estático.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, el valor devuelto es un identificador de un pincel que el sistema utiliza para pintar el fondo del control estático.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control estático.

Puede establecer el color de fondo del texto de un control de edición deshabilitado, pero no puede establecer el color de primer plano del texto. El sistema siempre usa el COLOR \_ GRAYTEXT.

Los controles de edición que no son de solo lectura o están deshabilitados no envían el mensaje de **WM \_ CTLCOLORSTATIC** ; en su lugar, envían el mensaje de [**\_ CTLCOLOREDIT de WM**](wm-ctlcoloredit.md) .

El mensaje de **\_ CTLCOLORSTATIC de WM** nunca se envía entre subprocesos; solo se envía dentro del mismo subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado. \_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C++ se muestra cómo establecer los colores de fondo y de primer plano del texto de un control estático en respuesta al mensaje de **\_ CTLCOLORSTATIC de WM** . La `hbrBkgnd` variable es una variable **hbrush** estática que se inicializa en NULL y almacena el pincel de fondo entre las llamadas a **WM \_ CTLCOLORSTATIC**. El pincel se debe destruir mediante una llamada a la función [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) cuando ya no se necesite, normalmente cuando se destruye el cuadro de diálogo asociado.


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CTLCOLORBTN de WM \_**](wm-ctlcolorbtn.md)
</dt> <dt>

[**CTLCOLOREDIT de WM \_**](wm-ctlcoloredit.md)
</dt> <dt>

[**CTLCOLORLISTBOX de WM \_**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**CTLCOLORSCROLLBAR de WM \_**](wm-ctlcolorscrollbar.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**CTLCOLORDLG de WM \_**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

