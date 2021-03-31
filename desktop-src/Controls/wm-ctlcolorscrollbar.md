---
title: Mensaje de WM_CTLCOLORSCROLLBAR (Winuser. h)
description: El \_ mensaje de CTLCOLORSCROLLBAR de WM se envía a la ventana primaria de un control de barra de desplazamiento cuando el control está a punto de dibujarse.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996328"
---
# <a name="wm_ctlcolorscrollbar-message"></a>Mensaje de CTLCOLORSCROLLBAR de WM \_

El mensaje de **\_ CTLCOLORSCROLLBAR de WM** se envía a la ventana primaria de un control de barra de desplazamiento cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de presentación para establecer el color de fondo del control de barra de desplazamiento.

Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto de dispositivo para el control de barra de desplazamiento.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la barra de desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver el identificador a un pincel. El sistema utiliza el pincel para pintar el fondo del control de barra de desplazamiento.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control de barra de desplazamiento.

El mensaje de **\_ CTLCOLORSCROLLBAR de WM** nunca se envía entre subprocesos; solo se envía dentro del mismo subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado. \_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

El **mensaje \_ CTLCOLORSCROLLBAR de WM** solo lo usan los controles de barra de desplazamiento secundarios. Las barras de desplazamiento adjuntas a una ventana (WS \_ Scroll y WS \_ VSCROLL) no generan este mensaje. Para personalizar la apariencia de las barras de desplazamiento asociadas a una ventana, use las funciones de barra de desplazamiento plana.

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

[**CTLCOLORSTATIC de WM \_**](wm-ctlcolorstatic.md)
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

 

