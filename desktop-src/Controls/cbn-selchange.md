---
title: Código de notificación de CBN_SELCHANGE (Winuser. h)
description: Se envía cuando el usuario cambia la selección actual en el cuadro de lista de un cuadro combinado.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997114"
---
# <a name="cbn_selchange-notification-code"></a>Código de notificación de SELCHANGE de CBN \_

Se envía cuando el usuario cambia la selección actual en el cuadro de lista de un cuadro combinado. El usuario puede cambiar la selección haciendo clic en el cuadro de lista o usando las teclas de dirección. La ventana primaria del cuadro combinado recibe este código de notificación en forma de mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro combinado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener el índice de la selección actual, envíe el mensaje [**CB \_ GETCURSEL**](cb-getcursel.md) al control.

El \_ código de notificación CBN SELCHANGE no se envía cuando la selección actual se establece mediante el mensaje [**CB \_ SETCURSEL**](cb-setcursel.md) .

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

[CBN \_ primer plano](cbn-closeup.md)
</dt> <dt>

[CBN \_ DBLCLK](cbn-dblclk.md)
</dt> <dt>

[**CB \_ GETCURSEL**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

