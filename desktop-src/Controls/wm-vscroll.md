---
title: WM_VSCROLL mensaje (Winuser.h)
description: El mensaje VSCROLL de WM se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento \_ vertical estándar de la ventana.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL controles de Windows mensaje
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
ms.openlocfilehash: 6bbb87f63cb0f4801787be1f2cb23b321470b1053a58b13d0f3eea34112b1341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636715"
---
# <a name="wm_vscroll-message"></a>Mensaje \_ VSCROLL de WM

El **mensaje \_ VSCROLL de WM** se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento vertical estándar de la ventana. Este mensaje también se envía al propietario de un control de barra de desplazamiento vertical cuando se produce un evento de desplazamiento en el control .

Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

HIWORD [**especifica la**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) posición actual del cuadro de desplazamiento si [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es SB THUMBPOSITION o \_ SB THUMBTRACK; de lo contrario, no se \_ usa esta palabra.

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un valor de barra de desplazamiento que indica la solicitud de desplazamiento del usuario. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ BOTTOM**</dt> </dl>                      | Se desplaza a la parte inferior derecha.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> </dl>             | Finaliza el desplazamiento.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl>                | Desplaza una línea hacia abajo.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> </dl>                      | Desplaza una línea hacia arriba.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> </dl>                | Desplaza una página hacia abajo.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**PÁGINA \_ DE SB**</dt> </dl>                      | Desplaza una página hacia arriba.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | El usuario ha arrastrado el cuadro de desplazamiento (thumb) y ha liberado el botón del mouse. HIWORD [**indica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posición del cuadro de desplazamiento al final de la operación de arrastre.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | El usuario está arrastrando el cuadro de desplazamiento. Este mensaje se envía repetidamente hasta que el usuario suelta el botón del mouse. HIWORD [**indica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posición a la que se ha arrastrado el cuadro de desplazamiento.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> </dl>                               | Se desplaza a la parte superior izquierda.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Si un control de barra de desplazamiento envía el mensaje, este parámetro es el identificador del control de barra de desplazamiento. Si una barra de desplazamiento estándar envía el mensaje, este parámetro es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

El código de solicitud SB THUMBTRACK lo usan normalmente las aplicaciones que proporcionan comentarios a medida \_ que el usuario arrastra el cuadro de desplazamiento.

Si una aplicación desplaza el contenido de la ventana, también debe restablecer la posición del cuadro de desplazamiento mediante la [**función SetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)

Tenga en cuenta que **el mensaje \_ WM VSCROLL** solo contiene 16 bits de datos de posición del cuadro de desplazamiento. Por lo tanto, las aplicaciones que se basan únicamente en **WM \_ VSCROLL** (y [**WM \_ HSCROLL)**](wm-hscroll.md)para los datos de posición de desplazamiento tienen un valor de posición máximo práctico de 65 535.

Sin embargo, dado que las funciones [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos,**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) [**SetScrollRange,**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) [**GetScrollInfo,**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)y [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) admiten datos de posición de barra de desplazamiento de 32 bits, hay una manera de eludir la barrera de 16 bits de los mensajes [**WM \_ HSCROLL**](wm-hscroll.md) y **WM \_ VSCROLL.** Vea **GetScrollInfo para** obtener una descripción de la técnica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

[**WM \_ HSCROLL**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (Barra de seguimiento)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

