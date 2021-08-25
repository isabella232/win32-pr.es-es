---
title: EM_UNDO mensaje (Winuser.h)
description: Este mensaje deshace la última operación de control de edición en la cola de deshacer del control. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d82e6d0685314a79f1f95cff487ee3f52e2d1b70925c3e6e72f9263f442e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047925"
---
# <a name="em_undo-message"></a>Mensaje \_ EM UNDO

Este mensaje deshace la última operación de control de edición en la cola de deshacer del control. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

Para un control de edición de una sola línea, el valor devuelto siempre es **TRUE.**

Para un control de edición multilínea, el valor devuelto es **TRUE** si la operación de deshacer es correcta o **FALSE** si se produce un error en la operación de deshacer.

## <a name="remarks"></a>Comentarios

**Controles de edición y Edición enriquecte 1.0:** También se puede deshacer una operación de deshacer. Por ejemplo, puede restaurar el texto eliminado con el primer mensaje **EM \_ UNDO** y quitar el texto de nuevo con un segundo mensaje **EM \_ UNDO** siempre que no haya ninguna operación de edición que intervenda.

**Rich Edit 2.0 y versiones posteriores:** La característica deshacer es de varios niveles, por lo que el envío de dos mensajes **EM \_ UNDO** deshacerá las dos últimas operaciones en la cola de deshacer. Para volver a hacer una operación, envíe el [**mensaje EM \_ REDO.**](em-redo.md)

**Edición enriqueceda:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> </dl>

 

 





