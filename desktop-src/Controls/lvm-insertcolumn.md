---
title: LVM_INSERTCOLUMN mensaje (Commctrl.h)
description: Inserta una nueva columna en un control list-view. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView InsertColumn.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c2316ed2a74c82cd4530eff2d71d4771f4042b903c7ee17fc62886009ed5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019243"
---
# <a name="lvm_insertcolumn-message"></a>Mensaje \_ INSERTCOLUMN de LVM

Inserta una nueva columna en un control list-view. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView InsertColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la nueva columna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contiene los atributos de la nueva columna.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la nueva columna si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Comentarios

Las columnas solo son visibles en la vista de informe (detalles).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





