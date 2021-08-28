---
title: LBN_SELCHANGE de notificación (Winuser.h)
description: Notifica a la aplicación que la selección de un cuadro de lista ha cambiado como resultado de la entrada del usuario. La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje \_ WM COMMAND.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef87aebcf2ce804a10b4682bfaf2cba900bd227a06671959d11babce5f46774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085185"
---
# <a name="lbn_selchange-notification-code"></a>Código de notificación \_ DE LBN SELCHANGE

Notifica a la aplicación que la selección de un cuadro de lista ha cambiado como resultado de la entrada del usuario. La ventana primaria del cuadro de lista recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del cuadro de lista. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador en el cuadro de lista.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este código de notificación solo se envía mediante un cuadro de lista que tiene el [**estilo NOTIFY \_ de LBS.**](list-box-styles.md)

Este código de notificación no se envía si el mensaje [**LB \_ SETSEL**](lb-setsel.md), [**LB \_ SETCURSEL,**](lb-setcursel.md) [**LB \_ SELECTSTRING,**](lb-selectstring.md) [**LB \_ SELITEMRANGE**](lb-selitemrange.md) o [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md) cambia la selección.

Para un cuadro de lista de selección múltiple, el código de notificación LBN SELCHANGE se envía cada vez que el usuario presiona una tecla de flecha, incluso si la selección \_ no cambia.

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

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> <dt>

[\_DBLCLK de LBN](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCANCEL](lbn-selcancel.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

