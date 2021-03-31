---
title: Mensaje de WM_UNDO (Winuser. h)
description: Una aplicación envía un \_ mensaje de deshacer de WM a un control de edición para deshacer la última operación. Cuando este mensaje se envía a un control de edición, se restaura el texto previamente eliminado o se elimina el texto agregado previamente.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491417"
---
# <a name="wm_undo-message"></a>\_Mensaje de deshacer de WM

Una aplicación envía un mensaje de **\_ Deshacer de WM** a un control de edición para deshacer la última operación. Cuando este mensaje se envía a un control de edición, se restaura el texto previamente eliminado o se elimina el texto agregado previamente.

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

Si el mensaje se realiza correctamente, el valor devuelto es **true**.

Si se produce un error en el mensaje, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** Se recomienda el uso de la [**\_ función**](em-undo.md) deshacer en lugar de **WM \_ Undo**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**\_borrado de WM**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**copia de WM \_**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**cortar de WM \_**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**pegar de WM \_**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

