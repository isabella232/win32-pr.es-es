---
title: Mensaje de EM_UNDO (Winuser. h)
description: Este mensaje deshace la última operación de control de edición en la cola de deshacer del control. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO controles de mensajes de Windows
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
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802335"
---
# <a name="em_undo-message"></a>\_Mensaje de deshacer em

Este mensaje deshace la última operación de control de edición en la cola de deshacer del control. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para un control de edición de una sola línea, el valor devuelto siempre es **true**.

Para un control de edición multilínea, el valor devuelto es **true** si la operación de deshacer se realiza correctamente, o **false** si se produce un error en la operación de deshacer.

## <a name="remarks"></a>Observaciones

**Controles de edición y edición enriquecida 1,0:** También se puede deshacer una operación de deshacer. Por ejemplo, puede restaurar el texto eliminado con el primer mensaje de **\_ Deshacer em** y volver a quitar el texto con un segundo mensaje de **\_ Deshacer de EM** siempre que no haya ninguna operación de edición que intervenga.

**Edición enriquecida 2,0 y versiones posteriores:** La característica deshacer es multinivel, por lo que el envío de dos mensajes de **\_ Deshacer largos** deshará las dos últimas operaciones en la cola de deshacer. Para rehacer una operación, envíe el mensaje de [**\_ rehacer em**](em-redo.md) .

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**la \_ CANUNDO em**](em-canundo.md)
</dt> </dl>

 

 





