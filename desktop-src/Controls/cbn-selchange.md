---
title: CBN_SELCHANGE de notificación (Winuser.h)
description: Se envía cuando el usuario cambia la selección actual en el cuadro de lista de un cuadro combinado.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE código de notificación Windows controles
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
ms.openlocfilehash: f808438f8592acfdede592fab352bbeb0dd7123b5dc41db86eadb6749ae8b4ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968625"
---
# <a name="cbn_selchange-notification-code"></a>Código de notificación \_ DE CBN SELCHANGE

Se envía cuando el usuario cambia la selección actual en el cuadro de lista de un cuadro combinado. El usuario puede cambiar la selección haciendo clic en el cuadro de lista o usando las teclas de dirección. La ventana primaria del cuadro combinado recibe este código de notificación en forma de mensaje [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del cuadro combinado. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro combinado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener el índice de la selección actual, envíe el [**mensaje \_ CB GETCURSEL**](cb-getcursel.md) al control .

El código de notificación DE CBN SELCHANGE no se envía cuando se establece la selección actual \_ mediante el [**mensaje \_ SETCURSEL de CB.**](cb-setcursel.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[CBN \_ CLOSEUP](cbn-closeup.md)
</dt> <dt>

[\_DBLCLK de CBN](cbn-dblclk.md)
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

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

