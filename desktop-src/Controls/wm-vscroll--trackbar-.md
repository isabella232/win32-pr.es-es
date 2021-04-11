---
title: Código de notificación de WM_VSCROLL (TrackBar) (Winuser. h)
description: El \_ mensaje de VSCROLL de WM se envía al propietario de un control de barra de desplazamiento vertical cuando cambia la posición del control deslizante. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- Controles de Windows de código de notificación de WM_VSCROLL (TrackBar)
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
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150531"
---
# <a name="wm_vscroll-trackbar-notification-code"></a>\_Código de notificación de VSCROLL (TrackBar) de WM

El mensaje de **\_ VSCROLL de WM** se envía al propietario de un control de barra de desplazamiento vertical cuando cambia la posición del control deslizante.

Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del control deslizante si el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es TB \_ THUMBPOSITION o TB \_ THUMBTRACK. En el resto de códigos de notificación, la palabra de orden superior es cero; Envíe el [**mensaje \_ GETPOS de TBM**](tbm-getpos.md) para determinar la posición del control deslizante.

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica un código de notificación que indica la interacción del usuario con el TrackBar. Esta palabra puede tener uno de los valores siguientes.



| Value                                                                                                                                                                  | Significado                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB en la \_ parte inferior**</dt> </dl>                      | El usuario presionó la tecla fin ([**VK \_ End**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB \_ ENDTRACK**</dt> </dl>                | La barra de Estado ha recibido el [**\_ KEYUP de WM**](/windows/desktop/inputdev/wm-keyup), lo que significa que el usuario liberó una clave que envió un código de tecla virtual relevante. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TB \_ LINEDOWN**</dt> </dl>                | El usuario presionó la tecla flecha derecha ([**VK \_ derecha**](/windows/desktop/inputdev/virtual-key-codes)) o flecha abajo ([**VK \_ abajo**](/windows/desktop/inputdev/virtual-key-codes)).<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**gama de TB \_**</dt> </dl>                      | El usuario presionó la tecla flecha izquierda ([**VK \_ izquierda**](/windows/desktop/inputdev/virtual-key-codes)) o flecha arriba ([**VK \_ arriba**](/windows/desktop/inputdev/virtual-key-codes)).<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ Av Pág**</dt> </dl>                | El usuario hizo clic en el canal siguiente o a la derecha del control deslizante ([**VK \_ siguiente**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB \_ RePág**</dt> </dl>                      | El usuario hizo clic en el canal situado encima o a la izquierda del control deslizante ([**VK \_ anterior**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB \_ THUMBPOSITION**</dt> </dl> | El TrackBar ha recibido [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) después de un código de notificación de TB \_ THUMBTRACK.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB \_ THUMBTRACK**</dt> </dl>          | El usuario arrastró el control deslizante.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB en la \_ parte superior**</dt> </dl>                               | El usuario presionó la tecla Inicio ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

El código de TB \_ THUMBTRACK se usa normalmente en aplicaciones que proporcionan comentarios cuando el usuario arrastra el cuadro de desplazamiento.

Tenga en cuenta que el mensaje de **\_ VSCROLL de WM** solo incluye 16 bits de datos de posición. Por lo tanto, las aplicaciones que se basan únicamente en **WM \_ VSCROLL** (y en [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) para los datos de posición del control deslizante tienen un valor de posición máximo práctico de 65.535.

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

[**HSCROLL de WM \_**](wm-hscroll--trackbar-.md)
</dt> </dl>

 

