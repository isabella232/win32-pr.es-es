---
title: LVM_DELETEITEM mensaje (Commctrl.h)
description: Quita un elemento de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ DeleteItem.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88520e7d4f9d0d3ff22f90d7cea033b7674cfcbadbf55358f7ced8cc36c2399a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958424"
---
# <a name="lvm_deleteitem-message"></a>Mensaje \_ DELETEITEM de LVM

Quita un elemento de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ DeleteItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista que se eliminará.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





