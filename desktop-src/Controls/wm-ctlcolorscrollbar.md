---
title: WM_CTLCOLORSCROLLBAR mensaje (Winuser.h)
description: El mensaje CTLCOLORSCROLLBAR de WM se envía a la ventana primaria de un control de barra de desplazamiento cuando el control está a punto \_ de dibujarse.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165221"
---
# <a name="wm_ctlcolorscrollbar-message"></a>Mensaje \_ CTLCOLORSCROLLBAR de WM

El **mensaje \_ CTLCOLORSCROLLBAR** de WM se envía a la ventana primaria de un control de barra de desplazamiento cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de presentación para establecer el color de fondo del control de barra de desplazamiento.

Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para el control de barra de desplazamiento.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la barra de desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver el identificador a un pincel. El sistema usa el pincel para pintar el fondo del control de barra de desplazamiento.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la [**función CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush),**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) la aplicación no necesita liberar el pincel.

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control de barra de desplazamiento.

El **mensaje \_ CTLCOLORSCROLLBAR de WM** nunca se envía entre subprocesos; solo se envía dentro del mismo subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **int \_ PTR** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo **devuelve FALSE,** se realiza el control de mensajes predeterminado. Se omite el valor MSGRESULT de DWL establecido por la función \_ [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

El **mensaje \_ WM CTLCOLORSCROLLBAR** solo lo usan los controles de barra de desplazamiento secundarios. Las barras de desplazamiento asociadas a una ventana (WS \_ SCROLL y WS \_ VSCROLL) no generan este mensaje. Para personalizar la apariencia de las barras de desplazamiento asociadas a una ventana, use las funciones de barra de desplazamiento plano.

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

[**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md)
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

 

