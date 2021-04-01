---
title: Mensaje de LVM_ISITEMVISIBLE (commctrl. h)
description: Indica si un elemento del control de vista de lista está visible. Envíe este mensaje explícitamente o mediante la \_ macro IsItemVisible de ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905498"
---
# <a name="lvm_isitemvisible-message"></a>\_Mensaje ISITEMVISIBLE LVM

Indica si un elemento del control de vista de lista está visible. Envíe este mensaje explícitamente o mediante la [**macro \_ IsItemVisible de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice del elemento en el control de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si está visible o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





