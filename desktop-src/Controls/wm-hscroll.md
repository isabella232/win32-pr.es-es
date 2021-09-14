---
title: WM_HSCROLL mensaje (Winuser.h)
description: El mensaje WM HSCROLL se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento horizontal estándar de \_ la ventana.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- WM_HSCROLL controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165205"
---
# <a name="wm_hscroll-message"></a>Mensaje \_ de WM HSCROLL

El **mensaje \_ WM HSCROLL** se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento horizontal estándar de la ventana. Este mensaje también se envía al propietario de un control de barra de desplazamiento horizontal cuando se produce un evento de desplazamiento en el control .

Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

HIWORD [**especifica la**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) posición actual del cuadro de desplazamiento si [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es SB THUMBPOSITION o \_ SB THUMBTRACK; de lo contrario, no se \_ usa esta palabra.

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un valor de barra de desplazamiento que indica la solicitud de desplazamiento del usuario. Esta palabra puede ser uno de los siguientes valores.



| Value                                                                                                                                                                  | Significado                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> </dl>             | Finaliza el desplazamiento.<br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ LEFT**</dt> </dl>                            | Se desplaza a la parte superior izquierda.<br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ RIGHT**</dt> </dl>                         | Se desplaza a la parte inferior derecha.<br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ LINELEFT**</dt> </dl>                | Se desplaza a la izquierda por una unidad.<br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ LINERIGHT**</dt> </dl>             | Se desplaza a la derecha por una unidad.<br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ PAGELEFT**</dt> </dl>                | Se desplaza a la izquierda por el ancho de la ventana.<br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ PAGERIGHT**</dt> </dl>             | Se desplaza a la derecha por el ancho de la ventana.<br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | El usuario ha arrastrado el cuadro de desplazamiento (thumb) y ha liberado el botón del mouse. HIWORD [**indica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posición del cuadro de desplazamiento al final de la operación de arrastre.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | El usuario está arrastrando el cuadro de desplazamiento. Este mensaje se envía repetidamente hasta que el usuario suelta el botón del mouse. HIWORD [**indica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posición a la que se ha arrastrado el cuadro de desplazamiento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Si un control de barra de desplazamiento envía el mensaje, este parámetro es el identificador del control de barra de desplazamiento. Si una barra de desplazamiento estándar envía el mensaje, este parámetro es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

El código de solicitud SB THUMBTRACK lo usan normalmente las aplicaciones que proporcionan comentarios a medida \_ que el usuario arrastra el cuadro de desplazamiento.

Si una aplicación desplaza el contenido de la ventana, también debe restablecer la posición del cuadro de desplazamiento mediante la [**función SetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)

Tenga en cuenta que **el \_ mensaje WM HSCROLL** solo contiene 16 bits de datos de posición del cuadro de desplazamiento. Por lo tanto, las aplicaciones que se basan únicamente en **WM \_ HSCROLL** (y [**WM \_ VSCROLL)**](wm-vscroll.md)para los datos de posición de desplazamiento tienen un valor de posición máximo práctico de 65 535.

Sin embargo, dado que las funciones [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos,**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) [**SetScrollRange,**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) [**GetScrollInfo,**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)y [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) admiten datos de posición de barra de desplazamiento de 32 bits, hay una manera de eludir la barrera de 16 bits de los mensajes **WM \_ HSCROLL** y [**WM \_ VSCROLL.**](wm-vscroll.md) Vea **GetScrollInfo para** obtener una descripción de la técnica.

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

[**WM \_ HSCROLL (barra de seguimiento)**](wm-hscroll--trackbar-.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

