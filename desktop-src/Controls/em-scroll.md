---
title: Mensaje de EM_SCROLL (Winuser. h)
description: Desplaza el texto verticalmente en un control de edición multilínea. Este mensaje es equivalente a enviar un mensaje de WM \_ VSCROLL al control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151148"
---
# <a name="em_scroll-message"></a>\_Mensaje de desplazamiento em

Desplaza el texto verticalmente en un control de edición multilínea. Este mensaje es equivalente a enviar un mensaje de [**WM \_ VSCROLL**](wm-vscroll.md) al control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Acción que va a tomar la barra de desplazamiento. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                   | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl> | Se desplaza hacia abajo una línea.<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**\_línea SB**</dt> </dl>       | Se desplaza hacia arriba una línea.<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**reavpág SB \_**</dt> </dl> | Se desplaza hacia abajo una página.<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**\_Re Pág de SB**</dt> </dl>       | Desplaza hacia arriba una página.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del valor devuelto es **true** y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el número de líneas que el comando desplaza. El número devuelto puede no ser el mismo que el número real de líneas desplazadas si el desplazamiento se desplaza hasta el principio o el final del texto. Si el parámetro *wParam* especifica un valor no válido, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Para desplazarse a una línea o posición de carácter concreta, use el mensaje [**\_ LINESCROLL em**](em-linescroll.md) . Para desplazar el símbolo de intercalación a la vista, use el mensaje [**\_ SCROLLCARET em**](em-scrollcaret.md) .

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

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

[**\_LINESCROLL em**](em-linescroll.md)
</dt> <dt>

[**\_SCROLLCARET em**](em-scrollcaret.md)
</dt> <dt>

[**VSCROLL de WM \_**](wm-vscroll.md)
</dt> </dl>

 

