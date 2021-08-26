---
title: EM_EMPTYUNDOBUFFER mensaje (Winuser.h)
description: Restablece la marca de deshacer de un control de edición. La marca deshacer se establece siempre que se puede deshacer una operación dentro del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d59dab38bca921e2125377889f8d18ddf6eb45c023badeead47f7e07b860fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915905"
---
# <a name="em_emptyundobuffer-message"></a>Mensaje \_ EM EMPTYUNDOBUFFER

Restablece la marca de deshacer de un control de edición. La marca deshacer se establece siempre que se puede deshacer una operación dentro del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

La marca de deshacer se restablece automáticamente cada vez que el control de edición recibe un mensaje [**\_ WM SETTEXT**](/windows/desktop/winmsg/wm-settext) [**o EM \_ SETHANDLE.**](em-sethandle.md)

**Editar controles y Rich Edit 1.0:** El control solo puede deshacer o rehacer la operación más reciente.

**Rich Edit 2.0 y versiones posteriores:** El **mensaje EM \_ EMPTYUNDOBUFFER** vacía todos los búferes de deshacer y rehacer. Los controles de edición enriquecciones permiten al usuario deshacer o rehacer varias operaciones.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

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

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

