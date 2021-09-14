---
title: LVM_GETSELECTIONMARK mensaje (Commctrl.h)
description: Recupera la marca de selección de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetSelectionMark.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061817"
---
# <a name="lvm_getselectionmark-message"></a>Mensaje \_ GETSELECTIONMARK de LVM

Recupera la marca de selección de un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetSelectionMark.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de selección de base cero o -1 si no hay ninguna marca de selección.

## <a name="remarks"></a>Observaciones

La *marca de selección* es el índice de elemento desde el que se inicia una selección múltiple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVM \_ SETSELECTIONMARK**](lvm-setselectionmark.md)
</dt> </dl>

 

 





