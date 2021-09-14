---
title: WM_CTLCOLORSTATIC mensaje (Winuser.h)
description: Un control estático, o un control de edición de solo lectura o deshabilitado, envía el mensaje WM CTLCOLORSTATIC a su ventana primaria cuando el control está a punto \_ de dibujarse.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165217"
---
# <a name="wm_ctlcolorstatic-message"></a>Mensaje \_ WM CTLCOLORSTATIC

Un control estático, o un control de edición de solo lectura o deshabilitado, envía el mensaje **\_ WM CTLCOLORSTATIC** a su ventana primaria cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer los colores de primer plano y fondo del texto del control estático.

Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Controlar el contexto del dispositivo para la ventana de control estático.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control estático.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, el valor devuelto es un identificador de un pincel que el sistema usa para pintar el fondo del control estático.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la [**función CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush),**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) la aplicación no necesita liberar el pincel.

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control estático.

Puede establecer el color de fondo del texto de un control de edición deshabilitado, pero no puede establecer el color de primer plano del texto. El sistema siempre usa COLOR \_ GRAYTEXT.

Los controles de edición que no son de solo lectura o están deshabilitados no envían el mensaje **\_ WM CTLCOLORSTATIC;** en su lugar, envían el mensaje [**\_ CTLCOLOREDIT de WM.**](wm-ctlcoloredit.md)

El **mensaje \_ WM CTLCOLORSTATIC** nunca se envía entre subprocesos; solo se envía dentro del mismo subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **int \_ PTR** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo **devuelve FALSE,** se realiza el control de mensajes predeterminado. Se omite el valor MSGRESULT de DWL establecido por la función \_ [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C++ se muestra cómo establecer los colores de primer plano y fondo de texto de un control estático en respuesta al mensaje **\_ WM CTLCOLORSTATIC.** La variable es una variable HBRUSH estática que se inicializa en NULL y almacena el pincel de fondo entre las llamadas `hbrBkgnd` a **WM \_ CTLCOLORSTATIC.**  El pincel debe destruirse mediante una llamada a la función [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) cuando ya no sea necesario, normalmente cuando se destruye el cuadro de diálogo asociado.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SeleccionarPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**WM \_ CTLCOLORDLG**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

