---
title: Mensaje de EM_EMPTYUNDOBUFFER (Winuser. h)
description: Restablece la marca de deshacer de un control de edición. La marca de deshacer se establece siempre que se puede deshacer una operación dentro del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER controles de mensajes de Windows
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
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491495"
---
# <a name="em_emptyundobuffer-message"></a>\_Mensaje EMPTYUNDOBUFFER em

Restablece la marca de deshacer de un control de edición. La marca de deshacer se establece siempre que se puede deshacer una operación dentro del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

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

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El indicador de deshacer se restablece automáticamente siempre que el control de edición recibe un mensaje de [**\_ SETHANDLE**](em-sethandle.md) de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) o EM.

**Controles de edición y edición enriquecida 1,0:** El control solo puede deshacer o rehacer la operación más reciente.

**Edición enriquecida 2,0 y versiones posteriores:** El **mensaje \_ EMPTYUNDOBUFFER em** vacía todos los búferes de deshacer y rehacer. Los controles Rich Edit permiten al usuario deshacer o rehacer varias operaciones.

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

[**la \_ CANUNDO em**](em-canundo.md)
</dt> <dt>

[**\_SETHANDLE em**](em-sethandle.md)
</dt> <dt>

[**deshacer EM \_**](em-undo.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**SETTEXT de WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

