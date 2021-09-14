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
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165190"
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

## <a name="remarks"></a>Observaciones

**Edición enriquecte:** Se recomienda usar [**EM \_ UNDO**](em-undo.md) en lugar de **WM \_ UNDO**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

 

