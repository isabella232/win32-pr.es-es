---
title: EM_SCROLL mensaje (Winuser.h)
description: Desplaza el texto verticalmente en un control de edición multilínea. Este mensaje es equivalente al envío de un mensaje \_ VSCROLL de WM al control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062136"
---
# <a name="em_scroll-message"></a>Mensaje DE DESPLAZAMIENTO DE EM \_

Desplaza el texto verticalmente en un control de edición multilínea. Este mensaje es equivalente al envío de un [**mensaje \_ VSCROLL**](wm-vscroll.md) de WM al control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Acción que debe realizar la barra de desplazamiento. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                   | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl> | Se desplaza hacia abajo una línea.<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> </dl>       | Se desplaza hacia arriba una línea.<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> </dl> | Se desplaza hacia abajo una página.<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**PÁGINA \_ DE SB**</dt> </dl>       | Desplaza hacia arriba una página.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el [**VALOR HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del valor devuelto es **TRUE** y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el número de líneas que se desplaza el comando. Es posible que el número devuelto no sea el mismo que el número real de líneas desplazadas si el desplazamiento se mueve al principio o al final del texto. Si el *parámetro wParam* especifica un valor no válido, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Observaciones

Para desplazarse a una posición específica de línea o carácter, use el [**mensaje EM \_ LINESCROLL.**](em-linescroll.md) Para desplazar el caret a la vista, use el [**mensaje EM \_ SCROLLCARET.**](em-scrollcaret.md)

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

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

[**LÍNEAS \_ EMCROLL**](em-linescroll.md)
</dt> <dt>

[**EM \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

