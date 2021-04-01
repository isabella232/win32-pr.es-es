---
title: Mensaje de EM_CANUNDO (Winuser. h)
description: Determina si hay alguna acción en la cola de deshacer del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150560"
---
# <a name="em_canundo-message"></a>\_Mensaje de CANUNDO em

Determina si hay alguna acción en la cola de deshacer del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

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

Si hay acciones en la cola de deshacer del control, el valor devuelto es distinto de cero.

Si la cola de deshacer está vacía, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Si la cola de deshacer no está vacía, puede enviar el mensaje de [**\_ Deshacer em**](em-undo.md) al control para deshacer la operación más reciente.

**Controles de edición y edición enriquecida 1,0:** La cola de deshacer solo contiene la operación más reciente.

**Edición enriquecida 2,0 y versiones posteriores:** La cola de deshacer puede contener varias operaciones.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**deshacer EM \_**](em-undo.md)
</dt> </dl>

 

 





