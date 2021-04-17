---
title: Mensaje de LVM_GETSELECTIONMARK (commctrl. h)
description: Recupera la marca de selección de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetSelectionMark de ListView.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658339"
---
# <a name="lvm_getselectionmark-message"></a>\_Mensaje GETSELECTIONMARK LVM

Recupera la marca de selección de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetSelectionMark de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de selección de base cero, o-1 si no hay ninguna marca de selección.

## <a name="remarks"></a>Observaciones

La *marca de selección* es el índice del elemento desde el que se inicia una selección múltiple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETSELECTIONMARK LVM**](lvm-setselectionmark.md)
</dt> </dl>

 

 





