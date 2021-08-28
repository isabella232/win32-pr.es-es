---
title: WM_UNDO mensaje (Winuser.h)
description: Una aplicación envía un mensaje \_ WM UNDO a un control de edición para deshacer la última operación. Cuando este mensaje se envía a un control de edición, se restaura el texto eliminado anteriormente o se elimina el texto agregado anteriormente.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6e4bd0715b7eeb5f99f34f5142ac3198c5c1eae53cf4486c3efce9dace19a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311345"
---
# <a name="wm_undo-message"></a>Mensaje \_ WM UNDO

Una aplicación envía un **mensaje \_ WM UNDO** a un control de edición para deshacer la última operación. Cuando este mensaje se envía a un control de edición, se restaura el texto eliminado anteriormente o se elimina el texto agregado anteriormente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es **TRUE.**

Si se produce un error en el mensaje, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

**Edición enriquecte:** Se recomienda usar [**EM \_ UNDO**](em-undo.md) en lugar de **WM \_ UNDO**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ CLEAR**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**WM \_ COPY**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**WM \_ CUT**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**WM \_ PASTE**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

