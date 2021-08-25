---
title: EM_CANUNDO mensaje (Winuser.h)
description: Determina si hay alguna acción en la cola de deshacer de un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b1cb56b07232c6b55a85b7387cf7b2fafd40ac29e5dc0520b45e1aa50cadcb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915995"
---
# <a name="em_canundo-message"></a>Mensaje \_ DE EM CANUNDO

Determina si hay alguna acción en la cola de deshacer de un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

Si hay acciones en la cola de deshacer del control, el valor devuelto es distinto de cero.

Si la cola de deshacer está vacía, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Si la cola de deshacer no está vacía, puede enviar el mensaje [**EM \_ UNDO**](em-undo.md) al control para deshacer la operación más reciente.

**Editar controles y Rich Edit 1.0:** La cola de deshacer solo contiene la operación más reciente.

**Rich Edit 2.0 y versiones posteriores:** La cola de deshacer puede contener varias operaciones.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





