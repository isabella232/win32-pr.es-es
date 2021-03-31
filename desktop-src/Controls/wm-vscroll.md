---
title: Mensaje de WM_VSCROLL (Winuser. h)
description: El mensaje de VSCROLL de WM \_ se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento vertical estándar de la ventana.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151110"
---
# <a name="wm_vscroll-message"></a>Mensaje de VSCROLL de WM \_

El mensaje de **\_ VSCROLL de WM** se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento vertical estándar de la ventana. Este mensaje también se envía al propietario de un control de barra de desplazamiento vertical cuando se produce un evento de desplazamiento en el control.

Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del cuadro de desplazamiento si [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es SB \_ THUMBPOSITION o SB \_ THUMBTRACK; de lo contrario, esta palabra no se utiliza.

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica un valor de la barra de desplazamiento que indica la solicitud de desplazamiento del usuario. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ inferior**</dt> </dl>                      | Se desplaza a la parte inferior derecha.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> </dl>             | Finaliza el desplazamiento.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl>                | Desplaza una línea hacia abajo.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**\_línea SB**</dt> </dl>                      | Desplaza una línea hacia arriba.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**reavpág SB \_**</dt> </dl>                | Desplaza una página hacia abajo.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**\_Re Pág de SB**</dt> </dl>                      | Desplaza una página hacia arriba.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | El usuario ha arrastrado el cuadro de desplazamiento (Thumb) y ha soltado el botón del mouse. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posición del cuadro de desplazamiento al final de la operación de arrastre.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | El usuario está arrastrando el cuadro de desplazamiento. Este mensaje se envía repetidamente hasta que el usuario suelta el botón del mouse. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posición a la que se ha arrastrado el cuadro de desplazamiento.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ superior**</dt> </dl>                               | Se desplaza a la parte superior izquierda.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Si el mensaje se envía mediante un control de barra de desplazamiento, este parámetro es el identificador del control de barra de desplazamiento. Si el mensaje se envía mediante una barra de desplazamiento estándar, este parámetro es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

El \_ código de solicitud THUMBTRACK de SB lo suelen usar las aplicaciones que proporcionan comentarios cuando el usuario arrastra el cuadro de desplazamiento.

Si una aplicación desplaza el contenido de la ventana, también debe restablecer la posición del cuadro de desplazamiento mediante la función [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .

Tenga en cuenta que el mensaje de **\_ VSCROLL de WM** solo incluye 16 bits de datos de posición del cuadro de desplazamiento. Por lo tanto, las aplicaciones que se basan únicamente en **WM \_ VSCROLL** (y [**WM \_ HSCROLL**](wm-hscroll.md)) para los datos de posición de desplazamiento tienen un valor de posición máximo práctico de 65.535.

Sin embargo, dado que las funciones [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)y [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) admiten datos de posición de la barra de desplazamiento de 32 bits, existe una manera de eludir la barrera de 16 bits de los mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) y **WM \_ VSCROLL** . Consulte **GetScrollInfo** para obtener una descripción de la técnica.

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

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**HSCROLL de WM \_**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (TrackBar)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

