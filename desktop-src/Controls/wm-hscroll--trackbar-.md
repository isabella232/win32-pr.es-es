---
title: WM_HSCROLL de notificación (Barra de seguimiento) (Winuser.h)
description: El mensaje WM HSCROLL se envía al propietario de un control de barra de seguimiento \_ horizontal cuando el control deslizante cambia de posición. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- WM_HSCROLL de notificación (Barra de seguimiento) Windows controles
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
ms.openlocfilehash: 10727b745900520e8af31561236c8e93eeeb3a81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165206"
---
# <a name="wm_hscroll-trackbar-notification-code"></a>Código de notificación de WM \_ HSCROLL (Trackbar)

El **mensaje \_ WM HSCROLL** se envía al propietario de un control de barra de seguimiento horizontal cuando el control deslizante cambia de posición.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del control deslizante si [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es TB \_ THUMBPOSITION o TB \_ THUMBTRACK. Para todos los demás códigos de notificación, la palabra de orden superior es cero; envíe el [**mensaje \_ GETPOS de TBM**](tbm-getpos.md) para determinar la posición del control deslizante.

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un código de notificación que indica la interacción del usuario con la barra de seguimiento. Esta palabra puede ser uno de los siguientes valores.



| Value                                                                                                                                                                  | Significado                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB \_ INFERIOR**</dt> </dl>                      | El usuario ha presionado la tecla END [**(VK \_ END).**](/windows/desktop/inputdev/virtual-key-codes)<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB \_ ENDTRACK**</dt> </dl>                | La barra de seguimiento recibió [**WM \_ KEYUP,**](/windows/desktop/inputdev/wm-keyup)lo que significa que el usuario publicó una clave que envió un código de clave virtual pertinente. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**LÍNEA \_ DE TB**</dt> </dl>                | El usuario ha presionado la tecla FLECHA DERECHA [**(VK \_ RIGHT)**](/windows/desktop/inputdev/virtual-key-codes)o FLECHA ABAJO [**(VK \_ DOWN).**](/windows/desktop/inputdev/virtual-key-codes)<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**ALINEACIÓN \_ DE TB**</dt> </dl>                      | El usuario ha presionado la tecla FLECHA IZQUIERDA [**(VK \_ LEFT)**](/windows/desktop/inputdev/virtual-key-codes)o FLECHA ARRIBA [**(VK \_ UP).**](/windows/desktop/inputdev/virtual-key-codes)<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ PAGEDOWN**</dt> </dl>                | El usuario hizo clic en el canal siguiente o a la derecha del control deslizante [**(VK \_ NEXT).**](/windows/desktop/inputdev/virtual-key-codes)<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**PAGEUP \_ de TB**</dt> </dl>                      | El usuario hizo clic en el canal anterior o a la izquierda del control deslizante [**(VK \_ PRIOR).**](/windows/desktop/inputdev/virtual-key-codes)<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB \_ THUMBPOSITION**</dt> </dl> | La barra de seguimiento recibió [**WM \_ LBUTTONUP después**](/windows/desktop/inputdev/wm-lbuttonup) de un código de notificación \_ THUMBTRACK de TB.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB \_ THUMBTRACK**</dt> </dl>          | El usuario arrastró el control deslizante.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB \_ TOP**</dt> </dl>                               | El usuario ha presionado la tecla HOME [**(VK \_ HOME).**](/windows/desktop/inputdev/virtual-key-codes) <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control trackbar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

El código THUMBTRACK de TB lo usan normalmente las aplicaciones \_ que proporcionan comentarios a medida que el usuario arrastra el cuadro de desplazamiento.

Tenga en cuenta **que el mensaje WM \_ HSCROLL** solo contiene 16 bits de datos de posición. Por lo tanto, las aplicaciones que se basan únicamente en **WM \_ HSCROLL** (y [**WM \_ VSCROLL)**](wm-vscroll--trackbar-.md)para los datos de posición del control deslizante tienen un valor de posición máximo práctico de 65 535.

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

[**WM \_ VSCROLL**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

