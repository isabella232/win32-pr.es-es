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
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246872"
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

## <a name="remarks"></a>Observaciones

Si la cola de deshacer no está vacía, puede enviar el mensaje [**EM \_ UNDO**](em-undo.md) al control para deshacer la operación más reciente.

**Controles de edición y Edición enriquecte 1.0:** La cola de deshacer solo contiene la operación más reciente.

**Rich Edit 2.0 y versiones posteriores:** La cola de deshacer puede contener varias operaciones.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





