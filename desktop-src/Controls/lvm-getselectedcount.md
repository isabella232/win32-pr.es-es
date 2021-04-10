---
title: Mensaje de LVM_GETSELECTEDCOUNT (commctrl. h)
description: Determina el número de elementos seleccionados en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetSelectedCount de ListView.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- LVM_GETSELECTEDCOUNT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905504"
---
# <a name="lvm_getselectedcount-message"></a>\_Mensaje GETSELECTEDCOUNT LVM

Determina el número de elementos seleccionados en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetSelectedCount de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) .

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





