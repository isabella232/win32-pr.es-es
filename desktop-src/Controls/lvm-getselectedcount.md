---
title: LVM_GETSELECTEDCOUNT mensaje (Commctrl.h)
description: Determina el número de elementos seleccionados en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetSelectedCount.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- LVM_GETSELECTEDCOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974083"
---
# <a name="lvm_getselectedcount-message"></a>Mensaje DE \_ LVM GETSELECTEDCOUNT

Determina el número de elementos seleccionados en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetSelectedCount.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos seleccionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





